---
title: 작업 노드 수행
description: 플레이스홀더
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1d0093ad5298593d291372d838794fe8cab5f646
workflow-type: tm+mt
source-wordcount: 821
ht-degree: 2%

---

# 작업 노드 수행

개인 여정에서 노드 경로의 모든 사용자에게 변경 사항을 적용하려면 사용자에 대한 작업을 사용하십시오.

## 작업 및 제한 {#actions}

| 액션 | 제한 |
| ------ | ----------- |
| **[!UICONTROL 대상에 활성화]** | <li>정적 목록 선택 또는 만들기 <li>목록에 활성화된 대상이 없으면 목록을 활성화합니다 |
| **[!UICONTROL 여정에 사용자 추가]** | <li>예약된 또는 라이브 여정 선택 <li>대상 여정의 대상 기준이 적용되지 않습니다 |
| **[!UICONTROL 목록에 추가]** | <li>새 정적 목록 만들기 또는 기존 정적 목록 선택 |
| **[!UICONTROL Marketo 목록에 추가]** | <li>Marketo Engage에서 정적 목록 선택 |
| **[!UICONTROL 데이터 값 변경]** | <li>개인 속성 선택 <li>새 값 설정 |
| **[!UICONTROL 프로그램 데이터 변경]** | <li>프로그램 속성 선택 <li>새 값 설정 |
| **[!UICONTROL 프로그램 상태 변경]** | <li>프로그램 선택<li>새 상태 선택 |
| **[!UICONTROL 목록에서 제거]** | <li>정적 목록 선택 <li>현재 구성원이 아닌 경우 사용자를 건너뜁니다. |
| **[!UICONTROL Marketo 목록에서 제거]** | <li>Marketo Engage에서 정적 목록 선택 <li>현재 구성원이 아닌 경우 사용자를 건너뜁니다. |
| **[!UICONTROL 여정에서 사용자 제거]** | <li>라이브 여정 선택 <li>현재 대상 여정의 멤버가 아닌 경우 사용자를 건너뜁니다. |
| **[!UICONTROL Marketo 캠페인 요청]** | <li>Marketo Engage 캠페인 선택 |
| **[!UICONTROL 전자 메일 보내기]** | <li>AI 개인화된 이메일 만들기, 편집 또는 사용 <li>전송 시간 최적화(선택 사항) |
| **[!UICONTROL WhatsApp 보내기]** | <li>WhatsApp 메시지 선택 |

## 작업 노드 추가 {#add-an-action-node}

1. 여정 캔버스로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 작업 수행]**&#x200B;을 선택합니다.

   ![여정 경로에서 추가 아이콘 클릭](./assets/person-journey-canvas-add-node.png){width="200"}

1. 오른쪽의 노드 속성에서 목록에서 작업을 선택하고 작업에 대한 값을 설정합니다.

+++대상에 활성화

이 작업을 사용하여 여정에서 직접 Experience Platform 대상으로 사용자를 활성화합니다. 대상을 선택하고 대상 이름을 입력하여 대상에서 활성화된 대상을 식별합니다.

![동작 수행 - 대상에 활성화](./assets/person-action-node-activate-to-destination.png){width="450"}

+++

+++[!UICONTROL 여정에 사용자 추가]

이 작업을 사용하여 다른 예약 또는 라이브 여정에 사용자를 추가합니다. 이 작업을 통해 추가된 직원은 대상 여정의 대상에 즉시 추가됩니다. 여정의 대상 기준은 적용되지 않습니다.

![작업 수행 - 여정에 사용자 추가](./assets/person-action-node-add-to-journey.png){width="450"}

+++

+++[!UICONTROL 목록에 추가]

이 작업을 사용하여 Journey Optimizer B2B Prime의 정적 목록에 사용자를 추가합니다.

![작업 수행 - 목록에 추가](./assets/person-action-node-add-to-list.png){width="450"}

다음 옵션 중 하나를 선택합니다.

* **[!UICONTROL 만들기]** — 새 정적 목록 자산을 만들고 사용자를 추가합니다. 이 목록은 Journey Optimizer B2B Prime의 다른 에셋에서 즉시 사용할 수 있습니다.
* **[!UICONTROL 선택]** — 노드에 연결된 사용자를 추가할 기존 정적 목록 자산을 선택합니다.

+++

+++[!UICONTROL Marketo 목록에 추가]

