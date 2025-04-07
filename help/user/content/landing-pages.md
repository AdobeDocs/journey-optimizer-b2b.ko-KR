---
title: 랜딩 페이지
description: 랜딩 페이지와 이를 만들고 관리하여 계정 여정 및 캠페인을 지원하는 방법에 대해 알아봅니다.
feature: Content
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
exl-id: 1a3b4519-e1c0-418a-979a-7ba3e5972edd
source-git-commit: d2ce1685bd8185f418cd28e37dc11d539e765ad9
workflow-type: tm+mt
source-wordcount: '2188'
ht-degree: 2%

---

# 랜딩 페이지

랜딩 페이지는 연락처와 고객이 이메일, SMS 메시지 또는 디지털 위치에서 연결된 항목을 클릭한 후 직접 연락할 수 있는 독립 실행형 웹 페이지입니다. 이 페이지들을 계정 여정에 통합하여 잠재 고객과 고객이 웹에서 메시지를 보고 계정 여정에서 진행하도록 할 수 있습니다. 랜딩 페이지 시각적 디자인 공간에서 랜딩 페이지를 만들고, 개인화하고, 미리 볼 수 있습니다.

고객이 특정 링크를 클릭할 때 정의된 웹 페이지로 안내하려면 Journey Optimizer B2B edition에서 랜딩 페이지를 만듭니다.

* 페이지 만들기
* 랜딩 페이지 디자인 및 콘텐츠 작성
* 페이지 테스트
* 페이지 게시
* 여정 컨텐츠의 페이지 링크

예를 들어 랜딩 페이지를 만들고 디자인하여 사용자를 온라인 정보로 안내할 수 있습니다. 페이지에는 커뮤니케이션 수신을 옵트인하거나 옵트아웃할 수 있는 양식이 포함될 수 있습니다. 또는 뉴스레터와 같은 반복되는 커뮤니케이션에 가입할 수 있습니다.

시각적 디자인 공간에서 랜딩 페이지를 만들고, 개인화하고, 미리 볼 수 있습니다.
<!-- 
For the Beta phase, you can only design landing pages from scratch and publish your landing pages. The landing pages will be served on adobe hosted domain for the Beta phase. The capability to define your branded domains for hosting will be delivered in a future release. -->

## 랜딩 페이지 액세스 및 관리

Adobe Journey Optimizer B2B edition의 랜딩 페이지에 액세스하려면 왼쪽 탐색으로 이동하여 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 랜딩 페이지]**&#x200B;를 클릭하십시오. 이 작업을 수행하면 인스턴스에 생성된 모든 랜딩 페이지가 표에 나열된 목록 페이지가 열립니다.

![랜딩 페이지 라이브러리에 액세스](./assets/landing-pages-list.png){width="800" zoomable="yes"}

표는 _[!UICONTROL 수정됨]_ 열을 기준으로 정렬되며 가장 최근에 업데이트된 항목이 기본적으로 맨 위에 있습니다. 오름차순과 내림차순 간을 변경하려면 열 제목을 클릭합니다.

### 랜딩 페이지 목록 필터링

이름별로 랜딩 페이지를 검색하려면 검색 막대에 일치 항목 텍스트 문자열을 입력합니다. _필터_ 아이콘(![필터 표시 또는 숨기기 아이콘](../assets/do-not-localize/icon-filter.svg) )을 클릭하여 사용 가능한 필터 옵션을 표시하고 설정을 변경하여 지정된 조건에 따라 표시된 항목을 필터링합니다.

![표시된 랜딩 페이지를 필터링](./assets/landing-pages-list-filtered.png){width="700" zoomable="yes"}

### 열 표시 사용자 정의

오른쪽 상단의 _표 사용자 지정_ 아이콘(![표 사용자 지정 아이콘](../assets/do-not-localize/icon-column-settings.svg))을 클릭하여 표에 표시할 열을 사용자 지정합니다.

대화 상자에서 표시할 열을 선택하고 **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

![표시할 열 선택](./assets/landing-pages-customize-table-dialog.png){width="300"}

### 랜딩 페이지 상태 및 라이프사이클

랜딩 페이지 상태는 이메일 및 SMS 콘텐츠에서 연결에 대한 가용성과 이에 대해 수행할 수 있는 변경 사항을 결정합니다.

