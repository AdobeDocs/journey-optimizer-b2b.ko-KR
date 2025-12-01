---
title: '[!DNL Adobe Target]개의 외부 대상'
description: 계정 여정을 통해  [!DNL Adobe Target] 에 외부 대상을 활성화합니다. B2B 웹 경험을 개인화하고 플랫폼 간 일관성을 유지합니다.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 1%

---

# [!DNL Adobe Target]개의 외부 대상

계정 여정을 통해 [!DNL Adobe Target]의 외부 대상자에 대한 경험을 활성화하고 개인화할 수 있습니다. 이 통합을 사용하여 참여를 늘리는 고급 맞춤 개인화를 수행하고 [!DNL Target] 및 [!DNL Journey Optimizer B2B Edition]에서 플랫폼 간 일관성을 유지할 수 있습니다. 이러한 일관성을 통해 팀은 전체 B2B 구매자 여정 동안 구매 그룹을 위한 웹 채널을 조정하고 개인화할 수 있습니다.

Adobe Target을 통해 외부 대상자를 활성화하는 2단계 워크플로우입니다.

1. 여정에서 [외부 고객 대상에 추가](#add-to-customer-external-audience-from-a-journey)합니다.
2. [외부 대상을 활성화](#activate-the-external-audience-to-target-as-a-destination)하여 [!DNL Target]을(를) Experience Platform의 대상으로 지정합니다.

## 여정에서 고객 외부 대상자에 추가

여정에서 [_동작 추가_ 노드 추가](../journeys/action-nodes.md)하여 _[!UICONTROL 외부 고객 대상에 추가]_ 동작을 실행합니다. 작업은 일반적으로 이벤트나 이전 작업과 같은 일종의 트리거 결과로 발생하려는 작업입니다. 여정은 개인 프로필이 있는 자격 있는 계정이 노드에 도달하면 작업을 실행합니다.

>[!NOTE]
>
>개인 프로필이 있는 자격 있는 계정이 게시된 여정의 _외부 고객 대상에 추가_ 노드에 도달하면 해당 프로필이 외부 대상에 채워지는 데 최대 48시간이 걸릴 수 있습니다.

1. 여정 캔버스에서 _작업 수행_ 노드를 선택한 상태에서 _[!UICONTROL 다음에 대한 작업]_ **[!UICONTROL 사람]** 옵션을 선택하십시오.

1. _[!UICONTROL 사용자에 대한 작업]_&#x200B;의 경우 **[!UICONTROL 외부 고객 대상에 추가]**&#x200B;를 선택하세요.

   ![여정 노드 - 사용자에 대한 작업 수행 - 외부 고객 대상에 추가](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. 오른쪽의 노드 속성에서 외부 대상을 설정합니다.

   * 이미 만들어진 외부 대상이 하나 이상 있는 경우 **[!UICONTROL 기존 대상 선택]** 및 [사용할 대상을 선택](#choose-an-external-audience)할 수 있습니다.

   * 노드에 사용할 대상을 [만들기](#create-an-external-audience)하려면 **[!UICONTROL 새로 만들기]**&#x200B;를 선택하세요.

### 외부 대상 만들기

1. 노드 속성에서 **[!UICONTROL 새로 만들기]** 옵션을 선택한 후 **[!UICONTROL 외부 고객 대상 만들기]**&#x200B;를 클릭합니다.

   ![사람들에게 조치 취하기 - 외부 고객 대상에 추가 - 새 옵션 만들기](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. 대화 상자에서 새 대상자에 대해 **[!UICONTROL 이름]**(필수)과 **[!UICONTROL 설명]**(선택 사항)을 입력합니다.

   ![외부 고객 대상 대화 상자 만들기](./assets/create-external-customer-audience-dialog.png){width="400"}

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   시스템이 새 대상을 만들고 확인 메시지를 표시합니다. 그런 다음 계속 진행하여 노드 작업의 기존 대상자로 사용할 수 있습니다.

### 외부 대상 선택

1. 노드 속성에서 **[!UICONTROL 기존 항목 선택]** 옵션을 선택한 후 **[!UICONTROL 외부 고객 대상 선택]**&#x200B;을 클릭합니다.

   ![사람에 대한 조치 수행 - 외부 고객 대상에 추가 - 기존 옵션 선택](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. _[!UICONTROL 대상 추가]_ 대화 상자에서 사용할 대상을 선택합니다.

   _검색_ 필드에 텍스트를 입력하여 대상 이름과 일치하는 항목을 표시할 수 있습니다.

   ![사람에 대해 조치 취하기 - 외부 고객 대상에 추가 - 대상자 추가 대화 상자](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. **[!UICONTROL 대상 추가]**&#x200B;를 클릭합니다.

## Target에 대한 외부 대상을 대상으로 활성화

외부 대상을 Adobe Target으로 활성화하려면 [!DNL Adobe Target]을(를) [!DNL Real-time Customer Data Platform (RTCDP)]의 대상으로 구성해야 합니다. 이 구성에 대한 자세한 내용은 [RTCDP 설명서](https://experienceleague.adobe.com/ko/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}를 참조하세요.

>[!IMPORTANT]
>
>여정을 통해 활성화를 사용하려면 RTCDP 구현에서 이메일 주소를 ID로 사용해야 합니다.

활성화 프로세스에서는 [!DNL Adobe Target]을(를) 외부 대상 또는 외부 대상으로 추가해야 합니다. 대상 빌더에서 [!DNL Target] 대상을 빌드하는 것부터 시작합니다. 자리 표시자 대상을 만들고 외부 대상 기능을 추가할 수도 있습니다.

>[!BEGINSHADEBOX]

![AEP 권한 아이콘](../../assets/do-not-localize/icon_permissions-outline.svg) 이 단계를 수행하려면 할당된 사용자 역할에 대해 다음 권한이 필요합니다.

* **[!UICONTROL Experience Platform]** - _[!UICONTROL 대상]_ 리소스의 경우: `Activate Destinations`, `Manage and Activate Dataset Destination` 및 `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. Experience Platform에서 왼쪽 탐색 영역에서 **[!UICONTROL 연결]** > **[!UICONTROL 대상]**(으)로 이동합니다.

1. **[!UICONTROL 찾아보기]** 탭을 선택합니다.

1. 세그먼트를 활성화하는 데 사용할 대상 연결을 찾은 다음 이름 옆에 있는 _추가 메뉴_(**...**) 아이콘을 클릭하고 **[!UICONTROL 대상 활성화]**&#x200B;를 선택합니다.

   표시된 대상을 이름별로 필터링하려면 _[!UICONTROL 검색]_ 필드에 텍스트를 입력하십시오.

   ![Experience Platform - 대상 - Target 대상 찾아보기 - 추가 메뉴](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. _[!UICONTROL 사용 가능한 대상]_ 목록에서 외부 대상을 선택하고 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   ![Experience Platform - 대상 - Target 대상 찾아보기 - 추가 메뉴](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. 대상에 대한 추가 필드 매핑을 수행하고(선택 사항) **[!UICONTROL 다음]**&#x200B;을(를) 클릭합니다.

1. 새 대상 매개 변수를 검토하고 **[!UICONTROL 마침]**&#x200B;을 클릭하세요.

   ![Experience Platform - 대상 - 대상 활성화 - 검토](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

활성화하면 [Adobe Target 대상](https://experienceleague.adobe.com/ko/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"}에서 대상을 보고 Adobe Target 활동에서 사용할 수 있습니다.

