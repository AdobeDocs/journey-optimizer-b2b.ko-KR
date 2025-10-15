---
title: 이메일 콘텐츠의 다크 모드
description: Journey Optimizer B2B edition의 다크 모드 이메일 디자인에 대해 알아봅니다. 미리보기 렌더링, 설정 사용자 정의, 접근성 확보 및 이메일 클라이언트 전반에서 테스트합니다.
feature: Email Authoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 다크 모드, 이메일, 색상, 디자인
source-git-commit: 890e7dc012ac08fc112d647f1294f26ce096041b
workflow-type: tm+mt
source-wordcount: '1600'
ht-degree: 6%

---

# 이메일 콘텐츠의 다크 모드 {#dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode"
>title="다크 모드로 전환"
>abstract="다크 모드로 전환하면 어떻게 렌더링되는지 미리 보고 특정 사용자 정의 설정을 정의할 수 있습니다. <br>최종 렌더링은 수신자의 이메일 클라이언트에 따라 다릅니다. 모든 이메일 클라이언트가 사용자 정의 다크 모드를 지원하지 않음에 유의하여 주십시오."

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_preview"
>title="다크 모드로 전환"
>abstract="다크 모드로 전환하여 지원되는 이메일 클라이언트에서 어떻게 렌더링되는지 미리 확인합니다. <br>최종 렌더링은 수신자의 이메일 클라이언트에 따라 다릅니다. 모든 이메일 클라이언트가 다크 모드를 지원하지 않음에 유의하여 주십시오."

_어두운 모드_&#x200B;를 사용하면 지원하는 전자 메일 클라이언트 또는 앱에서 텍스트, 단추 및 기타 시각적 요소에 대해 어두운 배경과 밝은 색상의 전자 메일을 표시할 수 있습니다. 이러한 유형의 디스플레이는 눈의 피로를 줄이고, 배터리 수명을 절약하며, 저조도 환경에서 가독성을 향상시켜 보다 편안한 시청 경험을 제공할 수 있다. 주요 운영 체제 및 앱에서 증가하는 추세로서, 이제 모든 사용자가 콘텐츠를 읽을 수 있고 시각적으로 호소력 있게 사용할 수 있도록 하는 것이 최신 이메일 디자인에서 중요한 고려 사항입니다.

![밝은 테마와 어두운 테마 모두에서 콘텐츠 렌더링을 표시하는 밝은 모드 및 어두운 모드 개념 다이어그램](../assets/do-not-localize/light-dark-mode.svg){width="50%"}

[ 시각적 디자인 공간에서 ](./email-authoring.md)이메일 콘텐츠를 만들기[!DNL Journey Optimizer B2B Edition]할 때 _**[!UICONTROL 어두운 모드]**_ 보기로 전환할 수 있습니다. 이 보기에서 다크 모드가 활성화되면 이메일 클라이언트 지원을 위한 특정 사용자 지정 설정을 정의할 수도 있습니다.

## 이메일 클라이언트 고려 사항

서로 다른 이메일 클라이언트와 앱이 다크 모드를 적용하는 방식에는 상당한 차이가 있습니다. 따라서 다크 모드 렌더링에 대한 기대를 신중하게 고려해야 합니다. 이메일 디자인 공간에서 다크 모드를 사용하기 전에 다음 이메일 클라이언트 사용 사례를 고려하십시오.
<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

+++다크 모드를 지원하지 않는 클라이언트

일부 이메일 클라이언트는 다음과 같이 이 기능을 전혀 지원하지 않습니다.

* [!DNL Yahoo! Mail]
* [!DNL AOL]

이메일 디자인에서 다크 모드 사용자 지정 설정을 정의하는 경우 이러한 이메일 클라이언트는 다크 모드 렌더링을 표시할 수 없습니다. <!--Regardless of whether the interface is in light or dark mode, your email will render the same.-->

+++

