---
title: 여정 세부 사항
description: Adobe Journey Optimizer B2B Edition에서 계정 및 개인 여정 성과를 모니터링합니다. 각 여정에 대한 완료, 참여 및 채널 지표를 검토합니다.
feature: Dashboards, Account Journeys, Person Journeys
role: User
exl-id: 09a0e06a-1fd3-44da-9774-23f125f2823d
autotag-review: 2026-03-30T23:21:08.953Z
TQID: 'https://experienceleague.adobe.com/a5tIOW39sq3Lq30pQ3yr7-IvLGaAXC6LKqY8-mpxCDY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: f979fe0e-02fe-4599-b492-7b3df1d4e7dc
    internal-label: Intelligent Insights
  - id: 7da10825-0f0b-5df3-8450-465ae8d76951
    internal-label: Dashboards
subfeature_v2:
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 5c053f91ea231cd8517e2329b7170aa08c33dc24
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---
# 여정 세부 정보

[!DNL Adobe Journey Optimizer B2B Edition]에서 게시된 계정 또는 사용자 여정을 열고 **[!UICONTROL 개요]** 탭을 선택합니다. 선택한 여정에 대한 진행 상황, 참여 및 채널 성능을 검토합니다.

계정 여정은 계정에 대한 진행 상황을 보고합니다. 개인 여정은 사용자에 대한 진행 상황을 보고합니다. 사용 가능한 위젯과 지표 레이블은 여정 유형별로 다릅니다. 대시보드 세부 사항에 해당하는 탭을 선택합니다.

여정 간에 집계된 전자 메일 지표의 경우 [전자 메일 성능 보고서](../dashboards/email-performance-dashboard.md)를 사용하십시오.

>[!BEGINTABS]

>[!TAB 계정 여정]

계정 여정 대시보드에는 계정 진행 상황, 참여, 채널 성과 및 생성 AI 요약이 표시됩니다. 데이터가 차트와 표를 채우는 데 약 4시간이 소요됩니다.

![진행 상황, 참여 및 채널 성능을 보여 주는 계정 여정 개요 탭](./assets/journey-detail-overview-account.png){width="700" zoomable="yes"}

## 여정 완료

이 섹션에는 두 개의 완료 지표가 표시됩니다.

* **[!UICONTROL 여정의 계정 상태]**: _완료됨_, _진행 중_, _중단됨_&#x200B;을 포함하여 여정 상태별 총 계정 수 및 분류를 표시합니다. 각 세그먼트에는 상태, 백분율 및 계정 수가 표시됩니다.
* **[!UICONTROL 시간 경과에 따라 완료된 여정]**: 시간 경과에 따라 계정을 완료한 계정의 수를 표시합니다. 가로 축은 날짜를 보여 주고 세로 축은 계정 수를 보여 줍니다.

>[!NOTE]
>
>계정 여정에서 **[!UICONTROL 여정의 계정 상태]** 차트에는 이후에 삭제된 경우에도 해당 여정을 거친 계정이 포함됩니다. **[!UICONTROL 드릴스루]**&#x200B;에서는 삭제된 계정을 제외하므로 차트보다 적은 수의 레코드를 표시할 수 있습니다. 이 차이가 예상됩니다. 계정을 삭제해도 과거 여정 상태 수는 변경되지 않습니다.

## 여정 참여

이 섹션에서는 두 가지 참여 지표를 제공합니다.

* **[!UICONTROL 계정별 참여]** - 이 원 차트는 여정의 계정을 _참여_ 및 _미참여_ 범주로 나눕니다. 중앙 그림에는 총 개수가 표시됩니다. 이 시각화는 전반적인 계정 참여를 빠르게 이해할 수 있도록 해줍니다.
* **[!UICONTROL 사용자별 참여]**: 여정에 참여 활동을 가진 사용자의 수를 표시합니다. 이 값은 참여 활동이 아닌 사람을 계산합니다.

## 여정 성능

이 섹션에서는 두 가지 중요한 지표를 제공합니다.

* **[!UICONTROL 여정 완료율]** - 여정을 성공적으로 완료한 계정의 비율입니다.
* **[!UICONTROL 평균 여정 완료 시간]**: 계정이 여정을 완료하는 데 걸린 평균 시간(일)입니다.

## 채널 성능 {#email-and-sms-performance}

대시보드에는 선택한 계정 여정의 **[!UICONTROL 이메일 성능]**, **[!UICONTROL SMS 성능]** 및 **[!UICONTROL WhatsApp 성능]** 테이블이 포함됩니다. 사용 가능한 게재 및 참여 지표를 사용하여 각 커뮤니케이션 접점을 평가합니다.

**[!UICONTROL 전자 메일 성능]** 테이블 열:

* _[!UICONTROL 자산 이름]_ - 자산의 이름
* _[!UICONTROL 전송됨]_ - 보낸 전자 메일 수
* _[!UICONTROL 게재율]_ - 게재된 이메일 수를 보낸 횟수로 나눈 값입니다.
* _[!UICONTROL 열람율]_ - 열람한 전자 메일 수를 게재된 숫자로 나눈 값입니다.
* _[!UICONTROL 클릭스루 비율]_ - 클릭한 이메일 수를 게재된 숫자로 나눈 값입니다.

