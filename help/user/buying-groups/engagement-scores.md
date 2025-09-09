---
title: 구매 그룹에 대한 참여 점수
description: Journey Optimizer B2B edition에서 가중 활동, 역할 기반 계산 및 30일 채점 기간을 사용하여 구매 그룹 및 개인 참여 점수를 계산합니다.
feature: Buying Groups, Engagement
role: User
exl-id: 424d9598-92dd-42de-8447-3c7cebc71a73
source-git-commit: 0eaf713deee1ae8bd04c82b6aaab0443bd60e5e7
workflow-type: tm+mt
source-wordcount: '1254'
ht-degree: 30%

---

# 참여 점수 {#engagement-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score"
>title="참여 점수"
>abstract="참여 점수는 구매 그룹 멤버의 참여 수준을 결정합니다."

참여 점수는 구매 그룹의 구성원에 대한 참여 수준을 나타내는 숫자입니다. 이러한 점수는 구매 집단 구성원 활동, 가중 행위 및 가중 역할을 기준으로 합니다. 결과 점수는 일관된 비교를 활성화하고 실행 가능한 통찰력을 허용하기 위해 테넌트(인스턴스) 내에서 표준화됩니다. 구매 그룹을 생성하면 바로 점수 계산이 시작됩니다. Journey Optimizer B2B edition 데이터 허브 시스템은 매일 점수를 계산하여 수집 서비스를 사용하여 MLM(Multi-Level Marketing) MySQL 시스템에 업로드합니다.

참여 점수에는 두 가지 유형이 있습니다.

* **구매 그룹 참여 점수** - 구매 그룹 참여 점수는 0에서 100 사이의 정규화된 점수이며 개인 수준에서 계산된 참여 점수를 기반으로 합니다.

  구매 그룹 참여 점수가 [구매 그룹 세부 정보](./buying-group-details.md) 페이지에 표시됩니다. 지능형 대시보드에서 가장 많이 참여하는 구매 그룹을 볼 수도 있습니다.

  ![가장 많이 참여하는 구매 그룹](./assets/person-engagement-score-attribute-filtering.png){width="700" zoomable="yes"}

