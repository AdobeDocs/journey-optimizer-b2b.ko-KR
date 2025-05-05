---
title: 여정 및 프로그램에서 계정 목록 사용
description: 여정에서 계정 목록 멤버십을 오케스트레이션하고, 계정 목록 멤버십을 기반으로 Marketo Engage 스마트 목록을 필터링하는 방법을 알아봅니다.
source-git-commit: 0845bff023741ebf8aca448c65950beceae77cf1
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# 여정 및 프로그램에서 계정 목록 사용

여러 가지 방법으로 라이브(게시된) 계정 목록을 계정 여정에 통합할 수 있습니다.

## 계정 대상자 노드

모든 계정 여정은 [_계정 대상자_ 노드](../journeys/account-audience-nodes.md)(으)로 시작합니다. 계정 목록을 사용하도록 이 노드를 설정하면 구성원 계정이 활성화(게시)될 때 해당 여정을 통해 이동합니다.

1. 시작 _계정 대상자_ 노드에 대해 **[!UICONTROL 계정 목록]** 옵션을 선택하십시오.

   ![계정 대상 노드의 계정 목록 옵션 선택](../journeys/assets/node-audience-account-list.png){width="500"}

1. **[!UICONTROL 계정 목록 추가]**&#x200B;를 클릭합니다.

1. 계정 목록에 대한 확인란을 선택하고 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   ![계정 대상 노드의 계정 목록 옵션 선택](../journeys/assets/node-audience-account-list-select-dialog.png){width="600" zoomable="yes"}

## 작업 노드 - 계정에 추가

**_정적 계정 목록만_**

계정 여정 내에서 [a _작업 수행_ 노드](../journeys/action-nodes.md)을 사용하여 정적 계정 목록에 계정을 추가합니다.

예를 들어, 이메일을 보내고 일부 계정에서 응답 작업으로 다양한 작업을 수행하는 여정 경로가 있을 수 있습니다. 이 활동을 여정의 자격 지점으로 간주하여 자격 있는 계정에 대해 다른 플로우를 가진 다른 여정의 대상자로 사용하는 계정 목록에 추가하려고 합니다.

>[!NOTE]
>
>노드가 실행될 때 계정이 이미 목록에 있는 경우 작업이 무시됩니다.

1. _&#x200B;**[!UICONTROL 계정]**&#x200B;에 대한_&#x200B;작업 옵션을 선택하십시오.

1. _[!UICONTROL 계정에 대한 작업]_&#x200B;의 경우 **[!UICONTROL 계정 목록에 추가]**&#x200B;를 선택하세요.

   ![계정 목록에 추가 선택](../journeys/assets/node-action-account-add-to-account-list.png){width="500"}

1. **[!UICONTROL 실시간 정적 계정 목록 선택]**&#x200B;의 경우 계정을 추가할 계정 목록을 선택하십시오.

   ![계정 목록에 추가 선택](../journeys/assets/node-action-account-add-to-account-list-select.png){width="500"}

## 작업 노드 - 계정에서 제거

**_정적 계정 목록만_**

계정 여정 내에서 [a _작업 수행_ 노드](../journeys/action-nodes.md)을 사용하여 정적 계정 목록에서 계정을 제거하십시오.

예를 들어, 이메일을 보내고 일부 계정에서 응답 작업으로 다양한 작업을 수행하는 여정 경로가 있을 수 있습니다. 이 활동을 여정의 자격 지점으로 간주하며 자격 커뮤니케이션이 중복되지 않도록 추가 이메일을 보내는 다른 여정의 대상자로서에 사용되는 계정 목록에서 해당 활동을 제거하려고 합니다.

>[!NOTE]
>
>계정이 제거가 예약된 목록에 없으면 작업이 무시됩니다.

1. _&#x200B;**[!UICONTROL 계정]**&#x200B;에 대한_&#x200B;작업 옵션을 선택하십시오.

1. _[!UICONTROL 계정에 대한 작업]_&#x200B;의 경우 **[!UICONTROL 계정 목록에서 제거]**&#x200B;를 선택하세요.

   ![계정 목록에 추가 선택](../journeys/assets/node-action-account-remove-from-account-list.png){width="500"}

1. **[!UICONTROL 실시간 정적 계정 목록 선택]**&#x200B;의 경우 계정을 제거할 계정 목록을 선택하십시오.

   ![계정 목록에 추가 선택](../journeys/assets/node-action-account-remove-from-account-list-select.png){width="500"}

## Marketo Engage 프로그램 - 계정 구성원 목록

마케터는 Journey Optimizer B2B edition의 계정 목록에 포함된 사람에 대해 Marketo Engage의 프로그램을 표시하지 않을 수 있습니다.

Journey Optimizer B2B edition에 연결된 Marketo Engage 인스턴스에서는 스마트 목록의 _[!UICONTROL 계정 목록 구성원]_ 필터를 사용하여 캠페인 전략에 따라 이러한 리드를 식별할 수 있습니다. 스마트 목록에 대한 자세한 내용은 [Marketo Engage 설명서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"}를 참조하세요.

### 스마트 목록에 필터 추가

1. Marketo Engage에서 캠페인을 선택하고 **[!UICONTROL 스마트 목록]** 탭을 클릭합니다.

1. 오른쪽에 표시된 필터 목록에서 `Member`을(를) 입력하고 **[!UICONTROL 계정 목록 구성원]** 필터를 찾습니다.

1. 필터를 스마트 목록 캔버스로 드래그합니다.

1. 스마트 목록 캔버스에서 **[!UICONTROL 계정의 구성원]** 목록 값을 설정합니다.

   아래쪽 화살표를 클릭하여 모든 계정 목록을 표시하거나 계정 목록 이름의 일부를 입력하여 필요한 계정 목록을 찾습니다.

   ![계정 목록 구성원에 대한 Marketo Engage 스마트 목록 필터](./assets/account-lists-marketo-engage-smart-list.png){width="800" zoomable="yes"}

1. 캠페인 흐름에서 **[!UICONTROL 목록에 추가]** 단계를 추가하고 Journey Optimizer B2B edition 계정 목록에서 사람을 채울 목록을 선택합니다.

   흐름에 단계를 추가하는 방법에 대한 자세한 내용은 Marketo Engage 설명서의 _[스마트 캠페인에 흐름 단계 추가](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/add-a-flow-step-to-a-smart-campaign){target="_blank"}_&#x200B;를 참조하십시오.

### 구성원 검토

흐름이 실행되면 목록에서 채워지는 사람 목록을 볼 수 있습니다. 목록을 열고 사람 탭을 선택합니다.

![계정 목록에서 채워진 Marketo Engage 캠페인 목록](./assets/account-lists-marketo-engage-smart-list-people.png){width="800" zoomable="yes"}

