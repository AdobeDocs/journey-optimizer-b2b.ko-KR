---
title: 스팸 보고서 검토
description: ISP 또는 사서함 공급자가 스팸으로 간주할지 여부를 예측하는 전용 스팸 보고서에서 이메일 콘텐츠 스팸 점수를 확인하는 방법을 알아봅니다.
feature: Email Authoring
level: Beginner
role: User
source-git-commit: 7992df497182b69c5103b603d69a70e1a40e903a
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# 스팸 보고서 검토

많은 이메일 받은 편지함 공급자 및 대부분의 회사 시스템에서 스팸 필터링 프로세스를 사용합니다. 이러한 필터를 트리거하는 이메일을 보내면 게재 기능에 심각한 영향을 줄 수 있습니다. Journey Optimizer B2B edition에서 스팸 보고서를 생성하여 이메일 콘텐츠 스팸 점수를 확인할 수 있습니다. 이 보고서는 [[!DNL SpamAssassin]](https://spamassassin.apache.org/)을(를) 사용하여 전자 메일을 테스트하고 스팸 방지 도구로 메시지를 스팸으로 간주할 수 있는지 여부를 확인하는 데 도움이 됩니다. 보고서의 정보를 사용하여 이메일 콘텐츠 점수 및 전달성을 개선하는 작업을 수행할 수 있습니다.

이메일 설정을 검토하거나 콘텐츠를 편집할 때 _[!UICONTROL 시뮬레이션]_ 페이지를 열고 _스팸 보고서_&#x200B;를 생성하여 스팸 방지 필터링을 트리거할 수 있는 점수 책정 및 플래그 지정된 요소를 검토합니다.

1. _[!UICONTROL 시뮬레이션]_ 페이지에서 오른쪽 상단의 **[!UICONTROL 스팸 보고서]**&#x200B;를 클릭합니다.

   ![스팸 보고서 단추](./assets/email-spam-report-button.png){width="700" zoomable="yes"}

   보고 프로세스는 이메일 콘텐츠를 스캔하고 점수를 생성하는 데 사용되는 트리거된 필터링 규칙 목록으로 점수를 생성합니다. 요소에는 본문 레이아웃, 구조, 이미지 크기, 스팸 트리거 단어 및 기타 요소가 포함됩니다. 전자 메일 요소에 대한 규칙 평가 테스트 목록을 보려면 [[!DNL SpamAssassin] 테스트 목록](https://spamassassin.apache.org/old/tests_3_0_x.html)을 참조하세요.

1. 각 항목에 대한 점수와 설명을 확인합니다.

   >[!NOTE]
   >
   >스팸 점수는 SpamAssassin을 통해 계산되며, Adobe은 규칙이나 점수 논리를 소유하지 않습니다. [!DNL SpamAssassin] 오픈 소스 프로젝트에 대한 자세한 내용은 [[!DNL SpamAssassin] 설명서](https://cwiki.apache.org/confluence/display/SPAMASSASSIN/)를 참조하세요.

   점수가 낮을수록 이메일이 스팸으로 표시될 가능성이 낮습니다.

   ![스팸 보고서 긍정적 점수](./assets/email-spam-report-positive.png){width="600" zoomable="yes"}

   점수가 5점보다 큰 이 보고서에는 일부 메시지가 수신 시 차단되거나 스팸으로 표시될 수 있다는 경고가 포함됩니다. 점수가 2점 이하가 되도록 하는 것이 모범 사례다.

   ![스팸 보고서 집계 점수](./assets/email-spam-report-negative.png){width="600" zoomable="yes"}

1. 이메일 콘텐츠 내에 개선할 수 있는 일부 요소가 있는 경우 콘텐츠를 편집하여 필요한 업데이트를 적용합니다.

1. 변경 사항이 완료되면 _[!UICONTROL 시뮬레이션]_ 페이지로 돌아가서 **[!UICONTROL 스팸 보고서]**&#x200B;를 다시 클릭하여 결과 점수 개선 사항을 확인하십시오.