**[!UICONTROL SMS 성능]** 테이블 열:

* _[!UICONTROL 자산 이름]_ - 자산의 이름
* _[!UICONTROL 전송됨]_ - 전송된 SMS 메시지 수
* _[!UICONTROL 게재율]_ - 게재된 SMS 메시지 수를 보낸 횟수로 나눈 값입니다.
* _[!UICONTROL 클릭스루 비율]_ - 클릭한 SMS 메시지 수를 게재된 숫자로 나눈 값입니다.
<!--
To generate a shareable PDF of your current view, click **[!UICONTROL Export]** at the top right of the page. 
-->

## 추가 작업

차트 또는 테이블에서 **..** 메뉴를 사용하여 사용 가능한 작업에 액세스하십시오.

### 드릴스루

**[!UICONTROL 여정]** 차트의 계정 상태에 대해 **[!UICONTROL 드릴스루]**&#x200B;를 선택하여 개별 계정 상태를 자세히 분석하십시오.

![그래프 데이터에 대한 드릴스루](./assets/journey-status-drill-through.png){width="600" zoomable="yes"}
<!--
The applied global filters are carried over to the view and displayed at the top. Click the _Filter_ icon at the top left to filter the data display by journey.
-->

### 더 보기

확장 데이터에 액세스하려면 **[!UICONTROL 자세히 보기]**&#x200B;를 선택하세요. 표시되는 팝업은 데이터 분류를 제공합니다.

![확장 데이터 보기](./assets/journey-completion-over-time-view-more.png){width="600" zoomable="yes"}

데이터를 다운로드하려면 **[!UICONTROL CSV 다운로드]**&#x200B;를 선택하십시오. _[!UICONTROL 개요]_ 대시보드로 돌아가려면 **[!UICONTROL 닫기]**&#x200B;를 선택합니다.

>[!TAB 개인 여정]

개인 여정 대시보드에는 선택한 여정의 사용자에 대한 완료, 참여 및 이메일 성능이 표시됩니다.

![진행 상황, 참여 및 전자 메일 성능을 보여 주는 개인 여정 개요 탭](./assets/journey-detail-overview-person.png){width="700" zoomable="yes"}

## 여정 완료 {#person-journey-completion}

다음 차트를 사용하여 여정 및 완료 트렌드에 있는 인력의 상태를 검토할 수 있습니다.

* **[!UICONTROL 여정에 있는 사용자의 상태]**: 여정 상태별로 총 사용자 수와 분류를 표시합니다. 각 세그먼트에는 상태, 백분율 및 인원 수가 표시됩니다.
* **[!UICONTROL 시간 경과에 따라 완료된 사용자]**: 시간 경과에 따라 여정을 완료한 사용자 수를 표시합니다. **[!UICONTROL 증분 완료]** 시리즈는 각 시간 간격에 대한 완료를 표시합니다. **[!UICONTROL 누적 완료]** 시리즈는 실행 중인 총 완료 횟수를 보여줍니다.

>[!NOTE]
>
>**[!UICONTROL 여정의 사용자 상태]** 차트에 있는 여정의 사용자가 있습니다. 이후에 삭제된 경우에도 이 여정을 거친 사용자가 포함됩니다. **[!UICONTROL 드릴스루]**&#x200B;에서는 삭제된 사용자가 제외되므로 차트보다 적은 수의 레코드를 표시할 수 있습니다. 이 차이가 예상됩니다. 사람을 삭제해도 과거 여정 상태 수는 변경되지 않습니다.

여정] 차트에 있는 사람들의 상태 _[!UICONTROL 에 대해_&#x200B;자세히_( **...**) 아이콘을 클릭하고 **[!UICONTROL 드릴스루]**&#x200B;를 선택하여 개인 상태를 검토합니다.

## 여정 참여 {#person-journey-engagement}

**[!UICONTROL 사용자별 참여]** 위젯은 여정에 참여 활동이 있는 사용자의 수를 표시합니다. 이 값은 참여 활동이 아닌 사람을 계산합니다.

## 여정 성능 {#person-journey-performance}

다음 지표를 사용하여 완료 성과를 검토하십시오.

* **[!UICONTROL 여정 완료율]**: 여정을 완료한 사람의 비율입니다.
* **[!UICONTROL 평균 여정 완료 시간]**: 사람들이 여정을 완료하는 데 걸린 평균 시간(일)입니다.

## 이메일 성과 {#person-journey-email-performance}

**[!UICONTROL 전자 메일 성능]** 테이블은 선택한 개인 여정의 각 전자 메일 에셋에 대한 비율 대신 개수를 표시합니다.

* **[!UICONTROL 자산 이름]**: 전자 메일 자산의 이름
* **[!UICONTROL 전송됨]**: 보낸 전자 메일 수
* **[!UICONTROL 배달됨]**: 배달된 이메일 수
* **[!UICONTROL 열림]**: 열린 전자 메일 수
* **[!UICONTROL 클릭됨]**: 클릭한 이메일 수

>[!ENDTABS]