| 상태 | 설명 |
| -------------------- | ----------- |
| 초안 | 랜딩 페이지를 만들 때 초안 상태입니다. 이 상태는 시각적 콘텐츠를 정의하거나 편집할 때 호스팅되는 페이지로 게시할 때까지 이 상태로 유지됩니다. 사용 가능한 작업: <br/><ul><li>이름 또는 설명 편집<li>링크 URL 편집<li>시각적 디자인 공간에서 편집<li>게시<li>복제<li>삭제 |
| 게시일 | 랜딩 페이지를 게시하면 Journey Optimizer B2B edition 인스턴스에서 호스팅되며 이메일 또는 SMS 메시지 콘텐츠에서 연결할 수 있습니다. 사용 가능한 작업: <br/><ul><li>이름 또는 설명 편집<li>링크 URL 편집<li>이메일 또는 SMS 메시지 콘텐츠에 링크 추가<li>초안 버전 만들기<li>복제<li>삭제 |
| 초안과 함께 게시됨 | 게시된 랜딩 페이지에서 초안을 만들면 게시된 버전이 유지되고 시각적 디자인 공간에서 초안 콘텐츠를 수정할 수 있습니다. 초안 버전을 게시하면 현재 게시된 버전이 대체되고 호스팅된 페이지에서 콘텐츠가 업데이트됩니다. 사용 가능한 작업: <br/><ul><li>이름 또는 설명 편집<li>링크 URL 편집<li>이메일 또는 SMS 메시지 콘텐츠에 링크 추가<li>시각적 디자인 공간에서 초안 버전 편집<li>초안 버전 게시<li>복제<li>삭제(두 버전 모두 삭제)<li>초안 삭제(게시된 상태로 돌아가기) |

![랜딩 페이지 상태 주기](./assets/status-lifecycle-diagram.png){zoomable="yes"}

## 랜딩 페이지 만들기

오른쪽 상단의 **[!UICONTROL 랜딩 페이지 만들기]**&#x200B;를 클릭하여 Journey Optimizer B2B edition에서 새 랜딩 페이지를 추가할 수 있습니다.

1. _[!UICONTROL 랜딩 페이지 만들기]_ 대화 상자에서 유용한 **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   랜딩 페이지 요구 사항:

   * 이름 - 최대 100자이며, 고유해야 하며 대소문자를 구분하지 않습니다.

   * 설명 - 최대 300자

   * Alpha, 숫자 및 특수 문자가 허용됩니다.

   * 예약된 문자가 **_허용되지 않음_**: `\ / : * ? " < > |`

   ![랜딩 페이지 만들기 대화 상자](./assets/landing-page-create-dialog.png){width="400"}

1. 필요한 경우 여러 하위 도메인이 구성되어 있는 경우 랜딩 페이지에 사용할 **[!UICONTROL 하위 도메인]**&#x200B;을(를) 변경하십시오.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   _[!UICONTROL 기본 랜딩 페이지 만들기]_ 홈 페이지가 열리고 페이지를 만들기 위한 여러 옵션이 제공됩니다. _[!UICONTROL 처음부터 디자인]_, _[!UICONTROL HTML 가져오기]_ 또는 저장된 템플릿 사용.

   ![랜딩 페이지 디자인 시작 방법 선택](./assets/landing-page-create-design.png){width="800" zoomable="yes"}

   랜딩 페이지 디자인을 시작하는 데 사용할 메서드를 선택한 후 시각적 디자인 공간을 사용하여 [페이지를 디자인](./landing-page-design.md)합니다.

### 처음부터 디자인

시각적 콘텐츠 편집기를 사용하여 랜딩 페이지 콘텐츠의 구조를 정의합니다. 간단한 드래그 앤 드롭 작업으로 구조 구성 요소를 추가 및 이동하여 페이지 콘텐츠의 형태를 몇 초 이내에 디자인할 수 있습니다.

1. _[!UICONTROL 기본 랜딩 페이지 만들기]_ 홈 페이지에서 **[!UICONTROL 처음부터 디자인]** 옵션을 선택합니다.

