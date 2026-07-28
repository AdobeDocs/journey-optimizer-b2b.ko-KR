---
title: 스크립트 빌더
description: 이메일 디자인 공간에서 AI 기반 도우미인 Script Builder를 사용하여 Handlebars 개인화 스크립트를 생성하고 Journey Optimizer B2B edition에서 Marketo Engage Velocity 스크립트를 변환합니다.
feature: AI Assistant, Generative AI, Personalization, Email Authoring
role: User, Developer
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
autotag-review: '2026-07-27T16:18:02.498Z'
TQID: 'https://experienceleague.adobe.com/JWnXAAbCuZVLv4ZhWubpNsZ61xbYU7xtdOXkG9uoWis'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2:
  - id: bd3c685c-6c92-4a4a-becb-535cc25215de
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0004f8fba0c3d4ae89063418e4d3ef8fea22b0c3
workflow-type: tm+mt
source-wordcount: 1074
ht-degree: 2%

---

# 스크립트 빌더

_Script Builder_&#x200B;은(는) [!DNL Adobe Journey Optimizer B2B Edition] 전자 메일 디자인 공간에서 사용할 수 있는 AI 기반 도우미입니다. 마케터와 이메일 개발자가 개인화 스크립트를 더 빨리 만들 수 있도록 도와주며, 코드를 수동으로 다시 작성하지 않고도 기존 개인화 논리를 [!DNL Journey Optimizer B2B Edition]&#x200B;(으)로 전환하여 [!DNL Marketo Engage]에서 마이그레이션하는 데 도움이 됩니다.

>[!AVAILABILITY]
>
>현재 Script Builder는 **_계정 여정 전용_**&#x200B;의 전자 메일에 대해 제한된 베타 릴리스로 고객을 선택할 수 있습니다. 개인 여정에 대한 지원은 향후 릴리스에서 제공될 예정입니다. 액세스하려면 Adobe 담당자에게 문의하십시오.

언어 블록을 로케일로 전환하거나, 지역 또는 담당자별로 콘텐츠를 교체하거나, 동적 프로필 또는 사용자 지정 개체 값을 삽입하는 등 조건부 전자 메일 개인화를 만들려면 _Handlebars_ 식을 작성해야 합니다. [!DNL Marketo Engage]에서 마이그레이션하는 경우 _Velocity_ 스크립트를 한 줄씩 다시 작성해야 합니다. Script Builder는 단일 대화 인터페이스에서 두 가지 장애 요소를 모두 해결합니다.

* 일반 언어 설명에서 새 Handlebars 개인화 스크립트를 생성합니다.
* [!DNL Marketo Engage] Velocity 스크립트를 붙여 넣고 자동 토큰 매핑을 사용하여 동등한 Handlebars 스크립트로 변환합니다.
* 도구 간에 복사하여 붙여넣지 않고 결과를 미리 보고, 편집하고, 검증하고, 이메일에 바로 저장할 수 있습니다.

## 지침 및 제한 사항

>[!IMPORTANT]
>
>Script Builder에 대한 사용자 액세스는 [!DNL Journey Optimizer B2B Edition]의 다른 생성 AI 기능에 사용된 것과 동일한 권한을 통해 제어됩니다. 기능 권한 부여에 대한 자세한 내용은 [AI Assistant 액세스 활성화](../ai-assistant/enable-ai-assistant-access.md)를 참조하십시오.

