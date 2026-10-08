---
title: 내보낸 Experience Platform 데이터 세트
description: Adobe Journey Optimizer B2B Edition에서 내보낸 Adobe Experience Platform 데이터 세트 이름 및 키 필드 경로에 대한 참조.
feature: Setup, Data Management
role: Admin
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
autotag-review: '2026-09-29T00:00:00.000Z'
source-git-commit: 801025ee02617d56fc8ab933b59385bca38f5097
workflow-type: tm+mt
source-wordcount: '4845'
ht-degree: 6%
---

# 내보낸 [!DNL Experience Platform]개 데이터 세트

[!DNL Adobe Journey Optimizer B2B Edition]은(는) [!DNL Adobe Experience Platform]에서 계정, 사용자, 구매 그룹 및 여정 정보를 사용할 수 있도록 합니다. 데이터 세트는 관련 레코드의 컬렉션입니다. 예를 들어, 개인 데이터 세트는 사람을 설명하고, 멤버십 데이터 세트는 사람을 계정 또는 여정에 연결하며, 이벤트 데이터 세트는 이메일 열기와 같은 작업을 기록합니다.

이 안내서를 사용하여 각 데이터 세트에 포함된 내용, 해당 필드의 의미 및 관련 레코드가 연결되는 방식을 이해할 수 있습니다. 데이터 세트 이름은 다음 패턴을 따릅니다.

**`AJOB2B-<datasetVersion>-<entity>`**

여기에서 `<entity>`은(는) `person`, `account_relational` 또는 `person_event` 등의 정보를 설명합니다. `<datasetVersion>`은(는) 데이터 집합의 필드 정의 버전을 식별합니다. 섹션 머리글에는 문서화된 이름이 표시되며 [!DNL Experience Platform] 환경에는 이전 버전도 포함될 수 있습니다.

이러한 내보내기를 지원하는 네임스페이스 및 스키마 설정에 대해서는 [B2B 네임스페이스 및 스키마](./namespaces-schemas.md)를 참조하십시오.

>[!NOTE]
>
>Adobe은 기존 사용을 중단하지 않도록 이전 데이터 세트 버전을 유지합니다. 따라서 샌드박스에서 동일한 데이터 세트의 여러 버전을 찾을 수 있습니다. 이전 데이터 세트를 더 이상 사용하지 않는 경우 Adobe에 제거를 요청할 수 있습니다. 제거를 요청하기 전에 데이터 세트가 더 이상 사용되지 않는지 확인하십시오.

## 이 안내서 읽기

- **필드 이름:** [!DNL Experience Platform]에 표시되는 정확한 이름. 점은 필드 내에서 `consents.marketing.email.val`과(와) 같은 수준을 구분합니다.
- **레코드 ID:**&#x200B;은(는) 해당 데이터 세트의 레코드를 식별합니다.
- **관계:**&#x200B;은(는) 식별자가 일치하는 데이터 집합 및 필드의 이름을 지정합니다. 예를 들어 `Matches AJOB2B-1_5_4-buying_group (_id)`은(는) 필드가 구매 그룹의 `_id`을(를) 참조함을 의미합니다. 전체 식별자를 일치시키십시오. 식별자를 줄이거나 다시 작성하지 마십시오.
- **표준 Adobe 형식:**&#x200B;에서 Adobe의 공유 필드 정의를 사용합니다.
- **관련 레코드 형식:**&#x200B;은(는) 일치하는 식별자를 사용하여 연결할 수 있는 레코드로 정보를 구성합니다.

예를 들어 `buying_group_member.buyingGroupID`은(는) `buying_group._id`과(와) 일치하고 해당 `personID`은(는) `person_relational._id` 또는 개인 데이터 세트 `personKey.sourceKey`과(와) 일치합니다. 이러한 링크는 구매 그룹에 속한 사용자를 이해하는 데 도움이 됩니다. [!DNL Experience Platform]은(는) 링크에서만 보고서 또는 대상자를 자동으로 만들지 않습니다.

일부 식별자는 마케팅 프로그램과 같이 이 안내서에 별도의 데이터 세트가 없는 정보를 나타냅니다. 관계 열에서는 여기에 존재하지 않는 데이터 세트의 이름을 지정하는 대신 이 점을 참고하십시오.

레코드가 삭제된 것으로 표시된 경우 `isDeleted`이(가) `true`이고, 삭제된 경우 `false`입니다. 일반적인 활성 구성원 또는 동의 표시로 취급하지 마십시오. `lastUpdatedDate`은(는) 레코드의 최신 데이터 업데이트를 설명합니다. 이벤트의 경우 `timestamp`을(를) 사용하여 활동이 발생한 시기를 파악합니다. 빈 필드는 정보를 사용할 수 없거나 해당 레코드에 적용되지 않음을 의미합니다.

관련 레코드 데이터 집합은 버전 `1_5_4`을(를) 사용합니다. 필드가 현재 채워져 있지 않거나 특별한 처리가 필요한 경우, 관련 섹션에서 고객이 볼 수 있는 제한 사항을 설명합니다.

대상은 선택한 기준을 충족하는 사용자 그룹입니다. 대상 만들기의 사용 가능 여부는 개인 프로필에 정보를 결합하는 [!DNL Experience Platform] 설정에 따라 다릅니다. [!DNL Experience Platform]에 데이터 세트가 있다고 해서 세그멘테이션에 사용할 수 있는 것은 아닙니다.

## 데이터 세트 선택

