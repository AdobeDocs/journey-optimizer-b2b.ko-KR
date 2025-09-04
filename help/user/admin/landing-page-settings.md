---
title: 랜딩 페이지 구성
description: 마케팅 팀이 캠페인을 지원할 웹 페이지를 작성하고 게시할 수 있도록 랜딩 페이지 설정에 액세스하고 구성하는 방법을 알아봅니다.
feature: Setup, Landing Pages, Content
role: Admin
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
exl-id: 54b812cb-0129-4253-8e9e-538c25fc4709
source-git-commit: 8bd3d696a52a813b88de9e3b58145b1cbfb3fa32
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 23%

---

# 랜딩 페이지 구성

관리자는 랜딩 페이지 설정이 이러한 페이지를 작성 및 게시하는 마케터용으로 구성되어 있는지 확인해야 합니다.

## 설정

랜딩 페이지 구성을 검토하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동하십시오. 탐색 패널의 _[!UICONTROL 랜딩 페이지]_&#x200B;에서 **[!UICONTROL 설정]**&#x200B;을 선택합니다.

![랜딩 페이지 설정](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

### 계정 문자열 {#account-string}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_account_string"
>title="랜딩 페이지 계정 문자열"
>abstract="계정 문자열은 랜딩 페이지를 호스팅하는 Adobe Journey Optimizer B2B Edition 인스턴스를 식별합니다."

계정 문자열은 랜딩 페이지를 호스팅하는 Adobe Journey Optimizer B2B edition 인스턴스를 식별합니다. 시스템 팀이 DNS 항목을 추가하고 구성하는지 확인합니다.

### 양식 미리 채우기 {#form-prefill}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_form_prefill"
>title="랜딩 페이지 양식 미리 채우기 설정"
>abstract="양식 미리 채우기 옵션을 활성화하여 랜딩 페이지 내의 양식에서 알려진 사용자에 대한 미리 채워진 정보를 사용하도록 할 수 있습니다."

랜딩 페이지 내의 양식에서 알려진 사용자에 대해 미리 채워진 정보를 사용할 수 있도록 하려면 **[!UICONTROL 양식 미리 채우기]** 옵션을 사용하도록 설정하십시오. 이 옵션이 비활성화되면 랜딩 페이지 작성자는 미리 채워진 양식 필드를 포함할 수 없습니다.

### 데이터 스트림 {#datastream}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_datastream"
>title="데이터스트림 요구 사항"
>abstract="이 도메인의 랜딩 페이지에서 페이지 이벤트를 수집하려면 데이터 스트림이 필요합니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_missing_datastream"
>title="데이터 스트림 ID 누락"
>abstract="하위 도메인에 데이터 스트림 ID가 누락되었습니다. 이 ID는 적절한 라우팅에 필요합니다. 계속하려면 설정에서 구성"

랜딩 페이지 이벤트 컬렉션에 사용할 데이터 스트림을 구성하려면 **[!UICONTROL 데이터 스트림]** 옵션을 설정하십시오.

## 하위 도메인 {#add-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_add_subdomain"
>title="랜딩 페이지 하위 도메인 추가"
>abstract="최대 50개의 하위 도메인을 추가할 수 있습니다. Adobe Journey Optimizer B2B Edition에 호스팅하려는 각 고유 브랜드 URL에 대해 새 하위 도메인을 설정합니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_configure_subdomain"
>title="랜딩 페이지 하위 도메인 구성"
>abstract="랜딩 페이지를 게시하려면 구성된 하위 도메인이 필요합니다. Adobe에 이미 위임된 하위 도메인을 사용하거나 새 하위 도메인을 만들 수 있습니다."

랜딩 페이지 하위 도메인은 콘텐츠 유형, 제품 이름 또는 캠페인을 식별하고 페이지 신뢰성을 강화하는 데 도움이 되어야 합니다. 하위 도메인을 구성하기 전에 랜딩 페이지에 사용할 CNAME을 하나 이상 정의합니다. 예:

* **제품**.[CompanyDomain].com
* **이동**.[CompanyDomain].com
* **등록**.[CompanyDomain].com

이 예제에서 첫 번째 부분(굵은 글꼴)은 `LandingPageCNAME`입니다.

Adobe Journey Optimizer B2B edition에서 호스팅하려는 각 고유 브랜드 URL에 대해 새 하위 도메인을 추가합니다. 최대 50개의 하위 도메인을 추가할 수 있습니다.

>[!IMPORTANT]
>
>잘못된 하위 도메인을 Adobe에 위임할 수 없습니다. _marketing.yourcompany.com_&#x200B;과 같이 조직에서 소유한 올바른 하위 도메인을 입력하십시오.

하위 도메인을 검토하고 새 도메인을 추가하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동하세요. 탐색 패널의 _[!UICONTROL 랜딩 페이지]_&#x200B;에서 **[!UICONTROL 하위 도메인]**&#x200B;을 선택합니다.

![랜딩 페이지 하위 도메인](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

랜딩 페이지 하위 도메인을 추가하려면(_T):_

1. 오른쪽 상단의 **[!UICONTROL 하위 도메인 추가]**&#x200B;를 클릭합니다.

1. _[!UICONTROL 하위 도메인 세부 정보]_&#x200B;에 하위 도메인 정보를 입력하십시오.

   * **[!UICONTROL 하위 도메인]** - 사용할 하위 도메인 URL(예: `marketing.yourcompany.com`)
   * **[!UICONTROL 기본 페이지]** - 기본 하위 도메인 페이지의 URL(예: `marketing.yourcompany.com/products`)
   * **[!UICONTROL 대체 페이지]** - 하위 도메인의 랜딩 페이지가 활성화되지 않은 경우 사용할 대체 페이지의 URL(예: `marketing.yourcompany.com/expired`)

   ![랜딩 페이지 하위 도메인 추가](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
