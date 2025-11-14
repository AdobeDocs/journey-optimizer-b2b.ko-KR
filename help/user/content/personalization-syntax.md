---
title: 개인화 구문
description: 표현식, 도우미, 리터럴 유형 및 형식 규칙을 포함한 Journey Optimizer B2B edition의 Handlebars 기반 개인화 구문에 대해 알아봅니다.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: 표현식, 편집기, 구문, 개인화
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 2%

---

# 개인화 구문 {#personalization-syntax}

[!DNL Journey Optimizer B2B Edition] [개인화 편집기](./personalization.md#personalization-editor)의 식은 _Handlebars_ 템플릿 구문을 기반으로 합니다. 템플릿과 입력 개체를 사용하여 HTML 또는 기타 텍스트 형식을 생성합니다. Handlebars 템플릿은 포함된 Handlebars 표현식이 있는 일반 텍스트처럼 보입니다.

Handlebars 및 작동 방식에 대한 자세한 내용은 [HandlebarsJS 설명서](https://handlebarsjs.com/){target="_blank"}를 참조하세요.

## 일반 규칙

단순 표현식 예:

```
{{account.accountName}}
```

위치:

* `account`은(는) 네임스페이스입니다.
* `accountName`은(는) 특성으로 구성된 토큰입니다.

  >[!NOTE]
  >
  >특성 구조가 [Adobe Experience Platform XDM 스키마](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}에 정의되어 있습니다.

* 식별자는 다음을 제외한 모든 유니코드 문자일 수 있습니다.

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 구문은 대/소문자를 구분합니다.

* **true**, **false**, **null** 및 **정의되지 않음**&#x200B;은(는) 경로 식의 첫 부분에서만 사용할 수 있습니다.

* Handlebars에서 {\{expression}\}이(가) 반환한 값은 _HTML 이스케이프_&#x200B;입니다. 식에 `&`이(가) 포함된 경우 반환된 HTML 이스케이프 출력은 `&amp;`(으)로 생성됩니다. Handlebars가 값을 이스케이프 처리하지 않게 하려면 +triple-stash_를 사용합니다.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* 리터럴 함수 인수의 경우 템플릿 언어 파서는 이스케이프 처리되지 않은 단일 백슬래시(`\`) 기호를 지원하지 않습니다. 이 문자는 추가 백슬래시(`\`) 기호로 이스케이프해야 합니다. 예 :

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## 도우미 {#helpers-all}

Handlebars 도우미 함수는 매개 변수를 추가할 수 있는 간단한 식별자입니다. 각 매개 변수는 Handlebars 표현식입니다. 이러한 도우미는 이메일 템플릿의 컨텍스트에서 액세스할 수 있습니다.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

이러한 함수에 대한 자세한 내용은 [도우미 함수](./personalization-helper-functions.md)를 참조하십시오.

## 리터럴 유형 {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition]은(는) 다음 리터럴 형식을 지원합니다.

| 리터럴 | 정의 |
| ------- | ---------- |
| 문자열 | 큰따옴표로 묶인 문자로 구성된 데이터 유형입니다. <br>예: `"prospect"`, `"jobs"`, `"articles"` |
| 부울 | true 또는 false인 데이터 유형입니다. |
| 정수 | 정수를 나타내는 데이터 형식입니다. 양수, 음수 또는 0일 수 있습니다. <br>예: `-201`, `0`, `412` |
| 배열 | 다른 리터럴 값의 그룹으로 구성된 데이터 유형입니다. 대괄호를 사용하여 그룹화하고 쉼표를 사용하여 서로 다른 값 사이를 구분합니다. <br> **참고:** 배열 내의 항목 속성에 직접 액세스할 수 없습니다. <br> 예: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>개인화 식에는 **xEvent** 변수를 사용할 수 없습니다. xEvent에 대한 모든 참조는 유효성 검사 실패를 초래합니다.
