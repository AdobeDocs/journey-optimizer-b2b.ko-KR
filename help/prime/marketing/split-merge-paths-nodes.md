---
title: 경로 노드 분할 및 병합
description: 플레이스홀더
autotag-review: '2026-06-12T23:04:27.208Z'
TQID: 'https://experienceleague.adobe.com/TZlkuuES1Q2ZlG-ND-tIu6cVBRA65hIfotDcroER9Mc'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: bf2854a777f62ba2f74f79942ee3336b6e8ab9dd
workflow-type: tm+mt
source-wordcount: 569
ht-degree: 0%

---

# 경로 노드 분할 및 병합



## 경로 노드 분할

정의한 조건에 따라 사람들을 세그먼트화하려면 분할 노드를 사용하십시오. 조건에 따라 대상 목록의 경로를 만들고, 세그먼트에 대한 작업 및 이벤트 노드로 각 경로를 정의한 다음, 경로를 결합하고 여정을 계속합니다.

분할된 경로 노드는 사람 필터에 따라 하나 이상의 분할된 경로를 정의합니다.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_&#x200B;**people 노드별 분할 경로가 작동하는 방식**&#x200B;_

* 각 경로의 평가는 위에서 아래로 내려옵니다. 한 사람이 첫 번째 및 두 번째 경로에 대해 일치하는 경우 첫 번째 경로만 따라 진행합니다.
* 노드는 정의된 세그먼트/경로 중 하나와 일치하지 않는 사용자에 대해 작업 또는 이벤트를 추가할 수 있는 _기타 사용자_ 경로의 정의를 지원합니다.

### 일치하는 필터

노드에 대해 정의하는 각 경로에 대해 다음 필터 유형을 사용하여 하나 이상의 조건에 따라 사람을 일치시킵니다.

* 활동 내역 - 다음과 관련된 개인의 활동에 따라 경로를 정의할 수 있습니다.

   * 이메일 메시지
   * 데이터 값 변경

* 개인 속성 - 국가, 직책 또는 목록 멤버십과 같은 개인의 속성에 따라 조건을 정의합니다.

### 분할 경로 노드 추가

<!--
>[!NOTE]
>
>When you split paths by people, a _Close split paths_ node is automatically inserted to end the split. A split-by-people path allows only _Take an action_ on people nodes.
-->

1. 여정 맵으로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 경로 분할]**&#x200B;을 선택합니다.

   <!-- ![Add journey node - split paths](./assets/add-node-split.png){width="300" zoomable="no"} -->

1. _[!UICONTROL 경로 1]_&#x200B;에 적용할 수 있는 조건을 정의하려면 **[!UICONTROL 조건 적용]**&#x200B;을 클릭하십시오.

1. 조건 편집기에서 하나 이상의 필터를 추가하여 분할 경로를 정의합니다.

   * 왼쪽 탐색에서 사람 필터를 끌어다 놓고 일치 정의를 완료합니다.

   * 맨 위에 있는 **[!UICONTROL 필터 논리]**&#x200B;를 적용하여 조건을 미세 조정하십시오. 모든 조건 또는 하나의 조건을 일치시키도록 선택합니다.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

   * **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

1. 경로를 더 추가하려면 **[!UICONTROL 경로 추가]**&#x200B;를 클릭하고 이전 단계를 반복하여 경로에 적용할 수 있는 조건을 추가합니다.

   이러한 조건을 기반으로 각 경로에 레이블을 지정하거나 기본 레이블을 사용할 수도 있습니다.

1. 필요한 경우 분할에 대해 원하는 우선 순위에 따라 경로 순서를 변경합니다.

   경로 필터링은 하향식으로 평가됩니다. 각 사용자는 일치하는 첫 번째 경로를 따라 진행합니다.

   각 경로 카드의 오른쪽 상단에 있는 위쪽 및 아래쪽 화살표를 클릭하여 경로 목록에서 위쪽 또는 아래쪽으로 이동합니다.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. 정의된 경로와 일치하지 않는 사람에 대한 기본 경로를 추가하려면 **[!UICONTROL 다른 사람]** 옵션을 활성화하십시오.

   이 옵션이 활성화되지 않으면 정의된 세그먼트/경로와 일치하지 않는 사람들이 분할을 지나 여정의 다음 단계로 이동합니다.

각 경로에 대해 조건이 정의된 경우 경로의 사람들에게 적용할 작업 또는 이벤트 노드를 추가할 수 있습니다.

## 경로 노드 병합

1. 여정 맵으로 이동하고 두 개 이상의 경로가 있는 분할 경로 노드를 찾습니다.

   각 경로에는 각 경로의 작업과 이벤트의 조합이 있어야 합니다.

1. 이러한 경로 중 하나의 끝에 있는 더하기(**+**) 아이콘을 클릭하고 표시된 옵션에서 **[!UICONTROL 경로 병합]**&#x200B;을 선택합니다.

   <!-- ![Journey node - merge paths](./assets/node-plus-icon-merge-paths.png){width="400" zoomable="no"} -->

1. 오른쪽의 노드 속성에서 병합할 경로를 선택합니다.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   이때 선택한 경로의 사람들이 여정을 계속 진행할 수 있는 단일 경로로 결합되도록 경로가 병합됩니다.

1. 필요한 경우 경로 병합 노드 속성으로 다시 이동하고 제거할 경로에 대한 확인란을 선택 취소하여 경로 병합을 취소할 수 있습니다.