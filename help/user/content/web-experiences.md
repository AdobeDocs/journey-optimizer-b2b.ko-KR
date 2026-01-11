---
title: 웹 경험
description: 계정 여정을 위한 개인화된 웹 경험을 만들고, 디자인하고, 게시합니다. - Journey Optimizer B2B edition의 웹 사이트 방문자에게 타겟팅된 콘텐츠 수정 사항을 제공합니다.
feature: Content, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
source-git-commit: 30bb44f9c308cd144a53a60b4f420380df5528e4
workflow-type: tm+mt
source-wordcount: '1497'
ht-degree: 1%

---

# 웹 경험

Adobe Journey Optimizer B2B edition의 웹 채널을 사용하면 웹 사이트에서 직접 개인화된 경험을 만들 수 있으므로 의미 있는 방식으로 고객과 연결할 수 있습니다. 이 기능은 맞춤형 콘텐츠와의 참여를 강화하고 이메일 및 SMS와 같은 다른 채널과 원활하게 통합하는 데 사용할 수 있는 유연한 툴킷을 제공합니다.

웹 경험을 통해 다음과 같은 작업을 수행할 수 있습니다.

* 타겟팅된 웹 사이트 방문자에게 개인화된 콘텐츠 수정 사항 제공
* 계정 속성에 따라 배너, 텍스트, 이미지 및 버튼과 같은 웹 사이트 요소를 사용자 정의합니다.
* URL 일치 규칙을 사용하여 특정 페이지를 타깃팅하거나 여러 페이지에 변경 사항 적용
* 참여를 추적하고 웹 개인화 노력의 영향을 모니터링합니다.

>[!BEGINSHADEBOX]

## 사전 요구 사항

웹 경험을 만들려면 먼저 다음 요구 사항이 충족되는지 확인하십시오.

* 제품 관리자가 웹 경험에 포함할 URL(페이지)을 정의하도록 하나 이상의 웹 채널을 구성했습니다. 자세한 내용은 [웹 채널 구성](../admin/configure-channels-web.md)을 참조하십시오.

* 웹 사이트에 방문자 식별 및 컨텐츠 전달을 위해 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/js/js-overview)&#x200B;(`alloy.js`)이(가) 구현되었습니다. Adobe Experience Platform Web SDK 버전이 2.16 이상인지 확인하십시오.