* **개인 참여 점수** - 개인 참여 점수는 개별 구매 그룹 구성원의 활동을 기반으로 합니다.

  각 구매 그룹 구성원의 개인 참여 점수가 구매 그룹 세부 정보 페이지 [_[!UICONTROL 구성원&#x200B;]_&#x200B;탭](./buying-group-details.md#buying-group-members)에 표시됩니다. 이러한 점수는 상위 참여 구성원 및 겹치는 연락처 정보가 포함된 페이지 및 대시보드에도 표시됩니다.

  ![가장 많이 참여하는 구매 그룹 구성원](./assets/top-engaged-buying-group-members.png){width="550" zoomable="yes"}

>[!BEGINSHADEBOX]

사용자 참여 점수는 [역할 템플릿](./buying-groups-role-templates.md#add-the-template-roles) 및 [여정 split-path-by-people 노드](../journeys/split-merge-paths-nodes.md#people-path-conditions)에서 필터링하는 데 사용할 수 있는 특성입니다.

![구성된 이벤트 정의에 액세스](./assets/most-engaged-buying-groups.png){width="550" zoomable="yes"}

>[!ENDSHADEBOX]

지난 30일 동안 구매 그룹의 구성원이 수행한 모든 참여 가중 활동은 점수를 계산하는 데 사용됩니다. 30일 기간을 사용하면 활동 발생이 만료되고 점수가 아래로 이동할 수 있습니다(점수 감소). 표시된 점수는 반올림됩니다(예: 75.89999 점수가 76으로 표시됨).

## 참여 점수에 사용되는 활동

구매 그룹 점수가 _트리거된 기반_&#x200B;이 아닙니다. 구매 그룹의 모든 멤버에서 활동을 평가하고 점수를 다시 계산하는 일별 프로세스입니다. 활동에서는 _가중치_&#x200B;를 사용하여 각 활동에 가중치를 부여하는 방법을 결정하는 활성 가중치 모델에 따라 구매 그룹 점수를 알립니다.

각 활동의 일일 빈도 상한은 20회입니다. 구매 그룹의 구성원이 하루에 동일한 활동을 20번 이상 수행하는 경우 활동에 대한 카운트는 20으로 제한됩니다.

| 활동 이름 | 설명 | 참여 유형 | 최대 일일 빈도 수 | 기본 모델 활동 가중치 |
|---------------|-------------|-----------------|---------------------------|-------------------------------|
| 이벤트 참여 | 멤버가 이벤트에 참여함 | 이벤트 | 20 | 60 |
| 이메일 클릭됨 | 멤버가 판매 이메일의 링크를 클릭함 | 이메일 | 20 | 30 |
| 이메일 열림 | 멤버가 이메일을 열람함 | 이메일 | 20 | 30 |
| 작성된 양식 | 멤버가 웹 페이지에서 양식을 작성하고 제출함 | 웹 | 20 | 40 |
| 즐거운 순간 | 멤버에게 “즐거운 순간”이 있음 | 선별 | 20 | 60 |
| 링크 클릭수 | 멤버가 웹 페이지의 링크를 클릭함 | 웹 | 20 | 40 |
| 페이지 보기 횟수 | 구성원이 웹 페이지를 봅니다. | 웹 | 20 | 40 |
| 이벤트 등록 | 이벤트에 등록된 멤버 | 이벤트 | 20 | 60 |

<!-- old list

| Activity name | Description | Engagement type | Max daily frequency count | Activity weight |
| --- | --- | --- | --- | --- |
| [!UICONTROL Visit Webpage]| A member visits a web page | Web | 20 | 40 |
| [!UICONTROL Fill Out Form]| A member fills and submits a form on a web page | Web | 20 | 40 |
| [!UICONTROL Click Link] | A member clicks a link on a web page | Web | 20 | 40 |
| [!UICONTROL Open Email] | A member opens an email | Email | 20 | 30 |
| [!UICONTROL Click Email] | A member clicks a link in an email | Email | 20 | 30 |
| [!UICONTROL Open Sales Email] | A member opens a sales email | Email | 20 | 30 |
| [!UICONTROL Click Sales Email] | A member clicks a link in a sales email | Email | 20 | 30 |
| [!UICONTROL Interesting Moment] | A member has an interesting moment | Curated | 20 | 60 |
| [!UICONTROL Tap Push Notification] | A member receives a push notification | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Activity] | A member performs an activity on a mobile app | Mobile | 20 | 30 |
| [!UICONTROL Mobile App Session] | A member is active on a mobile app session | Mobile | 20 | 30 |
| [!UICONTROL Fill Out Facebook Lead Ads Form] | A member fills and submits a Lead Ads form on a Facebook page | Social | 20 | 30 |
| [!UICONTROL Click RTP Call to Action] | A member clicks a personalized call to action | Web | 20 | 60 |
| [!UICONTROL View In-App Message] | A member views an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Tap In-App Message] | A member taps an in-app message | Mobile | 20 | 30 |
| [!UICONTROL Subscribe SMS] | A member subscribes to SMS communications | SMS | 20 | 90 |
| [!UICONTROL Reply to Sales Email] | A member replies to a sales email | Email | 20 | 30 |
| [!UICONTROL Engaged with a Dialogue] | A member engages with a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Dialogue] | A member interacts with a document in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Dialogue] | A member schedules an appointment in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Reached Dialogue Goal] | A member reaches a goal in a Dynamic Chat dialogue |  |20 | 90 |
| [!UICONTROL Responded to a poll in webinar] | A member responds to a poll in a webinar event | Chat | 20 | 90 |
| [!UICONTROL Call to action clicked in webinar] | A member clicks a call-to-action link in a webinar event | Call | 20 | 30 |
| [!UICONTROL Asset downloads in webinar] | A member downloads a file/asset in a webinar event | Event | 20 | 60 |
| [!UICONTROL Asks questions in webinar] | A member asks questions in a webinar event | Event | 20 | 60 |
| [!UICONTROL Has attended event] | A member attended an event | Event | 20 | 60 |
| [!UICONTROL Engaged with an Agent in Dialogue] | A member engages with an agent in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Dialogue] | A member clicks a link in a Dynamic Chat dialogue | Chat | 20 | 90 |
| [!UICONTROL Engaged with a Conversational Flow] | A member engages with a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Scheduled Meeting in Conversational Flow] | A member schedules an appointment in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Reached Conversational Flow Goal] | A member reaches a goal in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Interacted with Document in Conversational Flow] | A member interacts with a document in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Engaged with an Agent in Conversational Flow] | A member engages with an Agent in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Clicked Link in Chat in Conversational Flow] | A member clicks a link in a Dynamic Chat conversational flow | Chat | 20 | 90 |
| [!UICONTROL Click Link in SMS V2] | A member clicks a link in an SMS message | SMS | 20 | 90 | -->

