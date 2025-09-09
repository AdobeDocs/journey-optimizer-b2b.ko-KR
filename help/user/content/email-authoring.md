---
title: 이메일 메시지 작성
description: 시각적 디자인 도구, HTML 가져오기 또는 템플릿을 사용하여 이메일을 만듭니다. AI Assistant 컨텐츠 생성, 사용자 지정 CSS 및 Journey Optimizer B2B edition의 개인화를 사용합니다.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 2%

---

# 이메일 메시지 작성

[여정 작업 노드에 전자 메일 자산을 추가](./add-email.md)한 후 전자 메일 메시지의 콘텐츠를 정의할 수 있습니다.

오른쪽 패널의 **[!UICONTROL 세부 정보]** 탭에서 _[!UICONTROL 전자 메일 콘텐츠 편집]_&#x200B;을 클릭합니다.

![전자 메일 콘텐츠 편집 ](./assets/add-email-content.png){width="700" zoomable="yes"} 클릭

이 작업은 이메일 디자인 도구를 실행하며, 여기에서 다음 옵션 중 이메일을 디자인할 방법을 선택할 수 있습니다.

* 이메일 Designer 인터페이스를 사용하여 [이메일을 처음부터 디자인하기](#design-your-email-from-scratch).

* [파일 또는 .zip 폴더에서 기존 HTML 콘텐츠를 가져옵니다](#import-existing-html-content).

* 기본 제공 또는 사용자 지정 전자 메일 서식 파일 목록에서 [기존 서식 파일을 선택하십시오](#select-a-template).

이메일 콘텐츠를 만들고 개인화한 후에는 유효성 검사 또는 나중에 사용하기 위해 콘텐츠를 내보낼 수 있습니다. 콘텐츠를 HTML 및 자산을 포함하는 .zip 파일로 저장하려면 **[!UICONTROL HTML 내보내기]**&#x200B;를 클릭합니다.

>[!TIP]
>
>생성형 AI에서 제공하는 Adobe Journey Optimizer B2B edition의 AI Assistant를 사용하여 콘텐츠를 한 차원 높입니다. AI Assistant를 사용하면 전체 이메일, 타겟팅된 텍스트 콘텐츠를 생성하고, 대상자에게 반향을 일으키는 이미지에 대한 AI Assistant 권장 사항을 얻음으로써 게재의 영향을 최적화하는 데 도움이 될 수 있습니다. [자세히 알아보기](./ai-assistant-emails.md)

## 이메일 콘텐츠 처음부터 만들기 {#design-from-scratch}

시각적 콘텐츠 디자인 공간을 사용하여 이메일의 구조와 콘텐츠를 정의합니다. 간단한 드래그 앤 드롭 작업으로 구조 구성 요소를 추가 및 이동하여 초 내에 재사용 가능한 이메일 콘텐츠의 형태를 디자인할 수 있습니다.

1. _[!UICONTROL 템플릿 디자인]_ 홈 페이지에서 **[!UICONTROL 처음부터 디자인]** 옵션을 선택합니다.

1. _[!UICONTROL 전자 메일 만들기]_ 대화 상자에서 작성하려는 전자 메일 콘텐츠의 유형을 선택합니다.

   * **[!UICONTROL 테마 사용]** - _테마 모드_&#x200B;에서 전자 메일을 만들려면 이 옵션을 선택하세요. 이 모드에서는 정의된 브랜드 테마를 사용하여 콘텐츠 작성 프로세스를 간소화하고 디자인이 정의된 표준에 맞게 조정되도록 할 수 있습니다.

   * **[!UICONTROL 수동 스타일 지정]** - _수동 모드_&#x200B;에서 전자 메일을 만들려면 이 옵션을 선택하십시오. 이 모드에서는 빈 캔버스에 추가하는 모든 구조 및 콘텐츠 구성 요소의 스타일을 수동으로 설정합니다.

1. 템플릿에 [구조 및 콘텐츠 추가](./email-authoring.md#add-structure-and-content).

1. [링크 검토 및 업데이트](#preview-and-edit-linked-urls).

1. [이메일을 테스트합니다](#check-and-test-the-email).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual design space for this email after switching to the code editor. -->

내용이 만족스러우면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

## 기존 HTML 콘텐츠 가져오기

{{$include /help/_includes/content-design-import.md}}

![zip 파일에서 html 콘텐츠 가져오기](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>`<table>` 태그를 HTML 파일의 첫 번째 레이어로 사용하면 맨 위 레이어 태그의 배경 및 너비 설정을 포함하여 스타일이 손실될 수 있습니다.

시각적 이메일 편집기 도구를 사용하여 필요에 따라 가져온 콘텐츠를 개인화할 수 있습니다.

## 템플릿 선택

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> 저장된 템플릿에는 하나 이상의 구성 요소에 적용되는 거버넌스(콘텐츠 잠금) 설정이 있을 수 있습니다. [관리되는 템플릿에서 전자 메일을 작성](./email-authoring-governance.md)할 때 비주얼 디자인 스페이스에서 잠긴 구성 요소에 대한 지침을 제공합니다.

## 구조 및 콘텐츠 추가 {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### 사용자 정의 CSS 추가

이메일 디자인 공간 내에 직접 사용자 지정 CSS를 추가할 수 있습니다. 사용자 지정 CSS를 사용하여 콘텐츠의 모양을 보다 유연하게 제어하고, 고급 및 특정 스타일을 적용할 수 있습니다. 이미지, 단추 및 텍스트와 같은 콘텐츠 구성 요소를 포함하기 전에 이 최상위 수준의 스타일을 추가하는 것이 좋습니다.

캔버스에 콘텐츠 구성 요소가 하나 이상 있는 경우 왼쪽 탐색 트리에서 **[!UICONTROL 본문]** 구성 요소를 선택하여 사용자 지정 CSS 편집기에 액세스합니다.

>[!NOTE]
>
>전자 메일 메시지가 잠긴 콘텐츠가 있는 [템플릿을 사용하여 디자인된 경우](./template-content-governance.md), 사용자 지정 CSS를 콘텐츠에 추가할 수 없습니다. 단추 레이블이 **[!UICONTROL 사용자 지정 CSS 보기]**(으)로 변경되고 콘텐츠에 이미 있는 사용자 지정 CSS는 읽기 전용입니다.

![본문 스타일에 액세스](./assets/email-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### 조각 추가

>[!NOTE]
>
>전자 메일 콘텐츠의 _테마 모드_&#x200B;와(과) _수동 모드_ 간에 조각이 상호 호환되지 않습니다. 테마가 적용되는 전자 메일 콘텐츠에서 조각을 사용하려면 _테마 모드_&#x200B;에서도 조각을 만들어야 합니다.

{{$include /help/_includes/content-design-use-fragments.md}}

전자 메일이 저장되면 요약에서 _[!UICONTROL 사용자]_ 탭을 선택하면 조각 세부 정보 페이지에 전자 메일이 표시됩니다.

### 에셋 추가

{{$include /help/_includes/content-design-assets.md}}

### 레이어, 설정 및 스타일 탐색

{{$include /help/_includes/content-design-navigation.md}}

### 콘텐츠 개인화

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>계정 여정에 대해 _[!UICONTROL 내 토큰]_&#x200B;이 정의된 경우 전자 메일 콘텐츠에 대해 이러한 여정 관련 토큰을 사용할 수도 있습니다. 자세한 내용은 [전자 메일 개인화를 위한 사용자 지정 토큰](./personalization-my-tokens.md)을 참조하세요.

### 연결된 URL 추적 편집

{{$include /help/_includes/content-design-links.md}}

### 옵션 보기

시각적 이메일 편집기에서 사용할 수 있는 보기 및 콘텐츠 유효성 검사 옵션을 활용합니다.

* 사전 설정된 확대/축소 옵션에서 콘텐츠를 확대/축소합니다.

* 데스크탑, 모바일 또는 텍스트 전용/일반 텍스트에서 컨텐츠 보기를 전환합니다.
   * 여러 장치에서 콘텐츠를 미리 보려면 _보기_ 아이콘을 클릭하십시오.
   * 기본 제공 장치 중 하나를 선택하거나 사용자 지정 차원을 입력하여 콘텐츠를 미리 봅니다.

## 추가 옵션

시각적 디자인 스페이스 상단의 _[!UICONTROL 자세히...]_ 메뉴에서 다음 작업을 수행할 수 있습니다.

템플릿 작업에 액세스하려면 ![자세히 클릭](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL 전자 메일 재설정]** - 전자 메일 디자인 캔버스를 빈 슬레이트로 지우고 콘텐츠 작성을 다시 시작하려면 이 옵션을 클릭하십시오.
* **[!UICONTROL 조각으로 저장]** - 전자 메일의 전체 또는 일부를 조각으로 저장하여 여러 전자 메일 또는 전자 메일 템플릿에서 다시 사용할 수 있습니다. 조각의 이름과 설명을 입력하고 사용 가능한 조각 목록에 저장합니다.
* **[!UICONTROL 디자인 변경]** - _전자 메일 디자인_ 페이지로 돌아가기. 여기에서 다른 템플릿을 선택하여 디자인 프로세스를 재시작할 수 있습니다. 빈 캔버스(_클래식 모드_)를 사용하거나 [브랜드 테마](./brand-themes.md)(_테마 모드_)를 사용하여 콘텐츠를 처음부터 디자인하도록 선택할 수도 있습니다.
* **[!UICONTROL 콘텐츠 템플릿으로 저장]** - 여러 전자 메일 또는 전자 메일 템플릿에서 재사용할 수 있도록 전자 메일 본문을 전자 메일 템플릿으로 저장합니다. 템플릿의 이름과 설명을 입력하고 저장한 이메일 템플릿 목록에 저장합니다.
* **[!UICONTROL HTML 내보내기]** - zip 파일로 패키지된 HTML 형식의 로컬 시스템에 시각적 캔버스의 콘텐츠를 다운로드합니다.

## 이메일 확인 및 테스트 {#email-testing}

메시지 콘텐츠가 정의되면 테스트 프로필을 사용하여 콘텐츠를 미리 보고, 증명을 보내고, 데스크탑 및 모바일 종횡비로 렌더링을 검토할 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 사용하여 이 콘텐츠가 메시지에 표시되는 방식을 미리 볼 수 있습니다.

[전자 메일 콘텐츠를 미리 보려면](./email-simulate-content.md)하려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하고 테스트 프로필을 선택하여 개인 프로필 데이터를 사용하여 메시지를 확인하세요.

![디자인을 확인하기 위해 전자 메일 콘텐츠 시뮬레이션](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}

추가 도구에 액세스하여 이메일 콘텐츠를 확인하고 검토할 수 있습니다.

* [증명 보내기](./email-simulate-content.md#send-proofs)
* [이메일 클라이언트에서 렌더링 테스트](./email-test-rendering.md)
<!-- * Generate a spam report -->