1. 페이지에 [구조 및 콘텐츠 추가](./landing-page-design.md#add-structure-and-content).

### HTML 가져오기

Adobe Journey Optimizer B2B edition을 사용하면 기존 HTML 콘텐츠를 가져와서 랜딩 페이지를 디자인할 수 있습니다.

{{$include /help/_includes/content-design-import.md}}

![zip 파일에서 html 콘텐츠 가져오기](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>`<table>` 태그를 HTML 파일의 첫 번째 레이어로 사용하면 맨 위 레이어 태그의 배경 및 너비 설정을 포함하여 스타일이 손실될 수 있습니다.

필요에 따라 시각적 디자인 공간을 사용하여 가져온 콘텐츠를 개인화할 수 있습니다.

### 저장된 템플릿 선택

다음 중에서 선택할 수 있습니다.

* **샘플 템플릿**. Journey Optimizer 인터페이스는 선택할 수 있는 기본 랜딩 페이지 템플릿 컬렉션을 제공합니다.

* **저장된 템플릿**. _[!UICONTROL 템플릿]_ 메뉴 <!-- or the _[!UICONTROL Save as content template]_ option when designing a landing page. -->을(를) 사용하여 조직의 멤버가 만든 저장된 사용자 지정 템플릿을 사용하십시오.

_[!UICONTROL 디자인 템플릿 선택]_ 섹션을 사용하여 템플릿에서 콘텐츠 작성을 시작하십시오. Journey Optimizer B2B edition 인스턴스에서 샘플 템플릿 또는 저장된 사용자 지정 랜딩 페이지 템플릿을 사용할 수 있습니다.

>[!BEGINTABS]

>[!TAB 저장된 템플릿]

_기본 랜딩 페이지 만들기_ 홈 페이지에서 기본적으로 _샘플 템플릿_ 탭이 선택됩니다. 사용자 지정 템플릿을 사용하려면 **[!UICONTROL 저장된 템플릿]** 탭을 선택하십시오.

저장된 모든 랜딩 페이지 템플릿 목록이 표시됩니다. _[!UICONTROL 이름]_, _[!UICONTROL 마지막 수정 날짜]_ 및 _[!UICONTROL 마지막 생성 날짜]_&#x200B;별로 정렬할 수 있습니다.

![저장된 템플릿 선택](./assets/landing-page-design-saved-templates-sort-by.png){width="700" zoomable="yes"}

목록에서 원하는 템플릿을 선택합니다.

선택 후 템플릿의 미리보기가 표시됩니다. 미리보기 모드에서 오른쪽 및 왼쪽 화살표를 사용하여 한 범주(선택에 따라 샘플 또는 저장됨)의 모든 템플릿 사이를 이동할 수 있습니다.

![저장된 템플릿 미리 보기](./assets/landing-page-design-saved-template-preview.png){width="800" zoomable="yes"}

표시와 사용할 항목이 일치하면 미리 보기 창의 오른쪽 상단에 있는 **[!UICONTROL 이 서식 파일 사용]**&#x200B;을 클릭합니다.

이 작업은 콘텐츠를 필요에 따라 편집할 수 있는 시각적 디자인 공간으로 복사합니다.

>[!TAB 샘플 템플릿]

Adobe Journey Optimizer B2B edition은 고유한 랜딩 페이지 및 랜딩 페이지 템플릿을 만드는 데 사용할 수 있는 _즉시 사용 가능한_ 랜딩 페이지 템플릿을 제공합니다.

<!-- ![Choose a template provided by Adobe](../assets/content-design-shared/templates-design-samples.png){width="800" zoomable="yes"} -->

>[!ENDTABS]

<!-- 
>[!NOTE]
>
> Saved templates may have governance (content locking) settings applied to one or more components. The visual designer provides guidelines about locked components when you [author an email from a governed template](./email-authoring-governance.md). -->

## 랜딩 페이지 편집

랜딩 페이지에 대한 편집 내용은 현재 상태에 따라 다릅니다.

* 랜딩 페이지가 **_초안_** 상태일 때 랜딩 페이지의 세부 정보, URL 및 시각적 콘텐츠를 편집할 수 있습니다.
* 랜딩 페이지가 **_게시됨_** 상태일 때 설명을 편집할 수 있지만 이름은 편집할 수 없습니다. 시각적 콘텐츠를 변경하려면 페이지의 초안 버전을 만들어야 합니다.
* 랜딩 페이지가 **_초안으로 게시됨_** 상태일 때 세부 정보 편집은 설명으로 제한됩니다. 초안 버전의 시각적 콘텐츠를 편집할 수도 있습니다.

>[!BEGINTABS]

>[!TAB 초안]

1. _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 랜딩 페이지 이름을 클릭하여 엽니다.

   오른쪽에 랜딩 페이지 세부 정보가 있는 시각적 콘텐츠의 미리보기가 표시됩니다.

1. 이름, 설명 등 세부 사항을 수정합니다.

   ![초안 상태의 랜딩 페이지에 대한 세부 정보](./assets/landing-page-draft-details.png){width="700" zoomable="yes"}

1. 시각적 디자인 공간에서 콘텐츠를 변경하려면 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭하세요.

   필요에 따라 시각적 디자인 도구를 사용합니다.

   * [구조 및 콘텐츠 추가](./landing-page-design.md#add-structure-and-content)
   * [Assets 추가](./landing-page-design.md#add-assets)
   * [레이어, 설정 및 스타일 탐색](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [콘텐츠 개인화](./landing-page-design.md#personalize-content)
   * [연결된 URL 추적 편집](./landing-page-design.md#edit-linked-url-tracking)

1. 랜딩 페이지 세부 정보로 돌아가려면 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하십시오.

1. 페이지가 조건에 맞는 경우 표시할 수 있도록 하려면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

>[!TAB 게시됨]

1. _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 페이지 이름을 클릭하여 엽니다.

   오른쪽에 랜딩 페이지 세부 정보가 있는 시각적 콘텐츠의 미리보기가 표시됩니다.

1. 필요한 경우 설명을 수정합니다.

   게시된 랜딩 페이지의 경우 다른 모든 세부 사항을 변경할 수 없습니다.

1. 콘텐츠를 업데이트하려면 오른쪽의 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭하세요.

   대화 상자에서 **[!UICONTROL 초안 버전 만들기]**&#x200B;를 클릭하여 시각적 디자인 공간에서 초안 버전을 엽니다.

   ![초안 버전 만들기 대화 상자](./assets/landing-page-create-draft-version.png){width="300"}

   필요에 따라 시각적 디자인 도구를 사용합니다.

   * [구조 및 콘텐츠 추가](./landing-page-design.md#add-structure-and-content)
   * [Assets 추가](./landing-page-design.md#add-assets)
   * [레이어, 설정 및 스타일 탐색](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [콘텐츠 개인화](./landing-page-design.md#personalize-content)
   * [연결된 URL 추적 편집](./landing-page-design.md#edit-linked-url-tracking)

1. 랜딩 페이지 세부 정보로 돌아가려면 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하십시오.

1. 초안 랜딩 페이지가 조건을 충족하고 게시된 페이지에서 변경 사항을 사용할 수 있게 하려면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

   초안 버전을 게시하면 현재 게시된 버전이 대체되고 페이지 URL에 대한 콘텐츠가 업데이트됩니다.

>[!TAB 초안으로 게시됨]

랜딩 페이지를 열면 기본적으로 초안 버전이 표시됩니다. 미리보기 공간 맨 위에 있는 탭을 사용하여 게시된 버전과 초안 버전 간에 디스플레이를 전환할 수 있습니다. 초안 작업 및 세부 정보가 오른쪽에 표시됩니다.

![랜딩 페이지 초안 버전에 대한 미리 보기 및 세부 정보](./assets/landing-page-published-draft-details.png){width="700" zoomable="yes"}

콘텐츠를 업데이트하려면:

1. 오른쪽 상단의 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭합니다. 필요에 따라 시각적 디자인 도구를 사용합니다.

   * [구조 및 콘텐츠 추가](./landing-page-design.md#add-structure-and-content)
   * [Assets 추가](./landing-page-design.md#add-assets)
   * [레이어, 설정 및 스타일 탐색](./landing-page-design.md#navigate-the-layers-settings-and-styles)
   * [콘텐츠 개인화](./landing-page-design.md#personalize-content)
   * [연결된 URL 추적 편집](./landing-page-design.md#edit-linked-url-tracking)

1. 랜딩 페이지 세부 정보로 돌아가려면 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하십시오.

1. 초안 페이지가 조건을 충족하고 변경 사항을 사용할 수 있게 하려면 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

   초안 버전을 게시하면 현재 게시된 버전이 대체되고 호스팅된 페이지에서 콘텐츠가 업데이트됩니다.

>[!ENDTABS]

### 경고 확인

랜딩 페이지 콘텐츠를 디자인할 때 주요 설정이 누락된 경우 인터페이스(오른쪽 상단)에 경고가 표시됩니다.

![페이지 콘텐츠 문제에 대한 알림](./assets/alerts-button.png){width="250"}

이 단추가 표시되지 않으면 발견된 문제가 없습니다.

두 가지 유형의 경고를 감지할 수 있습니다.

* 권장 사항 및 모범 사례를 참조하는 **_경고_**:

   * `Placeholder links are present in the landing page body`: 자리 표시자를 올바른 링크로 바꾸는 것을 잊지 마십시오.

   * `Text version of HTML is empty`: 페이지 본문의 텍스트 버전을 정의해야 합니다. 텍스트 버전은 HTML 콘텐츠를 표시할 수 없을 때 사용됩니다.

   * `Empty link is present in page body`: 페이지의 모든 링크가 올바른지 확인하십시오.

* 여정/캠페인을 테스트하거나 활성화하지 못하는 **_오류_**(예:

   * `The landing page content is empty`: 페이지 컨텐츠는 필수입니다.

## 랜딩 페이지 복제

다음 방법 중 하나를 사용하여 랜딩 페이지를 복제할 수 있습니다.

* _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 랜딩 페이지 이름 옆에 있는 _자세히_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.
* 랜딩 페이지 세부 정보 페이지의 오른쪽 상단에서 **[!UICONTROL 을(를) 클릭합니다. 추가]**&#x200B;하고 **[!UICONTROL 복제]**&#x200B;를 선택하세요.

![랜딩 페이지 복제](./assets/landing-page-details-duplicate-delete.png){width="600" zoomable="yes"}

대화 상자에서 유용한 이름(고유)과 설명(선택 사항)을 입력합니다. 작업을 완료하려면 **[!UICONTROL 복제]**&#x200B;를 클릭하십시오.

![중복된 랜딩 페이지의 이름과 설명을 입력하십시오](./assets/landing-page-duplicate-dialog.png){width="350"}

그러면 복제된(새) 페이지가 _랜딩 페이지_ 목록에 나타납니다.

## 랜딩 페이지 삭제

다음 방법 중 하나를 사용하여 랜딩 페이지를 삭제할 수 있습니다.

* _[!UICONTROL 랜딩 페이지]_ 목록 페이지에서 랜딩 페이지 이름 옆의 _자세히_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.
* 랜딩 페이지 세부 정보 페이지의 오른쪽 상단에서 **[!UICONTROL 을(를) 클릭합니다. 자세히]**. **[!UICONTROL 삭제]**&#x200B;를 선택하세요.

이 작업을 수행하면 확인 대화 상자가 열립니다. **[!UICONTROL 취소]**&#x200B;를 클릭하여 프로세스를 중단하거나 **[!UICONTROL 삭제]**&#x200B;를 클릭하여 삭제를 확인할 수 있습니다.

![랜딩 페이지 삭제 대화 상자](./assets/landing-page-delete-dialog.png){width="400"}

## 랜딩 페이지 링크

이메일, 조각 및 페이지 컨텐츠를 만드는 마케터 또는 Designer은 Journey Optimizer B2B edition 인스턴스에 만든 게시된(라이브) 랜딩 페이지에 대한 링크를 포함할 수 있습니다.

1. 조각, 이메일, 랜딩 페이지 또는 템플릿에 대한 시각적 디자인 공간에서 작업할 때 링크의 텍스트 일부, 버튼 구성 요소 또는 이미지 구성 요소를 선택합니다.

   **[!UICONTROL 링크]** 옵션이 오른쪽 패널에 표시됩니다.

1. **[!UICONTROL Type]** 옵션에 대해 **[!UICONTROL 랜딩 페이지]**&#x200B;을(를) 선택하십시오.

   ![랜딩 페이지에 대한 링크 옵션](/help/assets/content-design-shared/content-design-link-settings.png){width="700" zoomable="yes"}

1. **[!UICONTROL 랜딩 페이지]** 옵션의 경우 _페이지 선택_ 아이콘(![링크 표시 아이콘](/help/assets/do-not-localize/icon-landing-page-select.svg))을 클릭합니다.

1. 랜딩 페이지 선택 대화 상자에서 **[!UICONTROL 랜딩 페이지 소스]**&#x200B;를 **[!UICONTROL Journey Optimizer B2B edition]**(으)로 설정하고 게시된 페이지 목록에서 랜딩 페이지에 대한 확인란을 선택한 다음 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   ![랜딩 페이지에 대한 링크 옵션](/help/assets/content-design-shared/content-design-link-landing-page-select.png){width="600" zoomable="yes"}

1. **[!UICONTROL Target]** 옵션의 경우 링크 대상 동작을 선택하십시오.

   * **[!UICONTROL 없음]** - 브라우저 기본 동작을 사용하여 링크를 엽니다.
   * **[!UICONTROL Blank]** - 새 창 또는 탭에서 링크를 엽니다.
   * **[!UICONTROL 자체]** - 같은 프레임에서 링크를 엽니다.
   * **[!UICONTROL 상위]** - 상위 프레임에서 링크를 엽니다.
   * **[!UICONTROL 위쪽]** - 창의 전체 본문에서 링크를 엽니다.

1. (텍스트 링크만 해당) 연결된 텍스트에 밑줄을 적용하려면 **[!UICONTROL 밑줄 링크]** 확인란을 선택합니다.

   오른쪽 패널에서 **[!UICONTROL 스타일]** 탭을 선택하여 링크 색상을 포함하여 링크 텍스트에 대한 추가 스타일을 설정할 수 있습니다.
