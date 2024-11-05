---
title: 이메일 템플릿 작성
description: 계정 여정 이메일에 사용하여 디자인을 쉽고 효율적으로 재사용할 수 있는 콘텐츠 이메일 템플릿을 작성하는 방법을 알아봅니다.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 10%

---

# 이메일 템플릿 작성

[전자 메일 템플릿을 만든](./email-templates.md#create-an-email-template) 후 비주얼 디자이너를 사용하여 전자 메일 템플릿의 구조적 구성 요소와 콘텐츠 구성 요소를 작성합니다.

## 구조 및 콘텐츠 추가 {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="구조 구성 요소 추가"
>abstract="구조 구성 요소는 템플릿 레이아웃을 정의합니다. **구조** 구성 요소를 캔버스로 드래그 앤 드롭하여 템플릿에 대한 콘텐츠 디자인을 시작할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="콘텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 템플릿 레이아웃 제작에 사용할 수 있는 빈 콘텐츠 플레이스홀더입니다."

{{$include /help/_includes/content-design-components.md}}

### 조각 추가

시각적 콘텐츠 편집기에서 _조각_ 아이콘이 왼쪽에 표시됩니다. 다음 예제에서는 템플릿 콘텐츠에 조각을 추가하는 단계에 대해 간략히 설명합니다.

1. 조각 목록을 열려면 _조각_ 아이콘( ![조각 아이콘](../assets/do-not-localize/icon-fragments.svg))을 선택합니다.

   다음과 같은 작업을 수행할 수 있습니다.

   * 목록을 정렬합니다.
   * 목록을 검색 또는 필터링합니다.
   * 썸네일 보기와 목록 보기 간에 전환합니다.
   * 최근에 만들어진 조각을 반영하도록 목록을 새로 고칩니다.

   ![목록에서 조각 선택](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. 조각을 구조 구성 요소 자리 표시자로 끌어서 놓습니다.

   편집기는 이메일 구조의 섹션/요소 내에서 조각을 렌더링합니다.

조각의 콘텐츠는 구조 내에서 동적으로 업데이트되어 이메일에 콘텐츠가 표시되는 방식을 보여 줍니다.

>[!TIP]
>
>조각이 이메일 내의 전체 수평 레이아웃을 차지하도록 하려면 1:1 열 구조를 추가한 다음 조각을 끌어서 놓습니다.

전자 메일이 저장되면 요약에서 _[!UICONTROL 사용자]_ 탭을 선택하면 조각 세부 정보 페이지에 전자 메일이 표시됩니다. 이메일 템플릿에 추가된 조각은 템플릿 내에서 편집할 수 없습니다. 소스 조각은 콘텐츠를 정의합니다.

### 에셋 추가

{{$include /help/_includes/content-design-assets.md}}

### 레이어, 설정 및 스타일 탐색

{{$include /help/_includes/content-design-navigation.md}}

### 콘텐츠 개인화

{{$include /help/_includes/content-design-personalization.md}}

### 연결된 URL 추적 편집

{{$include /help/_includes/content-design-links.md}}

## 옵션 보기

비주얼 디자이너에서 사용할 수 있는 보기 및 콘텐츠 유효성 검사 옵션을 활용합니다.

* 사전 설정된 확대/축소 옵션에서 콘텐츠를 확대/축소합니다.

* 데스크탑, 모바일 또는 텍스트 전용/일반 텍스트에서 컨텐츠 보기를 전환합니다.
   * 여러 장치에서 콘텐트 미리 보기를 위해 _눈_ 아이콘을 클릭합니다.
   * 기본 제공 장치 중 하나를 선택하거나 사용자 지정 차원을 입력하여 콘텐츠를 미리 봅니다.

### 추가 옵션

전자 메일 디자이너 상단의 _[!UICONTROL 자세히...]_ 메뉴에서 다음 작업을 수행할 수 있습니다.

템플릿 작업에 액세스하려면 ![자세히 클릭](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL 템플릿 재설정]** - 비주얼 디자이너 캔버스를 빈 슬레이트로 지우고 빌드 콘텐츠를 다시 시작하려면 이 옵션을 클릭하십시오.
* **[!UICONTROL 조각으로 저장]** - 여러 전자 메일 또는 전자 메일 템플릿에서 재사용할 조각으로 템플릿의 전체 또는 일부를 저장합니다. 조각의 이름과 설명을 입력하고 사용 가능한 조각 목록에 저장합니다.
* **[!UICONTROL 디자인 변경]** - _템플릿 디자인_ 페이지로 돌아가기 여기에서 템플릿을 처음부터 디자인하거나 기존 템플릿을 사용하여 디자인 프로세스를 다시 시작할 수 있습니다.
* **[!UICONTROL HTML 내보내기]** - zip 파일로 패키지된 HTML 형식의 시각적 캔버스에 있는 콘텐츠를 로컬 시스템으로 다운로드합니다.
