---
title: AI Assistant에 대한 질문 지침
description: Journey Optimizer B2B edition에서 AI Assistant에 대한 효과적인 질문을 작성하는 방법을 알아봅니다.
feature: AI Assistant
role: User
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 1%

---

# Journey Optimizer B2B edition의 AI Assistant에 대한 질문 지침

Journey Optimizer B2B edition의 AI Assistant 쿼리에 대한 다음 예제 질문 세트를 검토하십시오. 이 정보에는 AI Assistant에서 최적의 응답을 얻기 위해 질문을 구문 분석하는 방법에 대한 팁도 포함되어 있습니다.

## 목표 기반 질문

다음 예제 질문은 AI Assistant를 사용할 때 달성할 수 있는 목표에 따라 그룹화됩니다.

| 목표 | 설명 | 예 |
| --- | --- | --- |
| 학습 개념 및 지속적인 워크플로 | 초보 사용자는 AI Assistant를 사용하여 Real-Time CDP 및 Adobe Journey Optimizer B2B edition 개념을 학습하고 익숙하지 않은 제품 및 기능을 온보딩할 수 있습니다. <br>숙련된 사용자는 AI Assistant를 사용하여 워크플로를 차단할 수 있는 경계 사례를 해결할 수 있습니다. | <li>Real-Time CDP의 사용 사례를 알려 주십시오. <li>나에게 구매 그룹 개념을 설명하십시오. |
| 문제 해결 | AI Assistant를 사용하여 워크플로우에서 발생할 수 있는 기본 오류를 디버깅하는 방법을 학습합니다. | <li>이 오류 &lt;ERROR_MESSAGE>은(는) 무엇을 의미합니까? <li>이름이 &quot;..&quot;인 대상자를 삭제할 수 없는 이유는 무엇입니까? |
| 샌드박스 위생 | AI Assistant를 사용하여 중복 또는 사용하지 않는 오브젝트를 식별하면 샌드박스를 효율적으로 관리할 수 있습니다. | <li>유사한 계정 대상자를 보여줄 수 있습니까? <li>연관된 데이터 세트가 없는 스키마가 있습니까? |
| 값 분석 | AI Assistant를 사용하여 가장 많이 사용되는 데이터 객체를 식별하고 성능 지표를 평가하거나 가장 중요한 데이터 객체를 찾습니다. | <li>&quot;...&quot; 세그먼트 정의에 있는 계정은 몇 개입니까? <li>대상이 언제 Experience Cloud 대상 대상에 활성화되었습니까? |
| 검색 | 계정 대상자, 데이터 세트, 대상, 스키마, 소스, 계정 여정, 구매 그룹 템플릿 및 솔루션 관심 항목과 같이 지원되는 Experience Platform 및 Adobe Journey Optimizer B2B edition 개체를 AI Assistant를 사용하여 찾습니다 | <li>계정 여정에 사용된 이름에 &quot;Luma&quot;가 포함된 대상을 나열합니다. <li>Luma: 사용자 지정 작업 XDM 스키마에는 어떤 속성이 있습니까? |
| 영향 분석 | AI Assistant를 사용하여 특정 워크플로우에서 사용된 데이터 객체를 식별하여 변경 사항의 영향을 평가할 수 있습니다. | <li>대상이 &quot;B2B 사용자&quot; 스키마에서 `workEmail.address`을(를) 사용하는 계정 대상은 무엇입니까? <li>`jobTitle`에 저장된 데이터 세트는 무엇입니까? |

## 질문 표현

가능한 한 정확한 응답을 얻기 위해 명확성과 컨텍스트를 사용하여 AI Assistant에 질문을 구해야 합니다. 컨텍스트에 따라 명확한 질문을 하는 방법에 대한 지침은 다음 팁 목록을 참조하십시오.

* 작업 및/또는 질문을 간결하게 진술하십시오.
* 이해가 용이하도록 모호한 언어나 지나치게 복잡한 구문은 피한다.
* AI Assistant가 더 연관성 있는 응답을 생성하는 데 도움이 될 수 있으므로 작업 및/또는 질문에 대한 관련 컨텍스트를 제공합니다.

