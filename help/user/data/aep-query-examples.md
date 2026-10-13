---
title: 데이터 세트 쿼리
description: Adobe Journey Optimizer B2B Edition에서 내보낸 계정, 구매 그룹, 개인 및 여정 데이터를 분석하기 위해 쿼리 서비스의 SQL 쿼리 예를 사용하는 방법에 대해 알아봅니다.
feature: Reporting, Data Management
role: Admin, Developer
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
feature_v2:
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: 6db81a0b993f450a3ff448dcb4c417e3e81ec70a
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 1%
---

# 데이터 세트 쿼리

[!DNL Adobe Journey Optimizer B2B Edition]이(가) [!DNL Adobe Experience Platform]에 내보내는 계정, 개인, 구매 그룹 및 여정 데이터를 분석하기 위해 바로 사용할 수 있는 SQL 쿼리 예제를 찾으십시오. 계정, 구매 그룹, 전자 메일 참여 및 여정 활동에 대해 보고하려면 [!DNL Query Service]에서 쿼리를 실행하십시오.

이러한 쿼리에 사용되는 데이터 세트 및 필드에 대한 설명은 [내보낸 데이터 세트](./aep-exported-datasets.md)를 참조하십시오.

## 필요 조건 {#prerequisites}

이 페이지에서 쿼리를 실행하기 전에 다음 사항이 있는지 확인하십시오.

