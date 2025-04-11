---
title: AI 어시스턴트 사용
description: AI Assistant를 통해 Journey Optimizer B2B edition 기능을 최대한 활용하는 방법을 살펴볼 수 있습니다.
feature: AI Assistant
level: Beginner
exl-id: 2d642c34-6f6d-4a0f-98c5-4b9ea1cdaa29
source-git-commit: d19ed2bbe850a14cb0563f6e3563cd8f1c8d3226
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Journey Optimizer B2B edition에서 AI Assistant 사용

Journey Optimizer B2B edition에서 AI Assistant는 제품 개념을 이해하고, Journey Optimizer B2B edition 기능을 빠르게 탐색 및 학습하며, 특정 환경에 대한 운영 통찰력을 얻는 데 사용할 수 있는 사용자 인터페이스 기능입니다. Adobe Experience Cloud 전체의 여러 제품에서도 사용할 수 있습니다.

>[!IMPORTANT]
>
>AI Assistant를 사용하려면 Adobe Experience Cloud 생성 AI 사용 지침에 대한 동의가 필요합니다. 이 계약 및 사용 지침에 대한 자세한 내용은 [Adobe Experience Cloud Generative AI 사용 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)을 참조하세요.

AI Assistant에 액세스하려면 헤더에서 아이콘을 클릭합니다. AI Assistant가 오른쪽 패널에서 열립니다.

![아이콘을 클릭하여 AI Assistant에 액세스합니다](./assets/ai-assistant-icon-displayed.png){width="420" zoomable="yes"}

AI Assistant 인터페이스가 나타나고 시작하기 위한 정보가 즉시 제공됩니다. _아이디어 시작_&#x200B;에 제공된 옵션을 사용하여 다음과 같은 질문과 명령에 답변할 수 있습니다.

* 내 계정 여정 중 어떤 항목이 게시되었습니까?
* 어떤 솔루션 관심사가 생성되었습니까?
* Journey Optimizer B2B edition의 주요 이점을 알려 주십시오.

Adobe Journey Optimizer B2B edition에서 AI Assistant는 다음과 같은 사용 사례를 지원합니다.

## 제품 지식

제품 지식 질문은 Adobe Journey Optimizer의 측면과 관련된 Journey Optimizer B2B edition 개념에 대한 것입니다. 제품 지식 질문에 대한 몇 가지 예는 다음과 같습니다.

* SMS 공급자 계정을 설정하려면 어떻게 해야 합니까?
* 계정 여정 시 이메일을 보내려면 어떻게 해야 합니까?
* 이메일 콘텐츠를 개인화하려면 어떻게 해야 합니까?

제품 질문을 하려면 패널 하단의 필드에 질문을 입력하고 Enter 키를 누릅니다.

![텍스트 상자에 질문을 입력하십시오](./assets/ai-assistant-ask-question.png){width="420" zoomable="yes"}

모든 제품 지식 답변과 함께 제공되는 인용문을 검토하여 AI 어시스턴트가 반환하는 답변을 확인할 수 있습니다.

인용구를 보고 AI Assistant의 응답을 확인하려면 **[!UICONTROL 소스 표시]**&#x200B;를 선택하십시오.

![AI Assistant 쿼리의 결과](./assets/ai-assistant-answer.png){width="420" zoomable="yes"}

AI Assistant는 인터페이스를 업데이트하며 초기 응답을 확증하는 설명서 링크를 제공합니다. 또한 인용이 활성화되면 AI Assistant는 제공된 설명서를 참조하는 응답의 특정 부분을 표시하는 각주를 포함하도록 응답을 업데이트합니다.

엄지손가락을 위로 또는 아래로 사용하여 답의 질을 평가하십시오.

## Operational insights

Operational insight 질문은 조직의 샌드박스에 있는 여정 개체에 대한 것입니다. 작동 중인 insight 질문 또는 프롬프트의 몇 가지 예는 다음과 같습니다.

* Adobe Journey Optimizer B2B edition에는 라이브 여정이 몇 개 있습니까?
* 모든 예약된 여정 목록 제공
* 지난 7일 동안 얼마나 많은 여정이 생성되었습니까?

AI Assistant가 작동 인사이트에 대한 질문에 충분한 응답을 제공하려면 활성 샌드박스에 있어야 합니다.

>[!NOTE]
>
>AI Assistant Operational Insights 질문에서 지원하는 유일한 Adobe Journey Optimizer B2B edition 개체는 [operational insights 도메인 테이블](./ai-assistant-overview.md#operational-insights)에 나열되어 있습니다. 현재 속해 있는 샌드박스에 대한 데이터에만 액세스할 수 있습니다.

<!-- Select to view an example of an operational insights question.

In the following example, AI Assistant receives the following query: _Show me dataflows that were created using the Amazon S3 source._

screen

AI Assistant responds with a table list of your dataflows and their corresponding IDs. Click the _Download_ icon ( Download icon ) to download the table as a CSV file. To view the entire table, click the _Expand_ icon ( Expand icon ).

screen

An expanded view of the table appears, providing you with a more comprehensive list of dataflows based on the parameters of your query.

screen

When prompted with an operational insights question, AI Assistant provides an explanation of how it computed the answer. In the following example, AI Assistant outlines the steps it took in order to identify the dataflows that were created using the Amazon S3 source.

screen

You can also provide filters and modifications to your questions, and you can instruct AI Assistant to render its findings based on the filters that you include. For example, you can ask AI Assistant to show you a trend of the count of segment definitions in the order of their created date, remove segment definitions with zero total profiles, and use month names instead of integers when displaying the data.

### Verify operational insights responses

You can verify each response related to operational insights questions using an SQL query that AI Assistant provides.

Select to view example of verifying operational insights responses

After receiving an answer for an operational insights question, click **[!UICONTROL Show sources]** and then select **[!UICONTROL View source query]**.

screen

When queried with an operational insights question, AI Assistant provides an SQL query that you can use to verify the process that it took to compute its answer. This source query is for verification purposes only and is not supported on Query Service.

screen  

 -->
