---
title: In-CRM 인사이트
description: CRM에서 직접 Journey Optimizer B2B edition 구매 그룹에 액세스합니다. 영업 팀 구성원은 CRM 내 인사이트를 통해 참여 데이터를 보고 판매 기회를 식별할 수 있습니다.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: 2eb5b6226730a1948b480a9dee0c6f2786e01cc5
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---


# In-CRM 인사이트

[!DNL In-CRM Insights]은(는) Salesforce 및 Microsoft Dynamics 365에 통합되는 웹 기반 응용 프로그램으로, CRM 내에서 직접 [!DNL Journey Optimizer B2B Edition]개의 구매 그룹에 액세스할 수 있습니다. 영업 데이터 소스를 통합하여 참여도 및 영업 잠재력 향상을 위한 기회를 보다 쉽게 파악할 수 있습니다.

## 설치

설치 프로세스에는 다음이 포함됩니다.

* 사용자 권한 및 그룹 설정
* 소프트웨어 패키지 설치
* CRM을 통해 로그인

### 권한 설정

소프트웨어를 설치하는 사용자는 Salesforce 패키지를 설치할 수 있는 권한이 있어야 합니다.

애플리케이션에 액세스하려면 사용자에게 **Sales Insights:View Sales Insights** 권한이 있는 역할의 멤버십이 있어야 합니다.

사용자를 [!DNL In-CRM Insights]&#x200B;(으)로만 제한하려면 다음 작업을 수행하십시오.

1. [사용자 지정 역할](https://experienceleague.adobe.com/ko/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role)을(를) 만들고 **Sales Insights: Sales Insights 보기** 권한을 할당합니다.
1. 새 [사용자 그룹](https://experienceleague.adobe.com/ko/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group)을(를) 만듭니다.
1. Experience Platform 제품 프로필을 그룹에 추가합니다.

### 패키지 설치

In-CRM Insights 패키지를 설치하려면 Salesforce 또는 Microsoft Dynamics의 단계를 따르십시오.

#### Salesforce

1. [In-CRM Insights 설치 관리자 패키지](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce)를 다운로드하십시오.
1. 로그인 후 패키지 설치 페이지로 리디렉션됩니다.
1. **[!UICONTROL 모든 사용자에 대해 설치]** 옵션을 선택하고 **[!UICONTROL 설치]**&#x200B;를 클릭합니다.

   ![In-CRM Insights 패키지 설치](assets/incrm-install-sf.png){width=500}

1. 대화 상자에서 타사 액세스를 승인한 다음 **[!UICONTROL 계속]**&#x200B;을 클릭합니다.
1. 설치가 완료되면 **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

   이제 **설치된 패키지** 페이지에 나열되며 **Journey Optimizer B2B edition**&#x200B;이 앱 시작 관리자에 나열됩니다.

   ![Salesforce 내에서 CRM 내 인사이트 설정](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. [In-CRM Insights 설치 관리자 패키지](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics)를 다운로드하십시오.
1. [Power Apps 포털](https://make.powerapps.com/){target=_blank}(으)로 이동합니다.
1. 로그인한 후 패키지의 환경을 선택한 다음 왼쪽 메뉴에서 **[!UICONTROL 솔루션]**(으)로 이동합니다.
1. **[!UICONTROL 솔루션 가져오기]**&#x200B;를 클릭합니다.
1. 설치 관리자 패키지로 이동하여 업로드한 후 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.
1. 패키지 세부 정보를 확인하고 **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.
1. _환경 변수_&#x200B;에서 값이 `prod`(값을 변경하지 않음)로 설정되어 있는지 확인하고 **[!UICONTROL 가져오기]**&#x200B;를 클릭합니다.
1. 설치가 완료되면 왼쪽 탐색 모음에 **[!UICONTROL Journey Optimizer B2B edition]** > **[!UICONTROL 구매 그룹]**&#x200B;이 표시됩니다.

   ![Microsoft Dynamics에서 사용할 수 있는 CRM 내 인사이트](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## 구매 그룹 보기

화면의 지침에 따라 Adobe 계정에 로그인합니다. 구매 그룹이 로드되어 있고 볼 수 있습니다.

구매 그룹을 선택한 후 [그룹 세부 정보](https://experienceleague.adobe.com/ko/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#)를 검색할 수 있습니다. 이는 Journey Optimizer B2B edition에 표시되는 데이터 및 인사이트와 동일하지만 데이터는 [!DNL In-CRM Insights]을(를) 통해 읽기 전용입니다.
