---
title: 데이터 가용성 및 동기화 시간
description: '[!DNL Journey Optimizer B2B Edition] 여정에서 데이터 변경 내용이 표시되는 속도와 일반적인 타임라인을 알아봅니다.'
feature: Journeys, Data Management
role: User
autotag-review: '2026-10-08T18:36:33.252Z'
TQID: 'https://experienceleague.adobe.com/PA1IeRHnGWHmBtDpffzveoWIHOn99-Ctt4Y0OQb7CwE'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
    internal-label: Experience Platform
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: 095e8119-1425-57eb-9d8c-9e684f2c9771
    internal-label: Audiences
  - id: 33ca0c14-7e3b-55a1-8fd7-8a61b47da4e1
    internal-label: B2B
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: a50ad69b-1331-40e9-b634-531a085a6a54
    internal-label: Identities
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: eec185bd-7d60-4193-ba3f-da427569936a
    internal-label: Destinations
  - id: f2da1b69-6919-4386-a5d2-9c7b5c9033db
    internal-label: Data management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
source-git-commit: 827c313f032d482ac2b0a5fa8f41d6506e67b9cb
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%
---
# 데이터 가용성 및 동기화 시간 {#data-availability}

이 항목을 사용하여 [!DNL Adobe Journey Optimizer B2B Edition] 여정에서 데이터 변경 내용이 표시되는 속도와 일반적인 타임라인을 이해합니다. 예상 타이밍을 알면 그에 따라 여정을 디자인하고 지연이 예상되는 동작을 인식하는 데 도움이 됩니다.

## 예상 대기 시간