Script Builder를 사용하기 전에 [!DNL Journey Optimizer B2B Edition]의 생성 AI 기능에 적용되는 [지침 및 제한 사항](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations)을 검토하십시오. AI 기능을 사용하려면 [사용자 동의](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"} 동의도 필요합니다.

[!DNL Journey Optimizer B2B Edition]에서 지원되는 [Handlebars 템플릿 언어](https://handlebarsjs.com/guide/){target="_blank"}, [개인화 구문](./personalization-syntax.md) 및 [도우미 함수](./personalization-helper-functions.md)에 대해 숙지하십시오. Script Builder는 유효한 Handlebars를 생성하지만 구문을 이해하면 안심하고 출력을 검토하고 편집할 수 있습니다.

## 스크립트 빌더 열기 {#open-script-builder}

계정 여정을 위해 [전자 메일 콘텐츠를 작성](./email-authoring.md)하는 동안 [개인화 편집기](./personalization.md)에서 스크립트 빌더를 사용할 수 있습니다.

1. 이메일 디자인 공간에서 개인화 스크립트를 추가하거나 바꿀 구성 요소를 선택합니다.

1. 개인화 편집기를 열려면 _개인화 추가_( ![개인화 추가 아이콘](../../assets/do-not-localize/icon-personalization-field.svg) ) 아이콘을 클릭합니다.

1. 편집기에서 **[!UICONTROL 스크립트 빌더]**&#x200B;를 선택합니다.

   ![Personalization 편집기 - 스크립트 빌더 선택](./assets/personalization-script-builder-select.png){width="700" zoomable="yes"}

   >[!BEGINSHADEBOX]

   스크립트 빌더에 처음 액세스하면 [_[!UICONTROL 생성 AI 사용 약관&#x200B;]_](https://www.adobe.com/kr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}을 검토하고 동의를 확인하십시오.

   ![스크립트 빌더의 생성 AI 사용 약관 대화 상자](./assets/personalization-script-builder-gen-ai-terms.png){width="400"}

   >[!ENDSHADEBOX]

   대화식 채팅 인터페이스가 있는 Script Builder 패널이 열립니다.

   ![Personalization 편집기 - 스크립트 빌더 패널](./assets/personalization-script-builder-welcome.png){width="700" zoomable="yes"}

1. 원하는 작업에 따라 채팅을 시작합니다.

   * [새 스크립트 생성](#generate-personalization-script)
   * [기존 속도 스크립트 변환](#convert-marketo-velocity-script)

## 개인화 스크립트 생성 {#generate-personalization-script}

표현식을 직접 작성하지 않고 일반 언어 설명으로부터 새 Handlebars 개인화 스크립트를 작성하려면 Script Builder를 사용하십시오.

Script Builder에는 조직에 대해 정의된 [XDM 필드 매핑](../admin/xdm-field-management.md)을(를) 기반으로 [!DNL Marketo Engage] 리드 및 계정 필드를 해당 [!DNL Journey Optimizer B2B Edition] XDM 프로필 특성으로 확인하는 매핑 라이브러리가 포함되어 있습니다.

1. Script Builder 채팅 인터페이스에서 원하는 개인화 논리를 설명합니다.

   예를 들어 표시할 콘텐츠 변형을 결정하는 속성, 사용자 지정 개체 또는 조건을 설명합니다.

1. 미리 보기 창에서 생성된 Handlebars 스크립트를 검토합니다.

1. 논리나 단어를 세분화하려면 미리 보기 창에서 바로 스크립트를 편집합니다.

1. **[!UICONTROL 유효성 검사]**&#x200B;를 클릭하여 [!DNL Journey Optimizer B2B Edition] 스키마에 대한 스크립트를 확인합니다.

   유효성 검사는 스크립트를 저장하기 전에 구문 오류 및 해결되지 않은 토큰 참조를 catch하여 끊어진 개인화가 라이브 이메일에 게시되지 않도록 합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭하여 전자 메일의 선택한 위치에 스크립트를 직접 삽입합니다.

## Marketo Engage Velocity 스크립트 변환 {#convert-marketo-velocity-script}

Script Builder를 사용하여 기존 [!DNL Marketo Engage] Velocity 스크립트를 [!DNL Journey Optimizer B2B Edition]에 해당하는 Handlebars 스크립트로 마이그레이션합니다.

1. Script Builder 채팅에서 `Convert this`을(를) 입력하고 변환할 Velocity 스크립트를 붙여 넣습니다.

   Script Builder는 Velocity 구문을 구문 분석하고 토큰 참조를 XDM 프로필 속성에 일치시킨 다음 동일한 Handlebars 스크립트를 생성합니다.

1. [전환 보고서](#review-conversion-report)를 검토하고 [수동 매핑이 필요한 모든 토큰을 확인](#resolve-tokens-without-mapping)합니다.

1. 생성된 스크립트를 [미리 보고 확인](#preview-validate-script)한 다음 전자 메일에 직접 저장합니다.

### 지원되는 속도 구성 {#supported-velocity-constructs}

Script Builder는 다음 [!DNL Marketo Engage]개의 속도 제어 흐름 구문을 해당 Handlebars 또는 조건부 콘텐츠 표현식으로 변환합니다.

| 속도 구성 | Handlebars 또는 이에 상응하는 조건부 콘텐츠 |
| ------------------- | --------------------------------------------- |
| `#if` / `#elseif` / `#else` | Handlebars `{{#if}}`, `{{else if}}` 및 `{{else}}` 블록 도우미 또는 [!DNL Journey Optimizer B2B Edition] [조건부 콘텐츠](./conditional-content.md) 규칙 |
| `#set` | 생성된 스크립트 내의 Handlebars 변수 할당 |

세그먼트 기반 조건부 논리를 언어 변형 블록이 많은 이메일을 포함하여 분기 동작을 복제하는 [조건부 콘텐츠](./conditional-content.md) 규칙으로 변환합니다.

Velocity 구문에 직접 Handlebars 또는 이에 해당하는 조건부 콘텐츠가 없는 경우 Script Builder는 불완전하거나 잘못된 표현식을 생성하는 대신 [전환 보고서](#review-conversion-report)에 플래그를 지정합니다.

### 전환 보고서 검토 {#review-conversion-report}

각 변환 후 Script Builder는 다음을 나열하는 구조화된 보고서를 표시합니다.

* 정상적으로 매핑된 토큰입니다.
* 수동 해결이 필요한 토큰.
* Direct Handlebars에 상당하는 값이 없는 Velocity 구문입니다.

나머지 토큰을 해결하고 스크립트를 저장하기 전에 보고서를 사용하여 전환이 완료되었는지 확인합니다.

### 매핑 없이 토큰 확인 {#resolve-tokens-without-mapping}

사용자 지정 리드 특성 또는 사용자 지정 [!DNL Marketo Engage] 개체와 같이 매핑 라이브러리에 없는 토큰의 경우 Script Builder는 다음 순서로 매핑을 확인하려고 시도합니다.

1. 신뢰할 수 있는 일치가 존재하는 경우 사용 가능한 XDM 필드 및 사용자 지정 개체의 경우 조직에 대해 구성된 [모델 기반 클래스](./personalization.md#custom-datasets)를 기반으로 하는 가능한 매핑을 제안합니다.

1. 자신 있는 일치를 제안할 수 없는 경우 채팅에서 올바른 매핑을 요청합니다.

라이브러리에 없는 토큰에 대한 매핑을 확인하면 Script Builder에서 해당 결정을 기억할지 여부를 묻습니다. 동의하는 경우 해당 매핑은 해당 Munchkin ID로 식별되는 소스 [!DNL Marketo Engage] 인스턴스에 대해 기억되므로, 해당 인스턴스에서 다음에 스크립트를 변환할 때 동일한 토큰이 자동으로 확인됩니다.

### 스크립트 미리보기 및 유효성 검사 {#preview-validate-script}

변환을 커밋하기 전에 Script Builder는 인라인 편집을 지원하는 원본 Velocity 스크립트와 생성된 Handlebars 출력의 병렬 미리 보기를 표시합니다. 미리보기를 사용하여 두 버전을 비교하고 생성된 스크립트에서 직접 조정합니다.

**[!UICONTROL 유효성 검사]**&#x200B;를 클릭하여 [!DNL Journey Optimizer B2B Edition] 스키마에 대해 생성된 Handlebars를 확인합니다. 저장하면 유효성 검사가 다시 실행되어 중단된 개인화가 라이브 이메일에 게시되지 않습니다.

결과가 만족스러우면 **[!UICONTROL 저장]**&#x200B;을 클릭하여 선택한 전자 메일 위치에 스크립트를 직접 삽입합니다.

<!--
### Save reusable conversion profiles {#save-reusable-conversion-profiles}

Save your field mappings and segment mappings as a reusable conversion profile so that your token schema does not need to be re-entered for each script or migration batch. Select a saved profile at the start of a conversion to apply its mappings automatically.

### Audit logs {#conversion-audit-logs}

Script Builder records an audit log for every conversion event, including which scripts were processed, which tokens were remapped, which tokens required manual intervention, and who approved the final output. Use the audit log to review migration activity across your organization.

-->