+++자체 다크 모드 {#default-support}을(를) 적용하는 클라이언트

일부 이메일 클라이언트는 수신한 모든 이메일에 자체 기본 다크 모드를 체계적으로 적용합니다. 어두운 모드 설정에 따라 색상, 배경, 이미지 및 기타 요소를 자동으로 조정하며 외부 설정은 불가능합니다. 이러한 클라이언트에는 다음이 포함됩니다.

* Gmail(데스크탑 웹 메일, iOS, Android™, 모바일 웹 메일)
* Outlook Windows
* Outlook Windows 메일

<!--It is important to note that less than 25% of email clients offer customization options for dark mode. Clients such as Gmail implement their own dark mode rendering, which is not subject to external modification.-->
이 경우 클라이언트 다크 모드 설정은 [!DNL Journey Optimizer B2B Edition]에서 정의한 사용자 지정 다크 모드 설정보다 우선합니다.

+++

+++사용자 지정 다크 모드를 지원하는 클라이언트

가장 인기 있는 대부분의 전자 메일 클라이언트는 `@media (prefers-color-scheme: dark)` 전자 메일 스타일에 사용되는 메서드인 [!DNL Journey Optimizer B2B Edition] 쿼리를 사용하여 사용자 지정 어두운 모드를 렌더링하는 옵션을 제공합니다. 이 클라이언트 목록에는 다음이 포함됩니다.

* Apple 메일 macOS
* Apple 메일 iOS
* Outlook macOS
* Outlook.com
* Outlook iOS
* Outlook Android™

이 경우 [!DNL Journey Optimizer B2B Edition]에서 정의한 특정 설정이 렌더링됩니다. 그러나 각 이메일 클라이언트에 따라 몇 가지 제한 사항이 적용될 수 있습니다. 예를 들어 일부 클라이언트(예: Apple Mail 16(macOS 13))는 이메일 콘텐츠에 이미지가 있는 경우 다크 모드를 생성하지 않습니다.

최적의 결과를 얻으려면 타겟팅하는 이메일 클라이언트로 콘텐츠를 테스트합니다. 각 클라이언트의 최종 결과에 최대한 근접한 시뮬레이션을 보려면 이메일 디자인 공간에서 [리트머스 이메일 테스트 렌더링](./email-test-rendering.md) 통합을 사용하십시오.

+++

## 다크 모드를 위한 디자인

[!DNL Journey Optimizer B2B Edition]의 다크 모드로 전자 메일 콘텐츠를 스타일링할 때 비주얼 디자인 공간에서는 두 가지 유형의 도구를 제공합니다.

* [미리 보기 기능](#preview-default-dark-mode)을 사용하여 대부분의 지원 전자 메일 클라이언트에 대한 기본 다크 모드 렌더링을 검토하세요.

* 지원되는 이메일 클라이언트에 대한 기본 설정을 무시하려면 이메일 콘텐츠에 사용자 지정 다크 모드 설정을 정의하고 적용하십시오. [자세히 알아보기](#define-custom-dark-mode)

### 기본 다크 모드 미리 보기 {#preview-dark-mode}

<!-- Should work with templates and themes, NOT for LP and fragments - but TBC with eng. 
>[!NOTE]
>
>Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. 이메일 디자인 공간에서 이메일 콘텐츠를 엽니다.

   캔버스의 오른쪽 맨 위에는 컨텐츠 표시를 밝은 모드(기본값)와 어두운 모드 간에 전환하는 밝은 어두운 선택기가 있습니다.

   ![오른쪽 상단의 조명 모드 선택기를 보여주는 전자 메일 디자인 캔버스](./assets/email-color-mode-light-selector.png){width="700" zoomable="yes"}

1. 선택기를 _어두운 모드_( ![어두운 모드 아이콘](../assets/do-not-localize/icon-content-dark-mode.svg) )로 변경합니다.

   캔버스에는 기본 어두운 모드 preview.x를 사용하여 콘텐츠가 표시됩니다

   기본적으로 어두운 모드 미리 보기는 이미지와 아이콘을 제외한 모든 요소에 `full color invert` 색 구성표를 적용합니다. 이 색상 구성표는 밝은 요소와 어두운 요소가 있는 영역을 탐지하고 반전시킵니다. 밝은 배경은 어둡고 어두운 텍스트가 밝아지거나 어두운 배경은 밝고 밝은 텍스트가 어두워집니다.

   ![다크 모드 선택기와 다크 모드로 표시되는 이메일 콘텐츠를 보여 주는 이메일 디자인 캔버스](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

>[!CAUTION]
>
>최종 렌더링은 수신자의 이메일 클라이언트에 따라 달라질 수 있습니다. 각 이메일 클라이언트에 대한 최종 결과에 최대한 가까운 시뮬레이션을 보려면 [리트머스 테스트 이메일 렌더링](./email-test-rendering.md) 통합을 사용하십시오.

### 사용자 정의 다크 모드 설정 정의 {#custom-dark-mode}

>[!CONTEXTUALHELP]
>id="ajo-b2b_dark_mode_image"
>title="다크 모드용 특정 이미지 사용"
>abstract="다크 모드가 켜져 있을 때 표시할 다른 이미지를 선택할 수 있습니다. <br>다크 모드에 대한 특정 이미지를 추가한다고 해서 모든 이메일 클라이언트에서 올바르게 렌더링되는 것은 아닙니다. 모든 이메일 클라이언트가 사용자 정의 다크 모드를 지원하지 않음에 유의하여 주십시오."

다크 모드로 전환한 후에는 수신자의 이메일 클라이언트에서 다크 모드가 활성화되어 있을 때만 표시되는 콘텐츠의 특정 스타일 요소를 편집할 수 있습니다(해당 기능이 지원되는 경우).

>[!NOTE]
>
>다크 모드 최종 렌더링은 각 이메일 클라이언트에 따라 다르므로 결과가 서로 다를 수 있습니다. 자세한 내용은 [전자 메일 클라이언트 고려 사항](#email-client-considerations)을 검토하십시오.

이메일 디자인 공간에서 사용자 지정 어두운 모드 스타일은 <!-- `@media (prefers-color-scheme: dark)` method-->을(를) 사용합니다. `@media (prefers-color-scheme: dark)` CSS 쿼리로, 전자 메일 클라이언트가 다크 모드로 설정되어 있는지 여부를 감지하고 전자 메일에 정의된 다크 테마 디자인을 적용합니다.

사용자 지정 어두운 모드 설정을 정의하려면(_T):_

1. 필요한 경우 선택기를 디자인 캔버스의 오른쪽 상단에 있는 _어두운 모드_( ![어두운 모드 아이콘](../assets/do-not-localize/icon-content-dark-mode.svg) )로 이동합니다.

1. 텍스트, 배경 또는 단추와 같은 모든 스타일 색상 속성을 편집합니다.

   ![색상 및 글꼴 옵션을 보여 주는 어두운 모드 텍스트 스타일 설정 패널](./assets/email-color-mode-dark-text-settings.png){width="700" zoomable="yes"}

1. 이미지 및 아이콘의 경우 다크 모드에만 특정 에셋을 정의합니다.

   이미지와 아이콘의 색상을 변경할 수는 없지만 다크 모드에 사용할 대체 에셋을 정의할 수는 있습니다. 아이콘에 대해 다양한 색상 조합을 실험하거나 사진 이미지의 색상 및 채도를 조정할 수 있습니다.

   ![다른 색 조합을 사용하는 아이콘](../assets/do-not-localize/color-contrast-images-diagram.svg){width="80%"}

   이미지를 선택하고 **[!UICONTROL 설정]** 창의 전용 토글을 사용하여 **[!UICONTROL 어두운 모드]**(으)로 전환하십시오. 그런 다음 다른 이미지 자산을 선택합니다.

   ![다크 모드에 대해 다른 이미지 자산을 선택하는 옵션을 표시하는 다크 모드 이미지 설정](./assets/email-color-mode-dark-image-settings.png){width="700" zoomable="yes"}

   이미지 자산 선택에 대한 자세한 내용은 [이미지 자산 추가](./email-authoring.md#add-image-assets)를 참조하십시오.

1. 디자인을 변경하는 동안 언제든지 **[!UICONTROL 라이브 보기로 전환]**&#x200B;을 선택하여 콘텐츠가 다양한 장치 크기에서 어떻게 렌더링되는지 확인하십시오.

   이 보기에서 선택기를 _어두운 모드_( ![어두운 모드 아이콘](../assets/do-not-localize/icon-content-dark-mode.svg) )로 변경하여 다른 장치에서 콘텐츠의 어두운 모드 버전을 미리 봅니다.

   ![다양한 장치 크기에서 어두운 모드로 전자 메일 콘텐츠를 표시하는 실시간 보기 패널](./assets/email-color-mode-dark-live-view.png){width="800" zoomable="yes"}

   >[!CAUTION]
   >
   >라이브 보기는 다양한 장치 크기에서 렌더링이 어떻게 표시될 수 있는지 비교하도록 설계된 일반 미리 보기입니다. 최종 렌더링은 수신자의 이메일 클라이언트에 따라 달라질 수 있습니다.

1. 다크 모드 변경이 완료되면 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭하세요.

   ![어두운 모드를 테스트하기 위해 강조 표시된 콘텐츠 시뮬레이션 버튼이 있는 전자 메일 디자인 캔버스](./assets/email-color-mode-dark-simulate-content.png){width="700" zoomable="yes"}

   미리 보기 및 증명 도구를 사용하여 이메일 디자인을 테스트합니다. 자세한 내용은 [전자 메일 콘텐츠 미리 보기 및 테스트](./email-simulate-content.md)를 참조하십시오.

1. Litmus Enterprise 계정이 있는 경우 **[!UICONTROL 전자 메일 렌더링]**&#x200B;을 선택하여 Litmus의 다양한 전자 메일 클라이언트에 대한 최종 다크 모드 렌더링을 확인합니다.

   자세한 내용은 [Litmus를 사용하여 전자 메일 렌더링 테스트](./email-test-rendering.md)를 참조하십시오.

   >[!CAUTION]
   >
   >시뮬레이션은 이메일이 다크 모드로 표시되는 방식과 거의 유사하지만 실제 렌더링은 이메일 서비스 공급자 또는 장치 수준 설정의 변경으로 인해 달라질 수 있습니다.

## 모범 사례 {#best-practices}

주요 이메일 클라이언트에서 다크 모드 채택이 증가함에 따라 [사용자 지정 다크 모드](#define-custom-dark-mode)를 사용하는지 여부에 관계없이 밝은 환경과 어두운 환경 모두에서 이메일이 렌더링되는 방식을 고려해야 합니다.

어두운 모드는 색상, 배경 및 이미지를 변경할 수 있으며 디자인 선택 사항을 오버라이드할 수도 있습니다. 시각적 일관성, 접근성 및 브랜드 무결성을 보장하려면 다음 모범 사례를 따르십시오.

| 연습 |            |
| -------- | ---------- |
| 이미지 및 로고 최적화 | 체크리스트:<ul><li>어두운 모드에서 흰색 상자가 보이지 않도록 로고와 아이콘을 투명 배경이 있는 PNG 파일로 저장합니다. <li>흰색 또는 밝은 배경이 하드코딩된 이미지를 사용하지 마십시오. <li>투명도가 옵션이 아닌 경우 디자인에서 단색 배경에 이미지를 배치하여 어색한 색상 반전을 방지합니다. |
| 배경 살펴보기 | 체크리스트:<ul><li>밝은 모드와 어두운 모드 모두에서 가독성을 위해 텍스트와 배경색 간의 충분한 대비를 보장합니다. <li>중요한 콘텐츠에 배경색에만 의존하지 마십시오. 일부 클라이언트는 어두운 모드에서 배경색을 재정의하므로 키 정보가 계속 표시되는지 확인합니다. |
| 다크 모드로 액세스 가능한 콘텐츠 디자인 | 체크리스트:<ul><li>색맹이 있는 사람들을 구별하기 쉬운 색상 조합을 사용하십시오. <li>중간 색조 팔레트를 사용하여 밝은 배경과 어두운 배경의 대비를 보장합니다. <li>높은 대비로 접근성 있는 색상 조합을 사용하여 가독성을 높이고 [!DNL Web Content Accessibility Guidelines (WCAG)] 표준을 충족합니다. [!DNL WebAIM Contrast Checker]과(와) 같은 도구를 사용하여 색상 대비를 확인합니다. <li>가독성에 영향을 줄 수 있으므로 가는 글꼴을 사용하지 마십시오. 브랜드에 얇은 글꼴이 필요한 경우 어두운 모드에서 굵게 표시합니다. <li>눈의 피로를 유발할 수 있고 일부 이메일 클라이언트에서 자동으로 반전될 수 있는 순수한 검정에서 순수한 흰색을 건너뜁니다. <li>다크 모드가 지원되지 않는 경우 액세스 가능한 대체 스타일을 제공합니다. |
| 다크 모드 환경에서 이메일 테스트 | 체크리스트:<ul><li>역색 구성표를 사용하여 문제를 조기에 발견할 수 있는 이메일 디자인 공간에서 [어두운 모드 미리 보기](#preview-dark-mode)를 사용하십시오. <li>[[!UICONTROL 이메일 렌더링]](./email-test-rendering.md) 옵션과 함께 Litmus Enterprise 계정을 사용하여 주요 이메일 클라이언트(Apple Mail, Gmail 및 Outlook 등)에서 디자인을 시뮬레이션하고 어두운 모드에서 색상과 이미지가 어떻게 작동하는지 확인합니다. |

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->
