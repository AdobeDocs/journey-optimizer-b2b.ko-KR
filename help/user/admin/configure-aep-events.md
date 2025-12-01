---
title: 경험 이벤트 및 필드 선택
description: Experience Platform 이벤트 및 필드를 선택하여 고객 행동에 따라 여정에서 실시간 의사 결정을 트리거합니다.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 베타 릴리스에 있습니다"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 5f3d7bb8eb72c48409273de43b03114d273cb80c
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 7%

---

# 경험 이벤트 및 필드 선택

관리자는 경험 이벤트 유니온 스키마 내에서 특정 [AEP 경험 이벤트](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} 및 관련 필드를 선택할 수 있습니다. 선택 후 사용자는 의사 결정 규칙을 구성하여 이러한 경험 이벤트를 수신하여 실시간에 가까운 이벤트 데이터를 기반으로 동적이고 타깃팅된 캠페인 작업을 활성화할 수 있습니다.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
여정에서 AEP 경험 이벤트 사용은 두 단계 프로세스입니다.

1. 관리자 [이(가) Journey Optimizer B2B edition 구성에 AEP 경험 이벤트 및 필드를 추가](#add-an-event)합니다.

2. 여정에서 마케터가 _이벤트 수신_ 노드를 추가하고 [경험 이벤트를 선택합니다](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * 노드에서 사용할 이벤트를 선택합니다.
   * 제약 조건으로 사용할 필드를 선택합니다.

>[!BEGINSHADEBOX]

## 지침 및 제한 사항

조직 목표를 달성하기 위해 이벤트를 선택할 때는 다음 사항에 유의하십시오.

* 이벤트당 최대 50개의 이벤트와 최대 100개의 필드를 선택할 수 있습니다.

* 여정은 웹 SDK 또는 HTTP API와 같은 Experience Platform 스트리밍 기능을 사용하여 수집되는 Experience 이벤트를 수신할 수 있습니다.

* 여정 내에서 의사 결정 목적으로 Experience Event를 사용할 수 있지만 유지되지 않습니다. 따라서 Journey Optimizer B2B edition 내의 경험 이벤트에 대한 기록 레코드를 활용할 수 없습니다.

* 경험 이벤트를 사용하고 여정을 게시할 때 필드를 더 추가할 수 있지만 이전에 선택한 필드는 제거할 수 없습니다.

* 여러 여정에서 경험 이벤트를 참조하거나 동일한 여정 내에서 두 번 이상 사용할 수 있습니다.

>[!ENDSHADEBOX]

## 경험 이벤트 관리

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 구성]**&#x200B;을 선택합니다.

1. 중간 패널에서 **[!UICONTROL XDM 클래스]**&#x200B;를 클릭한 다음 **[!UICONTROL 이벤트]** 탭을 클릭하여 사용 가능한 이벤트 목록을 표시합니다.

   ![선택한 경험 이벤트에 액세스](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   표는 _[!UICONTROL 마지막 업데이트]_ 열을 기준으로 정렬되며 가장 최근에 업데이트된 이벤트가 기본적으로 맨 위에 있습니다.

   이 페이지에서 여정에 사용할 이벤트를 [선택](#add-an-event) 및 [편집](#edit-an-event)할 수 있습니다.

   선택한 이벤트에 대한 세부 정보에 액세스하려면 이벤트 이름을 클릭합니다.

### 이벤트 목록 필터링

_[!UICONTROL 검색]_ 필드에 텍스트를 입력하여 표시된 이벤트를 이벤트 이름과 일치하도록 필터링합니다.

![선택한 이벤트 목록을 이름별로 필터링](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### 이벤트 추가

여정의 _이벤트 수신_ 노드에서 경험 이벤트를 사용할 수 있도록 하려면 이벤트와 지원되는 필드를 선택합니다.

>[!NOTE]
>
>베타 릴리스에서는 목록에서 이벤트를 제거할 수 없습니다. 추가하는 각 이벤트가 조직에서 사용할 이벤트인지 확인하십시오.

1. 오른쪽 상단의 **[!UICONTROL 경험 이벤트 선택]**&#x200B;을 클릭합니다.

   이벤트 세부 사항 페이지가 표시됩니다. 이 페이지에서 이벤트 유형 및 필드를 선택할 수 있습니다.

   ![새 이벤트에 대한 이벤트 세부 정보](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. 이벤트 유형을 선택합니다.

   * **[!UICONTROL 이벤트 유형 선택]**&#x200B;을 클릭합니다.

   * 대화 상자에서 이벤트 유형을 선택합니다.

     _[!UICONTROL 검색]_ 필드를 사용하여 표시된 목록을 이름별로 필터링하십시오. **[!UICONTROL 선택한 필드만 표시]** 슬라이더를 사용하여 현재 선택 항목을 검토하십시오.

     ![이벤트 유형 선택 대화 상자](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

1. 이벤트 유형에 대해 하나 이상의 필드를 선택합니다.

   * **[!UICONTROL 필드 선택]**&#x200B;을 클릭합니다.

   * 대화 상자에서 일치 이벤트에 대한 제약 조건으로 사용할 필드를 선택합니다.

     _[!UICONTROL 검색]_ 필드를 사용하여 표시된 목록을 이름별로 필터링하십시오. **[!UICONTROL 선택한 필드만 표시]** 슬라이더를 사용하여 현재 선택 항목을 검토하십시오.

     ![필드 선택 대화 상자](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

1. 이벤트 세부 정보 페이지에서 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

저장된 이벤트가 _[!UICONTROL 이벤트]_ 탭의 목록에 표시됩니다.

### 이벤트 편집

이벤트 세부 사항을 편집하여 필드를 변경합니다.

1. 이벤트 이름을 클릭하거나 _추가 메뉴_(**...**) 아이콘을 클릭하고 **[!UICONTROL 편집]**&#x200B;을 선택하세요.

   ![기타 메뉴 아이콘 클릭](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. **[!UICONTROL 필드 선택]** 대화 상자에서 필드를 더 추가하거나 기존 선택 항목을 제거하려면 _[!UICONTROL 필드 편집]_&#x200B;을 클릭하십시오.

1. 선택 내용을 저장하려면 **[!UICONTROL 선택]**&#x200B;을 클릭하세요.

### 이벤트 제거

>[!NOTE]
>
>이 기능의 Beta 릴리스에서는 선택한 이벤트 목록에서 이벤트를 제거할 수 없습니다. GA 릴리스에서 이벤트가 제거될 예정입니다.

## 이벤트 및 필드

[!DNL Journey Optimizer B2B Edition]의 경우 특정 사용자 수준 활동이 [!DNL Experience Platform] 경험 이벤트로 캡처됩니다. 이러한 이벤트는 XDM 경험 이벤트 스키마를 사용하고 여정 특정 필드 그룹을 포함하는 시스템 데이터 세트에 저장됩니다. 다른 경험 이벤트처럼 [!UICONTROL Journey Optimizer B2B edition]에서 이러한 이벤트를 사용할 수 있습니다.

각 이벤트는 여정 _이벤트 수신_ 노드에서 사용할 수 있는 정의된 필드 집합을 표시합니다(이벤트를 기반으로 의사 결정). 사용 가능한 이벤트 유형 및 해당 필드를 검토하여 이러한 여정 노드에서 사용할 이벤트 및 필드를 결정하십시오.

### 이메일 전송됨

이 이벤트는 마케팅 이메일이 사용자에게 전송되면 추적합니다.

이벤트 유형: `directMarketing.emailSent`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 이메일 소스 ID | `directMarketing.emailSent.mailingKey.sourceID` |
| 이메일 소스 유형 | `directMarketing.emailSent.mailingKey.sourceType` |
| 이메일 소스 인스턴스 ID | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| 이메일 소스 키 | `directMailing.emailSent.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.emailSent.mailingName` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 이메일 전달됨

이 이벤트는 이메일이 개인의 이메일 서비스에 성공적으로 전달될 때 추적합니다.

이벤트 유형: `directMarketing.emailDelivered `

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 메일링 소스 ID | `directMarketing.mailingKey.sourceID` |
| 메일링 소스 유형 | `directMarketing.mailingKey.sourceType` |
| 메일링 소스 인스턴스 ID | `directMarketing.mailingKey.sourceInstanceID` |
| 메일링 소스 키 | `directMarketing.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.mailingName` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 이메일 열림

이 이벤트는 사용자가 마케팅 이메일을 열었을 때 추적합니다.

이벤트 유형: `directMarketing.emailOpened`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 메일링 소스 ID | `directMarketing.mailingKey.sourceID` |
| 메일링 소스 유형 | `directMarketing.mailingKey.sourceType` |
| 메일링 소스 인스턴스 ID | `directMarketing.mailingKey.sourceInstanceID` |
| 메일링 소스 키 | `directMarketing.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.mailingName` |
| 모바일 디바이스임 | `device.isMobileDevice` |
| 장치 모델 | `device.model` |
| 사용자 에이전트 | `environment.browserDetails.userAgent` |
| 운영 체제 | `environment.operatingSystem` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 이메일 클릭됨

이 이벤트는 사용자가 마케팅 이메일의 링크를 클릭했을 때 추적됩니다.

이벤트 유형: `directMarketing.emailClicked`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 메일링 소스 ID | `directMarketing.mailingKey.sourceID` |
| 메일링 소스 유형 | `directMarketing.mailingKey.sourceType` |
| 메일링 소스 인스턴스 ID | `directMarketing.mailingKey.sourceInstanceID` |
| 메일링 소스 키 | `directMarketing.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.mailingName` |
| 링크 URL | `directMarketing.linkURL` |
| 모바일 디바이스임 | `device.isMobileDevice` |
| 모델 | `device.model` |
| 사용자 에이전트 | `environment.browserDetails.userAgent` |
| 운영 체제 | `environment.operatingSystem` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 반송된 이메일

이 이벤트는 개인에게 전송된 이메일이 반송되면 추적합니다.

이벤트 유형: `directMarketing.emailBounced`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 메일링 소스 ID | `directMarketing.mailingKey.sourceID` |
| 메일링 소스 유형 | `directMarketing.mailingKey.sourceType` |
| 메일링 소스 인스턴스 ID | `directMarketing.mailingKey.sourceInstanceID` |
| 메일링 소스 키 | `directMarketing.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.mailingName` |
| 이메일 | `directMarketing.email` |
| 반송된 이메일 코드 | `directMarketing.emailBouncedCode` |
| 반송된 이메일 세부 정보 | `directMarketing.emailBouncedDetails` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 가볍게 반송된 이메일

이 이벤트는 개인에게 보낸 이메일이 소프트 바운스되면 추적합니다.

이벤트 유형: `directMarketing.emailBouncedSoft`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 메일링 소스 ID | `directMarketing.mailingKey.sourceID` |
| 메일링 소스 유형 | `directMarketing.mailingKey.sourceType` |
| 메일링 소스 인스턴스 ID | `directMarketing.mailingKey.sourceInstanceID` |
| 메일링 소스 키 | `directMarketing.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.mailingName` |
| 이메일 | `directMarketing.email` |
| 반송된 이메일 코드 | `directMarketing.emailBouncedCode` |
| 반송된 이메일 세부 정보 | `directMarketing.emailBouncedDetails` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 이메일 구독 취소됨

이 이벤트는 사용자가 마케팅 이메일의 구독을 취소하면 추적합니다.

이벤트 유형: `directMarketing.emailUnsubscribed `

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 메일링 소스 ID | `directMarketing.mailingKey.sourceID` |
| 메일링 소스 유형 | `directMarketing.mailingKey.sourceType` |
| 메일링 소스 인스턴스 ID | `directMarketing.mailingKey.sourceInstanceID` |
| 메일링 소스 키 | `directMarketing.mailingKey.sourceKey` |
| 메일 이름 | `directMarketing.mailingName` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### 웹 페이지 방문

이 이벤트 유형은 히트를 페이지 보기로 표시하는 표준 방법입니다.

이벤트 유형: `web.webpagedetails.pageViews`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 웹 페이지 소스 ID | `web.webPageDetails.webPageKey.sourceID` |
| 웹 페이지 소스 유형 | `web.webPageDetails.webPageKey.sourceType` |
| 웹 페이지 소스 인스턴스 ID | `web.webPageDetails.webPageKey.sourceInstanceID` |
| 웹 페이지 소스 키 | `web.webPageDetails.webPageKey.sourceKey` |
| 웹 페이지 이름 | `web.webPageDetails.name` |
| 웹 페이지 URL | `web.webPageDetails.URL` |
| 웹 페이지 쿼리 매개 변수 | `web.webPageDetails.queryParameters` |
| 웹 페이지 ID | `web.webPageDetails.webPageID` |
| 사용자 에이전트 | `environment.browserDetails.userAgent` |
| 레퍼러 URL | `web.webReferrer.URL` |

+++

### 작성된 양식

이 이벤트는 사용자가 웹 페이지에서 양식을 작성할 때 추적합니다.

이벤트 유형: `web.formFilledOut`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 웹 양식 소스 ID | `web.fillOutForm.webFormKey.sourceID` |
| 웹 양식 소스 유형 | `web.fillOutForm.webFormKey.sourceType` |
| 웹 양식 소스 인스턴스 ID | `web.fillOutForm.webFormKey.sourceInstanceID` |
| 웹 양식 소스 키 | `web.fillOutForm.webFormKey.sourceKey` |
| 웹 양식 ID | `web.fillOutForm.webFormID` |
| 웹 양식 이름 | `web.fillOutForm.webFormName` |
| 웹 페이지 쿼리 매개 변수 | `web.webPageDetails.queryParameters` |
| 웹 페이지 ID | `web.webPageDetails.webPageID` |
| 사용자 에이전트 | `environment.browserDetails.userAgent` |
| 레퍼러 URL | `web.webReferrer.URL` |

+++

### 클릭한 웹 링크

이 이벤트는 웹 SDK이 링크 클릭을 자동으로 기록했다는 신호를 보냅니다.

이벤트 유형: `web.webinteraction.linkClicks`

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 웹 인터랙션 소스 ID | `web.webInteraction.webInteractionKey.sourceID` |
| 웹 인터랙션 소스 유형 | `web.webInteraction.webInteractionKey.sourceType` |
| 웹 인터랙션 소스 인스턴스 ID | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| 웹 인터랙션 소스 키 | `web.webInteraction.webInteractionKey.sourceKey` |
| 웹 인터랙션 링크 ID | `web.webInteraction.linkID` |
| 웹 인터랙션 링크 URL | `web.webInteraction.linkURL` |
| 웹 페이지 쿼리 매개 변수 | `web.webPageDetails.queryParameters` |
| 웹 페이지 ID | `web.webPageDetails.webPageID` |
| 사용자 에이전트 | `environment.browserDetails.userAgent` |
| 레퍼러 URL | `web.webReferrer.URL` |

+++

### 즐거운 순간

이 이벤트는 한 사람에게 재미있는 순간을 기록할 때 추적합니다.

이벤트 유형: `leadOperation.interestingMoment `

+++필드

| 필드 | 필드 유형 |
| ----- | ---------- |
| 식별자 | `_id` |
| 이벤트 유형 | `eventType` |
| 타임스탬프 | `timestamp` |
| 개인 ID | `personID` |
| 개인 소스 ID | `personKey.sourceID` |
| 개인 소스 유형 | `personKey.sourceType` |
| 개인 소스 인스턴스 ID | `personKey.sourceInstanceID` |
| 개인 소스 키 | `personKey.sourceKey` |
| 모멘트 일자 | `leadOperation.interestingMoment.date` |
| 순간 설명 | `leadOperation.interestingMoment.description` |
| 모멘트 소스 | `leadOperation.interestingMoment.source` |
| 모멘트 유형 | `leadOperation.interestingMoment.type` |
| 여정 ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| 노드 ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->