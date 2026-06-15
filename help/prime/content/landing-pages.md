---
title: 랜딩 페이지
description: 개인 여정을 위한 랜딩 페이지를 만들고, 디자인하고, 게시합니다. Journey Optimizer B2B Prime에서 처음부터 빌드하고, HTML을 가져오고, 양식을 추가하고, 콘텐츠를 개인화하고, 이메일을 통해 연결합니다.
autotag-review: '2026-06-12T22:53:39.337Z'
TQID: 'https://experienceleague.adobe.com/BvtB0i5CzlVutPA6HAzZy-Gfymw7ppZwthyBauyciLc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: e666e996-b2cf-4c45-8fc2-1c625212ababid: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: a96755d6-1f54-4f3f-a971-d31f83705ab7id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 21f0ab524176df40128212fef920e10b06b5c317
workflow-type: tm+mt
source-wordcount: 2180
ht-degree: 4%

---

# 랜딩 페이지

랜딩 페이지는 연락처와 고객이 이메일, SMS 메시지 또는 디지털 위치에서 연결된 항목을 클릭한 후 직접 연락할 수 있는 독립 실행형 웹 페이지입니다. 이러한 페이지를 여정에 통합하여 잠재 고객과 고객이 웹에서 메시지를 보고 여정에서 진행되는 과정을 확인할 수 있습니다. 랜딩 페이지 시각적 디자인 공간에서 랜딩 페이지를 만들고, 개인화하고, 미리 볼 수 있습니다.

랜딩 페이지의 일반적인 사용 사례:

* 마케팅 커뮤니케이션 또는 특정 서비스에 대한 옵트인 또는 옵트아웃을 제공합니다. 이메일이나 다른 커뮤니케이션에서 타겟팅된 목록에 대한 링크를 사용하십시오.
* 통신을 보내기 전에 동의를 수집하고 옵트인 또는 옵트아웃 시 확인 이메일을 보냅니다.
* 랜딩 페이지의 양식을 사용하여 프로필 데이터(점진적 프로파일링, 환경 설정, 등록 및 유사한 시나리오)를 캡처하거나 업데이트합니다.
* 여정 오케스트레이션에 맞게 디자인된 캠페인 관련 정보를 대상자에게 안내합니다.
* Journey Optimizer B2B Prime 외부에서 외부 페이지를 작성하지 않고 전용 웹 양식으로 사용자를 리디렉션합니다.

<!-- 
## Landing page workflow

To direct members of a journey audience to a defined web page when they click a specific link, create a landing page in Journey Optimizer B2B Edition: 


1. [Create the page](./landing-pages-create-publish.md) - Select a preset, set up the primary page, and add any required subpages.
1. [Design the landing page content](./landing-page-design.md) - Build the page content using drag-and-drop visual design components.
1. [Test the landing page](./landing-pages-create.md) - Preview the page, test form behavior, and then publish to make it live.
1. [Link to the page from your journey](#link-to-a-landing-page) - Add the landing page URL to an email, SMS, or journey action so that recipients can reach it.


For example, you can create and design landing pages to direct your users to online information. The page could include a form where they can opt in or opt out from receiving your communications. Or it could be an opportunity to subscribe to a recurring communications, such as a newsletter. 

You can create, personalize, and preview landing pages in the visual design space.
-->

## 랜딩 페이지 액세스 및 관리 {#access-manage-landing-pages}

Journey Optimizer B2B Prime의 랜딩 페이지에 액세스하려면 왼쪽 탐색으로 이동하여 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 랜딩 페이지]**&#x200B;를 클릭하십시오. 이 작업은 인스턴스에서 만든 모든 랜딩 페이지 목록을 표시합니다.

목록은 _[!UICONTROL 수정됨]_ 열에 따라 정렬되며 가장 최근에 업데이트된 항목이 맨 위에 있습니다. 오름차순과 내림차순 간을 변경하려면 열 제목을 클릭합니다.

### 랜딩 페이지 목록 필터링 {#filter-list}

