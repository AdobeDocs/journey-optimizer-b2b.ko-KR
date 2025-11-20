---
title: In-CRM 인사이트
description: Salesforce에서 직접 Journey Optimizer B2B edition 구매 그룹에 액세스합니다. 영업 팀 구성원은 CRM 내 인사이트를 통해 참여 데이터를 보고 판매 기회를 식별할 수 있습니다.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# In-CRM 인사이트

In-CRM Insights는 Salesforce에 통합된 웹 기반 애플리케이션으로, Salesforce 내에서 직접 Journey Optimizer B2B edition 구매 그룹에 액세스할 수 있도록 합니다. 이를 통해 참여 및 판매 잠재력을 높일 수 있는 기회를 파악할 수 있습니다.

In-CRM Insights 애플리케이션은 [Marketo Sales Insights 패키지](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange)에서 사용할 수 있습니다.

## 권한

애플리케이션에 액세스하려면 사용자는 **Sales Insights:View Sales Insights** 권한이 있는 역할의 멤버십을 가지고 있어야 합니다.

사용자 그룹을 InCRM-Insights로 제한하려면 다음 지침을 사용하여 InCRM-Insights에 대해 특별히 사용자 지정 역할을 만드십시오.

* **Sales Insights:View Sales Insights** 권한 집합만 있는 사용자 지정 역할을 만드십시오.
* 제품 프로필을 추가하지 않고 새 사용자 그룹을 만듭니다.
* 다른 사용자 그룹을 만들고 AEP 제품 프로필을 추가하거나 기존 AEP 프로필을 방금 만든 사용자 그룹에 추가합니다.
* 새 사용자 그룹을 새 역할에 할당하고 새 사용자를 새 사용자 그룹에 추가합니다.

## CRM 내 인사이트 사용

In-CRM Insights 애플리케이션은 앱 런처를 통해 Salesforce에서 사용할 수 있습니다.

1. Salesforce에서 앱 런처 를 클릭합니다.
1. `Journey Optimizer B2B Edition`을(를) 선택하거나 검색하세요.
1. 표시된 탭에서 Adobe 자격 증명으로 로그인합니다.
1. 계정 여정을 호스팅하는 샌드박스를 선택합니다.

구매 그룹이 로드되어 사용 가능합니다. 데이터는 In-CRM Insights를 통해 읽기 전용입니다.

>[!NOTE]
>
>CRM 내 인사이트에 액세스하려면 [B2B 영업 사용자](../admin/user-management.md#b2b-built-in-roles) 제품 역할의 멤버십이 필요합니다.

구매 그룹을 선택한 후에는 Journey Optimizer B2B edition의 경우처럼 [그룹 세부 정보](https://experienceleague.adobe.com/ko/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#)를 검색할 수 있습니다.