| 데이터 유형 | 일반적인 가용성 |
| --- | --- |
| [대상자 멤버십](#daily-refresh) | 최대 24시간(일일 주기) |
| [계정 및 사용자 관계 변경](#daily-refresh) | 최대 24시간(일일 주기) |
| [데이터 원본 [!DNL Experience Platform] 부터 [!DNL Journey Optimizer B2B Edition]](#platform-sync) | 최대 30분(실시간에 가까움) |
| [데이터 원본 [!DNL Journey Optimizer B2B Edition] 부터 [!DNL Experience Platform]](#platform-sync) | 최대 4시간(마이크로 배치) |
| [클릭 및 열기와 같은 활동 이벤트](#activity-and-actions) | 최대 4시간 |
| [[!DNL Marketo Engage] 추가 또는 제거 목록](#activity-and-actions) | 30분 이내(실시간에 가까움) |
| [Journey Optimizer B2B Edition에서 생성된 이벤트](#activity-and-actions) | 일괄 처리 대상에서만 사용 가능 |
| [LinkedIn 대상 모집단](#linkedin-timing) | 같은 날 36-40시간(최악의 경우) |

## 대상 및 관계 데이터 {#daily-refresh}

[!DNL Journey Optimizer B2B Edition]은(는) 일괄 처리 작업 스케줄러에서 트리거된 계정 및 개인 대상 멤버십을 하루에 한 번 평가합니다. 그 결과는 다음과 같습니다.

* 신규 대상자 자격을 얻은 계정 또는 직원은 자격 취득 후 24시간 이내에 여정에 들어갈 수 있습니다.
* 대상 기준에 대한 변경 사항은 다음 일별 평가 주기에 적용됩니다.
* 오늘 대상의 자격이 있지만 아직 여정에 들어가지 않은 계정이 있는 경우 조사하기 전에 다음 일별 주기가 완료될 때까지 기다리십시오.
* 연락처가 다른 계정으로 이동하는 경우와 같이 개인의 계정 연결이 변경되면 관계 업데이트가 일별 동기화 주기를 통해 24시간 이내에 전파됩니다. 계정 멤버십에 의존하는 여정은 다음 일별 주기 후에 업데이트된 관계를 반영합니다. 조치가 필요하지 않습니다.

>[!TIP]
>
>대상 멤버십이 실시간으로 업데이트되지 않고 매일 새로 고쳐진다는 점을 이해하여 여정을 디자인합니다. 실시간에 가까운 응답이 필요한 경우 대상 기반 항목 대신 [이벤트 기반 트리거](../journeys/listen-for-event-nodes.md)를 사용하십시오.

## [!DNL Experience Platform]과(와) 데이터 동기화 {#platform-sync}

[!DNL Experience Platform]은(는) 계정, 사용자 및 기회에 대한 기본 데이터 저장소이며 [!DNL Journey Optimizer B2B Edition]은(는) 여정, 구매 그룹 및 구매 그룹 역할을 소유합니다. [아키텍처에 대해 자세히 알아보기](../about-journey-optimizer-b2b-edition.md#high-level-architecture).

데이터는 서로 다른 속도로 각 방향으로 두 시스템 간에 이동합니다.

* **[!DNL Experience Platform]에서[!DNL Journey Optimizer B2B Edition]**&#x200B;까지 - 데이터가 거의 실시간으로 동기화되며 최대 30분이 소요될 수 있습니다.
* **[!DNL Journey Optimizer B2B Edition]에서[!DNL Experience Platform]**&#x200B;까지 - 마이크로 배치로 데이터를 동기화하며 최대 4시간 정도 소요될 수 있습니다.

## 활동 이벤트 및 여정 작업 {#activity-and-actions}

활동 데이터 및 여정 작업의 타이밍은 시스템 간에 데이터가 이동하는 방식에 따라 다릅니다.

* **활동 데이터** - 전자 메일 열기, 링크 클릭, 양식 채우기와 같은 개인 활동 레코드는 [!DNL Journey Optimizer B2B Edition]에 표시되는 데 약 4시간이 걸릴 수 있습니다. 이 시간은 일괄 처리 활동 데이터에 적용됩니다. [!DNL Experience Platform] 경험 이벤트 트리거는 스트리밍 데이터를 사용하며 거의 실시간으로 반응할 수 있습니다.
* **[!DNL Marketo Engage]작업** - [!DNL Marketo Engage]을(를) 호출하는 여정 작업은 API 호출이므로 실시간에 가깝습니다. 예를 들어 여정 단계에서 [!DNL Marketo] 목록에서 사용자를 추가하거나 제거하면 일반적으로 작업은 30분 이내에 완료됩니다. [여정 작업에 대해 자세히 알아보기](../journeys/action-nodes.md).
* [!DNL Experience Platform]**을(를) 거치는**&#x200B;작업 - [!DNL Experience Platform]을(를) 먼저 반환하는 모든 작업은 일괄 처리되므로 실시간에 가까운 타이밍이 아닌 일괄 처리 타이밍이 적용됩니다.
* [!DNL Journey Optimizer B2B Edition]**에 의해 생성된**&#x200B;이벤트 - [!DNL Journey Optimizer B2B Edition]이(가) [!DNL Experience Platform]에서 생성하는 이벤트는 일괄 처리 대상에서만 사용할 수 있습니다.

## 대상 [!DNL LinkedIn]개 {#linkedin-timing}

여정에 [!DNL LinkedIn] 대상 작업이 포함된 경우 여정을 게시한 후에는 다음 타임라인이 필요합니다.

| 시나리오 | 예상 대기 |
| --- | --- |
| 여정이 게시되었을 때 계정이 이미 대상자에 있었습니다. | 현지 시간 자정 전에 처리가 완료되는 경우 같은 날 |
| 여정이 게시된 후 계정이 도착함 | 최대 24시간 |
| 첫 번째 일별 동기화 기간 후에 계정이 도착함 | 최대 36-40시간 |

[!DNL LinkedIn]개의 대상자 규모가 즉시 업데이트되지 않을 수 있습니다. 이 지연은 [!DNL Experience Platform]이(가) 대상 파일을 처리하고 [!DNL LinkedIn]에 전달하는 동안 예상되는 지연입니다. 48시간 후에도 대상자 규모가 여전히 0이면 조사합니다. [LinkedIn 계정 일치 대상에 대해 자세히 알아보세요](./linkedin-account-matched-audiences.md).
