---
title: 이벤트 노드 수신
description: 플레이스홀더
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
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 165
ht-degree: 10%

---

# 이벤트 노드 수신

이벤트가 발생할 때 대상을 여정의 다음 단계로 이동하려면 _이벤트 수신_ 노드를 추가하십시오.

## 사용자 이벤트 필터

| 필터 | 설명 |
| ------- | ----------- |
| 활동 내역 > 이메일 | 하나 이상의 선택한 이메일 메시지를 사용하여 평가되는 조건에 따른 이메일 활동: <li>이메일 링크 클릭됨 <li>이메일 열람함 |
| 활동 내역 > 데이터 값 변경됨 | 선택한 개인 속성의 경우 값이 변경되었습니다. 이러한 변경 유형은 다음과 같습니다. <li>새 값 <li>이전 값 <li>이유 <li>소스 <li>활동 날짜 <li> 최소. 횟수 |

## 이벤트 노드 추가

1. 여정 맵으로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 이벤트 수신]**&#x200B;을 선택합니다.

1. 오른쪽의 노드 속성에서 이벤트 유형으로 **[!UICONTROL 사람]**&#x200B;을(를) 선택합니다.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. 목록에서 이벤트를 선택합니다.

1. **[!UICONTROL 이벤트 편집]**&#x200B;을 클릭하고 이벤트에 대한 세부 정보를 정의하십시오.

>[!NOTE]
>
>이벤트 노드 수신에 대한 시간 제한 기능은 현재 작동하지 않으며 이후 단계에서 활성화됩니다.
