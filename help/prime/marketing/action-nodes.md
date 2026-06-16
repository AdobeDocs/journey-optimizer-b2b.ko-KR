---
title: 작업 노드 수행
description: 플레이스홀더
autotag-review: '2026-06-12T22:58:21.806Z'
TQID: 'https://experienceleague.adobe.com/uR-WvNz3gA6V7yyN3RRXH-MggrmGb1qvu1CBhMZRuAc'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: af7eab5e-3580-4254-9f56-3c20b4f6ef42id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 2%

---

# 작업 노드 수행

개인 여정에서 노드 경로의 모든 사용자에게 변경 사항을 적용하려면 사용자에 대한 작업을 사용하십시오. 계정 여정의 경우 이 노드 유형은 사람에 의한 분할 경로 또는 계정에 의한 분할 경로 내에서 사용할 수 있습니다.

## 작업 및 제한

| 액션 | 제한 |
| ------ | ---------- |
| **[!UICONTROL 전자 메일 보내기]** | <li>이메일 만들기 <li>전송 시간 최적화(선택 사항) |
| **[!UICONTROL 데이터 값 변경]** | <li>개인 속성 선택 <li>새 값 설정 |

## 작업 노드 추가 {#add-an-action-node}

1. 여정 맵으로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 작업 수행]**&#x200B;을 선택합니다.

1. 오른쪽의 노드 속성에서 목록에서 작업을 선택하고 작업에 대한 값을 설정합니다.

<!-- ![Person journey node - take an action](./assets/node-take-action-people.png){width="700" zoomable="yes"} -->

+++[!UICONTROL 전자 메일 보내기]

이 작업을 사용하여 이메일을 보냅니다. 노드에 대한 전자 메일을 만든 후에는 전자 메일 디자인 공간에서 전자 메일 메시지를 디자인하고, 개인화하고, 미리 볼 수 있습니다([전자 메일 작성](../content/email-authoring.md) 참조).

<!-- ![Take an action - Send email](./assets/node-action-send-email-from-marketo.png){width="300"} -->

[전송 시간 최적화](../marketing/email-send-time-optimization.md)를 사용하여 각 프로필이 참여할 가능성이 가장 높은 시기를 예측하여 이메일 게재 시기를 개인화할 수 있습니다.

<!--
>[!NOTE]
>
>You can use email deduplication in account journeys to ensure that the same email is not sent multiple times to the same email address within a journey. For more information, see [Email deduplication](../content/email-deduplication.md).
-->

+++

+++[!UICONTROL 데이터 값 변경]

이 작업을 사용하여 데이터베이스에서 사람 프로필 속성의 값을 변경합니다. 속성을 선택한 다음 새 값을 설정합니다.

<!-- ![Take an action - Update person profile](./assets/node-action-update-person-profile.png){width="300"} -->

+++