다음 표는 AI Assistant 사용 시 따를 수 있는 몇 가지 모범 사례를 제공합니다.

| 실행 | 예 |
| --- | --- |
| <li>검색하거나 분석할 개체 또는 정보에 대해 구체적으로 지정합니다. <li>데이터 개체 이름을 따옴표로 묶어 보십시오. <li>개체 이름의 일부만 알고 있는 경우에는 질문에 이를 지정할 수도 있습니다. | <li>다음 중 &quot;B2B 계정&quot; 스키마를 사용하는 데이터 세트는 무엇입니까? <li>이름에 &quot;계정&quot;이 있는 활성화된 대상을 표시합니다. 구성원 수에 따라 순위를 매깁니다. |
| <li>모호함을 피하고 명확한 언어를 사용하십시오. <li>쿼리의 명확성을 높이려면 정확한 용어를 사용하십시오. <li>Adobe Experience Platform 및 Adobe Journey Optimizer B2B edition과 관련된 질문을 할 때는 Experience Platform 또는 Adobe Journey Optimizer B2B edition에 관련된 용어를 사용하여 응답의 관련성을 개선해 보십시오. | <li>내 계정 대상에는 몇 명의 멤버가 있습니까? <li>얼마나 많은 계정 여정이 계정 대상자 &quot;내 계정 대상자&quot;를 사용합니까? |
| <li>컨텍스트를 제공하거나 결과를 필터링할 기준을 지정하십시오. <li>질문의 필터 기준을 사용하여 응답의 데이터 볼륨을 제한합니다. | <li>활성화되지 않았으며 6개월 이상 전에 만들어지고 수정되지 않은 계정 대상을 표시합니다. <li>지난 7일 동안 게시된 계정 여정을 확인하고 구성원이 1000명이 넘는 계정 대상을 사용합니다. |

| 안 함 | 예 |
| --- | --- |
| 모호하거나 모호한 언어를 사용하십시오. | <li>데이터 세트에 대한 정보를 제공합니다. <li>여정 x의 기능은 무엇입니까? <li>ACME Audience에는 사용자가 몇 명입니까? <li>세그먼트를 표시합니다. <li>목록 속성입니다. |
| 완료되지 않은 요청을 수행합니다. | <li>&quot;Luma - 충성도 데이터 세트&quot; |
| 컨텍스트가 없는 지식을 가정하십시오. | <li>지난 6개월 동안의 대상자입니다. <li>나를 위해 쿼리를 만듭니다. <li>나를 위한 여정 만들기 |
| 너무 복잡한 쿼리를 만듭니다. | <li>모든 객체와 해당 종속 항목에 대한 데이터 계보를 포괄적으로 분석할 수 있습니다. |
| 기준이나 매개 변수를 생략합니다. | <li>데이터 세트 표시 |

## 지원되지 않는 질문의 예

다음 목록에는 Journey Optimizer B2B edition의 AI Assistant가 현재 지원하지 않는 질문의 예가 포함되어 있습니다.

* 어떤 계정 대상자가 ... 필드 그룹의 workEmail.address 필드를 해당 조건에서 사용합니까? 
* 10,000개 이상, 5000-10,000개, 1000-5000개 및 1000 미만의 계정 대상을 사용하는 활성 여정 수를 분포 시각적 보기로 표시합니다
* 계정 여정 x에 대한 마지막 업데이트를 수행한 사람은 누구입니까?
* 얼마나 많은 활성 여정이 솔루션 관심사 x에 대한 구매 그룹 구성원을 추가합니까?
* 솔루션 관심사 x에 대해 구매 그룹 구성원을 추가하는 활성 여정은 무엇입니까?
* 그룹 템플릿을 구매하는 가장 일반적인 의사 결정자 제목은 무엇입니까?
* 그룹 템플릿 x를 구매하는 데 대한 의사 결정자는 누구입니까?

## 다음 단계

워크플로 중에 AI Assistant 기능을 사용하는 방법에 대한 자세한 내용은 [Journey Optimizer B2B edition에서 AI Assistant 사용](./use-ai-assistant.md)을 참조하십시오.
