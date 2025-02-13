---
title: 계정 여정
description: 계정 여정과 이를 만들고 관리하는 방법에 대해 알아봅니다.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---


# 계정 여정

이메일, SMS, 이벤트 등에 걸쳐 자동화된 참여를 사용하여 각 구매 그룹 및 구매 그룹 구성원에 맞게 조정된 여정을 작성하고 실행합니다. 계정 여정을 사용하면 수요 생성 및 구매 그룹 자격을 간소화하고 고객 확보, 상향 판매/교차 판매 및 유지 프로그램에 대한 보다 적합한 수요를 창출할 수 있습니다.

여정 이메일, SMS 등을 포함하는 판매 주도 참여를 정의하여 인바운드 마케팅과 각 구매 그룹 구성원에 대한 아웃바운드 판매 활동을 조정합니다.

![비디오](../../assets/do-not-localize/icon-video.svg){width="30"} [개요 비디오 보기](#overview-video)

## 계정 여정 액세스 및 찾아보기

1. Adobe Experience Platform 홈페이지에서 Adobe Journey Optimizer B2B edition 를 클릭합니다.

1. 왼쪽 탐색에서 **[!UICONTROL 계정 여정]**&#x200B;을 클릭합니다.

   ![계정 여정 액세스](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   표시된 여정 페이지에는 다음 열이 포함되어 있습니다.

   * [!UICONTROL 이름](편집할 계정 여정을 열려면 이름을 클릭하십시오.)
   * [!UICONTROL 상태]
   * [!UICONTROL 설명]
   * [!UICONTROL 만든 사람]
   * [!UICONTROL 마지막 업데이트 시간:]
   * [!UICONTROL 마지막으로 업데이트한 사람]
   * [!UICONTROL 게시 날짜]
   * [!UICONTROL 게시자]

이 표에는 이름 및 작성자별로 검색하는 기능이 포함되어 있습니다. 현재 정렬을 사용할 수 없습니다.

오른쪽 상단의 _열_ 아이콘을 클릭하고 확인란을 선택하거나 선택을 취소하여 표시된 테이블을 사용자 지정할 수 있습니다.

![계정 여정 목록에 표시할 열을 선택하십시오](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## 계정 여정 구조

_[!UICONTROL 계정 여정]_ 목록에서 링크로 표시된 이름을 클릭하여 세부 사항을 검토하고 변경하고 작업을 수행합니다.

![계정 여정 작업 공간](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

각 계정 여정의 편집기 헤더에는 다음이 포함됩니다.

* 여정 이름
* 이름 편집 기능(_편집_ 아이콘)
* 여정 상태

헤더에서는 다음 작업을 사용할 수 있습니다.

* **게시** - 차단기 오류가 없는 경우 여정을 게시할 수 있습니다. 게시되면 여정 상태가 _Live_(으)로 변경됩니다. 여정에 오류가 있으면 단추가 콘텐츠 정보 `Resolve errors before publishing`(으)로 흐리게 표시됩니다.
* **복제** - 이 작업은 복제 함수와 비슷하지만, 복제된 여정에 자산이 포함되지 않습니다.
* **새 항목에 닫기** - 여정을 닫으면 현재 여정에 있는 계정이 여정에서 경로를 계속 사용하며 더 이상 여정을 시작할 수 없습니다. 종료된 여정은 다시 시작할 수 없습니다. 닫힌 여정을 복제할 수 있습니다.
* **중단** - 여정을 중지하면 여정의 계정이 즉시 진행을 중지하며 더 이상 여정을 시작할 수 없습니다. 중지된 여정은 다시 시작할 수 없습니다. 사람들의 진도를 중단하지 않고 새로운 출입을 차단하는 경우 대신 여정을 종료하는 것이 좋습니다.
* **삭제** - 이 작업은 여정을 영구적으로 삭제합니다.

여정 상태는 적용하는 작업에 따라 변경됩니다. 여정 상태에 따라 헤더에서 특정 작업을 사용할 수 없거나 사용할 수 없습니다.

| 상태 | 설명 | 사용 가능한 작업 |
| ------ | ----------- | ----------------- |
| _**초안**_ | 편집할 수 있는 게시되지 않은 여정. | <ul><li>게시</li><li>복제 </li><li>삭제 </li></ul> |
| _**라이브**_ | 여정이 게시되면 여정 상태가 초안에서 라이브로 변경됩니다. 이 상태에서는 더 이상 편집할 수 없습니다. | <ul><li>복제 </li><li>새 항목에 닫기 </li><li>중단 </li></ul> |
| _**새 항목으로 닫힘**_ | 위쪽 탐색에서 [!UICONTROL 새 항목에 닫기]를 클릭하면 여정 상태가 _Live_&#x200B;에서 _새 항목에 닫힘_(으)로 변경됩니다. | <ul><li>복제 </li><li>중단 </li></ul> |
| _**중단됨**_ | 여정을 중단할 때 _Live_ 또는 _새 항목으로 닫힘_&#x200B;에서 여정 상태가 변경됩니다. 중단된 여정은 다시 시작할 수 없습니다. | <ul><li>복제 </li><li>삭제 </li></ul> |
| _**완료됨**_ | 여정의 모든 계정이 여정을 완료하면 상태가 라이브 또는 마감에서 새 항목으로 변경되고 완료됨으로 변경됩니다. | <ul><li>복제 </li><li>삭제 </li></ul> |

## 여정 시작

계정 여정을 시작하려면:

1. [여정 만들기](./create-publish-journey.md#create-an-account-journey).
1. [여정 맵에서 노드를 추가](./create-publish-journey.md#add-a-node) 및 [여정 흐름을 정의](./create-publish-journey.md#add-and-delete-a-path)합니다.
1. [여정 게시](./create-publish-journey.md#publish-an-account-journey).

## 개요 비디오

>[!VIDEO](https://video.tv.adobe.com/v/3443202/?learn=on)
