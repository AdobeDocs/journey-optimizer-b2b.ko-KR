---
title: 작업 수행
description: 계정 및 사용자 작업에 대한 작업 노드 구성 - 이메일 전송, 구매 그룹 업데이트, 점수 변경 및 Journey Optimizer B2B edition의 Marketo Engage과 통합.
feature: Account Journeys
role: User
exl-id: 167cb627-96ee-42a8-8657-bb8040bb4bfe
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1560'
ht-degree: 2%

---

# 액션 취하기

계정 여정에서 _[!UICONTROL 작업 수행]_ 노드를 추가하여 전자 메일 보내기, 점수 변경, 구매 그룹에 할당 등의 작업을 실행할 수 있습니다. 작업은 일반적으로 이벤트나 이전 작업과 같은 일종의 트리거 결과로 발생하려는 작업입니다.

![비디오](../../assets/do-not-localize/icon-video.svg){width="30"} [개요 비디오 보기](#overview-video)

## 계정 작업

노드 경로의 계정에 속한 모든 사람에게 변경 사항을 적용하려면 계정에 대한 작업을 사용하십시오.

### 작업 및 제한 {#account-action-constraints}

| 액션 | 제한 |
| ------ | ----------- |
| [!UICONTROL 계정 변경 데이터 값] | 특성 <br/>새 값 선택 |
| [!UICONTROL 관심 있는 계정] | 유형(전자 메일, 마일스톤 또는 웹)<br/>설명(선택 사항) |
| [!UICONTROL 대상에 활성화] | 대상 선택 |
| [!UICONTROL 여정에 계정 추가] | 라이브 계정 여정 선택 |
| [!UICONTROL 계정 목록에 추가] | 라이브 정적 계정 목록 선택 |
| [!UICONTROL 여정에서 계정 제거] | 라이브 계정 여정 선택 |
| [!UICONTROL 계정 목록에서 제거] | 라이브 정적 계정 목록 선택 |
| [!UICONTROL 판매 알림 보내기] | 솔루션 관심 항목 선택<br/>전자 메일 보내기 |
| [!UICONTROL 구매 그룹 단계 업데이트] | 솔루션 관심 분야 선택<br/>구매 그룹 단계 선택 |
| [!UICONTROL 구매 그룹 상태 업데이트] | 솔루션 관심 항목 선택<br/>상태(필수, 최대 50자) |

### 계정 기반 작업 추가

1. 여정 맵으로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 작업 수행]**&#x200B;을 선택합니다.

   ![여정 노드 추가 - 작업 수행](./assets/add-node-action.png){width="400"}

1. 오른쪽의 노드 속성에서 작업에 대해 **[!UICONTROL 계정]**&#x200B;을(를) 선택합니다.

1. 목록에서 작업을 선택하고 작업에 대한 값을 설정합니다.

   ![여정 노드 - 계정에서 작업 수행](./assets/node-take-action-account.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX]

### LinkedIn 대상에 활성화

여정에서 직접 Experience Platform 대상에 대한 계정을 활성화하려면 계정에 대해 _대상에 활성화_ 작업을 사용하십시오. 이 작업을 통해 구매 그룹 필터, 참여 점수 및 기타 기준에 따라 자격을 갖춘 계정을 지원되는 대상의 일치하는 대상자에게 푸시할 수 있습니다. It

2025.10 릴리스부터 **_LinkedIn_**&#x200B;은(는) 지원되는 첫 번째 대상 유형입니다. LinkedIn 대상에 대한 작업을 사용하여 다중 시스템 핸드오프를 제거하고 지연을 줄여 캠페인 실행을 간소화합니다. 예를 들어 마케터는 주요 구매 역할이 누락된 경우 재타겟팅을 위해 LinkedIn에 대한 고의도의 계정을 자동으로 활성화하거나 비활성 필터를 기반으로 휴면 계정을 다시 활성화할 수 있습니다.

LinkedIn 대상에 대해 계정 일치 대상을 사용하는 방법에 대한 자세한 내용은 [LinkedIn 계정 일치 대상](../data/linkedin-account-matched-audiences.md)을 참조하십시오.

+++ LinkedIn 대상에 대한 계정 활성화 설정

