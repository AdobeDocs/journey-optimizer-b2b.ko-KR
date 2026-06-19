---
title: 랜딩 페이지 만들기 및 게시
description: Journey Optimizer B2B edition에서 여정을 위한 랜딩 페이지를 만들고, 디자인하고, 게시합니다. 처음부터 빌드하고, HTML을 가져오고, 양식을 추가하고, 콘텐츠를 개인화하고, 이메일을 통해 연결합니다.
feature: Landing Pages, Content
role: User
autotag-review: '2026-05-27T16:10:09.537Z'
TQID: 'https://experienceleague.adobe.com/e-tguY-9v6CPOehYL7vI22fzQBk3L0h1EOpa-e54q7A'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e4bd5f48-22a4-465d-a046-5ffb52e27856
source-git-commit: 144848cff6a37691ccbe7a83b78f9db33d8a2b3d
workflow-type: tm+mt
source-wordcount: 1719
ht-degree: 9%

---

# 랜딩 페이지 만들기 및 게시

마케터는 계정 및 개인 여정에 통합할 페이지를 정의하고 게시할 수 있습니다. 새 랜딩 페이지를 추가할 때 기본 페이지와 하위 페이지를 구성하고, 콘텐츠를 디자인하고, 테스트하고, 게시합니다.

![랜딩 페이지 워크플로 다이어그램](./assets/landing-page-work-flow-diagram-no-subpages.svg)

>[!BEGINSHADEBOX]

## 랜딩 페이지 사전 요구 사항 {#landing-page-prerequisites}

마케터가 랜딩 페이지를 만들어 여정 및 캠페인을 지원하려면 먼저 다음 구성 및 자산을 사용해야 합니다.