* **[!DNL Query Service]에 액세스:** [!DNL Experience Platform] 샌드박스에서 [쿼리 서비스](https://experienceleague.adobe.com/ko/docs/experience-platform/query/home){target="_blank"}에 액세스할 수 있어야 합니다.
* **사용 가능한 데이터 세트:** 쿼리는 내보낸 [!DNL Journey Optimizer B2B Edition]개 데이터 세트를 대상으로 합니다. 샌드박스에서 **[!UICONTROL 데이터 세트]**(으)로 이동하여 데이터 세트가 존재하며 데이터를 포함하는지 확인하십시오.
* **스키마 필드 값:** 쿼리의 필드에 해당 스키마의 값이 있는지 확인하십시오. 빈 필드는 결과를 반환하지 않으며 오류를 생성하지 않습니다.

>[!NOTE]
>
>이 예제에서는 `account_table` 및 `person_activity_table`과(와) 같은 짧은 테이블 이름을 사용합니다. 각 테이블 이름을 샌드박스의 해당 데이터 세트 이름으로 바꿉니다. 데이터 세트 이름에 하이픈이 있으면 큰따옴표로 묶습니다. `Example Company` 및 `PASTE_COMPLETE_JOURNEY_ID_HERE`과(와) 같은 자리 표시자 값을 환경의 값으로 바꿉니다.

## 쿼리 실행 {#run}

이 페이지에서 예제를 실행하려면:

1. [!DNL Experience Platform]에서 **[!UICONTROL 쿼리 서비스]** > **[!UICONTROL 쿼리]**&#x200B;를 선택합니다.
1. 예제를 쿼리 편집기에 붙여 넣은 다음 테이블 이름 및 자리 표시자 값을 바꿉니다.
1. **[!UICONTROL 실행]**&#x200B;을 선택합니다.

날짜별로 필터링하는 예제는 지난 30일을 사용합니다. 시간 범위를 변경하려면 `INTERVAL '30' DAY` 값을 편집하십시오.

## 쿼리 선택

다음 표를 사용하여 보고 작업에 대한 쿼리를 선택합니다.

| 다음을 원합니다. | 다음으로 이동 |
|---|---|
| 계정 이름, 업계 및 위치 검토 | [계정 세부 정보 검토](#account-details) |
| 계약별 구매 그룹 비교 | [구매 그룹 참여 비교](#buying-group-engagement) |
| 계정과 연결된 사람 찾기 | [계정에서 사람 찾기](#account-people) |
| 구매 그룹 상태 변경 추적 | [구매 그룹 상태 변경 검토](#buying-group-status-changes) |
| 이메일을 클릭한 사람 찾기 | [전자 메일을 클릭한 사람 찾기](#email-clicks) |
| 유형별 최근 활동 비교 | [최근 사용자 활동 비교](#person-activity) |
| 크기별 계정 여정 비교 | [계정별 여정 수 비교](#account-journey-counts) |
| 여정 내 계정 나열 | [여정에 계정 나열](#journey-accounts) |
| 일일 계정 여정 활동 추적 | [일일 계정 활동 추적](#account-daily-activity) |
| 여정 내 계정 내역 조사 | [계정 여정 타임라인 검토](#account-timeline) |
| 크기 및 상태별 개인 여정 비교 | [여정에 따른 사용자 수 비교](#person-journey-counts) |
| 여정에 있는 사람 나열 | [여정에 있는 사람 나열](#journey-people) |
| 여정 내 사람 위치 확인 | [단계별로 사용자 수 비교](#person-step-counts) |
| 최근 개인 여정 활동 추적 | [최근 여정 활동 추적](#person-journey-activity) |
| 여정에 있는 사람의 내역 조사 | [개인 여정 타임라인 검토](#person-timeline) |

## 계정 및 구매 그룹 쿼리

이러한 쿼리를 사용하여 계정, 구매 그룹 및 보고에 사용할 수 있는 사람을 검토하십시오.

### 계정 세부 정보 검토 {#account-details}

계정 이름, 업종, 위치 및 회사 규모를 검토하여 보고에 사용할 수 있는 계정을 파악합니다.

```sql
SELECT
a._id AS accountID,
a.accountName,
a.industry,
a.country,
a.numberOfEmployees
FROM account_table a
WHERE a.isDeleted = FALSE
ORDER BY a.accountName
LIMIT 100;
```

### 구매 그룹 참여 비교 {#buying-group-engagement}

완전성 및 솔루션 흥미와 함께 기록된 참여 점수별로 구매 그룹을 비교합니다.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
bg.engagementScore,
bg.completenessScore,
bg.solutionInterest,
bg.buyingGroupStatus
FROM buying_group_table bg
WHERE bg.isDeleted = FALSE
ORDER BY bg.engagementScore DESC NULLS LAST, bg.buyingGroupName
LIMIT 100;
```

### 계정에서 사람 찾기 {#account-people}

계정과 연결된 직원과 직책을 찾아 연락처를 파악합니다. `Example Company`을(를) 샌드박스의 계정 이름으로 바꾸십시오.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
p._id AS personID,
p.firstName,
p.lastName,
p.email,
p.jobTitle
FROM account_member_table m
JOIN account_table a ON m.accountID = a._id
JOIN person_table p ON m.personID = p._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND p.isDeleted = FALSE
AND a.accountName = 'Example Company'
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### 구매 그룹 상태 변경 검토 {#buying-group-status-changes}

지난 30일 동안의 구매 그룹 상태 변경 사항을 검토하여 시간이 지남에 따라 그룹이 어떻게 변경되는지 파악합니다.

```sql
SELECT
bg._id AS buyingGroupID,
bg.buyingGroupName,
e.timestamp AS changedAt,
e.newStatus
FROM buying_group_event_table e
JOIN buying_group_table bg ON e.buyingGroupID = bg._id
WHERE bg.isDeleted = FALSE
AND e.eventType = 'buyingGroup.changeStatus'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## 개인 참여 쿼리

이러한 쿼리를 사용하여 이메일 참여 및 기타 기록된 개인 활동을 검토하십시오.

### 이메일을 클릭한 사람 찾기 {#email-clicks}

최근 이메일 참여를 검토하려면 지난 30일 동안 기록된 이메일 클릭으로 사용자를 식별합니다.

```sql
SELECT DISTINCT
p._id AS personID,
p.firstName,
p.lastName,
p.email
FROM person_activity_table e
JOIN person_table p ON e.personID = p._id
WHERE e.isDeleted = FALSE
AND p.isDeleted = FALSE
AND e.eventType = 'directMarketing.emailClicked'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY p.lastName, p.firstName
LIMIT 100;
```

### 최근 개인 활동 비교 {#person-activity}

기록된 활동 유형과 관련된 사람 수를 비교하여 최근 참여를 파악합니다.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC
LIMIT 100;
```

## 계정 여정 쿼리

이러한 쿼리를 사용하여 계정 여정을 분석합니다. `PASTE_COMPLETE_JOURNEY_ID_HERE`을(를) 계정 여정의 `_id` 값으로 바꾸고 `PASTE_COMPLETE_ACCOUNT_ID_HERE`을(를) 계정의 `_id` 값으로 바꿉니다.

### 계정별 여정 수 비교 {#account-journey-counts}

상태 및 기록된 멤버십 카운트별로 계정 여정을 비교하여 계정 인구가 가장 많은 여정을 확인합니다.

```sql
SELECT
j._id AS journeyID,
j.accountJourneyName,
j.accountJourneyStatus,
COUNT(DISTINCT m.accountID) AS accountsWithRecordedMembership
FROM account_journey_table j
LEFT JOIN account_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.accountID <> ''
WHERE j.isDeleted = FALSE
GROUP BY j._id, j.accountJourneyName, j.accountJourneyStatus
ORDER BY accountsWithRecordedMembership DESC, j.accountJourneyName
LIMIT 100;
```

### 여정 내 계정 나열 {#journey-accounts}

해당 업계 및 국가를 포함하여 특정 여정과 관련된 계정을 검토합니다.

```sql
SELECT DISTINCT
a._id AS accountID,
a.accountName,
a.industry,
a.country
FROM account_journey_member_table m
JOIN account_table a ON m.accountID = a._id
WHERE m.isDeleted = FALSE
AND a.isDeleted = FALSE
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY a.accountName, accountID
LIMIT 100;
```

### 일일 계정 활동 추적 {#account-daily-activity}

일별 계정 추가, 제거 및 단계 변경을 추적하여 지난 30일 동안의 여정 내 활동을 파악합니다.

```sql
SELECT
CAST(e.timestamp AS DATE) AS activityDate,
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.accountID) AS distinctAccounts
FROM account_activity_table e
WHERE e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.accountID IS NOT NULL
AND e.accountID <> ''
AND e.eventType IN (
'account.addAccountToJourney',
'account.removeAccountFromJourney',
'account.changeAccountJourneyNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY CAST(e.timestamp AS DATE), e.eventType
ORDER BY activityDate DESC, e.eventType
LIMIT 100;
```

### 계정 여정 타임라인 검토 {#account-timeline}

기록된 이벤트 및 여정 단계를 검토하여 계정의 최근 여정 내역을 조사합니다.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
n.nodeType,
e.previousJourneyNodeID,
e.buyingGroupID
FROM account_activity_table e
LEFT JOIN account_journey_node_table n
ON e.journeyNodeID = n._id
AND e.journeyID = n.accountJourneyID
AND n.isDeleted = FALSE
WHERE e.accountID = 'PASTE_COMPLETE_ACCOUNT_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```

## 개인 여정 쿼리

이러한 쿼리를 사용하여 개인 여정을 분석합니다. `PASTE_COMPLETE_JOURNEY_ID_HERE`을(를) 사용자 여정의 `_id` 값으로 바꾸고 `PASTE_COMPLETE_PERSON_ID_HERE`을(를) 사용자 `_id` 값으로 바꿉니다.

### 여정으로 개인 수 비교 {#person-journey-counts}

기록된 멤버십 수, 상태 및 날짜별로 개인 여정을 비교하여 크기 및 라이프사이클을 파악합니다.

```sql
SELECT
j._id AS journeyID,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate,
COUNT(DISTINCT m.personID) AS peopleWithRecordedMembership
FROM person_journey_table j
LEFT JOIN person_journey_member_table m
ON m.journeyID = j._id
AND m.isDeleted = FALSE
AND m.personID <> ''
WHERE j.isDeleted = FALSE
GROUP BY
j._id,
j.personJourneyName,
j.personJourneyStatus,
j.startDate,
j.endDate
ORDER BY peopleWithRecordedMembership DESC, j.personJourneyName
LIMIT 100;
```

### 여정에 사람 나열 {#journey-people}

여정과 연관된 사용자, 마지막으로 입력한 시기 및 입력한 빈도를 검토합니다.

```sql
SELECT DISTINCT
m.personID,
p.firstName,
p.lastName,
p.email,
m.membershipDate,
m.lastEntryDate,
m.entryCount,
m.reentryOpensAt,
m.journeyNodeID
FROM person_journey_member_table m
LEFT JOIN person_table p
ON m.personID = p._id
AND p.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
ORDER BY m.lastEntryDate DESC NULLS LAST, m.personID
LIMIT 100;
```

### 단계별로 개인 수 비교 {#person-step-counts}

사람들이 여정 멤버십에 기록된 단계를 가로질러 어떻게 분배되는지 확인하십시오.

```sql
SELECT
m.journeyNodeID,
n.nodeType,
COUNT(DISTINCT m.personID) AS peopleWithRecordedStep
FROM person_journey_member_table m
LEFT JOIN person_journey_node_table n
ON m.journeyNodeID = n._id
AND m.journeyID = n.personJourneyID
AND n.isDeleted = FALSE
WHERE m.isDeleted = FALSE
AND m.personID IS NOT NULL
AND m.personID <> ''
AND m.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
GROUP BY m.journeyNodeID, n.nodeType
ORDER BY peopleWithRecordedStep DESC, m.journeyNodeID
LIMIT 100;
```

### 최근 여정 활동 추적 {#person-journey-activity}

기록된 여정 시작, 종료 및 전환을 비교하여 지난 30일 동안 여정의 개인 활동을 이해합니다.

```sql
SELECT
e.eventType,
COUNT(*) AS recordedRows,
COUNT(DISTINCT e.personID) AS distinctPeople
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.personID IS NOT NULL
AND e.personID <> ''
AND e.eventType IN (
'person.journeyAdd',
'person.journeyRemove',
'person.journeyStart',
'person.journeyEnd',
'person.journeyNodeTransition',
'person.journeySplitNode'
)
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
GROUP BY e.eventType
ORDER BY recordedRows DESC, e.eventType
LIMIT 100;
```

### 개인 여정 타임라인 검토 {#person-timeline}

단계 전환, 분할 선택 사항 및 여정 속성 프로필 업데이트를 포함하여 개인의 최근 여정 내역을 조사합니다.

```sql
SELECT
e.timestamp AS activityAt,
e.eventType,
e.journeyNodeID,
e.previousJourneyNodeID,
e.newJourneyNodeID,
e.journeyChoiceNumber,
e.journeyEntryCount,
e.attributeName,
e.attributeOldValue,
e.attributeNewValue
FROM person_activity_table e
WHERE e.isDeleted = FALSE
AND e.personID = 'PASTE_COMPLETE_PERSON_ID_HERE'
AND e.journeyID = 'PASTE_COMPLETE_JOURNEY_ID_HERE'
AND e.timestamp >= CURRENT_TIMESTAMP - INTERVAL '30' DAY
AND e.timestamp < CURRENT_TIMESTAMP
ORDER BY e.timestamp DESC
LIMIT 100;
```