1. 여정 캔버스에서 _작업 수행_ 노드를 선택한 상태에서 **[!UICONTROL 계정에 대한 작업]**&#x200B;을(를) **[!UICONTROL 대상에 활성화]**(으)로 설정하십시오.

1. **[!UICONTROL 대상 선택]**&#x200B;을 클릭합니다.

   ![여정 노드 - 계정에 대해 동작 수행 - 대상에 활성화](./assets/node-activate-destination-select-destination.png){width="600" zoomable="yes"}

1. 대화 상자에서 구성된 LinkedIn 대상을 선택하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

![여정 노드 - 계정에 대해 작업 수행 - 대상에 활성화 - 대상 선택 대화 상자](./assets/node-activate-destination-select-destination-dialog.png){width="700" zoomable="yes"}

1. 대상에서 활성화된 대상을 식별하는 데 사용되는 **[!UICONTROL 대상 이름]**&#x200B;을(를) 입력하십시오.

   ![여정 노드 - 계정에서 작업 수행 - 대상에 활성화 - 완료된 설정](./assets/node-activate-destination-settings.png){width="550" zoomable="yes"}

+++

>[!ENDSHADEBOX]

## 사용자 작업

노드 경로의 모든 사람에게 변경 사항을 적용하려면 사람에 대한 작업을 사용하십시오. 이 노드 유형은 사람에 의한 분할 경로 또는 계정에 의한 분할 경로 내에서 사용할 수 있습니다.

### 작업 및 제한 {#people-action-constraints}