| 이해하고 싶은 내용 | 찾을 데이터 세트 |
|---|---|
| 직원 및 해당 이메일 환경 설정 | `person` |
| 계정 세부 정보 및 개인 연락처 세부 정보 | `account_relational`, `person_relational` |
| 계정과 연계된 사용자 | `account_member`, `account_person` |
| 구매 그룹, 해당 구성원 및 상태 변경 | `buying_group`, `buying_group_member`, `buying_group_event` |
| 계정 여정 및 참여 계정 | `account_journey`, `account_journey_member`, `account_event` |
| 개인 여정 및 참여 사용자 | `person_journey`, `person_journey_member` |
| 여정 내 단계 | `account_journey_node`, `person_journey_node`, `journey_node` |
| 이메일, 웹 및 기타 지원되는 개인 활동 | `person_event`, `person_event_relational` |

다음 섹션은 전체 데이터 세트 이름 및 필드 세부 사항을 제공합니다. 여정은 전체 경험을 설명하고, 멤버십은 사용자나 계정을 해당 여정에 연결하며, 이벤트는 발생한 사항을 설명합니다.

+++엔티티 관계 다이어그램

[!DNL Adobe Experience Platform]](./assets/ajo-b2b-data-model.svg)(으)로 내보낸 데이터 세트에 대한 ![엔터티 관계 다이어그램

+++

## `AJOB2B-1_5_1-person`

각 레코드는 사용자, 식별자 및 이메일 마케팅 환경 설정에 대해 설명합니다. 개인 수준 보고 및 프로필이 구성된 경우 이를 사용하여 대상을 구축할 수 있습니다.

**형식:** 표준 Adobe 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `personID` | 레코드 ID | 개인용 식별자. 관련 레코드를 일치시키려면 전체 값을 사용하십시오. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `identityMap` |  | 연결된 데이터에서 [!DNL Experience Platform]이(가) 같은 사람을 인식하는 데 도움이 되는 다른 식별자입니다. |
| `consents.marketing.email.val` |  | 이메일 마케팅 환경 설정: `n`은(는) 옵트아웃을 나타내며, `y`은(는) 이 필드에 옵트아웃이 기록되지 않았음을 나타냅니다. 이 필드만으로는 마케팅 이메일을 보낼 수 있는 권한을 설정하지 않습니다. |
| `consents.marketing.email.time` |  | 이메일 환경 설정을 마지막으로 업데이트한 날짜 및 시간입니다. |
| `consents.marketing.email.reason` |  | 제공된 경우 옵트아웃에 대한 사유(구독을 취소한 경우에만 설정됨). |
| `isDeleted` |  | 이 개인 레코드가 삭제된 것으로 표시되는지 여부. |

>[!NOTE]
>
>귀사에는 여기에 나열된 필드 외에 추가 사용자 필드가 있을 수 있습니다.

조직에서 자체 구성된 계정 또는 개인 데이터 세트를 사용하는 경우 해당 레코드에는 `isDeleted`도 포함될 수 있습니다. [고객 소유 데이터 세트](#customer-owned-datasets)를 참조하세요.

## `AJOB2B-1_5_4-account_member`

각 레코드는 하나의 계정을 한 사람에게 연결합니다. 이 데이터 세트를 사용하여 각 계정과 연결된 사람들을 보고합니다. 프로필이 아닌 관계를 설명합니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 관계 레코드 ID. |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 계정 식별자. |
| `personID` | `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치 | 개인 식별자. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-buying_group`

각 기록은 이름, 상태, 솔루션 관심도, 참여 및 완성도 점수를 포함하여 계정과 연결된 구매 그룹을 설명합니다. 구매 그룹 단계는 현재 채워져 있지 않습니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 구매 그룹 레코드 ID(전체 값 사용). |
| `buyingGroupName` |  | 구매 그룹 이름. |
| `engagementScore` |  | 참여 점수. |
| `completenessScore` |  | 완성도 점수. |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 관련 계정 식별자. |
| `solutionInterest` |  | 솔루션 관심 레이블. |
| `buyingGroupStatus` |  | 상태. |
| `buyingGroupStage` |  | 구매 그룹 단계 이름. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

>[!NOTE]
>
>**가용성 참고 사항:** `buyingGroupStage`이(가) 현재 비어 있습니다. 단계별로 구매 그룹을 필터링하거나 그룹화하는 데 사용하지 마십시오.

## `AJOB2B-1_5_4-buying_group_member`

각 레코드는 한 개인을 구매 그룹에 연결하고 해당 개인의 역할을 기록합니다. 구매 그룹 구성 및 역할 범위를 보고하는 데 사용합니다.

`isDeleted`은(는) 개인이 구매 그룹에서 제거되었는지 여부를 항상 나타내지는 않습니다. 이 필드만 사용하여 현재 멤버십을 결정하지 마십시오. 사용 가능한 역할 정보가 없을 경우 역할 이름을 비워 둘 수 있습니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 멤버십 레코드 ID. |
| `buyingGroupID` | `AJOB2B-1_5_4-buying_group`(`_id`)과(와) 일치 | 구매 그룹 식별자. |
| `personID` | `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치 | 개인 식별자. |
| `buyingGroupMemberRole` |  | 가능한 경우 역할 이름. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-account_journey`

각 레코드는 계정 여정에 대해 이름, 상태, 시작 및 종료 날짜를 설명합니다. 계정의 여정 라이프사이클 및 상태를 보고하는 데 사용합니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 여정 레코드 id(전체 값 사용). |
| `accountJourneyName` |  | 여정 이름. |
| `accountJourneyStatus` |  | 상태(예: 초안, 라이브, 완료됨) |
| `startDate` |  | 타임스탬프 시작. |
| `endDate` |  | 최종 타임스탬프. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-account_journey_member`

각 레코드는 계정을 계정 여정과 연결합니다. 각 여정에 참여하는 계정을 식별하고 보고하는 데 사용합니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 멤버십 레코드 ID. |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 계정 식별자. |
| `journeyID` | `AJOB2B-1_5_4-account_journey`(`_id`)과(와) 일치 | 계정 여정 식별자. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-person_journey`

각 레코드는 개인 여정에 대해 이름, 상태, 시작 및 종료 날짜를 설명합니다. 이 보고서를 사용하여 사용자 중심 여정의 여정 라이프사이클 및 상태를 보고할 수 있습니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 여정 레코드 id(전체 값 사용). |
| `personJourneyName` |  | 여정 이름. |
| `personJourneyStatus` |  | 상태(예: 초안, 라이브, 완료됨) |
| `startDate` |  | 타임스탬프 시작. |
| `endDate` |  | 최종 타임스탬프. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-person_journey_member`

각 레코드는 현재 여정 노드, 멤버십 및 입력 일자, 입력 수 등 여정에서 개인의 멤버십을 설명합니다. 등록, 재입력 및 여정 진행 상황을 보고하는 데 사용합니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 멤버십 레코드 ID. |
| `marketingProgramID` |  | 여정이 속한 마케팅 프로그램 식별자. |
| `personID` | `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치 | 개인 식별자. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 사용자가 현재 속한 여정 노드의 식별자입니다. |
| `membershipDate` |  | 개인이 마케팅 프로그램의 회원이 되었을 때입니다. |
| `lastEntryDate` |  | 여정에 마지막으로 입장한 시간. |
| `reentryOpensAt` |  | 여정을 다시 입력할 수 있는 경우. |
| `entryCount` |  | 여정에 들어간 횟수입니다. |
| `createdDate` |  | 레코드가 생성된 시간. |
| `updatedDate` |  | 레코드가 마지막으로 변경된 때입니다. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-account_journey_node`

각 레코드는 단계 및 단계가 속한 여정의 종류를 포함하여 여정의 단계를 설명합니다. 여정 노드는 시작, 대기 또는 결정과 같은 단계입니다. `person_journey_node`에 동일한 단계가 나타날 수 있습니다. 계정별로 단계를 처리하기 전에 `accountJourneyID`을(를) 계정 여정에 일치시키십시오.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 노드 레코드 ID(전체 값 사용). |
| `accountJourneyID` | `AJOB2B-1_5_4-account_journey`(`_id`)과(와) 일치 | 상위 여정 식별자. |
| `uuid` |  | 여정 단계에 대한 추가 식별자. |
| `journeyNodeTypeID` |  | 여정 단계 종류를 식별하는 번호입니다. |
| `nodeType` |  | 여정 단계 종류를 식별하는 레이블입니다. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `createdDate` |  | 레코드가 생성된 시간. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-person_journey_node`

각 레코드는 단계 및 단계가 속한 여정의 종류를 포함하여 여정의 단계를 설명합니다. 동일한 단계가 `account_journey_node`에 나타날 수 있습니다. 단계를 개인별로 처리하기 전에 `personJourneyID`을(를) 개인 여정에 맞추십시오.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 노드 레코드 ID(전체 값 사용). |
| `personJourneyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 상위 여정 식별자. |
| `uuid` |  | 여정 단계에 대한 추가 식별자. |
| `journeyNodeTypeID` |  | 여정 단계 종류를 식별하는 번호입니다. |
| `nodeType` |  | 여정 단계 종류를 식별하는 레이블입니다. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `createdDate` |  | 레코드가 생성된 시간. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-account_event`

각 레코드는 여정에 추가 또는 제거되는 계정 또는 여정 노드 간 이동하는 여정 이벤트를 캡처합니다. `eventType` 및 `timestamp`을(를) 사용하여 계정 활동 타임라인을 작성하십시오. `buyingGroupID`은(는) 이벤트가 구매 그룹 특성일 때 사용할 수 있습니다.

**형식:** 관련 레코드 형식

`eventType`에서 발생한 일에 대한 정보를 제공합니다. 다음 표에서는 각 활동 유형에 대한 필드를 설명합니다.

`lastUpdatedDate`은(는) 현재 이러한 이벤트에 대해 채워져 있지 않습니다. 활동 날짜에 `timestamp`을(를) 사용합니다.

### 여정(`account.addAccountToJourney`)에 추가된 계정

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `account.addAccountToJourney`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 계정 식별자. |
| `journeyID` | `AJOB2B-1_5_4-account_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-account_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자. |
| `buyingGroupID` | `AJOB2B-1_5_4-buying_group`(`_id`)과(와) 일치 | 여정 추가가 구매 그룹 속성인 경우 구매 그룹 식별자. |
| `lastUpdatedDate` |  | 업데이트 시간을 기록합니다. 현재 비어 있습니다. 활동 날짜에 타임스탬프를 사용하십시오. |

### 여정(`account.removeAccountFromJourney`)에서 제거된 계정

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `account.removeAccountFromJourney`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 계정 식별자. |
| `journeyID` | `AJOB2B-1_5_4-account_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-account_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자. |
| `buyingGroupID` | `AJOB2B-1_5_4-buying_group`(`_id`)과(와) 일치 | 여정 제거가 구매 그룹 속성인 경우 구매 그룹 식별자. |
| `lastUpdatedDate` |  | 업데이트 시간을 기록합니다. 현재 비어 있습니다. 활동 날짜에 타임스탬프를 사용하십시오. |

### 여정 단계(`account.changeAccountJourneyNode`) 간에 이동한 계정

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `account.changeAccountJourneyNode`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 계정 식별자. |
| `journeyID` | `AJOB2B-1_5_4-account_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-account_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자. |
| `previousJourneyNodeID` | `AJOB2B-1_5_4-account_journey_node`(`_id`)을 참조합니다. 값이 일치하지 않을 수 있습니다. | 이전 여정 단계의 식별자. 이 값은 해당 단계 레코드와 일치하지 않을 수 있습니다. 레코드 연결에만 의존하지 마십시오. |
| `buyingGroupID` | `AJOB2B-1_5_4-buying_group`(`_id`)과(와) 일치 | 노드 변경이 구매 그룹 속성인 경우 구매 그룹 식별자. |
| `lastUpdatedDate` |  | 업데이트 시간을 기록합니다. 현재 비어 있습니다. 활동 날짜에 타임스탬프를 사용하십시오. |

## `AJOB2B-1_5_4-buying_group_event`

각 레코드는 신규 상태 및 변경 시기를 포함하여 구매 그룹의 상태 변경을 캡처합니다. 새 단계 필드는 현재 채워져 있지 않습니다.

**형식:** 관련 레코드 형식

### 구매 그룹 상태가 변경됨(`buyingGroup.changeStatus`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `buyingGroup.changeStatus`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `buyingGroupID` | `AJOB2B-1_5_4-buying_group`(`_id`)과(와) 일치 | 구매 그룹 식별자. |
| `newStatus` |  | 새 상태 값입니다. |
| `newStage` |  | 새로운 구매 그룹 단계. 현재 비어 있습니다. |
| `lastUpdatedDate` |  | 업데이트 시간을 기록합니다. |

>[!NOTE]
>
>**가용성 참고 사항:** `newStatus`을(를) 사용하여 상태 변경 내용을 보고합니다. `newStage`은(는) 현재 비어 있으므로 단계 변경을 보고하지 마십시오.

## `AJOB2B-1_5-person_event`

각 레코드는 개인 수준의 웹, 이메일 또는 기타 지원되는 활동 이벤트에 대해 설명합니다. `eventType` 및 `timestamp`을(를) 사용하여 시간 경과에 따른 동작을 분석합니다. 이벤트 관련 세부 정보는 일치하는 이벤트 유형에 대해서만 채워집니다.

**형식:** 표준 Adobe 형식

`eventType`이(가) 발생한 상황을 알려줍니다. 다음 표에서는 각 활동 유형에 대한 필드를 설명합니다. 이벤트에 적용되지 않는 세부 사항은 비어 있습니다.

### 보낸 전자 메일(`directMarketing.emailSent`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailSent`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.emailSent.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.emailSent.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.emailSent.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.emailSent.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.emailSent.mailingName` |  | 메일 이름. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |

### 전자 메일 전달됨(`directMarketing.emailDelivered`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailDelivered`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.mailingName` |  | 메일 이름. |
| `directMarketing.email` |  | 이메일 주소. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |

### 이메일 구독 취소(`directMarketing.emailUnsubscribed`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailUnsubscribed`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.mailingName` |  | 메일 이름. |
| `directMarketing.email` |  | 이메일 주소. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |

### 전자 메일 열림(`directMarketing.emailOpened`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailOpened`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.mailingName` |  | 메일 이름. |
| `directMarketing.email` |  | 이메일 주소. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |
| `device.isMobileDevice` |  | 활동에 대해 모바일 장치가 기록되었는지 여부입니다. |
| `device.model` |  | 장치 또는 이메일 클라이언트 정보. |
| `environment.browserDetails.userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `environment.operatingSystem` |  | 운영 체제. |

### 클릭한 전자 메일 링크(`directMarketing.emailClicked`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailClicked`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.mailingName` |  | 메일 이름. |
| `directMarketing.email` |  | 이메일 주소. |
| `directMarketing.linkURL` |  | 링크 URL을 클릭했습니다. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |
| `device.isMobileDevice` |  | 활동에 대해 모바일 장치가 기록되었는지 여부입니다. |
| `device.model` |  | 장치 또는 이메일 클라이언트 정보. |
| `environment.browserDetails.userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `environment.operatingSystem` |  | 운영 체제. |

### 반송된 전자 메일(`directMarketing.emailBounced`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailBounced`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.mailingName` |  | 메일 이름. |
| `directMarketing.email` |  | 이메일 주소. |
| `directMarketing.emailBouncedCode` |  | 반송 범주/코드. |
| `directMarketing.emailBouncedDetails` |  | 세부 사항 텍스트. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |

### 전자 메일 소프트 바운스(`directMarketing.emailBouncedSoft`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `directMarketing.emailBouncedSoft`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `directMarketing.mailingKey.sourceID` |  | 자산 ID 메일링. |
| `directMarketing.mailingKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `directMarketing.mailingKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `directMarketing.mailingKey.sourceKey` |  | 전체 이메일 콘텐츠 식별자. |
| `directMarketing.mailingName` |  | 메일 이름. |
| `directMarketing.email` |  | 이메일 주소. |
| `directMarketing.emailBouncedCode` |  | 반송 범주/코드. |
| `directMarketing.emailBouncedDetails` |  | 세부 사항 텍스트. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |

### 웹 페이지 조회함(`web.webpagedetails.pageViews`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `web.webpagedetails.pageViews`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `web.webPageDetails.webPageKey.sourceID` |  | 페이지 자산 ID. |
| `web.webPageDetails.webPageKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `web.webPageDetails.webPageKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `web.webPageDetails.webPageKey.sourceKey` |  | 전체 페이지 식별자. |
| `web.webPageDetails.name` |  | 페이지 이름. |
| `web.webPageDetails.URL` |  | 페이지 URL. |
| `web.webPageDetails.queryParameters` |  | 웹 주소에 포함된 추가 정보. |
| `web.webPageDetails.webPageID` |  | 페이지 ID. |
| `environment.browserDetails.userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `web.webReferrer.URL` |  | 레퍼러 URL. |

### 클릭한 웹 링크(`web.webinteraction.linkClicks`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `web.webinteraction.linkClicks`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `web.webInteraction.webInteractionKey.sourceID` |  | 상호 작용 에셋 ID. |
| `web.webInteraction.webInteractionKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `web.webInteraction.webInteractionKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `web.webInteraction.webInteractionKey.sourceKey` |  | 전체 상호 작용 식별자. |
| `web.webInteraction.linkID` |  | 링크 ID. |
| `web.webInteraction.linkURL` |  | 대상 URL. |
| `web.webPageDetails.queryParameters` |  | 웹 주소에 포함된 추가 정보. |
| `web.webPageDetails.webPageID` |  | 페이지 ID. |
| `environment.browserDetails.userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `web.webReferrer.URL` |  | 레퍼러 URL. |

### 양식 제출됨(`web.formFilledOut`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `web.formFilledOut`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `web.fillOutForm.webFormKey.sourceID` |  | 양식 에셋 ID. |
| `web.fillOutForm.webFormKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `web.fillOutForm.webFormKey.sourceInstanceID` |  | 인스턴스 ID입니다. |
| `web.fillOutForm.webFormKey.sourceKey` |  | 전체 양식 식별자. |
| `web.fillOutForm.webFormID` |  | 양식 ID |
| `web.fillOutForm.webFormName` |  | 양식 이름. |
| `web.webPageDetails.queryParameters` |  | 웹 주소에 포함된 추가 정보. |
| `web.webPageDetails.webPageID` |  | 페이지 ID. |
| `environment.browserDetails.userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `web.webReferrer.URL` |  | 레퍼러 URL. |

### 즐거운 순간 기록됨(`leadOperation.interestingMoment`)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 활동 식별자. |
| `eventType` |  | `leadOperation.interestingMoment`. |
| `timestamp` |  | 활동이 발생한 시간. |
| `personID` | `AJOB2B-1_5_1-person`(`personID`)과(와) 일치 | 개인 식별자. |
| `personKey.sourceID` |  | 연결된 시스템의 개인 식별자. |
| `personKey.sourceType` |  | 연결된 제품의 이름입니다. |
| `personKey.sourceInstanceID` |  | [!DNL Experience Platform] 환경 또는 연결된 계정의 식별자입니다. |
| `personKey.sourceKey` |  | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `leadOperation.interestingMoment.date` |  | 모멘트 날짜/시간. |
| `leadOperation.interestingMoment.description` |  | 설명. |
| `leadOperation.interestingMoment.source` |  | 관련 제품 또는 캠페인의 이름입니다. |
| `leadOperation.interestingMoment.type` |  | 레이블을 입력합니다. |
| `_experience.journeyOrchestration.stepEvents.journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 id(속하는 경우). |
| `_experience.journeyOrchestration.stepEvents.nodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 id(속하는 경우). |

## `AJOB2B-1_5_4-journey_node`

각 레코드는 여정 단계, 여정이 속한 레코드 및 단계의 종류를 설명합니다. 계정 및 개인 여정 단계 데이터 세트에도 동일한 단계가 나타날 수 있습니다. `journeyID`을(를) 적절한 여정에 일치시키십시오. 여러 데이터 세트에 표시되므로 한 단계를 두 번 이상 계산하지 마십시오.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 노드 레코드 ID(전체 값 사용). |
| `journeyID` | `AJOB2B-1_5_4-account_journey` 또는 `AJOB2B-1_5_4-person_journey`(`_id`)와 일치 | 상위 여정 식별자. |
| `nodeType` |  | 시작, 종료, 대기 또는 결정 등 여정 단계의 종류. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-account_relational`

각 레코드는 조직 세부 사항, 위치, 크기, 매출 및 사용자 정의 필드를 포함한 계정을 설명합니다. 이 정보를 사용하여 구매 그룹 및 여정 보고서에 계정 컨텍스트를 추가합니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 계정 레코드 ID(전체 값 사용). |
| `accountName` |  | 계정 이름. |
| `industry` |  | 업계 분류. |
| `country` |  | 국가. |
| `sicCode` |  | 표준 산업 분류 코드. |
| `domainName` |  | 주 웹 도메인. |
| `primaryEmailDomain` |  | 기본 이메일 도메인. |
| `street` |  | 상세 주소. |
| `city` |  | 도시. |
| `state` |  | 주 또는 지역. |
| `postalCode` |  | 우편 번호. |
| `region` |  | 지리적 지역. |
| `phoneNumber` |  | 전화번호. |
| `logoUrl` |  | 계정 로고의 URL. |
| `annualRevenue` |  | 연간 매출액. |
| `numberOfEmployees` |  | 직원 수. |
| `createdDate` |  | 레코드가 생성된 시간. |
| `sourceType` |  | 계정을 식별하는 연결된 시스템의 이름입니다. |
| `sourceInstanceID` |  | 연결된 시스템에 있는 조직 또는 계정의 식별자입니다. |
| `sourceID` |  | 연결된 시스템의 계정 식별자입니다. |
| `customAttributes` |  | 사용자 정의 필드 이름 및 값이 텍스트로 함께 저장됩니다. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-person_relational`

각 레코드는 연락처 정보, 작업 세부 정보, 식별자 및 사용자 정의 필드를 포함하여 개인을 설명합니다. 멤버십, 여정 및 활동 보고서에 개인 정보를 추가하는 데 사용합니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 관련 레코드를 일치시키는 데 사용되는 전체 개인 식별자. |
| `email` |  | 이메일 주소. |
| `firstName` |  | 이름. |
| `middleName` |  | 가운데 이름. |
| `lastName` |  | 성. |
| `jobTitle` |  | 직함. |
| `personType` |  | 개인 유형: 연락처, 잠재 고객 또는 보류 중인 잠재 고객. |
| `isLead` |  | 개인이 잠재 고객인지 여부. |
| `isAnonymous` |  | 개인의 익명 여부. |
| `salutation` |  | 인사나 존댓말 |
| `phone` |  | 기본 전화번호. |
| `mobile` |  | 휴대폰 번호. |
| `sourceType` |  | 사용자를 식별하는 연결된 시스템의 이름입니다(예: [!DNL Marketo Engage]). |
| `sourceInstanceID` |  | 연결된 시스템에 있는 조직 또는 계정의 식별자입니다. |
| `sourceID` |  | 연결된 시스템의 개인 식별자. |
| `identityNamespace` |  | 추가 개인 식별자 종류를 식별하는 레이블입니다. |
| `identityValue` |  | 보조 ID 값. |
| `customAttributes` |  | 사용자 정의 필드 이름 및 값이 텍스트로 함께 저장됩니다. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-account_person`

각 레코드는 계정 프로필을 개인 프로필에 연결합니다. 이를 사용하여 계정 및 개인 프로필 데이터 세트 간 관계를 보고할 수 있습니다.

**형식:** 관련 레코드 형식

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 계정-사용자 관계 레코드 ID(전체 값 사용). |
| `accountID` | `AJOB2B-1_5_4-account_relational`(`_id`)과(와) 일치 | 전체 계정 식별자(`account_relational._id` 참조). |
| `personID` | `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치 | 전체 사용자 식별자(`person_relational._id` 참조). |
| `createdDate` |  | 계정-사용자 관계가 생성된 시간. |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

## `AJOB2B-1_5_4-person_event_relational`

각 레코드는 웹 페이지 보기, 이메일과 상호 작용 또는 여정 이동과 같은 지원되는 개인 활동을 설명합니다. 발생한 내용을 이해하려면 `eventType` 및 `activityTypeID`을(를) 사용합니다. 해당 활동 유형과 관련된 세부 사항만 채워집니다.

**형식:** 관련 레코드 형식

다음 필드 목록은 지원되는 모든 활동 유형을 다룹니다. 개별 레코드에는 활동에 적용되는 세부 사항만 포함됩니다.

>[!NOTE]
>
>**가용성:** 일부 활동에 빈 `_id`이(가) 있을 수 있습니다. 모든 활동에 사용 가능한 레코드 식별자가 있다고 가정하지 마십시오. 데이터 세트는 완전한 활동 내역을 보장하지 않습니다.

여정 활동(`person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`) 및 &quot;사용자 프로필 업데이트&quot; 여정 단계와 연결된 `person.attributeChanged` 활동에 대해 여정 세부 정보(`journeyID`, `journeyNodeID`, `journeyStepID` 및 유사한 필드)가 제공됩니다.

특성 변경 필드(`attributeName`, `attributeID`, `attributeNewValue`, `attributeOldValue`, `attributeChangeReason`)는 `person.attributeChanged`에 대해서만 채워집니다.

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id` | 레코드 ID | 사용 가능한 경우 활동의 식별자입니다. |
| `timestamp` |  | 활동이 발생한 시간. |
| `eventType` |  | 활동 레이블. 값: `web.webpagedetails.pageViews`, `web.formFilledOut`, `web.webinteraction.linkClicks`, `directMarketing.emailSent`, `directMarketing.emailDelivered`, `directMarketing.emailBounced`, `directMarketing.emailBouncedSoft`, `directMarketing.emailUnsubscribed`, `directMarketing.emailOpened`, `directMarketing.emailClicked`, `leadOperation.interestingMoment`, `person.attributeChanged`, `person.journeyAdd`, `person.journeyRemove`, `person.journeyStart`, `person.journeyEnd`, `person.journeyNodeTransition`, `person.journeySplitNode`. |
| `activityTypeID` |  | 활동 코드. `eventType`과(와) 함께 사용하여 동일한 이벤트 레이블을 공유하는 활동을 구분하십시오. |
| `personID` | `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치 | 활동을 개인 레코드에 일치시키는 데 사용되는 전체 개인 식별자. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 전체 여정 식별자. 여정과 연결되지 않은 활동의 경우 비어 있습니다. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 전체 여정 단계 식별자. 여정과 연결되지 않은 활동의 경우 비어 있습니다. |
| `previousJourneyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 이전 여정 노드(`person.journeyNodeTransition` 및 `person.journeySplitNode`에 대해 채워짐). |
| `newJourneyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 대상 여정 노드 ID(`person.journeyNodeTransition` 및 `person.journeySplitNode`)입니다. 일반적으로 `journeyNodeID`과(와) 같습니다. |
| `journeyStepID` |  | 활동과 연관된 여정 단계의 식별자입니다. |
| `journeyChoiceNumber` |  | `person.journeySplitNode`에 대한 분할 선택 번호입니다. 정수로 기록됩니다. |
| `journeyEntryCount` |  | 이 사용자가 여정(여정 추가/시작 이벤트에서 채워짐)에 들어간 횟수입니다. 정수로 기록됩니다. |
| `journeyProgramID` | 이 안내서에는 별도의 마케팅 프로그램 데이터 세트가 없습니다. | 여정 활동과 연관된 마케팅 프로그램의 식별자. |
| `activitySource` |  | 활동과 연관된 제품 또는 작업의 이름입니다. |
| `campaignID` |  | 활동이 캠페인 속성일 때 [!DNL Marketo Engage] 캠페인 id. |
| `attributeName` |  | 변경된 필드의 이름(`person.attributeChanged`만). |
| `attributeID` |  | 변경된 필드의 식별자입니다(`person.attributeChanged`만). |
| `attributeNewValue` |  | 텍스트로 기록된 새 필드 값(`person.attributeChanged`만). |
| `attributeOldValue` |  | 이전 필드 값이 텍스트로 기록되었습니다(`person.attributeChanged`만). |
| `attributeChangeReason` |  | 변경 이유 레이블(`person.attributeChanged`만). |
| `assetID` |  | 관련 이메일 콘텐츠, 페이지 또는 양식의 식별자입니다. |
| `assetName` |  | 관련 콘텐츠 이름. |
| `recipientEmail` |  | 가능한 경우 수신자 이메일 주소. 활동 코드 **27**(소프트 바운스) 및 **48**(판매 이메일 소프트 바운스)에 대해서만 채워지고, 다른 이메일 활동에 대해서는 비어 있습니다. 해당 활동에 대해 `personID`을(를) 사용하여 개인 레코드를 조회합니다. `assetName`은(는) 받는 사람의 주소가 아닌 전자 메일 콘텐츠를 식별합니다. |
| `bouncedCode` |  | 바운스 범주 코드(emailBounded/emailBoundedSoft만 해당). |
| `bouncedDetails` |  | 자세한 반송 이유(emailBounded/emailBoundedSoft만 해당). |
| `isMobileDevice` |  | 이메일 열기 또는 클릭에 대해 모바일 장치가 기록되었는지 여부. |
| `deviceModel` |  | 장치 모델(emailOpened/emailClicked만 해당). |
| `operatingSystem` |  | 운영 체제(emailOpened/emailClicked만 해당). |
| `userAgent` |  | 이메일 열기, 이메일 클릭 수 및 웹 활동에 대한 브라우저 또는 이메일 클라이언트 정보입니다. |
| `clickedLinkUrl` |  | 클릭한 이메일 링크 URL(emailClicked만 해당). |
| `webPageUrl` |  | 웹 페이지 URL(`web.webpagedetails.pageViews`만 해당). |
| `queryParameters` |  | 페이지 보기, 양식 제출 또는 웹 링크 클릭에 대한 웹 주소의 추가 정보입니다. |
| `webPageID` |  | [!DNL Marketo Engage] 웹 페이지 id(pageViews, formFilledOut, linkClicks). |
| `referrerUrl` |  | 레퍼러 URL(pageViews, formFilledOut, linkClicks). |
| `formID` |  | [!DNL Marketo Engage] 양식 id(`web.formFilledOut`만 해당). |
| `linkID` |  | [!DNL Marketo Engage] 링크 id(`web.webinteraction.linkClicks`만 해당). |
| `interestingMomentDate` |  | 모멘트 날짜(`leadOperation.interestingMoment`만 해당). |
| `interestingMomentDescription` |  | 자유 텍스트 설명(interestingMoment만 해당). |
| `interestingMomentSource` |  | 관련 제품 또는 캠페인(interestMoment만 해당). |
| `interestingMomentType` |  | 카테고리/유형(interestingMoment만 해당). |
| `isDeleted` |  | 이 레코드가 삭제된 것으로 표시되는지 여부. |
| `lastUpdatedDate` |  | 마지막 수정 시간. |

### 활동 유형별 필드 참조

다음 표는 각 활동에 적용되는 세부 사항을 보여 줍니다. 기타 세부 정보는 비어 있습니다. 일부 활동은 동일한 `eventType` 레이블을 공유합니다. 코드 8과 48은 모두 `directMarketing.emailBounced`을(를) 사용합니다. `activityTypeID`을(를) 사용하여 구분하십시오.

#### 본 웹 페이지(`web.webpagedetails.pageViews`)(활동 유형 1)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 페이지 ID. |
| `assetName` |  | 페이지 이름. |
| `webPageUrl` |  | 페이지 URL. |
| `queryParameters` |  | 웹 주소에 포함된 추가 정보. |
| `webPageID` |  | [!DNL Marketo Engage] 웹 페이지 id입니다. |
| `referrerUrl` |  | 레퍼러 URL. |
| `userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 양식 제출됨(`web.formFilledOut`)(활동 유형 2)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 양식 ID |
| `assetName` |  | 양식 이름. |
| `formID` |  | [!DNL Marketo Engage] 양식 id. |
| `queryParameters` |  | 웹 주소에 포함된 추가 정보. |
| `webPageID` |  | [!DNL Marketo Engage] 웹 페이지 id입니다. |
| `referrerUrl` |  | 레퍼러 URL. |
| `userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 클릭한 웹 링크(`web.webinteraction.linkClicks`)(활동 유형 3)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 상호 작용/링크 ID. |
| `assetName` |  | 대상 URL. |
| `linkID` |  | [!DNL Marketo Engage] 링크 id. |
| `queryParameters` |  | 웹 주소에 포함된 추가 정보. |
| `webPageID` |  | [!DNL Marketo Engage] 웹 페이지 id입니다. |
| `referrerUrl` |  | 레퍼러 URL. |
| `userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 보낸 전자 메일(`directMarketing.emailSent`)(활동 유형 6, 39)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 전달된 전자 메일(`directMarketing.emailDelivered`)(활동 유형 7, 45)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 이메일 구독 취소(`directMarketing.emailUnsubscribed`)(활동 유형 9)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 이메일 열림(`directMarketing.emailOpened`)(활동 유형 10, 40)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `isMobileDevice` |  | 활동에 대해 모바일 장치가 기록되었는지 여부입니다. |
| `deviceModel` |  | 디바이스 모델. |
| `operatingSystem` |  | 운영 체제. |
| `userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 클릭한 전자 메일 링크(`directMarketing.emailClicked`)(활동 유형 11, 41)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `clickedLinkUrl` |  | 링크 URL을 클릭했습니다. |
| `isMobileDevice` |  | 활동에 대해 모바일 장치가 기록되었는지 여부입니다. |
| `deviceModel` |  | 디바이스 모델. |
| `operatingSystem` |  | 운영 체제. |
| `userAgent` |  | 브라우저 또는 이메일 클라이언트 정보. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 반송된 전자 메일(`directMarketing.emailBounced`): 하드 바운스(활동 유형 8)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `bouncedCode` |  | 바운스 범주 코드. |
| `bouncedDetails` |  | 자세한 바운스 이유. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

이 활동은 `directMarketing.emailBounced` 레이블을 활동 코드 48과 공유하지만 코드 8에 대해 `recipientEmail`이(가) 비어 있습니다. `activityTypeID`을(를) 사용하여 두 항목을 구분하십시오.

#### 반송된 전자 메일(`directMarketing.emailBounced`): 판매 전자 메일 소프트 바운스(활동 유형 48)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `recipientEmail` |  | 수신자 이메일 주소. |
| `bouncedCode` |  | 바운스 범주 코드. |
| `bouncedDetails` |  | 자세한 바운스 이유. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 전자 메일 소프트 바운스(`directMarketing.emailBouncedSoft`)(활동 유형 27)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `assetID` |  | 메일링 ID. |
| `assetName` |  | 메일 이름. |
| `recipientEmail` |  | 수신자 이메일 주소. |
| `bouncedCode` |  | 바운스 범주 코드. |
| `bouncedDetails` |  | 자세한 바운스 이유. |
| `campaignID` |  | 캠페인 특성을 사용하는 경우 [!DNL Marketo Engage] 캠페인 id입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 즐거운 순간 기록됨(`leadOperation.interestingMoment`)(활동 유형 46)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `interestingMomentDate` |  | 모멘트 날짜/시간. |
| `interestingMomentDescription` |  | 자유 텍스트 설명. |
| `interestingMomentSource` |  | 관련 제품 또는 캠페인의 이름입니다. |
| `interestingMomentType` |  | 레이블을 입력합니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

`assetID` 및 `assetName`이(가) 이 활동 유형에 대해 채워지지 않았습니다.

#### 개인 필드 변경됨(`person.attributeChanged`)(활동 유형 13)

&quot;개인 프로필 업데이트&quot; 단계와 같이 변경 사항이 여정과 연결된 경우에만 포함됩니다. 여정 외부의 변경 사항은 포함되지 않습니다.

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `attributeName` |  | 변경된 필드의 이름. |
| `attributeID` |  | 변경된 필드의 식별자. |
| `attributeNewValue` |  | 텍스트로 기록된 새 필드 값. |
| `attributeOldValue` |  | 이전 필드 값, 텍스트로 기록됨. |
| `attributeChangeReason` |  | 변경 사유 레이블입니다. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자. |
| `journeyStepID` |  | 여정 단계의 식별자. |
| `journeyProgramID` | 이 안내서에는 별도의 마케팅 프로그램 데이터 세트가 없습니다. | 여정 프로그램 id. |
| `activitySource` |  | 활동과 연관된 제품 또는 작업입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 여정(`person.journeyAdd`, `person.journeyStart`)에 추가되거나 시작된 사용자(활동 유형 182, 184)

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자. |
| `journeyStepID` |  | 여정 단계의 식별자. |
| `journeyEntryCount` |  | 해당 사용자가 여정에 들어간 횟수입니다. |
| `journeyProgramID` | 이 안내서에는 별도의 마케팅 프로그램 데이터 세트가 없습니다. | 여정 프로그램 id. |
| `activitySource` |  | 활동과 연관된 제품 또는 작업입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 사용자가 여정(`person.journeyRemove`, `person.journeyEnd`)에서 제거되었거나 종료되었습니다(활동 유형 183, 185).

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자. |
| `journeyStepID` |  | 여정 단계의 식별자. |
| `journeyProgramID` | 이 안내서에는 별도의 마케팅 프로그램 데이터 세트가 없습니다. | 여정 프로그램 id. |
| `activitySource` |  | 활동과 연관된 제품 또는 작업입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 사용자가 여정 분기(`person.journeySplitNode`)를 팔로우했습니다(활동 유형 186).

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 여정 노드 식별자(분할 노드). |
| `previousJourneyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 분할 전에 사용자가 있었던 노드입니다. |
| `newJourneyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 사용자가 이동한 노드입니다(일반적으로 `journeyNodeID`과(와) 같음). |
| `journeyStepID` |  | 여정 단계의 식별자. |
| `journeyChoiceNumber` |  | 분할의 어느 분기가 가져갔습니까? |
| `journeyProgramID` | 이 안내서에는 별도의 마케팅 프로그램 데이터 세트가 없습니다. | 여정 프로그램 id. |
| `activitySource` |  | 활동과 연관된 제품 또는 작업입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

#### 여정 단계(`person.journeyNodeTransition`) 간에 사람이 이동했습니다(활동 유형 600).

| 필드 이름 | 관계 | 설명 내용 |
|------------|-------------|-------------|
| `_id`, `timestamp`, `eventType`, `activityTypeID`, `personID` | 레코드 ID: `_id`; `personID`이(가) `AJOB2B-1_5_4-person_relational`(`_id`)과(와) 일치함 | 공통 필드. |
| `journeyID` | `AJOB2B-1_5_4-person_journey`(`_id`)과(와) 일치 | 여정 식별자. |
| `journeyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 현재 여정 노드 식별자. |
| `previousJourneyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 개인이 전환된 노드입니다. |
| `newJourneyNodeID` | `AJOB2B-1_5_4-person_journey_node`(`_id`)과(와) 일치 | 사용자가 전환한 노드(일반적으로 `journeyNodeID`과(와) 같음). |
| `journeyStepID` |  | 여정 단계의 식별자. |
| `journeyProgramID` | 이 안내서에는 별도의 마케팅 프로그램 데이터 세트가 없습니다. | 여정 프로그램 id. |
| `activitySource` |  | 활동과 연관된 제품 또는 작업입니다. |
| `isDeleted`, `lastUpdatedDate` |  | 공통 필드. |

## 고객 소유 데이터 세트 {#customer-owned-datasets}

조직은 계정 또는 사용자에 대해 자체 [!DNL Experience Platform] 데이터 세트를 사용할 수 있습니다. 구성된 경우 [!DNL Adobe Journey Optimizer B2B Edition]은(는) 다른 계정이나 개인 데이터 세트를 만드는 대신 해당 데이터 세트에 정보를 추가할 수 있습니다.

이름 및 사용 가능한 필드는 조직의 설정에 따라 다릅니다. 구성된 계정 또는 개인 식별자를 사용하여 일치하는 레코드를 인식합니다. 이러한 데이터 세트에 레코드가 있다고 해서 대상자가 자동으로 사용할 수 있는 것은 아닙니다. 사용 가능 여부는 [!DNL Experience Platform] 구성에 따라 다릅니다.
