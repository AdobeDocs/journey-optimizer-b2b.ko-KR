---
title: 대상
description: 지원되는 Experience Platform 대상 및 Journey Optimizer B2B Edition에서 정적 사용자 목록을 활성화하기 위해 대상을 연결하는 방법에 대해 알아봅니다.
feature: Audiences, Integrations
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
    internal-label: Integrations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: 734966636b6d2addf014905431fa755f6fe92ee6
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 4%
---

# 대상

대상은 [정적 사용자 목록](./people-lists-static.md) 구성원 및 계정 여정 대상을 소셜 플랫폼으로 보낼 수 있는 미리 빌드된 통합입니다. 정적 목록을 대상으로 활성화하면 구성원 자격이 동기화됩니다. 사람들이 목록에 추가되거나 목록에서 제거되면 대상 대상자 및 확장에 따라 대상자가 피딩하는 모든 캠페인에도 추가되거나 제거됩니다.

연결된 대상에 사용자를 활성화하는 방법에는 세 가지가 있습니다.

* **정적 목록에서** - **_[!UICONTROL 사람 목록]_** 탭에서 직접 기존 정적 목록을 활성화합니다. [_대상에 활성화_](./people-lists-static.md#static-list-activate)&#x200B;를 참조하십시오.
* **계정 여정에서** - 자격 있는 계정이 해당 노드에 도달하면 대상에 대해 활성화되도록 **_[!UICONTROL 대상에 대해 활성화]_** 작업 노드를 여정 경로에 추가합니다. [_대상 활성화 또는 비활성화_](../journeys/action-nodes.md#activate-deactivate-destination)&#x200B;를 참조하십시오.
* **구매 그룹에서** - 구매 그룹에서 빈 역할을 채우려면 LinkedIn 일치 대상을 활성화하여 구매 그룹 매개 변수와 일치하는 잠재 고객을 타깃팅할 수 있습니다. [_LinkedIn 계정 일치 audience_s](../data/linkedin-account-matched-audiences.md#activate-buying-group)을(를) 참조하십시오.

>[!BEGINSHADEBOX]

## 필요한 권한 {#required-permissions}

전체 대상 기능을 사용하려면 다음 [!DNL Adobe Experience Platform] 권한이 필요합니다.

| 카테고리 | 사용 권한 |
|--- |--- |--- |
| 샌드박스 | 샌드박스 액세스 |
| 대시보드 | 표준 대시보드 보기 |
| 대시보드 | 표준 대시보드 관리 |
| 대상 | 대상 보기 |
| 대상 | 대상 관리 |
| 대상 | 대상 활성화 |
| 대상 | 매핑 없이 세그먼트 활성화 |
| 대상 | 데이터 세트 대상 관리 및 활성화 |
| 대상 | 대상 작성 |
| 데이터 거버넌스 | 데이터 사용 정책 보기 |
| 데이터 거버넌스 | 데이터 사용 정책 관리 |
| 데이터 수집 | 소스 보기 |
| 데이터 수집 | 소스 관리 |
| 프로필 관리 | 프로필 설정 보기 |
| 프로필 관리 | 프로필 설정 관리 |

>[!ENDSHADEBOX]

## 지원되는 대상 {#supported-destinations}

정적 목록을 활성화하려면 대상 카탈로그에 대상이 있어야 합니다. 왼쪽 탐색에서 **[!UICONTROL 연결]**&#x200B;을 확장하고 **[!UICONTROL 대상]**&#x200B;을 선택합니다. [!DNL Journey Optimizer B2B Edition]은(는) 현재 **[!UICONTROL LinkedIn 일치하는 대상]**(소셜) 대상을 지원합니다. 다음에 대한 [_LinkedIn 계정 일치 대상_](../data/linkedin-account-matched-audiences.md)&#x200B;을 참조하세요.

<!-- 
the following destinations:

* **[!UICONTROL Google Customer Match]** (Advertising)
* **[!UICONTROL Facebook Custom Audience]** (Social)
* **[!UICONTROL LinkedIn Matched Audience]** (Social)

![Access the available connector types](./assets/destinations-catalog.png){width="800" zoomable="yes"}

-->

>[!NOTE]
>
>표시된 카탈로그가 전체 [!DNL Adobe Experience Platform] 대상 카탈로그가 아닙니다. [!DNL Experience Platform]에서 바로 대상에 액세스하는 경우 더 큰 카탈로그가 표시되지만 현재 [!DNL Journey Optimizer B2B Edition]에서 활성화할 수 있는 대상만 있습니다. 향후 릴리스를 위해 추가 대상이 계획되어 있습니다.

## 대상 설정 {#set-up-destination}

지원되는 각 대상 카드에 **[!UICONTROL 새 대상 구성]**&#x200B;이 표시됩니다. 활성화 전 요구 사항은 대상을 구성하는 것입니다.

1. 커넥터 카드에서 **[!UICONTROL 새 대상 구성]**&#x200B;을 클릭합니다.

   ![새 대상 구성](./assets/destinations-configure-new.png){width="500"}

1. **[!UICONTROL 기존 계정]** 또는 **[!UICONTROL 새 계정]**&#x200B;을 선택하고 계정 이름, 설명 등 계정 세부 정보를 입력하십시오.

1. **[!UICONTROL 대상에 연결]**&#x200B;을 클릭합니다.

   OAuth 흐름을 사용하면 해당 계정인 LinkedIn, Google 또는 Facebook에 로그인할 수 있습니다.

   >[!IMPORTANT]
   >
   >지금은 _[!UICONTROL 대상 세부 정보]_&#x200B;를 입력하지 마십시오. 연결만 필요합니다.

1. 사용자 속성과 대상에 필요한 필드 간의 필수 필드 매핑을 완료합니다.

1. 데이터 거버넌스 및 마케팅 작업 설정을 검토한 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

전체 설정 단계는 [!DNL Experience Platform] 설명서에서 [새 대상 연결 만들기](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"}를 참조하십시오.

구성된 경우 [!DNL Journey Optimizer B2B Edition]에서 대상을 선택할 수 있는 모든 곳에서 대상을 활성화할 수 있습니다.

## 활성화 및 동기화 {#activation-sync}

활성화는 목록과 대상 대상 대상 간의 양방향 동기화를 통해 정적 목록 멤버십에 의해 결정됩니다.

* 정적 목록에 개인을 추가하면 24시간 내에 대상에 활성화되고 대상 대상에 추가되며 이후 대상이 피딩하는 모든 캠페인에 추가됩니다.
* 정적 목록에서 사용자를 제거하면 대상에서 비활성화됩니다. 대상 대상자 및 연결된 캠페인에서 제거됩니다.
* 동일한 목록을 여러 대상에 한 번에 활성화할 수 있습니다. 멤버십이 모든 멤버십과 동기화됩니다.

>[!TIP]
>
>세그먼트에 대해 LinkedIn 캠페인을 실행하려면 LinkedIn 일치하는 대상 대상에 이러한 사람들의 정적 목록을 활성화합니다. 목록의 모든 사람은 LinkedIn에서 일치하는 대상자에 추가됩니다. 여기서 캠페인은 이러한 대상자를 타깃팅할 수 있으며 대상자는 목록이 변경될 때 자동으로 현재 상태를 유지합니다.
