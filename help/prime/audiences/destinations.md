---
title: 대상
description: Journey Optimizer B2B Prime에서 대상을 연결하고 정적 사용자 목록을 활성화하여 대상 데이터를 광고, 이메일 및 기타 마케팅 플랫폼으로 내보내는 방법을 알아봅니다.
autotag-review: '2026-06-17T18:30:02.442Z'
TQID: 'https://experienceleague.adobe.com/xO1p-VvIfv1KB77g0l2-fFRHQ0w2hy97vnG1QHpMw8c'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1cb68e8933d6b1abba3cc82f154344d1dde51818
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 2%

---

# 대상

대상은 사용자 목록 데이터를 [!DNL Adobe Journey Optimizer B2B Prime]에서 광고 네트워크, 전자 메일 서비스 공급자 및 CRM 시스템과 같은 외부 마케팅 플랫폼으로 내보낼 수 있는 미리 빌드된 통합입니다. [!DNL Journey Optimizer B2B Prime]에서 해당 대상을 다운스트림 채널에서 타기팅 및 참여에 사용할 수 있도록 대상에 대해 [정적 사용자 목록](./people-lists.md#static-list)(Marketo Engage 사용자 레코드로 구성)을 활성화합니다.

<!-- 
Does not align w/AEP info for Beta

Activating a static list to a destination follows a three-step process:

1. **Connect** — Authenticate and configure a connection to a destination platform.
1. **Map** — Select the static list and map its people attributes to the fields required by the destination.
1. **Schedule** — Define when and how often the list data is exported to the destination.

Destination activations reflect the membership state of the static list at the time of each synch.

## Destination types {#destination-types}

[!DNL Journey Optimizer B2B Prime] supports the following destination types for activating static people lists:

| Type | Description |
|--- |--- |
| Streaming | Real-time API-based connections that push audience membership updates to the destination as they occur. |
| File-based (batch) | Scheduled exports that deliver audience data as structured files to cloud storage or SFTP locations, which the destination platform then ingests. |

-->

## 대상 연결 {#connect-destination}

1. 왼쪽 탐색에서 **[!UICONTROL 연결]**&#x200B;을 확장하고 **[!UICONTROL 대상]**&#x200B;을 선택합니다.

1. _[!UICONTROL 카탈로그]_ 탭에서 외부 대상 유형 커넥터를 찾습니다.

   >[!TIP]
   >
   >검색 상자에 `LinkedIn` 등의 이름을 입력하여 커넥터를 빠르게 찾을 수 있습니다.

   ![사용 가능한 커넥터 유형에 액세스](./assets/destinations-catalog.png){width="800" zoomable="yes"}

1. 커넥터 카드에서 **[!UICONTROL 새 대상 구성]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 새 계정]**&#x200B;을 선택하고 계정 자격 증명을 입력하십시오.

   ![새 대상 계정 연결](./assets/destinations-configure-new.png){width="500"}

1. **[!UICONTROL 대상에 연결]**&#x200B;을 클릭합니다.

   >[!IMPORTANT]
   >
   >이 시점에서 **하지 않음** _[!UICONTROL 대상 세부 정보]_&#x200B;를 입력하십시오. 연결만 필요합니다.

1. 데이터 거버넌스 및 마케팅 작업 설정을 검토한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

연결된 대상이 _[!UICONTROL 찾아보기]_ 탭의 목록에 나타나며 정적 목록 활성화에 사용할 수 있습니다.

## 대상에 정적 목록 활성화 {#activate}

>[!NOTE]
>
>[정적 사용자 목록](./people-lists.md#static-list)만 [!DNL Journey Optimizer B2B Prime]의 대상에 대해 활성화할 수 있습니다. [동적 목록](./people-lists.md#dynamic-lists)은(는) 대상 활성화에 적합하지 않습니다.

1. 왼쪽 탐색에서 **[!UICONTROL 마케팅 관리]**&#x200B;를 확장합니다.

1. **[!UICONTROL 마케팅]** 리소스 목록의 오른쪽에서 **[!UICONTROL 사람 목록]**&#x200B;을 선택합니다.

   ![대상자 목록을 관리하도록 액세스](./assets/people-lists.png){width="800" zoomable="yes"}

1. **[!UICONTROL 정적 목록]** 탭을 선택합니다.

1. 대상에 활성화할 정적 목록을 찾습니다.

1. 정적 목록 이름 옆에 있는 _활성화_( ![활성화 아이콘](../../assets/do-not-localize/icon-falco-activate-dest.svg) ) 아이콘을 클릭합니다.

1. 구성된 대상 연결에 대한 확인란을 선택합니다.

   ![구성된 대상을 활성화하도록 사용](./assets/static-list-activate-destination-select.png){width="600" zoomable="yes"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

<!--

This method not working for Beta

1. On the _[!UICONTROL Browse]_ tab, locate the destination you want to use for the activation and click the name to open it.

1. Select the **[!UICONTROL Activation data]** tab.

1. Click **[!UICONTROL Activate people lists]**.

1. Select the static people list you want to export and click **[!UICONTROL Next]**.

1. Map the people list attributes to the required fields of the destination schema and click **[!UICONTROL Next]**.

1. Set the export schedule:

   * **[!UICONTROL Frequency]** — Choose how often the list is exported (for example, daily or weekly).
   * **[!UICONTROL Start date]** — Set when the first export should run.

1. Review the activation summary and click **[!UICONTROL Finish]**.

The activation is created and the static list data is exported to the destination according to the defined schedule.

-->
