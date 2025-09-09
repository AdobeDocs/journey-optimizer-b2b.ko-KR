---
title: 구매 그룹 단계
description: 시작, 성공 및 실패 단계를 포함하는 사용자 정의 구매 그룹 단계 모델을 구축하여 진행률을 추적하고 Journey Optimizer B2B edition에서 계정 여정 작업을 트리거합니다.
feature: Buying Groups, Account Journeys
role: User
exl-id: 3067e51d-4cbe-47da-aed1-ec58496ca6d0
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '2351'
ht-degree: 1%

---

# 구매 그룹 단계

구매 그룹 단계는 기회를 고객으로 전환함에 있어 구매 그룹의 진행 상황을 추적하기 위해 설계되었습니다. 이 기능을 사용하여 구매 그룹 진행률을 추적하고 구매 그룹 구성원에 대한 다음 최적 작업을 식별합니다.

단일 스테이징 모델 내에서 여러 스테이지를 정의하고 여러 스테이지와 각 스테이지 간의 전환 흐름을 정의합니다. 라이프사이클 진입을 위해 하나 이상의 단계가 지정됩니다. 이 모델에서는 A 단계에서 B, C 또는 D 단계로의 전환과 같이 한 단계에서 다른 단계로의 전환을 지정할 수 있는 비선형 진행도 가능합니다. 구매 또는 체결된 계약과 같이 하나의 단계가 성공 단계로 지정될 것을 요구한다. 다른 공급업체의 경쟁 솔루션 구입 또는 계약 거부와 같이 다른 단계가 실패 단계로 지정되는 것은 선택 사항입니다. 영업 기회를 완료하거나 기회를 고객으로 전환하는 관점에서 구매 그룹이 어떻게 진행되고 있는지 보여 주는 [지능형 대시보드](../dashboards/intelligent-dashboard.md)를 통해 이러한 단계를 모니터링합니다.

![그룹 단계 구매 예제](assets/buying-group-stages-lifecycle-diagram.png){width="800" zoomable="yes"}

