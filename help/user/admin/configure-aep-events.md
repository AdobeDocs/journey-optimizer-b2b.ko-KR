---
title: 경험 이벤트 및 필드 선택
description: Experience Platform 이벤트 및 필드를 선택하여 고객 행동에 따라 여정에서 실시간 의사 결정을 트리거합니다.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 베타 릴리스에 있습니다"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# 경험 이벤트 및 필드 선택

관리자는 경험 이벤트 유니온 스키마 내에서 특정 [AEP 경험 이벤트](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} 및 관련 필드를 선택할 수 있습니다. 선택 후 사용자는 의사 결정 규칙을 구성하여 이러한 경험 이벤트를 수신하여 실시간에 가까운 이벤트 데이터를 기반으로 동적이고 타깃팅된 캠페인 작업을 활성화할 수 있습니다.

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
>베타 릴리스에서는 목록에서 이벤트를 제거할 수 없습니다. 추가하는 각 이벤트가 조직에서 사용되도록 하십시오.

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

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->