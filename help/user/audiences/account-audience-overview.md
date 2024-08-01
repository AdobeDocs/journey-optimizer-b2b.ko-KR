---
title: 계정 대상자
description: 계정 대상과 계정 기반 여정을 활성화하는 방법에 대해 알아봅니다.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 계정 대상자

대상자는 유사한 행동 및/또는 특성을 공유하는 사람들의 집합입니다. Journey Optimizer B2B 에디션은 Adobe Real-time Customer Data Platform B2B 및 B2P 에디션에 있는 계정 세분화 기능을 사용합니다. 계정 세분화를 통해 사용자는 시스템 내의 B2B 엔티티의 데이터를 활용하여 계정 대상을 생성할 수 있습니다. 이러한 계정 대상은 Journey Optimizer B2B 에디션 계정 여정의 입력 역할을 하여 원활한 활성화 및 개인화 기능을 용이하게 합니다.

[Adobe Experience Platform 세분화 서비스 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences)에서 계정 대상자와 이를 정의하는 방법에 대해 자세히 알아보세요.

## 계정 대상자 워크플로우

Journey Optimizer B2B 에디션은 대상 카탈로그에 표시되지 않는 Experience Platform(AEP) 대상으로 간주할 수 있습니다. 다음 단계를 사용하여 Journey Optimizer B2B 에디션에 계정 대상을 활성화합니다.

1. AEP에서 데이터에 대한 스키마를 만듭니다.
1. AEP로 데이터를 수집합니다.
1. 계정 세그먼트를 만들어 데이터를 평가합니다.
1. 평가된 데이터를 Journey Optimizer B2B 에디션으로 활성화합니다.

Journey Optimizer B2B 에디션에서 계정 대상은 계정 기반 여정에 대한 입력으로 사용되며, 이를 통해 해당 계정 내에서 사용자를 타겟팅할 수 있습니다. 예를 들어 계정 대상을 사용하여 COO(최고 운영 책임자) 또는 CMO(최고 마케팅 책임자)라는 타이틀을 가진 사람에 대한 연락처 정보가 없는 모든 계정의 기록을 검색할 수 있습니다.

Journey Optimizer B2B 에디션을 사용하면 왼쪽 탐색에서 직접 Adobe Experience Platform(AEP) 계정 대상을 빌드하고 계정 여정에 통합할 수 있습니다.

![계정 대상자 액세스](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## 계정 대상자 만들기

계정 세분화를 만들어 계정 대상자를 정의합니다. Journey Optimizer B2B 에디션 응용 프로그램 내에서 직접 계정 세분화를 만들 수 있는 옵션이 있거나 [세그먼트 빌더 UI](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder)를 사용할 수 있습니다. 다음은 Journey Optimizer B2B 에디션에서 계정 세분화를 만드는 데 사용할 수 있는 단계입니다.

1. 왼쪽 탐색에서 **[!UICONTROL 계정]** > **[!UICONTROL 대상]**&#x200B;을 선택합니다.

1. 오른쪽 상단의 **[!UICONTROL 대상 만들기]**&#x200B;를 클릭합니다.

1. 세그먼트 정의를 빌드합니다.

   계정 속성 및 대상은 왼쪽 탐색 모음에 표시됩니다. _[!UICONTROL 특성]_ 탭에서 플랫폼에서 만든 특성과 사용자 지정 특성을 모두 추가할 수 있습니다. 각 속성을 드래그하여 세그먼트에 대한 논리를 작성합니다.

   >[!TIP]
   >
   >계정 대상을 만들 때는 이벤트가 _[!UICONTROL 사람]_ 아래에 나열되어 있습니다. 이러한 특성은 사람과 연결되어 있기 때문입니다.<br/>
   >
   >_[!UICONTROL 대상]_ 탭에서 이전에 만든 사람 기반 대상을 추가하여 자신의 계정 대상을 만들 때 빌드할 수 있습니다.

   다음 예제에서는 `Country Code`, `Revenue Amount` 및 `Market segment`을(를) 사용하여 만든 대상을 정의합니다. 영어로 된 쿼리는 &quot;나는 수입이 100만 달러를 초과하는 금융 부문에 있는 미국의 모든 계정을 원한다.&quot;가 될 것입니다.

   ![계정 대상 세그먼트 빌더 예](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}

1. 오른쪽 상단의 **[!UICONTROL 저장 후 닫기]**&#x200B;를 클릭합니다.

Journey Optimizer B2B 에디션에 대한 여정 대상을 활성화하려면 [계정 여정에 추가](../journeys/journey-overview.md#add-the-account-audience-for-your-journey)하고 [계정을 게시](../journeys/journey-overview.md)해야 합니다.
