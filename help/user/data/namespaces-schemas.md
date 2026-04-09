---
title: B2B 네임스페이스 및 스키마
description: Postman 자동 생성 유틸리티를 사용하여 Journey Optimizer B2B edition에 대해 Experience Platform B2B 네임스페이스 및 스키마를 구성합니다.
feature: Setup, Data Management
role: Admin
exl-id: 40d01027-7cf2-4189-8a49-7a0783c00721
source-git-commit: 8073984ced07e86a3fa500c5bf0bd393abbe0990
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 100%

---

# B2B 네임스페이스 및 스키마

간소화된 아키텍처의 Journey Optimizer B2B edition 설정에는 B2B 소스와 함께 사용되는 Experience Platform 네임스페이스 및 스키마 구성이 포함됩니다. B2B 네임스페이스 및 스키마를 생성하려면 Postman 자동화 유틸리티가 필요합니다.

>[!AVAILABILITY]
>
>- B2B 스키마가 [실시간 고객 프로필](https://experienceleague.adobe.com/en/docs/experience-platform/profile/home){target="_blank"}에 적합하도록 하려면 [Adobe Real-Time Customer Data Platform B2B edition](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"}에 액세스할 수 있어야 합니다.
>
>- Experience Platform B2B 엔터티는 [B2B 네임스페이스 및 스키마 안내서](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"}에 설명된 표준 관계를 사용해야 합니다.

B2B 소스에서 사용할 네임스페이스 및 스키마에 대한 기본 설정에 대한 다음 정보를 검토하십시오. 또한 B2B 네임스페이스 및 스키마를 생성하는 데 필요한 Postman 자동화 유틸리티 설정에 대한 세부 정보도 제공합니다.

## 자동 생성 유틸리티 설정

B2B 네임스페이스 및 스키마 자동 생성 유틸리티를 지원하도록 [!DNL Postman] 환경을 설정하는 방법에 대한 자세한 내용과 사전 요구 사항에 대해서는 다음 리소스를 참조하십시오.

- [GitHub 저장소](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}에서 네임스페이스와 스키마 자동 생성 유틸리티 컬렉션 및 환경을 다운로드합니다.
- 필요한 헤더에 대한 값을 수집하고 샘플 API 호출을 읽는 방법에 대한 세부 정보를 포함하여 Experience Platform API 사용에 대한 자세한 내용은 [_Adobe Experience Platform API 시작하기_](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/platform-apis/api-guide){target="_blank"}를 참조하십시오.
- Experience Platform API에 대한 자격 증명을 생성하는 방법에 대한 자세한 내용은 [_Experience Platform API 인증 및 액세스_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}를 참조하십시오.
- Experience Platform API용 [!DNL Postman] 설정에 대한 자세한 내용은 Adobe Experience Platform의 [_[!DNL Postman]_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman){target="_blank"}을(를) 참조하십시오.

### 환경 값

Experience Platform 개발자 콘솔과 [!DNL Postman]을(를) 설정하면 [!DNL Postman] 환경에 적절한 환경 값을 적용할 수 있습니다. 다음 표에서는 [!DNL Postman] 환경 채우기에 대한 예제 값과 추가 정보를 제공합니다.

| 변수 | 설명 | 예 |
| --- | --- | --- |
| `CLIENT_SECRET` | `{ACCESS_TOKEN}`을(를) 생성하는 데 사용되는 고유 식별자입니다. | `{CLIENT_SECRET}` |
| `API_KEY` | Experience Platform API 호출을 인증하는 데 사용되는 고유 식별자입니다. | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | Experience Platform API 호출을 완료하는 데 필요한 인증 토큰입니다. | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | [!DNL Journey Optimizer B2B] 및 [!DNL Marketo Engage]과(와) 관련하여 이 값은 고정되어 있으며 항상 `ent_dataservices_sdk`(으)로 설정됩니다. | `ent_dataservices_sdk` |
| `CONTAINER_ID` | `global` 컨테이너에는 모든 표준 Adobe 및 Experience Platform 파트너가 제공한 클래스, 스키마 필드 그룹, 데이터 형식 및 스키마가 들어 있습니다. [!DNL Marketo]과(와) 관련하여 이 값은 고정되어 있으며 항상 `global`(으)로 설정됩니다. | `global` |
| `TECHNICAL_ACCOUNT_ID` | Adobe I/O에 통합하는 데 사용되는 자격 증명입니다. | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | IMS(Identity Management System)는 Adobe 서비스에 인증을 위한 프레임워크를 제공합니다. [!DNL Journey Optimizer B2B] 및 [!DNL Marketo Engage]과(와) 관련하여 이 값은 고정되어 있으며 항상 `ims-na1.adobelogin.com`(으)로 설정됩니다. | `ims-na1.adobelogin.com` |
| `IMS_ORG` | 제품 및 서비스를 소유하거나 라이선스를 부여하고 해당 구성원에 대한 액세스를 허용할 수 있는 법인 엔티티입니다. | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | 사용 중인 가상 샌드박스 파티션의 이름입니다. | `prod` |
| `TENANT_ID` | 만든 리소스의 이름 간격이 제대로 지정되고 조직 내에 포함되어 있는지 확인하는 데 사용되는 ID입니다. | `b2bcdpproductiontest` |
| `PLATFORM_URL` | API 호출을 수행하는 URL 엔드포인트. 이 값은 고정되어 있으며 항상 `http://platform.adobe.io/`(으)로 설정됩니다. | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### 스크립트 실행

환경 값이 준비되면 [!DNL Postman] 인터페이스를 사용하여 네임스페이스 및 스키마를 만들기 위한 스크립트를 실행합니다. 자동 생성기 유틸리티의 루트 폴더를 선택한 다음 상단 헤더에서 **[!DNL Run]**&#x200B;을(를) 선택합니다.

![Postman UI에서 네임스페이스 및 스키마 생성기의 루트 폴더](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

[!DNL Runner] 인터페이스가 나타납니다. 여기에서 모든 확인란이 선택되었는지 확인한 다음 **[!DNL Run Namespaces and Schemas Autogeneration Utility]**&#x200B;을(를) 선택하십시오.

![네임스페이스 및 스키마 컬렉션에서 여러 개의 요청이 선택된 Postman UI입니다.](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

요청이 성공하면 필요한 B2B 네임스페이스와 스키마가 만들어집니다.

## B2B 네임스페이스

ID 네임스페이스는 ID의 컨텍스트를 구분하는 역할을 하는 Experience Platform [[!DNL Identity Service]](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"}의 구성 요소입니다. 정규화된 ID에는 ID 값과 네임스페이스가 포함됩니다. 자세한 내용은 [네임스페이스 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces){target="_blank"}를 참조하십시오.

B2B 네임스페이스는 엔티티의 기본 ID에서 사용됩니다.

| 표시 이름 | ID 기호 | ID 유형 |
| --- | --- | --- |
| B2B 개인 | `b2b_person` | `CROSS_DEVICE` |
| B2B 계정 | `b2b_account` | `B2B_ACCOUNT` |
| B2B 기회 | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| B2B 영업 기회 사용자 관계 | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| B2B 캠페인 | `b2b_campaign` | `B2B_CAMPAIGN` |
| B2B 캠페인 멤버 | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| B2B 마케팅 목록 | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| B2B 마케팅 목록 멤버 | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| B2B 계정 사용자 관계 | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## B2B 스키마

Experience Platform은 스키마를 사용하여 데이터의 구조를 일관되고 재사용 가능한 방식으로 설명합니다. 여러 시스템에서 데이터를 일관되게 정의하면 의미를 쉽게 유지할 수 있으므로 데이터의 가치를 얻을 수 있습니다.

Experience Platform에서 데이터를 수집하려면 먼저 데이터의 구조를 설명하고 각 필드 내에 포함할 수 있는 데이터 유형에 제약 조건을 제공하는 스키마가 있어야 합니다. 스키마는 기본 클래스와 0개 이상의 스키마 필드 그룹으로 구성됩니다.

디자인 원칙 및 모범 사례를 포함하여 스키마 구성 모델에 대한 자세한 내용은 [_스키마 구성 기본 사항_](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}을 참조하십시오.

+++ B2B 계정

<table>
    <tr>
        <td style="width: 30%;">기본 클래스</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">XDM 비즈니스 계정</a></td>
    </tr>
    <tr>
        <td>필드 그룹</td>
        <td>XDM 비즈니스 계정 세부 정보</td>
    </tr>
    <tr>
        <td>[!DNL Profile] 스키마에서</td>
        <td>활성화됨</td>
    </tr>
    <tr>
        <td>기본 ID</td>
        <td><code>accountKey.sourceKey</code> 기본 클래스에서</td>
    </tr>
    <tr>
        <td>기본 ID 네임스페이스</td>
        <td>B2B 계정</td>
    </tr>
    <tr>
        <td>보조 ID</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> 기본 클래스에서</td>
    </tr>
    <tr>
        <td>보조 ID 네임스페이스</td>
        <td>B2B 계정</td>
    </tr>
    <tr>
        <td>관계</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> XDM 비즈니스 계정 세부 정보 필드 그룹</li><li>대상 속성: <code>/accountKey/sourceKey</code></li><li>유형: 일대일</li><li>참조 스키마: B2B 계정</li><li>네임스페이스: B2B 계정</li></ul> </td>
    </tr>
</table>

+++

+++ B2B 개인

<table>
    <tr>
        <td style="width: 30%;">기본 클래스</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile">XDM 개별 프로필</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>필드 그룹</td>
        <td><ul><li>XDM 비즈니스 사용자 세부 정보</li><li>XDM 비즈니스 사용자 구성 요소</li><li>IdentityMap</li><li>동의 및 환경 설정 세부 정보</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] 스키마에서</td>
        <td>활성화됨</td>
    </tr>
    <tr>
        <td>기본 ID</td>
        <td><code>b2b.personKey.sourceKey</code> XDM 비즈니스 사용자 세부 정보 필드 그룹</td>
    </tr>
    <tr>
        <td>기본 ID 네임스페이스</td>
        <td>B2B 개인</td>
    </tr>
    <tr>
        <td>보조 ID</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> / XDM 비즈니스 사용자 세부 정보 필드 그룹</li><li><code>workEmail.address</code> / XDM 비즈니스 사용자 세부 정보 필드 그룹</li></ol></td>
    </tr>
    <tr>
        <td>보조 ID 네임스페이스</td>
        <td><ol><li>B2B 개인</li><li>이메일</li></ol></td>
    </tr>
    <tr>
        <td>관계</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> / XDM 비즈니스 사용자 구성 요소 필드 그룹</li><li>유형: 다대일</li><li>참조 스키마: B2B 계정</li><li>네임스페이스: B2B 계정</li><li>대상 속성: accountKey.sourceKey</li><li>현재 스키마의 관계 이름: 계정</li><li>참조 스키마의 관계 이름: 사람</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++
-->