* [랜딩 페이지 하위 도메인](../admin/configure-channels-landing-pages.md#lp-subdomains) - 랜딩 페이지 호스팅 전용 하위 도메인을 설정합니다.
* [랜딩 페이지 사전 설정](../admin/configure-channels-landing-pages.md#lp-presets) - 사전 설정은 랜딩 페이지에 적용되는 하위 도메인 및 기타 설정을 정의합니다.
* [양식](./forms.md)(데이터 캡처 사용 사례의 경우) - 양식을 랜딩 페이지에 포함하고 데이터를 Experience Platform에 제출하려는 경우 필요합니다.
  <!-- * Subscription list (for subscription use cases) - Required if you want customers to subscribe to or unsubscribe from a specific service. This is in AJO B2C-->

>[!ENDSHADEBOX]

## 랜딩 페이지 만들기 {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_create"
>title="랜딩 페이지 정의 및 구성"
>abstract="랜딩 페이지를 만들려면 사전 설정을 선택한 다음 기본 페이지와 하위 페이지를 구성하고 게시하기 전에 마지막으로 테스트해야 합니다."

1. 왼쪽 탐색으로 이동하여 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 랜딩 페이지]**&#x200B;를 선택합니다.

1. 오른쪽 상단의 **[!UICONTROL 랜딩 페이지 만들기]**&#x200B;를 클릭합니다.

1. 페이지에서 유용한 **[!UICONTROL 제목]**(필수)과 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   제목 및 설명 기준:

   * 제목 - 최대 100자이며, 고유해야 하며 대소문자를 구분하지 않습니다.

   * 설명 - 최대 300자

   * Alpha, 숫자 및 특수 문자가 허용됩니다.

   * 예약된 문자가 **_허용되지 않음_**: `\ / : * ? " < > |`

   ![랜딩 페이지 만들기](./assets/landing-page-create.png){width="600"}

1. **[!UICONTROL 사전 설정]**&#x200B;을 선택하세요.

   제품 관리자 [은(는) 랜딩 페이지에 사용되는 하위 도메인 및 기타 설정을 정의하기 위해 사전 설정을 구성](../admin/configure-channels-landing-pages.md#lp-presets)합니다. 사전 설정을 선택한 다음 **[!UICONTROL 사전 설정 보기]**&#x200B;를 클릭하여 사전 설정 세부 정보를 열고 설정을 확인하여 랜딩 페이지 요구 사항과 일치하는지 확인할 수 있습니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   기본 페이지와 해당 속성이 표시됩니다.

   ![새 랜딩 페이지 - 기본 페이지 속성](./assets/landing-page-primary-new-properties.png){width="700" zoomable="yes"}

## 기본 페이지 구성 {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_primary_page"
>title="기본 페이지 설정 정의"
>abstract="수신자가 이메일 또는 웹 사이트에서 랜딩 페이지 링크를 클릭하면 즉시 표시될 기본 페이지를 정의합니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_lp_access_settings"
>title="랜딩 페이지 URL 정의"
>abstract="이 섹션에서는 고유 랜딩 페이지 URL을 정의합니다. URL의 첫 번째 부분의 경우 선택한 사전 설정의 일부로 랜딩 페이지 하위 도메인을 이전에 설정해 두었어야 합니다."

1. 필요에 따라 **[!UICONTROL 페이지 이름]**&#x200B;을 변경합니다. 기본적으로 _기본 페이지_&#x200B;입니다.

1. 페이지 URL의 끝 부분을 정의합니다.

   선택한 사전 설정에 따라 URL의 첫 번째 부분이 결정됩니다.

   >[!CAUTION]
   >
   >랜딩 페이지 URL은 고유해야 합니다.
   >
   >이 URL을 게시한 경우에도 웹 브라우저에 복사하여 붙여넣으면 랜딩 페이지에 액세스할 수 없습니다. 미리보기 기능을 사용하여 테스트합니다.

1. 익명 랜딩 페이지를 원하는 경우 **[!UICONTROL 식별된 사용자 필요]** 옵션을 비활성화하십시오.

   <!-- The option 'Require identified users' would be visible in both AJO & AJOB2B when the Landing page is of type 'Data capture' -->

1. _달력_( ![달력 아이콘](../assets/do-not-localize/icon-calendar.svg)) 아이콘을 클릭하여 **[!UICONTROL 페이지 만료]**&#x200B;를 설정합니다.

   만료 날짜를 선택한 후 페이지 만료 시 작업을 선택합니다.

   * **[!UICONTROL 리디렉션 URL]** - 리디렉션으로 사용할 페이지의 URL을 입력합니다.

     ![랜딩 페이지 만료 - 리디렉션 URL](./assets/landing-page-expiry-redirect-url.png){width="400"}

     <!-- * **[!UICONTROL Custom page]** - Configure a subpage and select it from the list. -->
   * **[!UICONTROL 브라우저 오류]** - 페이지 대신 표시할 오류 텍스트를 입력하십시오.

     ![랜딩 페이지 만료 - 브라우저 오류](./assets/landing-page-expiry-browser-error.png){width="400"}

## 콘텐츠 디자인 유형 선택 {#choose-design-type}

페이지에 대한 _[!UICONTROL 컨텐츠]_&#x200B;를 추가하려면 **[!UICONTROL Designer 열기]**&#x200B;를 클릭합니다. _[!UICONTROL 기본 랜딩 페이지 만들기]_ 홈 페이지가 로드되고 디자인 프로세스는 디자인을 시작할 방법을 선택하는 것으로 시작됩니다.

* [[!UICONTROL 처음부터 디자인]](#design-from-scratch)
* [[!UICONTROL 직접 코드 작성]](#code-your-own)
* [[!UICONTROL HTML 가져오기]](#import-html)
* [랜딩 페이지 템플릿 사용](#select-template)

![랜딩 페이지 디자인을 시작할 방법을 선택하세요](./assets/landing-page-create-design.png){width="800" zoomable="yes"}

랜딩 페이지 디자인을 시작하기 위한 기본 방법을 선택한 후 시각적 디자인 도구를 사용하여 [페이지 콘텐츠를 완료](./landing-page-design.md)합니다.

### 처음부터 디자인 {#design-from-scratch}

시각적 콘텐츠 편집기를 사용하여 랜딩 페이지 콘텐츠의 구조를 정의합니다. 간단한 드래그 앤 드롭 작업으로 구조 구성 요소를 추가 및 이동하여 페이지 콘텐츠의 형태를 몇 초 이내에 디자인할 수 있습니다.

1. _[!UICONTROL 기본 랜딩 페이지 만들기]_ 홈 페이지에서 **[!UICONTROL 처음부터 디자인]** 옵션을 선택합니다.

1. 페이지 콘텐츠에 대한 스타일을 관리하는 방법을 선택하십시오.

   * **[!UICONTROL 테마 사용]** - _테마 모드_&#x200B;에서 페이지 콘텐츠를 만들려면 이 옵션을 선택하십시오. 이 모드에서는 정의된 [브랜드 테마](./brand-themes.md)를 사용하여 콘텐츠 작성 프로세스를 간소화하고 디자인이 정의된 표준에 부합하는지 확인할 수 있습니다.

   * **[!UICONTROL 수동 스타일 지정]** - _수동 모드_&#x200B;에서 페이지 콘텐츠를 만들려면 이 옵션을 선택하십시오. 이 모드에서는 빈 캔버스에 추가하는 모든 구조 및 콘텐츠 구성 요소의 스타일을 수동으로 설정합니다.

1. **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

1. 페이지에 [구조 및 콘텐츠 추가](./landing-page-design.md#structure-content-landing-page).

### 나만의 코드 작성 {#code-your-own}

_직접 코드 작성_&#x200B;을 통해 원시 HTML을 작성하거나 붙여 넣어 디자인 공간에서 직접 페이지 콘텐츠를 작성할 수 있습니다. 마크업을 완전히 제어해야 할 때 이 모드를 사용합니다. 이 모드를 사용하려면 HTML 기술이 있어야 합니다.

이 모드를 선택하면 코드 편집기에 계속 남아 있으므로 비주얼 편집기로 전환할 수 없습니다.

1. _[!UICONTROL 기본 랜딩 페이지 만들기]_ 홈 페이지에서 **[!UICONTROL 직접 코드 작성]** 옵션을 선택합니다.

1. 원시 HTML 코드를 입력하거나 붙여넣습니다.

페이지 콘텐츠를 지우고 새 디자인에서 시작하려면 옵션 메뉴에서 **[!UICONTROL 디자인 변경]**&#x200B;을 선택하세요.

### HTML 가져오기 {#import-html}

Adobe Journey Optimizer B2B edition을 사용하면 기존 HTML 콘텐츠를 가져와서 랜딩 페이지를 디자인할 수 있습니다.

{{$include /help/_includes/content-design-import.md}}

![zip 파일에서 html 콘텐츠 가져오기](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>`<table>` 태그를 HTML 파일의 첫 번째 레이어로 사용하면 맨 위 레이어 태그의 배경 및 너비 설정을 포함하여 스타일이 손실될 수 있습니다.

필요에 따라 시각적 디자인 공간을 사용하여 가져온 콘텐츠를 개인화할 수 있습니다.

### 템플릿 선택 {#select-template}

[!BADGE Beta]{type=Informative tooltip="Beta 기능"}

랜딩 페이지 템플릿을 사용하려면 다음 중 하나를 선택할 수 있습니다.

* **샘플 템플릿**. Journey Optimizer B2B edition 인터페이스는 랜딩 페이지 디자인의 시작점으로 사용할 수 있는 기본 랜딩 페이지 템플릿 컬렉션을 제공합니다.

* **저장된 템플릿**. _[!UICONTROL 템플릿]_ 메뉴 <!-- or the _[!UICONTROL Save as content template]_ option when designing a landing page. -->을(를) 사용하여 조직의 멤버가 만든 저장된 사용자 지정 템플릿을 사용하십시오.

_[!UICONTROL 디자인 템플릿 선택]_ 섹션을 사용하여 템플릿에서 콘텐츠 작성을 시작하십시오. Journey Optimizer B2B edition 인스턴스에서 샘플 템플릿 또는 저장된 사용자 지정 랜딩 페이지 템플릿을 사용할 수 있습니다.

>[!BEGINTABS]

>[!TAB 저장된 템플릿]

_기본 랜딩 페이지 만들기_ 홈 페이지에는 기본적으로 _샘플 템플릿_ 탭이 표시됩니다. 사용자 지정 템플릿을 사용하려면 **[!UICONTROL 저장된 템플릿]** 탭을 선택하십시오.

저장된 모든 랜딩 페이지 템플릿 목록이 표시됩니다. _[!UICONTROL 이름]_, _[!UICONTROL 마지막 수정 날짜]_ 및 _[!UICONTROL 마지막 생성 날짜]_&#x200B;별로 정렬할 수 있습니다.

![저장된 템플릿 선택](./assets/landing-page-design-saved-templates-sort-by.png){width="700" zoomable="yes"}

미리 보기를 표시할 템플릿 썸네일을 선택합니다. 미리보기 모드에서 오른쪽 및 왼쪽 화살표를 사용하여 한 범주(선택에 따라 샘플 또는 저장됨)의 모든 템플릿 사이를 이동할 수 있습니다.

![저장된 템플릿 미리 보기](./assets/landing-page-design-saved-template-preview.png){width="800" zoomable="yes"}

표시와 사용할 항목이 일치하면 미리 보기 창의 오른쪽 상단에 있는 **[!UICONTROL 이 서식 파일 사용]**&#x200B;을 클릭합니다.

이 작업은 콘텐츠를 필요에 따라 편집할 수 있는 시각적 디자인 공간으로 복사합니다.

<!-- 
>[!NOTE]
>
>Saved templates may have governance (content locking) settings applied to one or more components. The design tools provide guidelines about locked components when you [author content from a governed template](./email-authoring-governance.md). 
-->

>[!TAB 샘플 템플릿]

Adobe Journey Optimizer B2B edition은 고유한 랜딩 페이지 및 랜딩 페이지 템플릿을 만드는 데 사용할 수 있는 _즉시 사용 가능한_ 랜딩 페이지 템플릿을 제공합니다.

<!-- ![Choose a sample template provided by Adobe](../assets/content-design-shared/templates-design-samples.png){width="800" zoomable="yes"} -->

>[!ENDTABS]

## 경고 확인 {#check-alerts}

랜딩 페이지 콘텐츠를 디자인할 때 주요 설정이 누락된 경우 오른쪽 상단에 경고가 표시됩니다.

![페이지 콘텐츠 문제에 대한 알림](./assets/alerts-button.png){width="250"}

이 단추가 표시되지 않으면 발견된 문제가 없습니다.

경고에는 두 가지 유형이 있습니다.

* 권장 사항 및 모범 사례를 참조하는 **_경고_**:

   * `Placeholder links are present in the landing page body`: 자리 표시자를 올바른 링크로 바꾸는 것을 잊지 마십시오.

   * `Text version of HTML is empty`: 페이지 본문의 텍스트 버전을 정의해야 합니다. 텍스트 버전은 HTML 콘텐츠를 표시할 수 없을 때 사용됩니다.

   * `Empty link is present in page body`: 페이지의 모든 링크가 올바른지 확인하십시오.

* 여정/캠페인을 테스트하거나 활성화하지 못하는 **_오류_**(예:

   * `The landing page content is empty`: 페이지 컨텐츠는 필수입니다.

## 랜딩 페이지 테스트 {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b_preview_lp_profiles"
>title="랜딩 페이지 미리보기 및 테스트"
>abstract="랜딩 페이지 설정 및 콘텐츠가 정의된 후 테스트 프로필을 사용하여 페이지를 미리보기할 수 있습니다."

랜딩 페이지 설정 및 콘텐츠가 정의되면 테스트 프로필을 사용하여 페이지를 미리 볼 수 있습니다. [개인 맞춤화된 콘텐츠](./personalization.md)를 삽입한 경우 테스트 프로필 데이터를 사용하여 이 콘텐츠가 랜딩 페이지에 표시되는 방식을 확인할 수 있습니다.

>[!PREREQUISITES]
>
>랜딩 페이지를 미리 보고 테스트하려면 **[!UICONTROL 메시지 게시]** 권한과 [테스트 프로필](../audiences/test-profiles.md)을 포함하는 정의된 데이터 세트가 있어야 합니다.

1. 테스트 프로필 선택을 열려면 **[!UICONTROL 미리 보기 및 테스트]**&#x200B;를 클릭하십시오.

   >[!NOTE]
   >
   >시각적 디자인 영역에 있는 경우 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 사용할 수도 있습니다.

1. _[!UICONTROL 시뮬레이션]_ 화면에서 테스트 프로필을 선택합니다.

   ![선택한 프로필에 대한 랜딩 페이지 콘텐츠 시뮬레이션](./assets/landing-page-simulate.png){width="700" zoomable="yes"}

   필요한 프로필이 목록에 없으면 **[!UICONTROL 테스트 프로필 관리]**&#x200B;를 클릭하여 알려진 [테스트 프로필](../audiences/test-profiles.md) 전자 메일 주소를 사용하고 목록에 추가하십시오.

   +++테스트 프로필 추가

   **[!UICONTROL ID 네임스페이스]**&#x200B;의 경우 _Select_( ![Select 아이콘](../assets/do-not-localize/icon-select-data.svg) ) 아이콘을 클릭하고 프로필을 테스트하는 데 사용할 `Email` 네임스페이스를 선택하십시오.

   ![테스트 프로필 설정 전자 메일 ID 네임스페이스 관리](./assets/manage-test-profiles.png){width="700" zoomable="yes"}

   **[!UICONTROL ID 값]** 필드에 테스트 프로필을 식별할 전자 메일 주소를 입력하고 **[!UICONTROL 프로필 추가]**&#x200B;를 클릭합니다. 이 작업을 반복하여 여러 프로필을 추가할 수 있습니다.

   ![테스트 프로필 관리 프로필 추가](./assets/manage-test-profiles-add.png){width="700" zoomable="yes"}

   왼쪽 상단의 뒤로 화살표를 클릭하여 _[!UICONTROL 시뮬레이션]_ 페이지로 돌아갑니다.

   +++

1. **[!UICONTROL 미리 보기 열기]**&#x200B;를 선택하여 랜딩 페이지를 테스트합니다.

   랜딩 페이지 미리보기가 새 탭에서 열립니다. 선택한 테스트 프로필 데이터가 개인화된 요소를 대체합니다.

   ![프로필 데이터가 있는 랜딩 페이지 미리 보기](assets/landing-page-preview.png){width="600"}

1. 다른 테스트 프로필을 선택하여 랜딩 페이지의 각 변형에 대한 렌더링을 미리 봅니다.

## 페이지 게시 {#publish-landing-page}

>[!PREREQUISITES]
>
>랜딩 페이지를 게시하려면 **[!UICONTROL 메시지 게시]** 권한이 있어야 합니다.  게시하기 전에 [모든 경고를 확인 및 해결](#check-alerts)하세요.

초안 페이지가 조건을 충족하고 여정 메시지에서 페이지를 연결할 수 있도록 하려면 오른쪽 상단의 **[!UICONTROL 게시]**&#x200B;를 클릭하십시오. 확인 대화 상자에서 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

![게시용 확인 대화 상자](./assets/landing-page-publish-confirm.png){width="250"}

랜딩 페이지가 게시되면 랜딩 페이지 목록에 **_[!UICONTROL 게시됨]_** 상태로 표시됩니다. 즉, 라이브가 되어 여정을 통해 전송된 이메일, SMS 또는 WhatsApp 메시지에 사용할 준비가 되었습니다.

URL을 웹 브라우저에 복사하여 붙여 넣으면 게시된 랜딩 페이지에 액세스할 수 없습니다. [미리 보기 함수](#test-landing-page)를 사용하여 언제든지 테스트할 수 있습니다.

특정 보고서를 통해 랜딩 페이지 영향을 모니터링할 수 있습니다.