![비디오](../../assets/do-not-localize/icon-video.svg){width="30"} [비디오 개요 보기](#overview-video)

## 구매 그룹 단계 모델을 정의합니다.

다음과 같은 방법으로 구매 그룹 단계 모델을 생성하고 구성합니다.

* 라이프사이클 단계 추가
* 전환 흐름 정의
* 시작 및 대상 단계 지정

하나의 모델만 지원되므로 Journey Optimizer B2B edition에서 모델을 만들어 게시하기 전에 마케팅 및 영업 팀에서 조직에 대한 최적의 모델을 계획하는 것이 중요합니다.<!-- Initially, only one stage model can be created, but future releases will support multiple stage models, allowing users to select which model to use in a journey. -->

구매 그룹 단계 모델을 만들 때 자동으로 _초안_ 상태가 되며 삭제하거나 이름을 바꿀 수 없습니다. 단계를 정의하고 단계 간 전환 흐름을 구성할 때 이 상태는 유지됩니다. 모델이 게시됨(_Live_) 상태인 경우 변경할 수 없습니다.

### 모델 만들기

1. 왼쪽 탐색에서 **[!UICONTROL 계정]** > **[!UICONTROL 구매 그룹]**(으)로 이동합니다.

1. [구매 그룹] 페이지에서 **[!UICONTROL 단계]** 탭을 선택합니다.

   ![단계 탭](assets/stages-tab-none.png){width="800" zoomable="yes"}

   이 _[!UICONTROL 단계]_ 탭은 모델을 만들 때까지 _empty_ 상태입니다.

1. 페이지 중앙에 있는 **[!UICONTROL 모델 만들기]**&#x200B;를 클릭합니다.

1. 대화 상자에서 모델의 **[!UICONTROL 이름]**(필수)과 **[!UICONTROL 설명]**(선택 사항)을 입력합니다.

   ![모델의 이름과 설명을 추가하십시오.](assets/stages-create-model-dialog.png){width="700" zoomable="yes"}

   이 대화 상자에서 _[!UICONTROL 취소]_&#x200B;를 클릭하면 _[!UICONTROL empty]_ 상태로 _단계_ 탭으로 돌아갑니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

### 단계 정의

모델을 생성하면 작업공간에서 열리고 모델의 단계를 생성하라는 메시지가 표시됩니다.

1. **[!UICONTROL 단계 편집]**&#x200B;을 클릭합니다.

   ![빈 모델에 단계 추가](assets/stages-model-empty.png){width="700" zoomable="yes"}

1. **[!UICONTROL 이름]**(필수) 및 **[!UICONTROL 설명]**(선택 사항)을 입력하여 첫 번째 단계를 정의하십시오.

   ![첫 번째 단계에 대한 이름과 설명을 추가합니다](assets/stages-model-stage-1.png){width="700" zoomable="yes"}

   단계는 특정 순서로 추가할 필요가 없지만 모델 세부 사항 페이지에 단계가 어떻게 나열되는지 결정합니다. 변환 규칙을 정의할 때 시작 단계와 단계 간의 흐름을 지정합니다.

1. **[!UICONTROL 단계 추가]**&#x200B;를 클릭하고 2단계를 반복하여 다른 단계를 정의합니다.

   모델에 필요한 단계가 있을 때까지 이 단계를 반복합니다.

   모델에 대해 ![정의된 단계](assets/stages-model-stages-added.png){width="700" zoomable="yes"}

1. 정의한 단계에 만족하면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   >[!IMPORTANT]
   >
   >**구매 그룹 단계가 저장되면 삭제할 수 없습니다.** 그러나 모델이 _초안_ 상태에 있는 한 모든 단계의 이름과 설명을 변경할 수 있습니다.

### 워크플로우 및 전환 규칙 구성

단계를 저장하면 모델 작업공간으로 돌아갑니다. _[!UICONTROL 허용된]_ 전송 대상 열이 비어 있습니다. 이는 모델 단계에 대한 전환 규칙이 아직 정의되지 않았음을 나타냅니다.

![전환 규칙이 아직 정의되지 않음](assets/stages-model-stages-empty-rules.png){width="700" zoomable="yes"}

전환 규칙은 구매 그룹이 한 단계에서 다른 단계로 이동할 수 있는 방법을 결정합니다. 예를 들어, 진입단계에서 중간단계로, 중간단계에서 다른 여러 단계로 이동할 수 있다. 진입단계는 구매집단이 공백 상태에서 진입할 수 있는 초기 단계로, 목적지 단계는 성공 또는 실패 단계로 분류된다.

1. 오른쪽 상단의 **[!UICONTROL 전환 규칙 편집]**&#x200B;을 클릭합니다.

   이 작업을 수행하면 _[!UICONTROL 단계 규칙 편집]_ 대화 상자가 열리고 여기서 흐름 논리를 정의합니다.

   옵션을 설정할 때 흐름에서 논리 오류가 발생하지 않도록 하는 데 도움이 되는 몇 가지 내장 보호 기능 및 메시징이 있습니다. _[!UICONTROL 취소]_&#x200B;를 클릭하여 대화 상자를 닫고 변경 없이 _[!UICONTROL 단계]_ 탭 페이지로 돌아갈 수 있습니다.

1. _[!UICONTROL 단계 선택]_ 섹션에서 흐름의 시작 및 끝 단계를 지정합니다.

   * **[!UICONTROL 진입점 단계]**(필수) - 구매 그룹 영업 기회에 대해 하나 이상의 진입점을 지정합니다.

   * **[!UICONTROL 성공 단계]**(필수) - 구매 그룹 영업 기회가 성공적임을 나타내는 단계(대상)를 지정합니다.

   * **[!UICONTROL 실패 단계]**(선택 사항) - 구매 그룹 영업 기회가 실패 지점(대상)에 도달했음을 나타내는 단계를 하나 이상 지정합니다.

   ![진입점 단계 및 선택적 실패 단계를 구성합니다](./assets/stages-model-edit-stage-rules.png){width="700" zoomable="yes"}

1. 대상이 아닌 각 단계에 대해 플로우(전환)의 다음에 오는 단계를 하나 이상 정의합니다.

   대상이 아닌 모든 단계에는 최소 하나 이상의 **[!UICONTROL 허용된]** 단계로의 전송이 선택되어야 합니다. 그렇지 않으면 모델 논리가 올바르지 않아 성공 또는 실패로 진행할 방법 없이 해당 단계에서 계정이 _중단_&#x200B;될 수 있습니다.

   ![대상이 아닌 단계 간 전환 구성](./assets/stages-model-edit-stage-rules-transitons.png){width="700" zoomable="yes"}

   선택적으로 실패 단계에서 전환을 지정할 수 있습니다. 예를 들어 _응답 없음_ 단계를 실패 단계로 지정할 수 있습니다. 또한 휴면 계정이 다시 활성화되는 경우를 식별하기 위해 _재확산_ 단계를 가능한 전환으로 지정합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   모델 세부 정보 페이지로 돌아가면 허용된 전환, 대상 및 항목 등록 정보가 있는 테이블에 단계가 나열됩니다.

| 열 | 설명 |
| ------ | ---------- |
| **[!UICONTROL 단계 이름]** | 단계 이름. 정보 아이콘을 눌러 단계에 대한 설명을 봅니다. |
| **[!UICONTROL 허용된]** 전송 | 모델 내의 _이동_ 작업에 유효한 단계를 나열합니다. |
| **[!UICONTROL 진입점 단계]** | 단계가 진입점 단계로 유효한지 여부를 나타냅니다([!UICONTROL 예] 또는 [!UICONTROL 아니요]). |
| **[!UICONTROL 대상]** | 단계가 대상 단계로 지정되었는지 여부를 나타냅니다([!UICONTROL 성공] 또는 [!UICONTROL 실패]). |

![초안 모델에 대해 정의된 단계 및 전환 규칙](assets/stages-model-draft-details.png){width="700" zoomable="yes"}

## 초안 모델 편집

구매 그룹 단계 모델이 _초안_ 상태에 있는 한 단계 및 전환 규칙을 편집할 수 있습니다.

초안 모델을 보려면(_T):_

1. 왼쪽 탐색에서 **[!UICONTROL 계정]** > **[!UICONTROL 구매 그룹]**(으)로 이동합니다.

1. _구매 그룹_ 페이지에서 **[!UICONTROL 단계]** 탭을 선택합니다.

1. 모델 이름을 클릭하여 모델 세부 정보를 엽니다.

### 모델의 단계 변경

1. **[!UICONTROL 단계 편집]**&#x200B;을 클릭합니다.

   _[!UICONTROL 단계 편집]_ 대화 상자에서 새 단계를 추가하거나 기존 단계의 이름 및 설명을 변경할 수 있습니다.

   * 필요에 따라 모든 단계의 **[!UICONTROL 이름]** 또는 **[!UICONTROL 설명]**&#x200B;을 변경합니다.

   * 필요한 경우 맨 아래로 스크롤하고 **[!UICONTROL 단계 추가]**&#x200B;를 클릭하여 모델의 새 단계를 정의합니다.

1. 정의한 단계에 만족하면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   _[!UICONTROL 취소]_&#x200B;를 클릭하여 대화 상자를 닫고 변경 없이 모델 세부 정보 페이지로 돌아갈 수도 있습니다.

### 모델의 전환 규칙 편집

1. **[!UICONTROL 전환 규칙 편집]**&#x200B;을 클릭합니다.

1. _단계 규칙 편집_ 대화 상자에서 필요에 따라 흐름 옵션을 변경합니다.

   이러한 옵션과 이러한 옵션이 모델 흐름에 미치는 영향에 대한 자세한 내용은 [워크플로 및 전환 규칙 구성](#configure-the-workflow-and-transition-rules)을 참조하십시오.

1. 정의된 전환 규칙에 만족하면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   _[!UICONTROL 취소]_&#x200B;를 클릭하여 대화 상자를 닫고 변경 없이 모델 세부 정보 페이지로 돌아갈 수도 있습니다.

## 구매 그룹 단계 모델 게시

유효성 검사 오류가 없는 경우 모델을 게시할 수 있습니다. 게시되면 _Live_ 상태로 변경되며 계정 여정에서 구매 그룹 단계를 진행하는 데 사용할 수 있습니다.

>[!IMPORTANT]
>
>**모델이 게시된 후에는 업데이트하거나 삭제할 수 없습니다.** 모델을 게시하기 전에 보유하고 있는 항목이 올바른지 확인하십시오.

1. 정의된 단계 및 전환을 주의 깊게 검토하십시오.

   개정이 필요한 경우 모델 단계를 편집합니다.

1. **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

1. 확인 대화 상자에서 **[!UICONTROL 게시]**&#x200B;를 클릭합니다.

   모델 세부 정보 페이지로 돌아가면 모델이 _[!UICONTROL Live]_(으)로 지정됩니다. 왼쪽 상단의 _뒤로_ 화살표를 클릭하여 _[!UICONTROL 단계]_ 탭 페이지로 돌아갑니다.

![게시된 모델](assets/stages-tab-model-live.png){width="700" zoomable="yes"}
<!-- list these later when the Published columns are working correctly

Columns - Name, Status, Created by, Created date, Last updated by, Last update, Published by, Published on.
Name - Name of the stage model, hyperlinked. Clicking on it will navigate to the stage inventory page. 
Info icon beside the name - display the description on click.
Status - Live, Draft. If a draft stage model is Published, then its status is updated to Live. -->

## 구매 그룹 단계 모델을 삭제합니다.

구매 그룹 단계 모델이 초안 또는 게시된 상태일 때 삭제할 수 있습니다. 게시된 경우(라이브) 솔루션 관심사와 연결되어 있지 않은 경우에만 삭제할 수 있습니다.

1. 왼쪽 탐색에서 **[!UICONTROL 계정]** > **[!UICONTROL 구매 그룹]**(으)로 이동합니다.

1. _구매 그룹_ 페이지에서 **[!UICONTROL 단계]** 탭을 선택합니다.

1. 단계 모델 이름 옆의 _자세히_ 메뉴 아이콘(**...**)을 클릭하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.

   ![구매 그룹 단계 모델 추가 메뉴](./assets/stages-model-list-more-menu.png){width="700"}

1. 대화 상자에서 **[!UICONTROL 삭제]**&#x200B;를 클릭하여 확인합니다.

## 계정 여정에서 모델 사용

구매 단계 모델이 _Live_ 상태(게시됨)이면 구매 그룹 진행률을 추적하는 데 사용할 솔루션 관심 항목에 모델을 추가하십시오. 계정 여정에 계정을 지정된 단계로 전환하는 작업을 포함하고 계정이 여정을 통해 이동하는 방식을 결정하는 이벤트로 단계 전환을 추가할 수 있습니다.

### 솔루션 관심 연계

구매 그룹 단계 모델을 연결하려는 각 기존 솔루션 관심사에 대해 솔루션 관심사 세부 정보를 열고 모델을 추가합니다. [관심 있는 솔루션을 만들](./solution-interests.md#create-a-solution-interest)때 속성에 모델을 추가할 수도 있습니다.

1. _[!UICONTROL 솔루션 관심]_ 탭을 선택합니다.

1. 다음 방법 중 하나를 사용하여 솔루션 관심사를 열고 편집할 솔루션 관심사에 대한 속성을 엽니다.

   * 솔루션 관심사 이름을 클릭합니다.
   * 옆에 있는 줄임표(**..**)를 클릭하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.

   ![솔루션 관심 영역 추가 메뉴](assets/solution-interests-more-menu.png){width="500" zoomable="no"}

1. 구매 그룹 단계 진행률(선택 사항)을 사용하려면 **[!UICONTROL 구매 그룹 단계 모델]**&#x200B;을 선택하세요.

   ![솔루션 관심사에 대한 구매 그룹 단계 모델을 선택하십시오](assets/solution-interest-edit-buying-group-stages-model.png){width="700" zoomable="yes"}

1. 필요한 경우 **[!UICONTROL 기존 구매 그룹 업데이트]** 설정을 변경하십시오.

   이 옵션이 활성화되면 솔루션 관심사와 쌍을 이루는 모든 기존 구매 그룹이 24시간 동기화 주기를 통해 업데이트됩니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

### 경로 분할

[분할 경로 노드](../journeys/journey-nodes.md#split-paths)를 사용하면 구매 그룹 단계에 따라 계정 수준 또는 사용자 수준에서 필터링할 수 있습니다. 예를 들어 구매 그룹 구성원을 사용하여 경로를 분할할 때 구매 그룹 단계를 경로 조건으로 추가합니다.

>[!BEGINTABS]

>[!TAB 계정 수준]

1. 편집기에서 계정 여정을 엽니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 경로 분할]**&#x200B;을 선택합니다.

   ![여정 노드 추가 - 경로 분할](../journeys/assets/add-node-split.png){width="300"}

1. 오른쪽의 노드 속성에서 분할을 위해 **[!UICONTROL 계정]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL 경로 1]_&#x200B;에 적용할 수 있는 조건을 정의하려면 **[!UICONTROL 조건 적용]**&#x200B;을 클릭하십시오.

   ![경로 노드 분할 - 조건 추가](../journeys/assets/node-split-properties-apply-condition.png){width="500"}

1. 조건 편집기에서 구매 그룹 필터를 추가하여 분할 경로를 정의합니다.

   * 왼쪽의 맨 아래에 있는 **[!UICONTROL 특수 필터]**&#x200B;를 확장하고 **[!UICONTROL 구매 그룹 있음]** 특성을 필터 작업 영역으로 끌어서 놓습니다.

   * **[!UICONTROL 솔루션 관심 분야]**&#x200B;를 구매 그룹 단계 모델과 연결된 솔루션 관심 분야로 설정하십시오.

   * **[!UICONTROL 제한 추가]**&#x200B;를 클릭하고 **[!UICONTROL 그룹 단계 구매]**&#x200B;를 선택합니다.

     ![경로 노드 분할 - 조건 필터 논리](./assets/stages-split-condition-buying-group-stage.png){width="700" zoomable="yes"}

   * **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

   분할 경로는 오른쪽의 노드 속성에 정의됩니다.

   ![여정 분할 노드 속성](./assets/stages-split-node-account-properties.png){width="600" zoomable="yes"}

1. 분할된 노드에 대한 다른 여정을 계속 정의하고 경로를 저장합니다.

>[!TAB 사람 수준]

1. 편집기에서 계정 여정을 엽니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 경로 분할]**&#x200B;을 선택합니다.

   ![여정 노드 추가 - 경로 분할](../journeys/assets/add-node-split.png){width="300"}

1. 오른쪽의 노드 속성에서 분할을 위해 **[!UICONTROL 사람]**&#x200B;을(를) 선택합니다.

   조건에 사용되는 _[!UICONTROL 특성]_&#x200B;의 기본값을 **[!UICONTROL 사람 특성만]**(으)로 둡니다.

1. _[!UICONTROL 경로 1]_&#x200B;에 적용할 수 있는 조건을 정의하려면 **[!UICONTROL 조건 적용]**&#x200B;을 클릭하십시오.

   ![경로 노드 분할 - 조건 추가](../journeys/assets/node-split-properties-apply-condition.png){width="500"}

1. 조건 편집기에서 구매 그룹 필터를 추가하여 분할 경로를 정의합니다.

   * 왼쪽의 맨 아래에 있는 **[!UICONTROL 특수 필터]**&#x200B;를 확장하고 **[!UICONTROL 구매 그룹의 구성원]** 특성을 필터 작업 영역으로 끌어서 놓습니다.

   * **[!UICONTROL 솔루션 관심 분야]**&#x200B;를 구매 그룹 단계 모델과 연결된 솔루션 관심 분야로 설정하십시오.

   * **[!UICONTROL 제한 추가]**&#x200B;를 클릭하고 **[!UICONTROL 그룹 단계 구매]**&#x200B;를 선택합니다.

     ![경로 노드 분할 - 조건 필터 논리](./assets/stages-split-condition-member-of-buying-group.png){width="700" zoomable="yes"}

   * **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

   분할 경로는 오른쪽의 노드 속성에 정의됩니다.

   ![여정 노드 - 계정에서 이벤트를 수신](./assets/stages-split-node-people-properties.png){width="600" zoomable="yes"}

1. 분할된 노드에 대한 다른 여정을 계속 정의하고 경로를 저장합니다.

>[!ENDTABS]

### 구매 그룹 단계 계정 작업 업데이트

[계정 작업 노드](../journeys/journey-nodes.md#add-an-account-action)를 사용하여 구매 그룹 단계를 업데이트할 수 있습니다. 이 노드를 정의하는 작업에는 솔루션 관심사를 선택하고 구매 그룹에 대한 새 단계를 정의하는 작업이 포함됩니다.

>[!NOTE]
>
>새 단계가 유효한 전환이 아닌 경우(모델에 정의된 대로) 작업이 계정에 적용되지 않습니다.

1. 편집기에서 계정 여정을 엽니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 작업 수행]**&#x200B;을 선택합니다.

   ![여정 노드 추가 - 작업 수행](../journeys/assets/add-node-action.png){width="400"}

1. 오른쪽의 노드 속성에서 작업에 대해 **[!UICONTROL 계정]**&#x200B;을(를) 선택합니다.

1. 구매 그룹 단계를 업데이트하는 조치를 정의합니다.

   * **[!UICONTROL 계정에 대한 작업]**&#x200B;에 대해 **[!UICONTROL 구매 그룹 단계 업데이트]**&#x200B;를 선택하세요.

   * **[!UICONTROL 솔루션 관심사 선택]**&#x200B;에 대해 구매 그룹 단계 모델과 연결된 솔루션을 선택하십시오.

   * **[!UICONTROL 새 단계]**&#x200B;의 경우 계정을 전환할 단계를 선택하십시오.

   작업은 오른쪽의 노드 속성에 정의됩니다.

   ![여정 노드 - 계정에서 작업 수행](./assets/stages-take-action-node-update-buying-group-stage.png){width="600" zoomable="yes"}

1. 다른 변경 내용을 계속 적용하고 여정을 저장합니다.

### 계정 이벤트

구매 그룹 단계 변경 발생을 사용하여 계정을 여정의 다음 단계로 이동합니다. 이 노드를 정의하는 작업에는 이벤트 트리거를 충족하는 솔루션 관심 및 추가 제약 조건이 선택됩니다.

1. 편집기에서 계정 여정을 엽니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 이벤트 수신]**&#x200B;을 선택합니다.

   ![여정 노드 추가 - 이벤트를 수신](../journeys/assets/add-node-event.png){width="400"}

