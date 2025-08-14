---
title: 계정 대상 노드
description: Journey Optimizer B2B edition에서 계정 여정에 대한 입력을 정의하는 데 사용할 수 있는 계정 대상 노드 유형에 대해 알아봅니다.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 82553c9ee6205e0ad47cc5a56112590471c03d0e
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# 계정 대상자 여정 노드

계정 대상 노드는 여정을 입력하는 계정을 지정합니다. [계정 여정을 만듭니다](./journey-overview.md#create-an-account-journey). 여정은 항상 입력을 정의하는 계정 대상 노드로 시작합니다.

이 여정 노드에 대해 다음 입력 옵션 중 하나를 사용합니다.

* **[계정 대상자](../audiences/account-audience-overview.md)** — 계정 대상자는 Experience Platform 세분화 서비스에서 동기화되는 기본 대상자를 나타냅니다.
* **[계정 목록](../accounts/account-lists.md)** — 계정 목록은 타깃팅된 여정 오케스트레이션에 사용하는 명명된 계정의 컬렉션입니다. 계정 목록은 업계, 위치 또는 회사 크기와 같은 정의된 기준을 사용하여 계정이라는 이름을 타겟으로 합니다.

## 계정 대상자 노드에 대한 대상자 설정

1. **[!UICONTROL 계정 대상자]** 노드를 클릭합니다. 이 작업은 오른쪽에 노드 속성을 표시합니다.

   ![계정 대상자 여정 노드](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. 여정을 입력하는 계정의 입력 유형을 선택합니다.

   * **[!UICONTROL 계정 대상자]**

     계정 대상자 옵션을 선택합니다. 그런 다음 **[!UICONTROL 계정 대상자 추가]**&#x200B;를 클릭합니다.

     _[!UICONTROL 대상 추가]_ 대화 상자에서 이전에 만든 대상 세그먼트를 선택합니다. 그런 다음 **[!UICONTROL 대상 추가]**&#x200B;를 클릭합니다.

     ![노드의 대상 세그먼트 선택](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL 계정 목록]**

     계정 목록 옵션을 선택합니다. **[!UICONTROL 계정 목록 추가]**&#x200B;를 클릭합니다.

     _[!UICONTROL 라이브 계정 목록 선택]_ 대화 상자에서 게시된 계정 목록을 선택합니다. 그런 다음 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

     ![노드의 실시간 계정 목록 선택](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     계정 목록을 만들고 게시하는 방법에 대한 자세한 내용은 [계정 목록](../accounts/account-lists.md)을 참조하세요.

## 대상 세그먼트 만들기

1. 왼쪽 탐색에서 **[!UICONTROL 계정]** > **[!UICONTROL 대상]**&#x200B;을 선택합니다.

1. 오른쪽 상단에서 **[!UICONTROL 대상 만들기]**&#x200B;를 클릭합니다.

   ![대상 세그먼트 만들기](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. [세그먼테이션 서비스 안내서](https://experienceleague.adobe.com/ko/docs/ experience-platform/segmentation/types/account-audiences){target="_blank"}의 단계를 따릅니다.
