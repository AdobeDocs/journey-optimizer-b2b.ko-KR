---
title: 정적 사용자 목록
description: Journey Optimizer B2B Edition의 정적 사용자 목록에 대한 구성원을 추가하고 제거합니다.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 2%
---

# 정적 사용자 목록

정적 [사용자 목록](./people-lists.md)은(는) 사용자를 추가하거나 제거할 때만 구성원 자격이 변경되는 사용자 프로필의 컬렉션입니다. 개인 속성 및 활동을 참조하는 간단한 필터는 정적 목록 멤버십을 정의합니다. 구성원을 추가하거나 제거할 때만 구성원 자격이 변경됩니다. 다음과 같은 작업을 수행할 수 있습니다.

* 필터를 적용할 때 한 번 평가된 필터 집합을 적용하여 [사용자를 추가](#static-list-add-members)합니다.
* [!UICONTROL 사람 목록에 추가] 및 [!UICONTROL 사람 목록에서 제거] 작업을 사용하여 계정 또는 사용자 여정을 통해 사람을 추가하고 제거합니다. ([여정에서 사람 목록 사용](./people-lists-journeys.md)을 참조하십시오.)
<!-- * [Activate the list to a destination](#static-list-activate) to sync its membership downstream. -->

>[!NOTE]
>
>정적 목록 필터 정의는 목록에 멤버를 추가할 때 한 번 적용됩니다. 정의된 필터는 나중에 사용할 수 없습니다. 필터를 사용하여 일관된 대상 정의를 유지하려면 [동적 목록](./people-lists-dynamic.md)을(를) 대신 사용하십시오.

## 구성원 추가 {#static-list-add-members}

>[!NOTE]
>
>정적 목록을 비우려면 필터를 적용하지 마십시오. 빈 정적 목록은 여정을 통해 멤버를 추가할 때 유용합니다.

1. 정적 목록을 열고 오른쪽 상단에서 **[!UICONTROL 사람 추가]**&#x200B;를 클릭합니다.

   ![정적 사용자 목록에 사용자 추가](./assets/people-list-static-add-people.png){width="700" zoomable="yes"}

1. _[!UICONTROL 사람 추가]_ 대화 상자에서 왼쪽 패널에서 필터를 끌어 프로필에 대한 규칙을 정의합니다.

   다음을 조합하여 프로필 필터링:

   * 활동 기록
   * Experience Platform 활성화 개인 필드
   * 사용자 정의 필드
   * 의도 데이터
   * 개인 속성
   * 여정 멤버십과 같은 특수 필터

   필터는 범주 폴더에 중첩됩니다. 각 폴더를 확장하고 사용 가능한 필터를 스크롤하거나 맨 위의 _검색_ 필드를 사용하여 필요한 필터를 찾습니다. 추가하는 각 필터에 대해:

   * 왼쪽 패널에서 필터 정의 공간으로 필터를 드래그합니다.
   * 일치 평가 정의를 완료합니다.
   * **[!UICONTROL 제약 조건 추가]**&#x200B;를 클릭하여 일치하는 기준을 구체화합니다.

   맨 위에 있는 **[!UICONTROL 필터 논리]**&#x200B;를 적용하여 조건을 미세 조정하십시오. 모든 조건, 모든 조건을 일치시키거나 고급 논리를 정의하도록 선택할 수 있습니다.

   ![정적 목록에 사용자를 추가하려면 제약 조건이 있는 필터를 추가하십시오.](./assets/people-list-static-add-people-filters.png){width="800" zoomable="yes"}

1. 변경 내용을 저장하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하세요.

   시스템이 요청을 처리하고 사람이 추가되면 확인 메시지를 표시합니다. 처리 시간은 평가할 사람 수와 선택한 필터 기준에 따라 다릅니다. 목록이 계속 채워지면 _[!UICONTROL 자세히]_ 메뉴에서 **[!UICONTROL 구성원 새로 고침]**&#x200B;을 사용하여 목록을 새로 고치십시오.

   자격을 갖춘 멤버는 잠시 지연된 후 목록에 표시됩니다. 필터 세트는 한 번 평가되므로 나중에 해당 필터와 일치하는 사용자는 자동으로 추가되지 않습니다. 언제든지 이 프로세스를 반복하여 목록에 더 많은 사용자를 추가할 수 있습니다.

   정적 사용자 목록의 ![구성원](./assets/people-list-static-members.png){width="700" zoomable="yes"}

## 멤버 제거 {#static-list-remove-members}

[!UICONTROL 사람 목록에서 제거] 동작을 사용하여 여정을 통해 정적 목록에서 사람을 자동으로 제거할 수 있습니다. ([여정에서 사람 목록 사용](./people-lists-journeys.md)을 참조하십시오.)

<!--
TODO: Restore this section when the activate to a destination function is released.

## Activate to a destination {#static-list-activate}

Activating a static people list sends its membership to a connected destination, with ongoing sync instead of a one-time export. This is useful for paid media targeting, suppression, and downstream orchestration.

* The static list acts as a container for the people.
* The activation sends and syncs that membership to a destination.
* People added to the list later are propagated automatically.
* People removed later are deactivated automatically.

>[!PREREQUISITES]
>
>You must have one or more configured destinations for your [!DNL Journey Optimizer B2B Edition] sandbox before you can activate a static list to a destination. See [Destinations](./destinations.md).

1. Select the **[!UICONTROL Static lists]** tab.

1. Locate the static list that you want to activate, click the _More menu_ ( **...** ) icon next to the list, and choose **[!UICONTROL Activate to destination]**.

   ![Access the More menu for a static people list](./assets/people-lists-static-more-menu.png){width="450"}

   You can also open the static list and use the **[!UICONTROL More]** menu at the top right.

1. Select the check box for the configured destination connection.

   ![Configured destinations available for activation](./assets/people-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

1. In the _[!UICONTROL Activate list to destination]_ dialog, click **[!UICONTROL Activate]** to confirm.

When activation completes, a confirmation message appears and the destination shows as **[!UICONTROL Active]** on the **[!UICONTROL Destinations]** tab of the list. You can activate a static list to more than one destination at a time. Membership syncs to all of them.

To review the destinations that a static list is activated to, open the list and select the **[!UICONTROL Destinations]** tab.

### Deactivate a destination {#deactivate-destination}

Remove a destination connection from a static list when you no longer want its membership synced downstream.

1. Open the static list and select the **[!UICONTROL Destinations]** tab.

1. Use the row action to remove the destination that you want to disconnect.

1. Confirm in the _[!UICONTROL Deactivate destination]_ dialog.

Deactivating removes the destination from the list. The people in the list are also removed from the connected destination audience.

-->