1. 오른쪽의 노드 속성에서 이벤트 유형으로 **[!UICONTROL 계정]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL 계정 이벤트 선택]**&#x200B;에 대해 **[!UICONTROL 구매 그룹 단계 변경]**&#x200B;을 선택하세요.

1. **[!UICONTROL 이벤트 편집]**&#x200B;을 클릭하고 이벤트에 대한 세부 정보를 정의하십시오.

   * **[!UICONTROL 솔루션 관심 분야]**&#x200B;의 경우 구매 그룹 단계 모델과 연결된 솔루션 관심 분야에 대한 조건을 맞추십시오.

   * **[!UICONTROL 제약 조건 추가]**&#x200B;를 클릭하고 이벤트를 트리거하는 데 사용할 구매 그룹 단계 변경 내용을 선택합니다.

     ![여정 노드 - 계정에서 이벤트를 수신](./assets/stages-event-node-edit-buying-group-stage-change.png){width="700" zoomable="yes"}

   * **[!UICONTROL 완료]**&#x200B;를 클릭합니다.

   이벤트는 오른쪽의 노드 속성에 정의됩니다.

   ![여정 노드 - 계정에서 이벤트를 수신](./assets/stages-event-node-stage-change-properties.png){width="700" zoomable="yes"}

1. 다른 변경 내용을 계속 적용하고 여정을 저장합니다.

## 개요 비디오

>[!VIDEO](https://video.tv.adobe.com/v/3448634/?learn=on)
