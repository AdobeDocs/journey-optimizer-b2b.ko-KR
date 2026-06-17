---
title: 개인 대상 여정 노드
description: 개인 여정에 대한 자리 표시자 페이지입니다.
autotag-review: '2026-06-16T21:21:01.614Z'
TQID: 'https://experienceleague.adobe.com/pk1NGg3M67oRieuCOZFdaguKl2bVkiZyEPVnJDTUBJs'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 1cb68e8933d6b1abba3cc82f154344d1dde51818
workflow-type: tm+mt
source-wordcount: 197
ht-degree: 0%

---

# 개인 대상 노드

_개인 대상_ 노드는 여정에 들어오는 개인 프로필을 지정합니다. [개인 여정을 만듭니다](./person-journeys.md). 여정은 항상 입력을 정의하는 개인 대상 노드로 시작합니다. 개인 대상 노드에는 정적 사람 목록과 동적 사람 목록의 두 대상 입력 유형 중 하나가 있을 수 있습니다.

개인 여정에 필요한 사람 목록이 이미 없는 경우 [사람 목록을 만들고](../audiences/people-lists.md#create-a-people-list) Peson 대상 노드를 구성하십시오.

## 대상자 설정

1. **[!UICONTROL 개인 대상]** 노드를 클릭합니다.

   이 작업은 오른쪽에 노드 속성을 표시합니다.

   ![개인 대상 여정 노드](./assets/person-audience-node-properties.png){width="500" zoomable="yes"}

1. 개인 대상에 대해 다음 대상 구성 옵션 중 하나를 사용합니다.

   * **[!UICONTROL 동적 목록]** - 규칙 기반의 동적 사용자 목록을 사용합니다. 목록 규칙은 여정 런타임 시 평가되어 여정 멤버를 우량으로 선별합니다. 나중에 다이내믹 목록의 자격을 박탈하는 사람은 여정에서 제거되지 않습니다.

   * **[!UICONTROL 이벤트 대상]** - 이벤트 대상을 사용하면 자격 있는 이벤트를 기반으로 여정 대상을 정의할 수 있습니다. 개인 프로필 필터링을 사용하여 대상 구성원을 정의하고 이벤트 기준을 사용하여 여정 항목을 트리거합니다.

## 이벤트 대상자 정의

PM에서 정보를 가져오는 경우 를 추가합니다.

