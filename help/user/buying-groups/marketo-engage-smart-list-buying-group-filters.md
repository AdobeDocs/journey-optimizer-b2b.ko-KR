---
title: Marketo Engage의 구매 그룹 필터
description: 캠페인 및 잠재 고객 점수를 최적화하기 위해 완성도 점수와 같은 제약 조건이 있는 Marketo Engage 스마트 목록의 그룹 구성원을 구입하여 잠재 고객을 필터링합니다.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 764ea8631241b8da3cfae4ce59a29b1c82b53f0c
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---

# Marketo Engage의 구매 그룹 필터

>[!IMPORTANT]
>
>**기능 사용 중단**</br></br>
>
>Journey Optimizer B2B edition용 [간소화된 아키텍처](../simplified-architecture.md)을(를) 사용하면 연결된 Marketo Engage 인스턴스에서 구매 그룹 필터를 더 이상 사용할 수 없습니다.</br></br>
>
>또는 각 솔루션에 관심 있는 정적 목록을 만든 다음 여정 노드에서 [Marketo 목록에 추가&#x200B;_작업을 사용_&#x200B;할 수 있습니다. ](../journeys/action-nodes.md#marketo-engage-actions) 이렇게 하면 연결된 Marketo Engage 인스턴스의 특정 정적 목록에 구매 그룹 구성원이 추가됩니다. 그런 다음 스마트 목록 필터에 대해 솔루션 관심 집중 정적 목록을 사용합니다.

마케터는 Journey Optimizer B2B edition의 구매 그룹에 속하는 사람들을 위해 Marketo Engage의 캠페인을 제한할 수 있습니다. 구매 그룹과 관련된 리드에 대한 정보를 사용하여 Marketo Engage의 리드 채점 워크플로우에 알릴 수도 있습니다. 예:

* 이 주연 그룹이 구매 그룹의 일부입니까?
* 구매 그룹이 완료되어 참여 중입니까?

이러한 조건이 참인 경우 리드를 더 높게 점수화하는 것을 선택할 수 있습니다. 그렇지 않은 경우 마케팅 적격 리드(MQL)로 표시하지 않도록 선택할 수 있습니다.

Journey Optimizer B2B edition에 연결된 Marketo Engage 인스턴스에서는 스마트 목록의 _[!UICONTROL 구매 그룹 구성원]_ 필터를 사용하여 캠페인 전략에 따라 이러한 리드를 식별할 수 있습니다.

1. [Marketo Engage에서 스마트 목록을 만들기](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"}한 후 **[!UICONTROL 스마트 목록]** 탭을 선택하여 필터 편집기를 엽니다.

1. 오른쪽의 필터 목록에서 목록을 아래로 스크롤하고 **[!UICONTROL 특수 필터]** 폴더를 확장합니다.

1. **[!UICONTROL 구매 그룹 구성원]** 필터를 클릭하고 필터 정의 영역으로 끌어서 놓습니다.

   ![스마트 목록에 구매 그룹 구성원 필터 추가](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. _[!UICONTROL 구매 그룹의 구성원]_ 옵션을 **[!UICONTROL true]** 또는 **[!UICONTROL false]**(으)로 설정하십시오.

   이 제한은 정의에 필요합니다.

1. (선택 사항) Smart List에 대한 가망 고객을 식별하는 방법에 따라 다른 구매 그룹 관련 제약 조건을 필터에 추가합니다.

   * 필터 카드의 오른쪽 상단에서 **[!UICONTROL 제한 추가]**&#x200B;를 클릭합니다.

     ![다른 제약 조건 선택](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * _완전성 점수_ 또는 _솔루션 관심사_&#x200B;와 같이 추가할 제약 조건을 선택하십시오.

   * 일치에 사용할 평가를 설정합니다.

     점수에 대해 정확히 일치하는 항목 또는 입력한 숫자의 위 또는 아래 범위를 사용할 수 있습니다.

     구매 그룹에서 제거된 구성원을 제외하려면 _[!UICONTROL (으)로 설정된]_&#x200B;제거됨`false` 제약 조건을 사용하십시오. 이 제약 조건을 `true`(으)로 설정하여 스마트 목록에 제거된 멤버를 명시적으로 포함할 수도 있습니다.

     Journey Optimizer B2B edition에 정의된 솔루션 관심사와 같은 개별 항목의 경우 목록에 대해 하나 이상의 항목을 선택할 수 있습니다.

     ![목록에서 제약 조건의 값을 선택하십시오](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     첫 번째 선택기를 선택하고 선택기를 다시 클릭하여 _[!UICONTROL 다중 값 선택기]_ 대화 상자를 엽니다.

     ![제약 조건에 대한 여러 값을 선택하십시오](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     나머지 항목을 오른쪽으로 이동하고 제한에 사용할 항목 목록이 있으면 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   * 이러한 작업을 반복하여 필요한 제한 수를 추가합니다.

   ![여러 제약 조건을 가진 구매 그룹 구성원 필터](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