| 컨텍스트 | 액션 | 제한 |
| ------- | ------ | ----------- |
| [Journey Optimizer B2B](#journey-optimizer-b2b-actions) | [!UICONTROL 외부 고객 대상에 추가] | 외부 고객 대상자 선택 |
| | [!UICONTROL 구매 그룹에 할당] | 솔루션 관심 항목 선택<br/>역할 선택 |
| | [!UICONTROL 데이터 값 변경] | 사용자 특성 선택<br/>새 값 설정 |
| | [!UICONTROL 점수 변경] | 점수 이름<br/>점수 변경 |
| | [!UICONTROL 즐거운 인물] | 유형<br/>설명 |
| | [!UICONTROL 구매 그룹에서 제거] | 솔루션 관심 분야 선택 |
| | [!UICONTROL 전자 메일 보내기] | 새 전자 메일 만들기<br/>Marketo Engage에서 전자 메일 선택 |
| | [!UICONTROL SMS 보내기] | SMS 만들기 |
| [Marketo Engage](#marketo-engage-actions) | [!UICONTROL Marketo Engage 요청 캠페인에 추가] | Marketo Engage 작업 공간 선택<br/>요청 캠페인 선택 |
| | [!UICONTROL Marketo 목록에 추가] | 외부 Marketo 연결 이름 <br/>목록 이름 선택 |
| | [!UICONTROL Marketo 목록에서 제거] | 외부 Marketo 연결 이름 <br/>목록 이름 선택 |

>[!NOTE]
>
>_[!UICONTROL Marketo Engage에서 사용자 파티션 변경]_ 작업은 2025.10 릴리스에서 더 이상 사용되지 않으며 Journey Optimizer B2B edition의 간소화된 아키텍처에서 사용할 수 없습니다.

### 사용자 기반 작업 추가

1. 여정 맵으로 이동합니다.

1. 경로에서 더하기(**+**) 아이콘을 클릭하고 **[!UICONTROL 작업 수행]**&#x200B;을 선택합니다.

1. 오른쪽의 노드 속성에서 작업에 대해 **[!UICONTROL 사람]**&#x200B;을(를) 선택합니다.

1. 목록에서 작업을 선택하고 작업에 대한 값을 설정합니다.

![여정 노드 - 사용자에 대한 작업 수행](./assets/node-take-action-people.png){width="700" zoomable="yes"}

### Journey Optimizer B2B 작업

Journey Optimizer B2B 사용자 기반 작업은 구성된 채널을 통해 통신을 관리하고 구매 그룹 및 계정 내에서 사용자 분류를 관리하도록 설계되었습니다. 이 여정은 개인 프로필이 있는 자격 있는 계정이 해당 노드에 도달하면 작업을 적용합니다.

+++[!UICONTROL 외부 고객 대상에 추가]

이 작업을 사용하여 구매 그룹의 구성원을 추가로 타겟팅하기 위해 유료 미디어 채널에서 활성화할 수 있는 외부 대상자로 사람들을 푸시할 수 있습니다. 이 작업은 Real-Time CDP B2B/P 에디션을 통해 실행됩니다.

>[!NOTE]
>
>개인 프로필이 있는 자격 있는 계정이 게시된 여정의 _외부 고객 대상에 추가_ 노드에 도달하면 해당 프로필이 외부 대상에 채워지는 데 최대 48시간이 걸릴 수 있습니다.

![작업 수행 - 외부 고객 대상에 추가](./assets/node-action-add-to-external-audience-options.png){width="300"}

이 사람 기반 작업을 선택하면 새 외부 대상을 만들거나 기존 외부 대상에서 선택할 수 있습니다. 기존 대상의 경우 Journey Optimizer B2B edition에서만 만든 외부 고객 대상 중에서 선택할 수 있습니다. 대상을 만들고 이 여정 작업에 사용할 때는 대상을 연결해야 합니다. 자세한 내용은 Experience Platform 설명서에서 [새 대상 연결 만들기](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} 및 [활성화 개요](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview#activate-audiences-from-the-destinations-catalog){target="_blank"}를 참조하십시오.

![비디오](../../assets/do-not-localize/icon-video.svg){width="30"} [유료 미디어 오케스트레이션에 대한 비디오 개요 보기](../data/linkedin-account-matched-audiences.md#orchestrate-paid-media-engagement)

외부 대상을 만들려면(_T):_

1. **[!UICONTROL 새로 만들기]**&#x200B;를 선택하세요.

1. **[!UICONTROL 외부 고객 대상 만들기]**&#x200B;를 클릭합니다.

1. 새 외부 대상에 대해 **[!UICONTROL 이름]**(필수)과 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   ![외부 고객 대상에 추가 - 대상 만들기](./assets/node-action-add-to-external-create-new.png){width="300"}

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   시스템이 새 대상을 만들고 확인 메시지를 표시합니다. 그런 다음 계속 진행하여 노드 작업의 기존 대상자로 사용할 수 있습니다.

   >[!NOTE]
   >
   >Journey Optimizer B2B edition에서 새 외부 고객 대상을 만들면 더미 레코드(`test@email.com`)로 시드됩니다. 이 레코드는 첫 번째 실제 프로필이 여정에서 외부 대상에 추가되자마자 덮어쓰여집니다.

기존 대상을 사용하려면(_T):_

1. **[!UICONTROL 외부 고객 대상 선택]**&#x200B;을 클릭합니다.

1. 대화 상자에서 사용할 대상자를 선택합니다.

   ![외부 고객 대상에 추가 - 대상 추가](./assets/node-action-add-to-external-audience-select.png){width="700" zoomable="yes"}

1. **[!UICONTROL 대상 추가]**&#x200B;를 클릭합니다.

+++

+++[!UICONTROL 구매 그룹에 할당]

선택한 솔루션 관심 분야 및 역할을 기반으로 [구매 그룹](../buying-groups/buying-groups-overview.md)에 사용자 프로필을 추가하려면 이 작업을 사용하십시오.

![작업 수행 - 구매 그룹에 추가](./assets/node-action-add-to-buying-group.png){width="300"}

+++

+++[!UICONTROL 데이터 값 변경]

이 작업을 사용하여 [사람 프로필 특성](../admin/field-mapping.md#xdm-business-person-attributes)의 값을 변경합니다. 속성을 선택한 다음 새 값을 설정합니다.

![작업 수행 - 데이터 값 변경](./assets/node-action-change-data-value.png){width="300"}

+++

+++[!UICONTROL 점수 변경]

이 작업을 사용하여 Marketo Engage에서 개인 점수를 변경합니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-learn){target="_blank"}

![동작 수행 - 점수 변경](./assets/node-action-change-score.png){width="300"}

+++

+++[!UICONTROL 즐거운 인물]

이 작업을 사용하여 사람들에게 흥미로운 순간을 기록하십시오. 유형(이메일, 마일스톤 또는 웹)을 선택하고 설명을 추가합니다(선택 사항).

![액션 수행 - 즐거운 시간](./assets/node-action-person-interesting-moment.png){width="300"}

+++

+++[!UICONTROL 구매 그룹에서 제거]

선택한 솔루션 관심사를 기준으로 [구매 그룹](../buying-groups/buying-groups-overview.md)에서 사람 프로필을 제거하려면 이 작업을 사용하세요.

![작업 수행 - 구매 그룹에 추가](./assets/node-action-remove-from-buying-group.png){width="300"}

+++

+++[!UICONTROL 전자 메일 보내기]

이 작업을 사용하여 이메일을 보냅니다. 노드에 대해 [전자 메일을 만들고](../content/add-email.md#add-an-email-to-your-journey)한 후에는 전자 메일 디자인 공간에서 전자 메일 메시지를 디자인하고, 개인화하고, 미리 볼 수 있습니다([전자 메일 작성](../content/email-authoring.md) 참조). Marketo Engage에서 [전자 메일](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/creating-an-email/create-an-email){target="_blank"}을 보낼 수도 있습니다. Marketo Engage 작업 영역을 선택한 다음 전송할 이메일을 선택합니다.

![작업 수행 - 전자 메일 보내기](./assets/node-action-send-email-from-marketo.png){width="300"}

+++

+++[!UICONTROL SMS 보내기]

이 작업을 사용하여 SMS 메시지를 보냅니다. 시각적 디자인 공간에서 SMS 메시지를 만들고, 개인화하고, 미리 볼 수 있습니다([SMS 작성](../content/sms-authoring.md) 참조).

![작업 수행 - SMS 보내기](./assets/node-action-send-sms.png){width="300"}

+++

### Marketo Engage 작업

Marketo Engage 사용자 기반 작업은 Journey Optimizer B2B edition에서의 계정 기반 마케팅 오케스트레이션과 Marketo Engage에서의 리드 기반 마케팅 노력을 조정하도록 설계되었습니다. 이러한 작업을 사용하여 목록 멤버십을 오케스트레이션하고 캠페인을 요청합니다.

>[!NOTE]
>
>Marketo Engage 작업을 수행하려면 하나 이상의 외부 Marketo Engage 인스턴스와 구성된 통합이 필요합니다. <!-- For detailed information about configuring these connections, see #. -->

예를 들어 Journey Optimizer B2B edition의 구매 그룹에 속하는 사람에 대해 Marketo Engage의 캠페인을 억제하려고 할 수 있습니다. 이 경우 솔루션 관심분야에 특히 적합한 정적 목록을 Marketo Engage에서 만들 수 있습니다. 그런 다음 구매 그룹을 통한 분할 경로에서 여정 노드에서 _Marketo 목록에 추가_ 작업을 사용합니다. 이렇게 하면 연결된 Marketo Engage 인스턴스의 특정 정적 목록에 구매 그룹 구성원이 추가됩니다. 그런 다음 Marketo Engage의 스마트 목록 필터에 대해 솔루션 관심 집중 정적 목록 을 사용하십시오.

+++[!UICONTROL Marketo Engage 요청 캠페인에 추가]

이 작업을 사용하여 Marketo Engage의 [요청 캠페인](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/request-campaign){target="_blank"}에 사용자 프로필을 추가하십시오.

먼저 연결된 Marketo Engage 인스턴스를 선택합니다. 그런 다음 요청 캠페인 이름을 선택합니다.

![작업 수행 - Marketo Engage 요청 캠페인에 추가](./assets/node-action-add-to-request-campaign-options.png){width="300"}

+++

+++[!UICONTROL Marketo 목록에 추가]

이 동작을 사용하여 Marketo Engage의 [정적 목록](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"}에 사용자를 추가하십시오.

먼저 연결된 Marketo Engage 인스턴스를 선택합니다. 그런 다음 목록 이름을 선택합니다.

![작업 수행 - Marketo 목록에 추가](./assets/node-action-add-to-list-options.png){width="300"}

+++

+++[!UICONTROL Marketo 목록에서 제거]

Marketo Engage의 [정적 목록](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"}에서 사용자를 제거하려면 이 작업을 사용하십시오.

먼저 연결된 Marketo Engage 인스턴스를 선택합니다. 그런 다음 목록 이름을 선택합니다.

![작업 수행 - Marketo 목록에서 제거](./assets/node-action-remove-from-list-options.png){width="300"}

+++

## 개요 비디오

>[!VIDEO](https://video.tv.adobe.com/v/3443207/?learn=on)
