---
title: 이메일 템플릿 작성
description: 계정 여정 이메일에 사용하여 디자인을 쉽고 효율적으로 재사용할 수 있는 콘텐츠 이메일 템플릿을 작성하는 방법을 알아봅니다.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: f8d70f2e1cff6055ff353bad0c5a0f625d426db8
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 3%

---

# 이메일 템플릿 작성

[전자 메일 템플릿을 만든](./email-templates.md#create-an-email-template) 후 시각적 디자인 공간을 사용하여 전자 메일 템플릿의 구조적 구성 요소와 콘텐츠 구성 요소를 작성합니다.

## 구조 및 콘텐츠 추가 {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### 사용자 정의 CSS 추가

이메일 템플릿 디자인 공간 내에 직접 사용자 지정 CSS를 추가할 수 있습니다. 사용자 지정 CSS를 사용하여 콘텐츠의 모양을 보다 유연하게 제어하고, 고급 및 특정 스타일을 적용할 수 있습니다. 이미지, 단추 및 텍스트와 같은 구성 요소를 포함하기 전에 이 최상위 수준의 스타일을 추가하는 것이 좋습니다.

캔버스에 콘텐츠 구성 요소가 하나 이상 있는 경우 왼쪽 탐색 트리에서 **[!UICONTROL 본문]** 구성 요소를 선택하여 사용자 지정 CSS 편집기에 액세스합니다.

![본문 스타일에 액세스](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### 조각 추가

>[!NOTE]
>
>전자 메일 콘텐츠의 _테마 모드_&#x200B;와(과) _수동 모드_ 간에 조각이 상호 호환되지 않습니다. 테마가 적용되는 전자 메일 콘텐츠에서 조각을 사용하려면 _테마 모드_&#x200B;에서도 조각을 만들어야 합니다.

{{$include /help/_includes/content-design-use-fragments.md}}

템플릿을 저장한 후 요약에서 _[!UICONTROL 사용한 사람]_ 탭을 선택하면 조각 세부 정보 페이지에 해당 템플릿이 표시됩니다.

### 에셋 추가

{{$include /help/_includes/content-design-assets.md}}

### 레이어, 설정 및 스타일 탐색

{{$include /help/_includes/content-design-navigation.md}}

### 콘텐츠 개인화

{{$include /help/_includes/content-design-personalization-email.md}}

### 연결된 URL 추적 편집

{{$include /help/_includes/content-design-links.md}}

## 옵션 보기

시각적 디자인 공간에서 사용할 수 있는 보기 및 콘텐츠 유효성 검사 옵션을 활용합니다.

* 사전 설정된 확대/축소 옵션에서 콘텐츠를 확대/축소합니다.

* 데스크탑, 모바일 또는 텍스트 전용/일반 텍스트에서 컨텐츠 보기를 전환합니다.
   * 여러 장치에서 콘텐트 미리 보기를 위해 _눈_ 아이콘을 클릭합니다.
   * 기본 제공 장치 중 하나를 선택하거나 사용자 지정 차원을 입력하여 콘텐츠를 미리 봅니다.

### 추가 옵션

전자 메일 디자인 영역 상단의 _[!UICONTROL 자세히...]_ 메뉴에서 다음 작업을 수행할 수 있습니다.

템플릿 작업에 액세스하려면 ![자세히 클릭](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL 템플릿 재설정]** - 디자인 캔버스를 빈 슬레이트로 지우고 빌드 콘텐츠를 다시 시작하려면 이 옵션을 클릭합니다.
* **[!UICONTROL 조각으로 저장]** - 여러 전자 메일 또는 전자 메일 템플릿에서 재사용할 조각으로 템플릿의 전체 또는 일부를 저장합니다. 조각의 이름과 설명을 입력하고 사용 가능한 조각 목록에 저장합니다.
* **[!UICONTROL 디자인 변경]** - _전자 메일 디자인_ 페이지로 돌아가기. 여기에서 다른 템플릿을 선택하여 디자인 프로세스를 재시작할 수 있습니다. 빈 캔버스(_클래식 모드_)를 사용하거나 [브랜드 테마](./brand-themes.md)(_테마 모드_)를 사용하여 콘텐츠를 처음부터 디자인하도록 선택할 수도 있습니다.
* **[!UICONTROL HTML 내보내기]** - zip 파일로 패키지된 HTML 형식의 로컬 시스템에 시각적 캔버스의 콘텐츠를 다운로드합니다.