>[!NOTE]
>
>참여 점수 활동은 개인의 Marketo Engage 활동 로그에 기록됩니다. 연결된 Marketo Engage 인스턴스에서 이 로그에 액세스할 수 있습니다. 자세한 내용은 Marketo Engage 설명서에서 [사용자에 대한 활동 로그 찾기](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person){target="_blank"}를 참조하십시오.

## 역할 템플릿 가중치 {#engagement-score-weighting}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_engagement_score_weighting"
>title="참여 점수 역할 가중치"
>abstract="역할 가중치를 사용하여 참여 점수 계산을 사용자 정의합니다."

사용자는 [역할 템플릿](./buying-groups-role-templates.md)에서 각 역할에 _가중치_&#x200B;를 설정하여 역할별로 서로 다른 가중치를 할당하고 참여 점수를 계산할 수 있습니다.

![역할 템플릿에서 각 역할에 대한 가중치 설정](./assets/roles-templates-weighting.png){width="700" zoomable="yes"}

각 가중치 수준은 참여 점수를 계산하는 데 사용되는 값으로 변환됩니다.

* [!UICONTROL 매우 사소] = 20
* [!UICONTROL 사소] = 40
* [!UICONTROL 보통] = 60
* [!UICONTROL 중요] = 80
* [!UICONTROL 매우 중요] = 100

_[!UICONTROL 매우 중요]_, _[!UICONTROL 중요]_, _[!UICONTROL 보통]_&#x200B;으로 가중치가 지정된 세 가지 역할이 포함된 역할 템플릿은 다음과 같은 가중치 백분율로 변환됩니다.

| 역할 | 가중치 | 시스템 값 | 값 계산 | 백분율 |
|-------------- |--------- |------------- |------------------ |---------- |
|               |          |              |                   |           |
| 의사 결정자 | 매우 중요 | 100 | 100/240 | 41.67% |
| 영향력 있는 사용자 | 중요 | 80 | 80/240 | 33.33% |
| 실무자 | 보통 | 60 | 60/240 | 25% |
|               | 합계 | 240 |                   |           |

## 점수 계산 예

다음 예에서는 참여 점수 계산을 보여 줍니다. 요약된 역할 가중치 백분율, 각 구매 그룹 구성원에 대한 인바운드 활동 수 및 각 이벤트 발생에 대한 일일 상한 20을 사용합니다.

| 역할 | 멤버 | 활동 유형 | 어제의 활동 수 | 오늘의 활동 수 | 계산 | 총점 |
|-------------- |--------- |-------------|-----------------|-------------|------|-----------|
|               |          |             |                 |             |      |           |
| 의사 결정자 | Adam | 웹 사이트를 방문함 | 37 | 15 | 20 + 15 | 35 |
|               |          | 이메일을 클릭함 | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Mark | 웹 사이트를 방문함 | 5 | 3 | 5 + 3 | 8 |
|               |          | 이메일을 클릭함 | 1 | 1 | 1 + 1 | 2 |
|               |          | 게시물을 다운로드함 | 3 | 2 | 3 + 2 | 5 |
| **의사 결정자 총점** |         |             |                 |             |      | **52** |
|               |          |             |                 |             |      |           |
| 영향력 있는 사용자 | John | 웹 사이트를 방문함 | 19 | 9 | 19 + 9 | 28 |
| **영향력 있는 사용자 총점** |         |             |                 |             |      | **28** |
|               |          |             |                 |             |      |           |
| 실무자 | Bob | 이메일을 클릭함 | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Paul | 이메일을 클릭함 | 1 | 1 | 1 + 1 | 2 |
|               |          |             |                 |             |      |           |
|               | Calvin | 이메일을 클릭함 | 1 | 1 | 1 + 1 | 2 |
|               |          | 웹 사이트를 방문함 | 1 | 7 | 1 + 7 | 8 |
|               |          | 게시물을 다운로드함 | 1 | 2 | 1 + 2 | 3 |
| **실무자 총점** |         |             |                 |             |      | **17** |

