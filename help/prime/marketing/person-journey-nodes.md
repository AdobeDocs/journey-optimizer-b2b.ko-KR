---
title: 여정 노드 추가
description: 개인 여정 노드에 대한 자리 표시자 페이지입니다.
autotag-review: '2026-06-12T23:02:52.147Z'
TQID: 'https://experienceleague.adobe.com/sTnrOvrGIrgboPqOMrrkUvNU1y6zZJX42zEJxuUInKQ'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2: id: d270a788-eb1d-40ed-b74e-9158ed975b1fid: ba367494-9862-4596-bd6f-299c7e10a46b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: cb3217c9fd7beb712d0c61638d143b798010d2b7
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 2%

---

# 여정 노드 추가

개인 여정을 만든 후 대상을 추가하고 노드를 사용하여 여정을 빌드합니다. 여정 맵은 다중 단계 B2B 마케팅 사용 사례를 빌드할 수 있는 캔버스를 제공합니다.

_[!UICONTROL 개인 대상]_ 노드는 자동으로 여정의 첫 번째 노드입니다. 대상을 선택한 후 다양한 작업, 이벤트 및 지정 노드를 다중 단계 크로스 채널 시나리오로 결합하여 여정을 구축합니다. 여정의 각 노드는 논리적 경로를 따라 단계를 나타냅니다.

## 개인 대상 노드

개인 대상 노드는 여정을 입력하는 개인 레코드를 지정합니다. 개인 여정을 만들 때 여정은 항상 입력을 정의하는 개인 대상 노드로 시작합니다.

1. 노드를 클릭하여 선택합니다.
1. 오른쪽의 노드 속성 패널에서 개인 대상 여정 노드에 대해 다음 입력 옵션 중 하나를 사용합니다.

   * **[!UICONTROL 동적 목록]** - 규칙 기반의 동적 사용자 목록을 사용합니다. 목록 규칙은 여정 런타임 시 평가되어 여정 멤버를 우량으로 선별합니다. 나중에 다이내믹 목록의 자격을 박탈하는 사람은 여정에서 제거되지 않습니다.

   * **[!UICONTROL 정적 목록]** - 여정 구성원으로 정적 사용자 목록을 사용합니다. 현재 목록 멤버십은 여정 런타임 시 평가되어 여정에 멤버를 우량으로 합니다. 나중에 정적 목록에서 제거되는 사람은 여정에서 제거되지 않습니다.

## 사람 작업 노드

개인 여정에서 노드 경로의 모든 사용자에게 변경 사항을 적용하려면 사용자에 대한 작업을 사용하십시오. 계정 여정의 경우 이 노드 유형은 사람에 의한 분할 경로 또는 계정에 의한 분할 경로 내에서 사용할 수 있습니다.

### 작업 및 제한

| 액션 | 제한 |
| ------ | ---------- |
| **[!UICONTROL 전자 메일 보내기]** | <li>이메일 만들기 <li>전송 시간 최적화(선택 사항) |
| **[!UICONTROL 데이터 값 변경]** | <li>개인 속성 선택 <li>새 값 설정 |

### 작업 노드 추가

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

## 이벤트 노드

이벤트가 발생할 때 대상을 여정의 다음 단계로 이동하려면 _이벤트 수신_ 노드를 추가하십시오.

### 사용자 이벤트 필터

| 필터 | 설명 |
| ------- | ----------- |
| 활동 내역 > 이메일 | 하나 이상의 선택한 이메일 메시지를 사용하여 평가되는 조건에 따른 이메일 활동: <li>이메일 링크 클릭됨 <li>이메일 열람함 |
| 활동 내역 > 데이터 값 변경됨 | 선택한 개인 속성의 경우 값이 변경되었습니다. 이러한 변경 유형은 다음과 같습니다. <li>새 값 <li>이전 값 <li>이유 <li>소스 <li>활동 날짜 <li> 최소. 횟수 |

### 이벤트 노드 추가

1. 여정 맵으로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 이벤트 수신]**&#x200B;을 선택합니다.

1. 오른쪽의 노드 속성에서 이벤트 유형으로 **[!UICONTROL 사람]**&#x200B;을(를) 선택합니다.

   <!-- ![Journey node - listen to events on people](./assets/node-listen-events-people.png){width="700" zoomable="yes"} -->

1. 목록에서 이벤트를 선택합니다.

1. **[!UICONTROL 이벤트 편집]**&#x200B;을 클릭하고 이벤트에 대한 세부 정보를 정의하십시오.

>[!NOTE]
>
>이벤트 노드 수신에 대한 시간 제한 기능은 현재 작동하지 않으며 이후 단계에서 활성화됩니다.

## 경로 노드 분할

정의한 조건에 따라 사람들을 세그먼트화하려면 분할 노드를 사용하십시오. 조건에 따라 대상 목록의 경로를 만들고, 세그먼트에 대한 작업 및 이벤트 노드로 각 경로를 정의한 다음, 경로를 결합하고 여정을 계속합니다.

분할된 경로 노드는 사람 필터에 따라 하나 이상의 분할된 경로를 정의합니다.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->


_**people 노드별 분할 경로가 작동하는 방식**_

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
