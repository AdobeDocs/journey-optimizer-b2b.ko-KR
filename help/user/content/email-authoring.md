---
title: 이메일 메시지 작성
description: Adobe Journey Optimizer B2B에서 이메일 콘텐츠를 만드는 방법을 알아봅니다. 템플릿, HTML 가져오기 및 AI 기반 도구를 사용하여 이메일 커뮤니케이션을 개인화하고 최적화합니다.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 15%

---

# 이메일 메시지 작성

[여정 작업 노드에 새 <!-- or duplicated --> 이메일 자산을 추가](./add-email.md)한 후 이메일 메시지의 콘텐츠를 정의할 수 있습니다.

_[!UICONTROL 전자 메일]_ 미리 보기 패널 위쪽에 있는 **[!UICONTROL 전자 메일 콘텐츠 추가]**&#x200B;를 클릭합니다.

![전자 메일 콘텐츠 추가 ](./assets/add-email-content.png){width="700" zoomable="yes"} 클릭

이 작업은 이메일 디자인 도구를 실행하며, 여기에서 다음 옵션 중 이메일을 디자인할 방법을 선택할 수 있습니다.

* 이메일 Designer 인터페이스를 사용하여 [이메일을 처음부터 디자인하기](#design-your-email-from-scratch).

* [파일 또는 .zip 폴더에서 기존 HTML 콘텐츠를 가져옵니다](#import-existing-html-content).

* 기본 제공 또는 사용자 지정 전자 메일 서식 파일 목록에서 [기존 서식 파일을 선택하십시오](#select-a-template).

표현식 편집기로 제목 줄을 구성하고 개인화하려면 _Personalization_ 아이콘을 클릭하고 Marketo Engage 토큰을 추가합니다.

이메일 콘텐츠를 만들고 개인화한 후에는 유효성 검사 또는 나중에 사용하기 위해 콘텐츠를 내보낼 수 있습니다. 콘텐츠를 HTML 및 자산을 포함하는 .zip 파일로 저장하려면 **[!UICONTROL HTML 내보내기]**&#x200B;를 클릭합니다.

>[!TIP]
>
>생성형 AI에서 제공하는 Adobe Journey Optimizer B2B edition의 AI Assistant를 사용하여 콘텐츠를 한 차원 높입니다. AI Assistant를 사용하면 전체 이메일, 타겟팅된 텍스트 콘텐츠를 생성하고, 대상자에게 반향을 일으키는 이미지에 대한 AI Assistant 권장 사항을 얻음으로써 게재의 영향을 최적화하는 데 도움이 될 수 있습니다. [자세히 알아보기](./ai-assistant-emails.md)

## 이메일 콘텐츠 처음부터 만들기 {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="구조 구성 요소 추가"
>abstract="구조 구성 요소는 랜딩 페이지 레이아웃을 정의합니다. **구조** 구성 요소를 캔버스로 드래그 앤 드롭하여 랜딩 페이지의 콘텐츠 디자인을 시작할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="콘텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 랜딩 페이지 레이아웃 제작에 사용할 수 있는 빈 콘텐츠 플레이스홀더입니다."

시각적 콘텐츠 편집기를 사용하여 이메일 콘텐츠 구조를 정의합니다. 간단한 드래그 앤 드롭 작업으로 구조 구성 요소를 추가 및 이동하여 초 내에 재사용 가능한 이메일 콘텐츠의 형태를 디자인할 수 있습니다.

1. _[!UICONTROL 템플릿 디자인]_ 홈 페이지에서 **[!UICONTROL 처음부터 디자인]** 옵션을 선택합니다.

1. 전자 메일 메시지에 [구조 및 콘텐츠를 추가](#add-structure-and-content)합니다.
1. 전자 메일 메시지에 [이미지 자산 추가](#add-assets).
1. [전자 메일 콘텐츠 개인화](#personalize-content).
1. [링크 검토 및 업데이트](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

콘텐츠가 완료되면 맨 위에 있는 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하여 렌더링을 확인합니다. 데스크탑 또는 모바일 보기를 선택할 수 있습니다.

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
> 저장된 템플릿에는 하나 이상의 구성 요소에 적용되는 거버넌스(콘텐츠 잠금) 설정이 있을 수 있습니다. 비주얼 디자이너는 [관리되는 템플릿에서 전자 메일을 작성](./email-authoring-governance.md)할 때 잠긴 구성 요소에 대한 지침을 제공합니다.

## 구조 및 콘텐츠 추가 {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="구조 구성 요소 추가"
>abstract="구조 구성 요소는 이메일 레이아웃을 정의합니다. **구조** 구성 요소를 캔버스로 드래그 앤 드롭하여 이메일 콘텐츠 디자인을 시작할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="콘텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 이메일 레이아웃 제작에 사용할 수 있는 빈 콘텐츠 플레이스홀더입니다."

{{$include /help/_includes/content-design-components.md}}

### 조각 추가

{{$include /help/_includes/content-design-use-fragments.md}}

전자 메일이 저장되면 요약에서 _[!UICONTROL 사용자]_ 탭을 선택하면 조각 세부 정보 페이지에 전자 메일이 표시됩니다.

### 에셋 추가

{{$include /help/_includes/content-design-assets.md}}

### 레이어, 설정 및 스타일 탐색

{{$include /help/_includes/content-design-navigation.md}}

### 콘텐츠 개인화

{{$include /help/_includes/content-design-personalization.md}}

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

### 추가 옵션

전자 메일 디자인 영역 상단의 _[!UICONTROL 자세히...]_ 메뉴에서 다음 작업을 수행할 수 있습니다.

템플릿 작업에 액세스하려면 ![자세히 클릭](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL 전자 메일 재설정]** - 시각적 전자 메일 디자이너 캔버스를 빈 슬레이트로 지우고 콘텐츠 작성을 다시 시작하려면 이 옵션을 클릭합니다.
* **[!UICONTROL 조각으로 저장]** - 전자 메일의 전체 또는 일부를 조각으로 저장하여 여러 전자 메일 또는 전자 메일 템플릿에서 다시 사용할 수 있습니다. 조각의 이름과 설명을 입력하고 사용 가능한 조각 목록에 저장합니다.
* **[!UICONTROL 디자인 변경]** - _전자 메일 디자인_ 페이지로 돌아가기. 여기에서 다른 템플릿을 선택하여 디자인 프로세스를 다시 시작하거나, 검정색 캔버스에 컨텐츠를 처음부터 디자인하도록 선택할 수 있습니다.\
* **[!UICONTROL 콘텐츠 템플릿으로 저장]** - 여러 전자 메일 또는 전자 메일 템플릿에서 재사용할 수 있도록 전자 메일 본문을 전자 메일 템플릿으로 저장합니다. 템플릿의 이름과 설명을 입력하고 저장한 이메일 템플릿 목록에 저장합니다.
* **[!UICONTROL HTML 내보내기]** - zip 파일로 패키지된 HTML 형식의 로컬 시스템에 시각적 캔버스의 콘텐츠를 다운로드합니다.

## 이메일 확인 및 테스트 {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="콘텐츠 렌더링 방식 확인"
>abstract="콘텐츠가 정의되면 미리 보고 사용 중인 채널에 대해 렌더링이 올바른지 확인할 수 있습니다."

메시지 콘텐츠가 정의된 경우 테스트 프로필을 사용하여 콘텐츠를 미리 보고, 증명을 보내고, 인기 있는 데스크탑, 모바일 및 웹 기반 클라이언트에서 렌더링을 제어할 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 사용하여 이 콘텐츠가 메시지에 표시되는 방식을 미리 볼 수 있습니다.

전자 메일 콘텐츠를 미리 보려면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭한 다음 테스트 프로필을 추가하여 테스트 프로필 데이터를 사용하여 메시지를 확인하세요.

![디자인을 확인하기 위해 전자 메일 콘텐츠 시뮬레이션](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