최종 참여 점수는 각 역할 점수에 대한 가중치를 적용하여 계산됩니다.

| 역할 | 역할 총점 | 역할 가중치 % | 점수 X 가중치 % |
|-------------- |---------------- |------------- |---------------- |
| 의사 결정자 | 52 | 41.67% | 21.67 |
| 영향력 있는 사용자 | 28 | 33.33% | 9.33 |
| 실무자 | 17 | 25% | 4.25 |
| **최종 참여 점수** |                |             | **35.25** |

## 채점 논리

계산 예제에 설명된 계산 논리 외에도, 시스템의 모든 사용자, 구매 그룹 및 계정에서 상당히 복잡한 점수 표준화가 발생합니다. 구매 그룹 참여 점수는 다음과 같은 순서가 지정된 논리에 따라 개인 참여 점수에 종속됩니다.

### 개인 참여 점수 계산 논리

1. 웹 사이트 방문, 전자 메일 클릭 수 및 웨비나 참석과 같이 가중치와 일일 할당량이 연결된 모든 _참여 가중치_ 활동 유형을 식별합니다.

1. 현재 30일로 하드 코딩된 활동 전환 확인 기간 내에서 수행되는 모든 사용자 _참여 가중치_ 작업을 식별합니다.

1. 전환 확인 기간 내에 발생하지 않은 가중치를 무시하고 1단계에서 식별된 모든 _참여 가중치_ 활동 유형 가중치에 대해 활동 유형 가중치를 정규화합니다.

   이 단계에서는 _최소-최대 정규화_&#x200B;를 활용하고 대부분을 활용하지 않는 테넌트에 대한 활동 유형 가중치의 인위적인 희석을 크게 줄입니다.

1. 개인 및 활동 유형별 일일 할당량 필터링을 적용합니다.

   이 단계는 점수를 왜곡하는 낮은 값/높은 볼륨 활동을 방지하여 매우 큰 이상치를 갖는 것을 완화합니다.

1. 활동 유형별 일일 활동을 합산하고, 여기에 관련 가중치를 곱한 다음 전환 확인 기간의 모든 일에 대한 결과를 합산하여 원시 개인 참여 점수를 계산합니다.

1. 가능한 이상치를 줄여 분산을 안정시키려면 _전원 변환_(제곱근) 변환을 사용합니다.

   이러한 변환은 왜곡의 정도를 줄이고 데이터의 패턴을 더 선형적으로 만드는 데 도움이 됩니다.

1. 추가 _크기 조정된 정규화_ 변환을 적용하여 점수가 0에서 100 사이의 전체 범위를 활용하도록 합니다.

### 구매 그룹 참여 점수 계산 논리

1. 역할 템플릿에 구성된 가중치에 따라 역할별로 각 구매 그룹 멤버에 정규화된 가중치를 적용합니다.

1. 각 구매 그룹에 대한 구매 그룹 역할 가중치를 표준화합니다.

   구매 그룹이 모든 역할을 사용하지 않는 경우 이러한 표준화를 통해 불필요한 역할 가중치 희석이 발생하지 않습니다.

1. 개인 참여 점수에 개인의 역할 표준화된 역할 가중치를 곱하여 모든 구매 그룹 구성원 개인 참여 점수를 집계한 후 합산합니다.

1. 특히 대규모 구매 그룹의 경우 가능한 이상치를 줄여 분산을 안정시키려면 _전원 변환_(제곱근) 변환을 적용하십시오.

1. 추가 _크기 조정된 정규화_ 변환을 적용하여 점수가 0에서 100 사이의 전체 범위를 활용하도록 합니다.
