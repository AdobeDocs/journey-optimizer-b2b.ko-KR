---
title: 이벤트 노드 수신
description: Journey Optimizer B2B edition Prime에서 이벤트 노드 수신 대기를 구성 - 이벤트 트리거를 설정하고, 선택적 필터를 적용하고, 활동이나 데이터 변경이 발생할 때 인력을 배치합니다.
autotag-review: '2026-06-12T23:00:36.531Z'
TQID: 'https://experienceleague.adobe.com/SBEfrrIKSCnO5x1tGXQTz1EZryH0IKhQx4tuqVn78FI'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d0031543-532c-4a26-8f90-01af2b91e6d0
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3368f815edc0ce817cb7ed371157b63fa548d848
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 8%

---

# 이벤트 노드 수신

이벤트가 발생할 때 대상을 여정의 다음 단계로 이동하려면 _이벤트 수신_ 노드를 추가하십시오.

## 이벤트 트리거 {#event-triggers}

PM에서 목록 가져오기

## 이벤트 필터 {#event-filters}

PM에서 업데이트 목록 받기

| 필터 | 설명 |
| ------- | ----------- |
| 활동 내역 > 이메일 | 하나 이상의 선택한 이메일 메시지를 사용하여 평가되는 조건에 따른 이메일 활동: <li>이메일 링크 클릭됨 <li>이메일 열람함 |
| 활동 내역 > 데이터 값 변경됨 | 선택한 개인 속성의 경우 값이 변경되었습니다. 이러한 변경 유형은 다음과 같습니다. <li>새 값 <li>이전 값 <li>이유 <li>소스 <li>활동 날짜 <li> 최소. 횟수 |

## 이벤트 노드 추가 {#add-event-node}

1. 여정 캔버스로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 이벤트 수신]**&#x200B;을 선택합니다.

   ![여정 경로에서 추가 아이콘 클릭](./assets/person-journey-canvas-add-node.png){width="200"}

1. 오른쪽의 노드 속성에서 **[!UICONTROL 이벤트 조건 추가]**&#x200B;를 클릭합니다.

1. _[!UICONTROL 이벤트 편집]_ 대화 상자에서 트리거할 이벤트를 추가합니다.

   ![이벤트 편집 - 이벤트 트리거](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (선택 사항) 대화 상자에서 **[!UICONTROL 필터]** 탭을 선택하고 트리거에 대한 필터링 기준을 추가합니다.

1. **[!UICONTROL 이벤트 편집]**&#x200B;을 클릭하고 이벤트에 대한 세부 정보를 정의하십시오.

   ![이벤트 편집 - 이벤트 필터링](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](../../user/journeys/assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>이벤트 노드 수신에 대한 시간 제한 기능이 현재 작동하지 않습니다. 향후 릴리스로 예정되어 있습니다.
