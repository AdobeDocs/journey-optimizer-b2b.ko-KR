---
title: 웹 경험 디자인
description: 시각적 및 비시각적 편집기로 웹 경험 디자인 - Journey Optimizer B2B edition에서 수정 사항 추가, 콘텐츠 업데이트 관리, 클릭 추적 활성화 및 콘텐츠 개인화.
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# 웹 경험 디자인

[웹 경험을 만들기](./web-experiences.md#create-a-web-experience)한 후 콘텐츠 디자인 공간을 사용하여 웹 페이지에 적용할 수정 사항을 정의합니다.

>[!BEGINSHADEBOX]

**전제 조건**

웹 경험을 디자인하려면 먼저 다음 요구 사항이 충족되는지 확인하십시오.

* 제품 관리자가 웹 경험에 포함할 URL(페이지)을 정의하도록 하나 이상의 웹 채널을 구성했습니다. 자세한 내용은 [웹 채널 구성](../admin/configure-channels-web.md)을 참조하십시오.

* 웹 사이트에 방문자 식별 및 컨텐츠 전달을 위해 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview)&#x200B;(`alloy.js`)이(가) 구현되었습니다. Adobe Experience Platform Web SDK 버전 2.16 이상이 필요합니다.

* 여정에서 웹 경험을 만들고 관리하는 데 필요한 [권한](../admin/user-management.md#b2b-product-permissions)이 있습니다.
   * _[!UICONTROL 캠페인]_ > _[!UICONTROL 캠페인 관리]_ - 웹 개인화 작업 노드를 추가하거나 업데이트하는 데 필요합니다.
   * _[!UICONTROL 캠페인]_ > _[!UICONTROL 캠페인 보기]_ - 웹 개인화 작업 노드에 대한 세부 정보를 보는 데 필요합니다.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>웹 경험을 디자인하기 전에 웹 브라우저용으로 설치된 Adobe Experience Cloud Visual Editing Helper 브라우저 확장이 있는지 확인하십시오. 이 확장은 Journey Optimizer B2B edition 웹 경험 디자인 공간에서 웹 페이지를 안정적으로 열고, 작성하고, 미리 보는 데 필요합니다.<br/>
>
>Google Chrome 및 Microsoft Edge은 현재 Journey Optimizer B2B edition에서 확장 및 웹 환경 작성을 지원하는 유일한 브라우저입니다. 자세한 내용은 [Visual Editing Helper 확장 기능 설치](./web-experiences.md#install-the-visual-editing-helper-extension)를 참조하십시오.

## 웹 경험 편집기

Journey Optimizer B2B edition은 웹 수정 사항 디자인을 위한 두 가지 유형의 편집기를 제공합니다.

| 편집자 | 설명 | 다음에 최적 |
| ------ | ----------- | -------- |
| [비주얼 편집기](#visual-editor) | 웹 사이트를 표시하고 요소를 직접 선택하고 수정할 수 있는 WYSIWYG(_What You See Is What You Get_) 편집기. Google Chrome 또는 Microsoft Edge 웹 브라우저에서 [Visual Editing Helper 확장 기능](./web-experiences.md#install-the-visual-editing-helper-extension)이 필요합니다. | 텍스트, 이미지, 단추 및 배너 등 표시되는 페이지 요소를 시각적으로 변경합니다. |
| [비시각적 편집기](#non-visual-editor) | 시각적 편집기를 통해 수정할 수 없는 내용을 적용하기 위한 코드 기반 편집기입니다. | 시각적으로 선택하기 어려운 요소를 타겟팅하거나, 고급 CSS 변경 사항을 적용하거나, 숨겨진 요소를 수정합니다. |

웹 경험 속성에서 **[!UICONTROL 시각적 편집기]** 옵션을 사용하여 편집기 유형을 결정합니다. 시각적 편집기를 사용하려면 옵션을 활성화하고, 비시각적 편집기를 사용하려면 옵션을 비활성화합니다.

![비주얼 편집기 옵션 사용](./assets/web-experience-design-visual-editor-option.png){width="400"}

## 비주얼 편집기 {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="찾아보기 모드 사용"
>abstract="이 모드에서는 선택한 웹 채널 구성에 대해 개인화할 정확한 페이지로 이동할 수 있습니다."

시각적 편집기는 iframe 내에 웹 페이지를 로드하며, 여기서 요소를 선택하고 페이지 미리보기에서 직접 수정 사항을 적용할 수 있습니다. 웹 경험을 디자인하기 위해 시각적 편집기를 사용하려면 다음 단계를 완료하십시오.

1. 웹 경험 세부 정보 페이지에 _[!UICONTROL 콘텐츠]_ 탭이 표시된 상태로 오른쪽 패널에서 **[!UICONTROL 웹 경험 편집]**&#x200B;을 클릭합니다.

   시각적 편집기는 웹 채널 구성에 따라 웹 사이트를 로드합니다.

   ![웹 경험 비주얼 편집기](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. 필요한 경우 오른쪽 상단의 **[!UICONTROL 찾아보기]**&#x200B;를 클릭하고 사이트 탐색 모음을 사용하여 수정할 특정 페이지를 로드합니다.

   맨 위의 필드에 페이지 URL을 입력할 수도 있습니다.

   >[!NOTE]
   >
   >로드된 페이지가 웹 채널 구성에 정의된 URL 패턴과 일치하는지 확인합니다. 선택한 웹 채널 구성에 대한 URL 또는 페이지 일치 규칙을 보려면 오른쪽 상단의 **[!UICONTROL 구성 세부 정보 보기]**&#x200B;를 클릭하십시오.

   ![시각적 편집기의 찾아보기 모드](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   디자인 공간에서 페이지를 로드하려면 오른쪽 상단의 **[!UICONTROL 디자인]**&#x200B;을 클릭하세요.

1. 웹 경험에 대해 표시된 페이지를 수정하는 방법을 정의하려면 다음을 수행할 수 있습니다.

   * [웹 환경을 위한 페이지에 새 구성 요소를 삽입](#insert-new-components)(구분선, HTML, 이미지, 제목, 단락 또는 링크)합니다.

   * 페이지에서 이미지, 단추, 단락, 텍스트, 컨테이너, 머리글 또는 링크와 같은 기존 요소를 선택합니다. [웹 경험을 위해 수정](#modify-elements)합니다.

   * 참여를 측정하고 인사이트를 수집할 요소에 대한 [클릭 추적을 추가](#click-tracking-for-web-experiences)합니다.

1. 웹 경험에 포함할 다른 페이지를 로드하려면 2단계를 반복하고 페이지 수정 사항을 정의하려면 3단계를 반복합니다.

1. [수정 사항을 검토하고](#manage-modifications) 필요한 조정 작업을 수행합니다.

1. 수정 사항이 완료되면 편집기 위의 왼쪽 화살표를 클릭하여 웹 경험 속성으로 돌아갑니다.

### 요소 수정

표시된 페이지에서 요소를 클릭하여 선택합니다. 파란색 테두리는 선택한 요소를 나타내며 수정 옵션이 있는 상황별 도구 모음이 나타납니다.

![수정할 요소 선택](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

도구 모음 옵션은 선택한 구성 요소 유형에 따라 다릅니다.

| 액션 | 설명 |
| ------ | ----------- |
| **[!UICONTROL 텍스트 옵션]** | 선택한 요소의 텍스트 요소 클래스 또는 텍스트 스타일을 변경합니다. |
| **[!UICONTROL 이미지 선택]** | 이미지 소스를 바꾸거나 요소에 이미지를 추가합니다. |
| **[!UICONTROL 링크 편집/링크 추가]** | 링크 URL을 수정하거나 추가합니다. |
| **[!UICONTROL 정렬]** | 선택한 요소를 디스플레이 내에서 뒤로 또는 앞으로 이동합니다. |
| **[!UICONTROL 개인화 추가]** | 개인화를 삽입합니다. |
| **[!UICONTROL 추적 요소 클릭]** | 요소에 대한 클릭 추적을 추가합니다. |
| **[!UICONTROL 삭제]** | 페이지에서 선택한 요소를 제거합니다. |

선택한 요소의 경우 오른쪽 패널의 속성이 사용 가능한 스타일 및 작업을 반영하도록 변경됩니다. 패널 맨 위에 있는 작업 아이콘을 클릭하여 선택한 요소를 복제, 클릭 추적, 삭제 또는 숨깁니다.

![선택한 요소의 동작 아이콘을 클릭합니다](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++텍스트 요소

1. 페이지에서 텍스트 요소를 선택합니다.

1. 새 텍스트 콘텐츠를 입력하거나 텍스트 문자열을 선택하고 대체 텍스트를 입력합니다.

1. (선택 사항) 굵게, 기울임꼴, 정렬 등의 [텍스트 서식 옵션](./content-components.md#text)을 사용합니다.

1. 텍스트 요소 외부를 클릭하여 변경 사항을 적용합니다.

텍스트 구성 요소의 텍스트 스타일 옵션에 대한 자세한 내용은 [콘텐츠 구성 요소](./content-components.md#text)를 참조하십시오.

+++

+++이미지 요소

1. 페이지에서 이미지 요소를 선택합니다.

1. 상황별 도구 모음 또는 오른쪽 패널에서 _[!UICONTROL 이미지 선택]_ 아이콘을 클릭합니다.

1. 에셋 라이브러리에서 이미지를 검색하여 선택합니다.

1. 필요에 따라 오른쪽 패널의 [이미지 스타일 옵션](./content-components.md#image)을 사용하십시오.

+++

+++단추 요소

1. 페이지에서 단추 요소를 선택합니다.

1. (선택 사항) 단추에 새 텍스트를 입력하거나 텍스트 문자열을 선택하고 대체 텍스트를 입력합니다.

   개인화를 사용하여 계정 또는 개인 프로필의 데이터를 사용하여 단추 텍스트를 변경할 수 있습니다.

1. 필요에 따라 오른쪽 패널의 [단추 스타일 옵션](./content-components.md#button)을 사용하십시오.

+++

+++ 컨테이너 요소

1. 페이지에서 컨테이너 요소를 선택합니다.

1. 필요에 따라 오른쪽 패널의 [컨테이너 스타일 옵션](./content-components.md#container)을 사용하십시오.

+++

### 새 구성 요소 삽입

시각적 편집기의 디자인 왼쪽 탐색에서 **+** 아이콘을 선택하면 다음 구성 요소 유형을 웹 경험 수정으로 페이지에 추가할 수 있습니다.

* **[!UICONTROL 분할자]** - 이 구성 요소를 사용하여 전자 메일의 레이아웃과 콘텐츠를 구성하는 구분선을 삽입합니다. 오른쪽 패널의 속성에서 선 색상, 스타일 및 높이와 같은 스타일 속성을 조정할 수 있습니다. 자세한 내용은 [콘텐츠 구성 요소](./content-components.md#divider)의 _분할기_&#x200B;를 참조하십시오.
* **[!UICONTROL HTML]** - 이 구성 요소를 사용하여 기존 구조의 HTML 코드를 복사하여 붙여 넣으십시오. 이를 통해 자유 모듈식 HTML 구성 요소를 만들어 일부 외부 콘텐츠를 재사용할 수 있습니다. 자세한 내용은 [콘텐츠 구성 요소](./content-components.md#html)의 _HTML_&#x200B;을(를) 참조하십시오.
* **[!UICONTROL 이미지]** - 이 구성 요소를 사용하여 페이지에 이미지 파일을 삽입합니다. 오른쪽 패널의 속성에서 너비 및 높이와 같은 스타일 속성을 조정할 수 있습니다. 자세한 내용은 [콘텐츠 구성 요소](./content-components.md#image)의 _이미지_&#x200B;를 참조하십시오.
* **[!UICONTROL 제목]** - 이 구성 요소를 사용하여 제목 클래스 텍스트를 삽입합니다. 오른쪽 패널의 속성에서 텍스트 색상, 스타일, 글꼴 및 크기와 같은 스타일 속성을 조정할 수 있습니다. 자세한 내용은 [콘텐츠 구성 요소](./content-components.md#text)의 _텍스트_&#x200B;을(를) 참조하십시오.
* **[!UICONTROL 단락]** - 이 구성 요소를 사용하여 표준 텍스트 요소를 삽입합니다. 오른쪽 패널의 속성에서 텍스트 색상, 스타일, 글꼴 및 크기와 같은 스타일 속성을 조정할 수 있습니다. 자세한 내용은 [콘텐츠 구성 요소](./content-components.md#text)의 _텍스트_&#x200B;을(를) 참조하십시오.
* **[!UICONTROL 링크]** - 이 구성 요소를 사용하여 지정된 URL에 기본 텍스트 링크를 삽입합니다. 오른쪽 패널의 속성에서 텍스트 색상, 스타일, 정렬 및 크기와 같은 스타일 속성을 조정할 수 있습니다.

왼쪽의 구성 요소 유형을 선택한 다음 추가하려는 위치에 인접한 요소를 마우스로 가리킵니다.

![비주얼 편집기 인터페이스 - 새 구성 요소](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

표시된 버튼 중 하나를 클릭하여 구성 요소를 배치합니다.

* ***[!UICONTROL 다음 항목 앞에 삽입]** - 선택한 요소 앞에 구성 요소를 삽입합니다.
* ***[!UICONTROL 다음 항목 뒤에 삽입]** - 선택한 요소 뒤에 구성 요소를 삽입합니다.

삽입할 구성 요소 유형을 선택 취소하려면 페이지 맨 위에 표시된 파란색 상황에 맞는 배너에서 **[!UICONTROL ESC]**&#x200B;을(를) 클릭합니다.

## 비시각적 편집기 {#non-visual-editor}

비주얼 편집기에서 쉽게 수정할 수 없는 내용을 수정해야 하는 경우 비비주얼 편집기를 사용하십시오. 이 코드 기반 접근 방식을 사용하면 요소 타깃팅 및 수정을 정밀하게 제어할 수 있습니다. 다음 단계를 완료하여 비시각적 편집기를 사용하여 웹 경험을 디자인합니다.

1. 웹 경험 세부 정보 페이지에 _[!UICONTROL 콘텐츠]_ 탭이 표시된 상태로 오른쪽 패널에서 **[!UICONTROL 수정 추가]**&#x200B;를 클릭합니다.

   비시각적 편집기는 웹 채널 구성을 기반으로 페이지를 로드합니다.

   ![비시각적 편집기 인터페이스](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. 만들려는 첫 번째 수정 사항을 정의합니다.

   왼쪽 패널에 기존 수정 사항 목록(있는 경우)이 표시됩니다. 새 수정 사항을 정의하려면 **[!UICONTROL 추가]**&#x200B;를 클릭하십시오. 수정 사항이 정의되지 않은 경우 패널은 기본적으로 _[!UICONTROL 수정 사항 추가]_ 옵션으로 설정됩니다.

   * **[!UICONTROL 수정 유형]**&#x200B;을(를) 선택하십시오.

     | 유형 | 설명 |
     | ---- | ----------- |
     | [**[!UICONTROL CSS 선택기]**](#css-selector-modifications) | CSS 선택기 문자열을 사용하여 요소를 타깃팅합니다. |
     | [**[!UICONTROL 페이지]**](#page-modifications) | 사용자 지정 HTML, CSS 또는 JavaScript을 `<head>` 또는 `<body>`과(와) 같은 페이지 수준 요소에 삽입합니다. |

   * 유형에 따라 수정 매개변수를 구성합니다.

      * **[!UICONTROL CSS 선택기]** - 특정 요소를 타깃팅할 올바른 CSS 선택기를 입력하십시오.
      * **[!UICONTROL 작업 유형]** - 수행할 작업(편집, 숨기기, 삭제, 삽입, 바꾸기)을 선택합니다.
      * **[!UICONTROL 콘텐츠]** - 적용할 콘텐츠 또는 스타일을 제공합니다.

1. 수정 사항을 적용하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

### CSS 선택기 수정 사항

CSS 선택기 수정 사항을 사용하면 표준 CSS 선택기 구문을 사용하여 요소를 정확하게 타깃팅할 수 있습니다.

1. 수정 유형으로 **[!UICONTROL CSS 선택기]**&#x200B;을(를) 선택하십시오.

1. **[!UICONTROL CSS 요소 선택기]** 필드에 선택기를 입력합니다.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **예제 선택기:**
    
    | 선택기 | 타겟 |
    | -------- | ------- |
    | &#39;#hero-banner&#39; | ID가 &#39;hero-banner&#39;인 요소 |
    | &quot;.cta-button&quot; | 클래스 &#39;cta-button&#39;이 있는 모든 요소 |
    | &#39;헤더 탐색 a&#39; | 탐색 내의 링크, 헤더 내부 |
    | &quot;[data-offer=&quot;premium&quot;]&quot; | 특정 데이터 속성이 있는 요소 |

1. **[!UICONTROL 작업 유형]**&#x200B;을(를) 선택하고 필요한 정보/콘텐츠를 지정하십시오.

   * **[!UICONTROL 콘텐츠 설정]** - **[!UICONTROL CSS 요소 선택기]** 값으로 식별된 요소의 _[!UICONTROL 콘텐츠]_ 필드에 텍스트를 입력합니다.

   * **[!UICONTROL 특성 설정]** - 이 특성으로 요소를 식별할 수 있도록 현재 CSS 선택기와 연결할 특성을 지정합니다. **[!UICONTROL 특성 이름]** 필드에 이름을 입력하고 **[!UICONTROL 콘텐츠]** 필드에 값을 입력하십시오. 속성이 이미 있으면 값이 업데이트되고, 그렇지 않으면 지정된 이름과 값으로 새 속성이 추가됩니다.

   ![비시각적 편집기 css 선택기 수정](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (선택 사항) **[!UICONTROL 개인화 추가]**&#x200B;를 클릭하고 [개인화 편집기](./personalization.md#personalization-editor)를 사용하여 콘텐츠에 대한 사용자 지정 개인화를 만듭니다.

### 페이지 수정 사항

`<head>` 페이지 수정 형식을 사용하여 사용자 지정 코드를 추가할 수 있습니다. `<head>` 요소는 메타데이터(데이터에 대한 데이터)의 컨테이너이며 `<html>` 태그와 `<body>` 태그 사이에 있습니다. 이 경우 코드는 본문 또는 페이지 로드 이벤트를 기다리지 않고 페이지 로드 시작 시 실행됩니다.

`<head>` 요소는 일반적으로 JavaScript 또는 CSS 코드를 페이지의 맨 위에 추가하는 데 사용됩니다. 후속 시각적 작업을 위한 선택기는 이 탭에 추가된 HTML 요소에 따라 다릅니다.

>[!NOTE]
>
>사용자 지정 코드는 방문자의 브라우저에서 실행됩니다. 코드가 안전하고 테스트되었으며 페이지 성능이나 사용자 경험에 부정적인 영향을 주지 않는지 확인하십시오.

1. 수정 유형으로 **[!UICONTROL 페이지`<head>`]**&#x200B;을(를) 선택하십시오.

1. **[!UICONTROL 콘텐츠]** 상자에 사용자 지정 코드를 추가합니다.

   >[!CAUTION]
   >
   >`<script>` 섹션에는 `<style>` 및 `<head>` 요소만 추가할 수 있습니다. `<div>`개 태그 및 기타 요소를 추가하면 나머지 `<head>`개 요소가 `<body>` 내에 채워질 수 있습니다.

   ![비시각적 편집기 페이지 헤드 수정](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (선택 사항) **[!UICONTROL 개인화 추가]**&#x200B;를 클릭하고 [개인화 편집기](./personalization.md#personalization-editor)를 사용하여 콘텐츠에 대한 사용자 지정 개인화를 만듭니다.

## 수정 사항 관리 {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="손쉽게 모든 변경 내용 관리"
>abstract="이 창을 사용하면 웹 페이지에 대해 정의된 모든 조정 및 추가 사항을 탐색하고 관리할 수 있습니다."

만든 모든 수정 내용은 추적되며 시각적 편집기와 비시각적 편집기 모두의 **[!UICONTROL 수정 사항]** 패널에서 관리할 수 있습니다. 모든 수정 사항을 보려면 왼쪽 도구 모음에서 _[!UICONTROL 수정 사항]_ <!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) -->아이콘을 클릭하십시오.

각 수정 기록에는 다음이 포함됩니다.

* 대상 요소 또는 선택기
* 수정 유형(예: 편집, 숨기기 또는 삽입)
* 변경 사항에 대한 미리보기

![수정 패널](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### 수정 사항 편집

1. _[!UICONTROL 수정 사항]_ 목록에서 편집할 수정 사항을 찾습니다.

1. _추가 메뉴_( **...**) 아이콘을 클릭하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.

1. 필요에 따라 수정 속성을 업데이트합니다.

1. 변경 내용을 저장하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

### 수정 사항 삭제

1. _[!UICONTROL 수정 사항]_ 목록에서 제거할 수정 사항을 찾으십시오.

1. _추가 메뉴_( **...**) 아이콘을 클릭하고 **[!UICONTROL 수정 삭제]**&#x200B;를 선택합니다.

1. 메시지가 표시되면 제거를 확인합니다.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## 수정 사항 미리보기

게시하기 전에 수정 사항이 방문자에게 어떻게 표시되는지 미리 봅니다.

시각적 편집기 상단의 장치 미리 보기 옵션을 사용하여에 대한 수정 사항을 확인합니다.

* 데스크탑
* 태블릿
* 모바일

![미리 보기에 대한 장치 크기 조정 변경](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

미리보기가 업데이트되어 수정 사항이 각 장치 크기에서 렌더링되는 방식을 보여 줍니다.

URL 막대를 사용하여 웹 채널 구성 내의 다른 페이지로 이동합니다. 그런 다음 URL 일치 규칙에 따라 수정 사항이 타겟팅된 페이지에 올바르게 적용되는지 확인하십시오.

## 웹 경험에 대한 클릭 추적 {#web-click-tracking}

요소와의 사용자 상호 작용을 추적하여 참여를 측정하고 통찰력을 수집합니다. 클릭 추적 데이터는 참여 보고서에서 사용할 수 있으며 웹 경험 수정 사항의 효과를 측정하는 데 사용할 수 있습니다.

웹 경험이 활성화(라이브)되면 Adobe Customer Journey Analytics(제품 구독 필요)를 사용하여 보고서를 작성할 수도 있습니다. 웹 경험 모니터링을 개선하기 위해 웹 사이트의 특정 요소에 대한 클릭 수를 추적할 수도 있습니다. 추적을 사용하면 웹 보고서에서 해당 요소의 클릭 수를 표시할 수 있습니다.

Customer Journey Analytics 및 웹 보고서 작성에 대한 자세한 내용은 [Customer Journey Analytics 설명서](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)를 참조하세요.

1. 웹 경험 편집기에서 이미지 또는 링크와 같은 요소를 선택합니다.

1. 요소 속성 또는 상황별 도구 모음에서 _[!UICONTROL 추적 요소 클릭]_ 아이콘을 클릭합니다.

   ![웹 경험 요소에 대한 클릭 추적 사용](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. 왼쪽 패널의 클릭 추적 목록을 열고 **[!UICONTROL 추적된 작업]** 값을 수정하여 보고서에서 이 상호 작용을 식별합니다.

   ![웹 경험에 대한 클릭 추적 ID 설정](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