이름별로 랜딩 페이지를 검색하려면 검색 막대에 일치 항목 텍스트 문자열을 입력합니다. _필터_ 아이콘(![필터 표시 또는 숨기기 아이콘](../../user/assets/do-not-localize/icon-filter.svg) )을 클릭하여 사용 가능한 필터 옵션을 표시하고 설정을 변경하여 지정된 조건에 따라 표시된 항목을 필터링합니다.

![표시된 랜딩 페이지를 필터링](./assets/landing-pages-list-filtered.png){width="800" zoomable="yes"}

<!-- 
This is going away? ### Customize the column display

Customize the columns that you want to display in the table by clicking the _Customize table_ icon ( ![Customize table icon](../assets/do-not-localize/icon-column-settings.svg) ) at the top right. 

In the dialog, select the columns to display and click **[!UICONTROL Apply]**.

![Select the columns that you want to display](./assets/landing-pages-customize-table-dialog.png){width="300"} 
-->

### 랜딩 페이지 상태 및 라이프사이클 {#landing-page-status}

랜딩 페이지 상태는 이메일 및 SMS 콘텐츠에서 연결에 대한 가용성과 이에 대해 수행할 수 있는 변경 사항을 결정합니다.

| 상태 | 설명 |
| -------------------- | ----------- |
| 초안 | 랜딩 페이지를 만들 때 초안 상태입니다. 이 상태는 시각적 콘텐츠를 정의하거나 편집할 때 호스팅되는 페이지로 게시할 때까지 이 상태로 유지됩니다. 사용 가능한 작업: <br/><ul><li>이름 또는 설명 편집</li><li>링크 URL 편집</li><li>시각적 디자인 공간에서 편집</li><li>게시</li><li>복제</li><li>삭제</li></ul> |
| 게시일 | 랜딩 페이지를 게시하면 Journey Optimizer B2B Prime 인스턴스에서 호스팅되며 이메일 또는 SMS 메시지 콘텐츠에서 연결할 수 있습니다. 사용 가능한 작업: <br/><ul><li>이름 또는 설명 편집</li><li>링크 URL 편집</li><li>이메일 또는 SMS 메시지 콘텐츠에 링크 추가</li><li>초안 버전 만들기</li><li>복제</li><li>삭제</li></ul> |
| 초안과 함께 게시됨 | 게시된 랜딩 페이지에서 초안을 만들면 게시된 버전이 유지되고 시각적 디자인 공간에서 초안 콘텐츠를 수정할 수 있습니다. 초안 버전을 게시하면 현재 게시된 버전이 대체되고 호스팅된 페이지에서 콘텐츠가 업데이트됩니다. 사용 가능한 작업: <br/><ul><li>이름 또는 설명 편집</li><li>링크 URL 편집</li><li>이메일 또는 SMS 메시지 콘텐츠에 링크 추가</li><li>시각적 디자인 공간에서 초안 버전 편집</li><li>초안 버전 게시</li><li>복제</li><li>삭제(두 버전 모두 삭제)</li><li>초안 삭제(게시된 상태로 돌아가기)</li></ul> |

<!-- ![Landing page status lifecycle](./assets/status-lifecycle-diagram.png){zoomable="yes"} -->

## 랜딩 페이지 만들기 {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_create"
>title="랜딩 페이지 정의 및 구성"
>abstract="랜딩 페이지를 만들려면 사전 설정을 선택한 다음 기본 페이지와 하위 페이지를 구성하고 게시하기 전에 마지막으로 테스트해야 합니다."