이 작업을 사용하여 Marketo Engage의 정적 목록에 사용자를 추가합니다.

![작업 수행 - Marketo 목록에 추가](./assets/person-action-node-add-to-marketo-list.png){width="450"}

+++

+++[!UICONTROL 데이터 값 변경]

이 작업을 사용하여 개인 레코드의 속성 값을 업데이트합니다. 속성을 선택하고 새 값을 설정합니다.

>[!TIP]
>
>특성 값을 지우려면 값을 `NULL`(으)로 설정합니다.

![작업 수행 - 데이터 값 변경](./assets/person-action-node-change-data-value.png){width="450"}

+++

+++[!UICONTROL 프로그램 데이터 변경]

이 작업을 사용하여 프로그램 속성 값을 업데이트합니다. 프로그램 속성을 선택하고 새 값을 설정합니다.

![작업 수행 - 프로그램 데이터 변경](./assets/person-action-node-change-program-data.png){width="450"}

+++

+++[!UICONTROL 프로그램 상태 변경]

이 작업을 사용하여 Marketo Engage 프로그램의 개인 상태를 변경할 수 있습니다. 프로그램을 선택한 다음 새 상태를 선택합니다.

![동작 수행 - 프로그램 상태 변경](./assets/person-action-node-change-status-program.png){width="450"}

+++

+++[!UICONTROL 목록에서 제거]

이 작업을 사용하여 Journey Optimizer B2B Prime의 정적 목록에서 사람을 제거합니다. 현재 사용자가 목록의 멤버가 아닌 경우 해당 사용자에 대해 작업을 건너뜁니다.

![작업 수행 - 목록에서 제거](./assets/person-action-node-remove-from-list.png){width="450"}

+++

+++[!UICONTROL Marketo 목록에서 제거]

이 작업을 사용하여 Marketo Engage의 정적 목록에서 사람을 제거합니다. 현재 사용자가 목록의 멤버가 아닌 경우 해당 사용자에 대해 작업을 건너뜁니다.

![작업 수행 - Marketo 목록에서 제거](./assets/person-action-node-remove-from-marketo-list.png){width="450"}

+++

+++[!UICONTROL 여정에서 사용자 제거]

다른 라이브 사용자 여정에서 사용자를 제거하려면 이 작업을 사용하십시오. 대상자는 즉시 대상 여정에서 제거되며 더 이상 조치가 취해지지 않습니다. 현재 사용자가 대상 여정의 구성원이 아닌 경우 해당 사용자에 대해 작업을 건너뜁니다.

![작업 수행 - 여정에서 사용자 제거](./assets/person-action-node-remove-from-journey.png){width="450"}

+++

+++[!UICONTROL Marketo 캠페인 요청]

이 작업을 사용하여 연결된 Marketo Engage 인스턴스의 요청 캠페인에 사용자를 추가합니다. 요청할 Marketo Engage 캠페인을 선택합니다.

![작업 수행 - Marketo 캠페인 요청](./assets/person-action-node-request-marketo-campaign.png){width="450"}

+++

+++[!UICONTROL 전자 메일 보내기]

이 작업을 사용하여 옵트인 사용자에게 이메일을 보냅니다. 구독 취소되거나, 차단 목록에 등록되거나, 이메일이 일시 중단되거나, 마케팅이 일시 중단된 사람은 이 작업을 건너뜁니다.

![작업 수행 - 전자 메일 보내기](./assets/person-action-node-send-email.png){width="450"}

이메일을 만들거나 기존 이메일을 편집하거나 AI가 개인화한 이메일을 사용할 수 있습니다. 전자 메일 만들기 및 편집에 대한 자세한 내용은 [전자 메일 작성](../content/email-authoring.md)을 참조하세요.

[전송 시간 최적화](../marketing/email-send-time-optimization.md)를 사용하여 각 프로필이 참여할 가능성이 가장 높은 시기를 예측하여 이메일 게재 시기를 개인화할 수 있습니다.

+++

+++[!UICONTROL WhatsApp 보내기]

이 작업을 사용하여 WhatsApp 메시지를 보냅니다. 시각적 디자인 공간에서 WhatsApp 메시지를 만들고, 개인화하고, 미리 볼 수 있습니다([WhatsApp 작성](../content/whatsapp-authoring.md) 참조).

![작업 수행 - WhatsApp 보내기](./assets/person-action-node-send-whatsapp.png){width="450"}

+++
