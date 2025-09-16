---
title: 계정 대상자
description: Journey Optimizer B2B Edition에서 특정 계정 대상 세분화를 통해 계정 대상자를 구축하고 개인화된 계정 기반 여정을 이용하십시오.
feature: Audiences
role: User
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: ae1885dbe724dcc751a72325d90641decd355a4c
workflow-type: ht
source-wordcount: '561'
ht-degree: 100%

---

# 계정 대상자

대상자는 유사한 행동 및/또는 특성을 공유하는 사용자 집합입니다. Journey Optimizer B2B Edition은 Adobe Real-Time Customer Data Platform B2B 및 B2P 에디션에서 제공되는 계정 세분화 기능을 사용합니다. 계정 세분화를 통해 사용자는 시스템 내 모든 B2B 엔티티의 데이터를 활용하여 계정 대상자를 생성할 수 있습니다. 이러한 계정 대상자는 Journey Optimizer B2B Edition 계정 여정에 대한 입력 역할을 하며 원활한 활성화 및 개인화 기능을 용이하게 합니다.

[Adobe Experience Platform 세분화 서비스 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}에서 계정 대상자와 이를 정의하는 방법에 대해 자세히 알아보십시오.

## 계정 대상자 워크플로

Journey Optimizer B2B Edition은 대상 카탈로그에 나타나지 않는 Experience Platform(AEP) 대상이라고 생각하면 됩니다. 다음 단계에 따라 Journey Optimizer B2B Edition에 대한 계정 대상자를 활성화할 수 있습니다.

1. AEP에서 데이터에 대한 스키마를 만듭니다.
1. 데이터를 AEP에 수집합니다.
1. 데이터를 평가하기 위한 계정 세그먼트를 만듭니다.
1. 평가된 데이터를 Journey Optimizer B2B Edition에 활성화합니다.

Journey Optimizer B2B Edition에서 계정 대상자는 계정 기반 여정에 대한 입력으로 사용되며, 이를 통해 해당 계정 내의 사람들을 타기팅할 수 있습니다. 예를 들어 계정 대상자 그룹을 사용하면 최고운영책임자(COO)나 최고마케팅책임자(CMO)라는 직책을 가진 사람의 연락처 정보가 없는 모든 계정의 레코드를 검색할 수 있습니다.

Journey Optimizer B2B Edition을 사용하면 왼쪽 탐색 영역에서 직접 Adobe Experience Platform(AEP) 계정 대상자를 빌드하고 이를 계정 여정에 통합할 수 있습니다.

![계정 대상자 액세스](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## 계정 대상자 만들기

계정 세분화를 통해 계정 대상자를 정의합니다. Journey Optimizer B2B Edition 애플리케이션 내에서 직접 계정 세분화를 만들 수도 있고, [세그먼트 빌더 UI](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/segment-builder){target="_blank"}를 사용할 수도 있습니다. 다음은 Journey Optimizer B2B Edition에서 계정 세분화를 만드는 데 사용할 수 있는 단계입니다.

1. 왼쪽 탐색 영역에서 **[!UICONTROL 계정]** > **[!UICONTROL 대상자]**&#x200B;를 선택합니다.

1. 오른쪽 상단에서 **[!UICONTROL 대상자 만들기]**&#x200B;를 클릭합니다.

1. 세그먼트 정의를 작성합니다.

   계정 속성과 대상자는 왼쪽 탐색 막대에 표시됩니다. _[!UICONTROL 속성]_ 탭에서 Platform에서 생성된 속성과 사용자 정의 속성을 모두 추가할 수 있습니다. 각 속성을 드래그하여 세그먼트에 대한 논리를 작성합니다.

   >[!TIP]
   >
   >계정 대상자를 만들 때 이벤트가 _[!UICONTROL 사람]_&#x200B;에 나열되어 있는지 확인하십시오. 이들 속성은 사람과 연관되어 있기 때문입니다.<br/>
   >
   >_[!UICONTROL 대상자]_ 탭에서는 이전에 만든 사람 기반 대상자를 추가하여 고유한 대상자를 만들 때 활용할 수 있습니다.

   다음 예에서는 `Country Code`, `Revenue Amount` 및 `Market segment`를 사용하여 생성된 대상자를 정의합니다. 영어로 된 쿼리는 “I want all accounts in the US who are in the Finance Segment whose revenue exceeds $1M.”가 됩니다.

   ![계정 대상자 세그먼트 빌더 예시](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >계정 레코드의 `Account Name` 속성에는 계정 여정에 포함할 값이 포함되어야 합니다. 이 속성이 비어 있으면(null) 계정 레코드가 제외됩니다.<br/>
   >비어 있지 않은 계정 이름을 가진 계정만 포함되도록 하려면 **[!UICONTROL 계정 이름]** 속성을 추가하고 일치 조건으로 _[!UICONTROL 존재함]_&#x200B;을 선택합니다.<br/>
   >![계정 이름 속성이 존재함](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>계정 이름에 사용자 정의 속성을 사용하는 경우 _[!UICONTROL 계정 이름]_ 대신 사용자 정의 속성 이름을 사용하십시오.

1. 오른쪽 상단에 있는 **[!UICONTROL 저장 후 닫기]**&#x200B;를 클릭합니다.

Journey Optimizer B2B Edition에 대한 계정 대상자를 활성화하려면 [해당 계정 대상자를 계정 여정에 추가](../journeys/journey-overview.md#add-the-account-audience-for-your-journey)하고 [여정을 게시](../journeys/journey-overview.md)해야 합니다.