개인 여정 대상의 구성원이 특정 링크를 클릭할 때 정의된 웹 페이지로 이동하려면 [!DNL Journey Optimizer B2B Prime]에 랜딩 페이지를 만드십시오. 사전 설정을 선택하고, 기본 페이지와 하위 페이지를 구성하고, [페이지를 테스트하고](#test-landing-page)게시합니다.

>[!IMPORTANT]
>
>첫 번째 랜딩 페이지를 만들기 전에 랜딩 페이지 설정을 완료합니다. 여기에는 랜딩 페이지를 호스팅하도록 하위 도메인을 구성하는 작업과 하위 도메인 및 기타 채널 설정을 지정하는 하나 이상의 사전 설정을 정의하는 작업이 포함됩니다. 랜딩 페이지를 만들 때 사전 설정을 선택합니다. 관리자 설정에 대해서는 [랜딩 페이지 구성](../admin/configuration-presets-landing-pages.md)을 참조하십시오.
>
>데이터 캡처 사용 사례의 경우 랜딩 페이지에 임베드하기 전에 [양식](./forms.md)을(를) 만드십시오.

랜딩 페이지를 만들려면 다음 단계를 수행합니다.

1. 왼쪽 탐색으로 이동하여 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 랜딩 페이지]**&#x200B;를 선택합니다.

1. 랜딩 페이지 목록에서 **[!UICONTROL 랜딩 페이지 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 제목]**(필수) 및 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   제목 및 설명 기준:

   * **제목** — 최대 100자. 고유해야 합니다(대/소문자 구분 안 함).
   * **설명** — 최대 300자.
   * Alpha, 숫자 및 특수 문자가 허용됩니다.
   * 예약된 문자가 **_허용되지 않음_**: `\ / : * ? " < > |`