* 여정에서 웹 경험을 만들고 관리하는 데 필요한 [권한](../admin/user-management.md#b2b-product-permissions)이 있습니다.
   * _[!UICONTROL 캠페인]_ > _[!UICONTROL 캠페인 관리]_ - 웹 개인화 작업 노드를 추가하거나 업데이트하는 데 필요합니다.
   * _[!UICONTROL 캠페인]_ > _[!UICONTROL 캠페인 보기]_ - 웹 개인화 작업 노드에 대한 세부 정보를 보는 데 필요합니다.
   * _[!UICONTROL 캠페인]_ > _[!UICONTROL 캠페인 승인 및 게시]_ - 하나 이상의 웹 개인화 작업 노드가 있는 여정을 게시하는 데 필요합니다.

* 웹 브라우저용으로 Adobe Experience Cloud [Visual Editing Helper 브라우저 확장 기능](#install-the-visual-editing-helper-extension)이 설치되어 있습니다. 이 확장은 Journey Optimizer B2B edition 콘텐츠 디자인 공간으로 웹 페이지를 안정적으로 열고, 작성하고, 미리 보는 데 필요합니다.

  >[!NOTE]
  >
  >Google Chrome 및 Microsoft Edge은 현재 Journey Optimizer B2B edition에서 웹 페이지 작성을 지원하는 유일한 브라우저입니다.

>[!ENDSHADEBOX]

## Visual Editing Helper 확장 기능 설치

1. 브라우저에서 새 탭을 엽니다([!DNL Google Chrome] 또는 [!DNL Microsoft Edge]).

1. [Google Chrome 웹 스토어](https://chromewebstore.google.com/category/extensions)로 이동합니다.

   [!DNL Microsoft Edge]을(를) 사용하는 경우 상단 배너의 다른 스토어에서 _확장 허용_&#x200B;을(를) 선택하십시오. 이 옵션을 활성화하면 [!DNL Chrome Web Store]에서 [!DNL Microsoft Edge]&#x200B;(으)로 확장을 추가할 수 있습니다.

1. _[!DNL Adobe Experience Cloud Visual Editing Helper]_&#x200B;브라우저 확장을 검색하여 탐색합니다.

   ![Google Chrome용 Adobe Experience Cloud Visual Editing Helper 확장 기능](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. 확인 대화 상자에서 **[!UICONTROL Chrome에 추가]**&#x200B;를 클릭한 다음 **[!UICONTROL 확장 추가]**&#x200B;를 클릭합니다.

   [!DNL Microsoft Edge]을(를) 사용하는 경우 이 작업은 확장을 [!DNL Edge]에 추가합니다.

1. 브라우저 도구 모음에 [!DNL Visual Editing Helper] 브라우저 확장이 올바르게 활성화되어 있는지 확인하십시오.

   ![Adobe Experience Cloud Chrome 도구 모음의 Google Visual Editing Helper 확장 기능 아이콘](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

이제 웹 경험용 Journey Optimizer B2B edition 비주얼 편집기에서 웹 사이트를 열면 [!DNL Adobe Experience Cloud Visual Editing Helper]이(가) 자동으로 활성화됩니다. 확장 기능에는 조건부 설정이 없으며 SameSite 쿠키 설정을 포함하여 모든 설정을 자동으로 처리합니다.

>[!NOTE]
>
>다음 이유 중 하나로 인해 일부 웹 사이트가 Journey Optimizer B2B edition 웹 편집기에서 안정적으로 열리지 않을 수 있습니다.
>
>* 웹 사이트에는 엄격한 보안 정책이 있습니다.
>* 웹 사이트가 iframe으로 되어 있습니다.
>* 고객 QA 또는 스테이지 사이트를 외부에서 사용할 수 없습니다(사이트가 내부임).

## 웹 경험 만들기

[여정에 _[!UICONTROL 작업 추가]_ 노드 추가](../journeys/action-nodes.md)하고 다음 작업을 수행하면 노드에서 웹 경험을 설정할 수 있습니다.

1. _[!UICONTROL Action on]_ 대상에 대해 **[!UICONTROL 사람]**&#x200B;을 선택하세요.

1. _[!UICONTROL 사용자에 대한 작업]_&#x200B;에 대해 **[!UICONTROL 웹 경험 개인화]**&#x200B;를 선택하세요.

![작업 수행 - 웹 경험 개인화](./assets/web-experience-add-journey-node.png){width="500"}

1. **[!UICONTROL 웹 경험 만들기]**&#x200B;를 클릭합니다.

1. _[!UICONTROL 웹 경험 만들기]_ 대화 상자에서 유용한 **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   * 이름 - 최대 100자이며, 고유해야 하며 대소문자를 구분하지 않습니다.

   * 설명 - 최대 300자

   >[!NOTE]
   >
   >이름 및 설명 필드는 영문자, 숫자 및 특수 문자를 지원합니다. 예약된 문자(`\ / : * ? " < > |`)는 **_허용되지 않습니다_**.

   ![웹 경험 대화 상자 만들기](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. **[!UICONTROL 속성]** 탭에서 웹 경험에 대한 설명을 입력합니다.

1. **[!UICONTROL 작업]** 탭을 클릭하고 웹 경험에 사용할 **[!UICONTROL 웹 채널]**&#x200B;을 선택합니다.

   웹 채널 구성은 구성된 페이지 일치 규칙을 기반으로 콘텐츠 수정 사항의 적용 위치를 결정합니다. 자세한 내용은 [웹 채널 구성](../admin/configure-channels-web.md)을 참조하십시오.

   ![선택한 웹 채널 구성](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. 웹 수정 사항을 정의하려면 **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭합니다.

   편집기가 _[!UICONTROL 콘텐츠]_ 탭에서 열리고 여기서 웹 경험에 대한 수정 사항을 정의할 수 있습니다. 디자인 도구를 사용하여 웹 경험 콘텐츠 수정 사항을 추가하는 방법에 대한 자세한 내용은 [웹 경험 디자인](./web-experience-design.md)을 참조하십시오.

1. 오른쪽 패널에서 정의 및 관리 방법에 따라 웹 경험 속성을 설정합니다.

   * **[!UICONTROL 시각적 편집기]** - 웹 경험 수정 디자인을 위해 [시각적 및 비시각적 편집기](./web-experience-design.md#web-design-tools) 간을 전환합니다.
   * **[!UICONTROL 방문자 리디렉션]** - 콘텐츠 탭에서 새 변형을 작성하는 대신 [방문자를 다른 기존 URL로 리디렉션](#redirect-to-url)하려면 이 옵션을 사용합니다.

   ![시각적 편집기의 속성을 전환하고 URL을 리디렉션합니다](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"}

1. **[!UICONTROL 웹 페이지 편집]**&#x200B;을 클릭하여 [웹 수정 사항을 디자인](./web-experience-design.md)합니다.

1. 수정이 완료되면 편집기 위의 왼쪽 화살표를 클릭하여 콘텐츠 탭과 개인화된 웹 경험 노드 속성으로 돌아갑니다.

   맨 위에 있는 왼쪽 화살표를 클릭하여 여정 캔버스로 돌아갈 수 있습니다.

## 웹 경험 편집

1. 여정을 열고 **[!UICONTROL 웹 경험 개인화]** 작업 노드를 선택합니다.

1. 웹 채널 구성 또는 콘텐츠를 변경하려면 **[!UICONTROL 웹 경험 편집]**&#x200B;을 클릭하세요.

1. **[!UICONTROL 작업]** 탭을 선택하고 필요에 따라 웹 구성을 변경합니다.

1. **[!UICONTROL 콘텐츠]** 탭을 선택하고 필요에 따라 시각적 디자인 도구를 사용하십시오.

   * _비주얼 편집기_ - **[!UICONTROL 콘텐츠 편집]**&#x200B;을 클릭합니다.
   * _시각적이지 않은 편집기_ - **[!UICONTROL 수정 추가]**&#x200B;를 클릭합니다.

   자세한 내용은 [웹 경험 디자인](./web-experience-design.md)을 참조하세요.

1. 수정 정의가 완료되면 편집기 위의 왼쪽 화살표를 클릭하여 콘텐츠 탭과 웹 경험 속성으로 돌아갑니다.

   맨 위에 있는 왼쪽 화살표를 클릭하여 여정 캔버스로 돌아갈 수 있습니다.

## URL로 리디렉션

웹 경험을 만들 때 콘텐츠 편집기에서 새로운 변형을 작성하는 대신 방문자를 다른 기존 URL로 리디렉션할 수 있습니다. 이 옵션은 페이지 내의 몇 가지 요소만 변경하는 대신 두 개의 다른 경험을 비교하는 콘텐츠 실험을 실행하려는 경우에 유용합니다.

예를 들어 다음 두 가지 처리를 사용하여 웹 캠페인을 만듭니다.

처리 A에서 타겟팅된 모집단의 절반에 대해 콘텐츠 편집기를 사용하여 웹 경험을 작성하십시오.

처리 B에서 대상 모집단의 나머지 절반에 대해 _[!UICONTROL URL로 리디렉션]_ 옵션을 선택합니다. Journey Optimizer B2B edition 외부에서 작성한 대체 디자인이 있는 페이지의 URL을 입력합니다.

![방문자를 특정 URL로 리디렉션하도록 방문자 리디렉션 설정](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"}

>[!NOTE]
>
>이 옵션을 선택하면 웹 사이트 미리 보기가 표시되지 않고 _[!UICONTROL 시각적 편집기]_ 전환이 비활성화됩니다.

웹 캠페인이 라이브 상태일 때는 Journey Optimizer B2B edition에서 정의한 웹 경험이 대체 페이지로의 리디렉션을 사용한 웹 경험에 대해 어떻게 작동하는지 추적할 수 있습니다.

## 웹 경험 테스트

웹 환경에 대한 콘텐츠 디자인이 완료되면 _콘텐츠 시뮬레이션_ 기능을 사용하여 웹 페이지 수정 사항을 미리 볼 수 있습니다. 개인화된 콘텐츠를 삽입한 경우 테스트 프로필 데이터를 사용하여 콘텐츠가 렌더링되는 방식을 확인할 수 있습니다. 시뮬레이션 도구는 웹 환경의 _[!UICONTROL 콘텐츠]_ 탭이나 콘텐츠 비주얼 디자인 편집기에서 사용할 수 있습니다.

1. 오른쪽 상단의 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭합니다.

1. 테스트 프로필을 선택합니다.

1. 테스트 프로필 데이터를 사용하여 웹 페이지를 확인하는 테스트 프로필을 추가합니다.

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## 웹 경험 활성화

[여정을 게시](../journeys/create-publish-journey.md#publish-an-account-journey)할 때 웹 경험이 활성화되고 대상자에게 표시됩니다. 여정을 통해 웹 경험을 활성화하기 전에 다음 사항을 고려하십시오.

* 이미 라이브 상태인 다른 여정과 동일한 페이지에 영향을 주는 웹 경험이 있는 여정을 게시하는 경우 모든 변경 사항이 웹 페이지에 적용됩니다.

* 여러 여정이 웹 사이트의 동일한 요소를 업데이트하는 경우 가장 최근에 적용된 변경 사항이 우선합니다.

### 게재 요구 사항

웹 경험 전달을 활성화하려면 다음 설정을 정의해야 합니다.

* Adobe Experience Platform 데이터 수집에서 Adobe Experience Platform 서비스 아래에 Adobe Journey Optimizer B2B edition 옵션이 활성화된 데이터 스트림이 정의되어 있는지 확인합니다.

  이 구성은 Adobe Experience Platform Edge이 인바운드 이벤트를 올바르게 처리할 수 있도록 합니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/datastreams/configure)

* Adobe Experience Platform에서 _[!UICONTROL Active-On-Edge 병합 정책]_ 옵션이 활성화된 하나의 병합 정책이 있는지 확인하십시오.

  고객 > 프로필 > 정책 병합 Experience Platform 메뉴에서 정책을 선택합니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  이 병합 정책은 Journey Optimizer B2B edition 인바운드 채널에서 에지에서 인바운드 웹 경험을 올바르게 활성화하고 게시하는 데 사용됩니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/merge-policies/ui-guide)

### 문제 해결

Adobe Experience Platform Assurance 내의 Edge Delivery 보기를 사용하여 Journey Optimizer B2B edition 웹 경험 전달 문제를 해결할 수 있습니다. 이 플러그인을 사용하면 요청 호출을 자세히 검사하고, 예상 Edge 호출을 확인하고, 프로필 데이터를 검사할 수 있습니다. 이 프로필 데이터에는 ID 맵, 세그먼트 멤버십 및 동의 설정이 포함됩니다. 요청에 대한 자격 조건을 갖춘 활동 및 자격 조건을 갖추지 않은 활동을 검토할 수도 있습니다.

Assurance의 Edge Delivery 보기에 대한 자세한 내용은 [Experience Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/view/edge-delivery)를 참조하세요.