1. **[!UICONTROL 사전 설정]**&#x200B;을 선택하세요.

   관리자 [랜딩 페이지에 사용되는 하위 도메인 및 기타 설정을 정의하는 랜딩 페이지 사전 설정을 만듭니다](../admin/configuration-presets-landing-pages.md#lp-presets). 사전 설정을 선택한 다음 **[!UICONTROL 사전 설정 보기]**&#x200B;를 클릭하여 설정을 검토하고 랜딩 페이지 요구 사항과 일치하는지 확인하십시오.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   기본 페이지와 해당 속성이 표시됩니다. [기본 페이지 설정을 구성](#configure-primary-page)하는 방법에 대해 알아봅니다.

1. 하위 페이지(예: 감사 또는 오류 페이지)를 추가하려면 **+** 아이콘을 클릭합니다.

   랜딩 페이지당 최대 2개의 하위 페이지를 추가할 수 있습니다.

기본 페이지와 하위 페이지를 구성하고 디자인한 후에는 게시하기 전에 [랜딩 페이지를 테스트](#test-landing-page)하십시오.

>[!CAUTION]
>
>페이지가 게시되었더라도 정의된 URL을 복사하여 웹 브라우저에 붙여넣으면 랜딩 페이지에 액세스할 수 없습니다. [랜딩 페이지 테스트](#test-landing-page)에 설명된 대로 미리 보기 기능을 사용하여 페이지를 테스트합니다.

## 기본 페이지 구성 {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_primary_page"
>title="기본 페이지 설정 정의"
>abstract="수신자가 랜딩 페이지 링크를 클릭할 때(예: 이메일 또는 웹 사이트에서) 즉시 표시되는 기본 페이지를 정의합니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_access_settings"
>title="랜딩 페이지 URL 정의"
>abstract="이 섹션에서는 고유 랜딩 페이지 URL을 정의합니다. URL의 첫 번째 부분을 사용하려면 이전에 선택한 사전 설정의 일부로 랜딩 페이지 하위 도메인을 설정해야 합니다."

기본 페이지는 수신자가 랜딩 페이지 링크를 클릭할 때(예: 이메일 또는 웹 사이트에서) 즉시 표시되는 페이지입니다.

기본 페이지 설정을 정의하려면 다음 단계를 수행합니다.

1. 필요에 따라 **[!UICONTROL 페이지 이름]**&#x200B;을 변경합니다. 기본적으로 _기본 페이지_&#x200B;입니다.

1. 페이지 URL의 끝 부분을 정의합니다.

   선택한 사전 설정에 따라 URL의 첫 번째 부분이 결정됩니다. 관리자는 [랜딩 페이지 하위 도메인](../admin/configuration-presets-landing-pages.md#lp-subdomains)을 사전 설정의 일부로 구성합니다.

   >[!CAUTION]
   >
   >랜딩 페이지 URL은 고유해야 합니다.
   >
   >페이지가 게시되었더라도 이 URL을 복사하여 웹 브라우저에 붙여넣으면 랜딩 페이지에 액세스할 수 없습니다. [랜딩 페이지 테스트](#test-landing-page)에 설명된 대로 미리 보기 기능을 사용하여 테스트합니다.

1. 익명 랜딩 페이지를 원하는 경우 **[!UICONTROL 식별된 사용자 필요]** 옵션을 비활성화하십시오.

1. _달력_ 아이콘을 클릭하여 **[!UICONTROL 페이지 만료]**&#x200B;를 설정합니다.

   만료 날짜를 선택한 후 페이지 만료 시 작업을 선택합니다.

   * **[!UICONTROL 리디렉션 URL]** - 리디렉션으로 사용할 페이지의 URL을 입력합니다.
   * **[!UICONTROL 브라우저 오류]** - 페이지 대신 표시할 오류 텍스트를 입력하십시오.

## 랜딩 페이지 테스트 {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_preview_lp_profiles"
>title="랜딩 페이지 미리보기 및 테스트"
>abstract="랜딩 페이지 설정 및 콘텐츠를 정의한 후 테스트 프로필을 사용하여 페이지를 미리 봅니다."

랜딩 페이지 설정 및 콘텐츠가 정의되면 테스트 프로필을 사용하여 페이지를 미리 볼 수 있습니다. [개인 맞춤화된 콘텐츠](email-authoring.md#personalization)를 삽입한 경우 테스트 프로필 데이터를 사용하여 랜딩 페이지에 이 콘텐츠가 어떻게 표시되는지 확인할 수 있습니다.

>[!PREREQUISITES]
>
>랜딩 페이지를 미리 보고 테스트하려면 **[!UICONTROL 메시지 게시]** 권한과 테스트 프로필을 포함하는 정의된 데이터 세트가 있어야 합니다.

1. 테스트 프로필 선택을 열려면 **[!UICONTROL 미리 보기 및 테스트]**&#x200B;를 클릭하십시오.

   >[!NOTE]
   >
   >시각적 디자인 영역에 있는 경우 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 사용할 수도 있습니다.

1. _[!UICONTROL 시뮬레이션]_ 화면에서 테스트 프로필을 선택합니다.

   필요한 프로필이 목록에 없으면 **[!UICONTROL 테스트 프로필 관리]**&#x200B;를 클릭하여 알려진 테스트 프로필 전자 메일 주소를 사용하고 목록에 추가하십시오.

   +++테스트 프로필 추가

   **[!UICONTROL ID 네임스페이스]**&#x200B;의 경우 _Select_ 아이콘(![Select 아이콘](../../user/assets/do-not-localize/icon-select-data.svg) )을 클릭하고 프로필을 테스트하는 데 사용할 `Email` 네임스페이스를 선택하십시오.

   **[!UICONTROL ID 값]** 필드에 테스트 프로필을 식별할 전자 메일 주소를 입력하고 **[!UICONTROL 프로필 추가]**&#x200B;를 클릭합니다. 이 작업을 반복하여 여러 프로필을 추가할 수 있습니다.

   왼쪽 상단의 뒤로 화살표를 클릭하여 _[!UICONTROL 시뮬레이션]_ 페이지로 돌아갑니다.

   +++

1. **[!UICONTROL 미리 보기 열기]**&#x200B;를 선택하여 랜딩 페이지를 테스트합니다.

   랜딩 페이지 미리보기가 새 탭에서 열립니다. 선택한 테스트 프로필 데이터가 개인화된 요소를 대체합니다.

1. 다른 테스트 프로필을 선택하여 랜딩 페이지의 각 변형에 대한 렌더링을 미리 봅니다.

## 랜딩 페이지 편집 {#edit-landing-page}

랜딩 페이지에 대한 편집 내용은 현재 상태에 따라 다릅니다.

* 랜딩 페이지가 **_초안_** 상태일 때 랜딩 페이지의 세부 정보, URL 및 시각적 콘텐츠를 편집할 수 있습니다.
* 랜딩 페이지가 **_게시됨_** 상태일 때 설명을 편집할 수 있지만 이름은 편집할 수 없습니다. 시각적 콘텐츠를 변경하려면 페이지의 초안 버전을 만들어야 합니다.
* 랜딩 페이지가 **_초안으로 게시됨_** 상태일 때 세부 정보 편집은 설명으로 제한됩니다. 초안 버전의 시각적 콘텐츠를 편집할 수도 있습니다.

>[!BEGINTABS]

>[!TAB 초안]

1. _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 랜딩 페이지 이름을 클릭하여 엽니다.

   오른쪽에 랜딩 페이지 세부 정보가 있는 시각적 콘텐츠의 미리보기가 표시됩니다.

1. 이름, 설명 등 세부 사항을 수정합니다.

   <!-- ![Details for landing page with Draft status](./assets/landing-page-draft-details.png){width="700" zoomable="yes"} -->

1. 시각적 디자인 공간에서 콘텐츠를 변경하려면 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭하세요.

1. 랜딩 페이지 세부 정보로 돌아가려면 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하십시오.

1. 페이지가 조건에 맞는 경우 표시할 수 있도록 하려면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

>[!TAB 게시됨]

1. _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 페이지 이름을 클릭하여 엽니다.

   오른쪽에 랜딩 페이지 세부 정보가 있는 시각적 콘텐츠의 미리보기가 표시됩니다.

1. 필요한 경우 설명을 수정합니다.

   게시된 랜딩 페이지의 경우 다른 모든 세부 사항을 변경할 수 없습니다.

1. 콘텐츠를 업데이트하려면 오른쪽의 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭하세요.

   대화 상자에서 **[!UICONTROL 초안 버전 만들기]**&#x200B;를 클릭하여 시각적 디자인 공간에서 초안 버전을 엽니다.

1. 랜딩 페이지 세부 정보로 돌아가려면 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하십시오.

1. 초안 랜딩 페이지가 조건을 충족하고 게시된 페이지에서 변경 사항을 사용할 수 있게 하려면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

   초안 버전을 게시하면 현재 게시된 버전이 대체되고 페이지 URL에 대한 콘텐츠가 업데이트됩니다.

>[!TAB 초안으로 게시됨]

랜딩 페이지를 열면 초안 버전이 표시됩니다. 미리보기 공간 맨 위에 있는 탭을 사용하여 게시된 버전과 초안 버전 간에 디스플레이를 전환할 수 있습니다. 초안 작업 및 세부 정보가 오른쪽에 표시됩니다.

<!-- ![Preview and details for the landing page draft version](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"} -->

콘텐츠를 업데이트하려면:

1. 오른쪽 상단의 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭합니다.

1. 랜딩 페이지 세부 정보로 돌아가려면 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하십시오.

1. 초안 페이지가 조건을 충족하고 변경 사항을 사용할 수 있게 하려면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

   초안 버전을 게시하면 현재 게시된 버전이 대체되고 호스팅된 페이지에서 콘텐츠가 업데이트됩니다.

>[!ENDTABS]

## 랜딩 페이지 복제 {#duplicate-landing-page}

다음 방법 중 하나를 사용하여 랜딩 페이지를 복제할 수 있습니다.

* _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 _자세히_ 아이콘(**...**)을 클릭합니다. 랜딩 페이지 이름 옆에 있는 **[!UICONTROL 복제]**&#x200B;를 선택합니다.
* 랜딩 페이지 세부 정보 페이지의 오른쪽 상단에서 **[!UICONTROL 을(를) 클릭합니다. 추가]**&#x200B;하고 **[!UICONTROL 복제]**&#x200B;를 선택하세요.

<!-- ![Duplicate the landing page](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"} -->

대화 상자에서 유용한 이름(고유)과 설명(선택 사항)을 입력합니다. 작업을 완료하려면 **[!UICONTROL 복제]**&#x200B;를 클릭하십시오.

<!-- ![Enter a name and description for the duplicated landing page](./assets/landing-page-duplicate-dialog.png){width="350"} -->

그러면 복제된(새) 페이지가 _랜딩 페이지_ 목록에 나타납니다.

## 랜딩 페이지 삭제 {#delete-landing-page}

다음 방법 중 하나를 사용하여 랜딩 페이지를 삭제할 수 있습니다.

* _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 _자세히_ 아이콘(**...**)을 클릭합니다. 랜딩 페이지 이름 옆에 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.
* 랜딩 페이지 세부 정보 페이지의 오른쪽 상단에서 **[!UICONTROL 을(를) 클릭합니다. 자세히]**. **[!UICONTROL 삭제]**&#x200B;를 선택하세요.

이 작업을 수행하면 확인 대화 상자가 열립니다. **[!UICONTROL 취소]**&#x200B;를 클릭하여 프로세스를 중단하거나 **[!UICONTROL 삭제]**&#x200B;를 클릭하여 삭제를 확인할 수 있습니다.

<!-- ![Delete landing page dialog](./assets/landing-page-delete-dialog.png){width="400"} -->

## 랜딩 페이지 링크 {#link-to-landing-page}

이메일, 조각 및 페이지 콘텐츠를 생성하는 마케터 또는 크리에이티브는 Journey Optimizer B2B Prime 인스턴스에 생성된 게시된(라이브) 랜딩 페이지에 대한 링크를 포함할 수 있습니다.

1. 조각, 이메일, 랜딩 페이지 또는 템플릿에 대한 시각적 디자인 공간에서 작업할 때 링크의 텍스트 일부, 버튼 구성 요소 또는 이미지 구성 요소를 선택합니다.

   **[!UICONTROL 링크]** 옵션이 오른쪽 패널에 표시됩니다.

1. **[!UICONTROL Type]** 옵션에 대해 **[!UICONTROL 랜딩 페이지]**&#x200B;을(를) 선택하십시오.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"} -->

1. **[!UICONTROL 랜딩 페이지]** 옵션의 경우 _페이지 선택_ 아이콘(![링크 표시 아이콘](../../user/assets/do-not-localize/icon-landing-page-select.svg))을 클릭합니다.

1. 랜딩 페이지 선택 대화 상자에서 **[!UICONTROL 랜딩 페이지 소스]**&#x200B;를 **[!UICONTROL Journey Optimizer B2B edition]**(으)로 설정하고 게시된 페이지 목록에서 랜딩 페이지에 대한 확인란을 선택한 다음 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   <!-- ![Link options for a landing page](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"} -->

1. **[!UICONTROL Target]** 옵션의 경우 링크 대상 동작을 선택하십시오.

   * **[!UICONTROL 없음]** - 브라우저 기본 동작을 사용하여 링크를 엽니다.
   * **[!UICONTROL Blank]** - 새 창 또는 탭에서 링크를 엽니다.
   * **[!UICONTROL 자체]** - 같은 프레임에서 링크를 엽니다.
   * **[!UICONTROL 상위]** - 상위 프레임에서 링크를 엽니다.
   * **[!UICONTROL 위쪽]** - 창의 전체 본문에서 링크를 엽니다.

1. (텍스트 링크만 해당) 연결된 텍스트에 밑줄을 적용하려면 **[!UICONTROL 밑줄 링크]** 확인란을 선택합니다.

   오른쪽 패널에서 **[!UICONTROL 스타일]** 탭을 선택하여 링크 색상을 포함하여 링크 텍스트에 대한 추가 스타일을 설정할 수 있습니다.
