---
title: Journey Optimizer B2B edition의 AI 지원
description: 플레이스홀더
feature: AI Assistant
level: Beginner
source-git-commit: 168bd128de8845c1ccd4e33b290aecebc28064ef
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 4%

---

# Journey Optimizer B2B edition의 AI 지원

Journey Optimizer B2B edition의 AI 도우미는 Adobe Experience Platform의 [AI 도우미](https://experienceleague.adobe.com/ko/docs/experience-platform/ai-assistant/home)와 동일한 기술 기반에서 만들어집니다. Adobe Journey Optimizer B2B edition에서 워크플로를 가속화하는 데 사용할 수 있는 대화형 경험입니다. AI Assistant를 사용하여 제품 기능을 보다 깊이 이해하고, 문제를 해결하거나, 정보를 검색하고, Journey Optimizer B2B edition에 대한 운영 통찰력을 찾을 수 있습니다.

>[!IMPORTANT]
>
>Journey Optimizer B2B edition에서 AI 도우미를 사용하려면 [사용자 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)에 동의해야 합니다. 이 계약에는 추가 AI Assistant 기능이 베타 용량으로 롤아웃될 때 사용할 수 있도록 공개 베타 계약도 포함되어 있습니다.

+++사용자 계약 인터페이스 보기

![사용자 계약의 첫 페이지입니다.](./assets/user-agreement-1.png)

![사용자 계약의 마지막 페이지.](./assets/user-agreement-2.png)

+++

## Journey Optimizer B2B edition의 AI Assistant 기능

제출된 질문에 대한 답변을 작성하기 위해 AI Assistant는 데이터베이스를 쿼리하고 데이터베이스의 데이터를 사람이 읽을 수 있는 답변으로 변환합니다. 이 응답은 기본 데이터의 내부 표현이며, 지정된 질문에 대한 개념, 데이터 및 메타데이터의 포괄적인 웹인 _**_지식 그래프_**_&#x200B;라고도 합니다. 지식 그래프는 쿼리가 제출될 때마다 참조되는 하위 그래프로 구성됩니다.

* Experience League 설명서입니다.
* 스키마, 필드, 대상 및 여정 등 운영 객체

AI Assistant 쿼리를 제출하기 전에 필요한 조회 유형을 고려하십시오.

### 제품 지식

제품 지식은 Adobe Experience League의 Journey Optimizer B2B edition 설명서에 나와 있는 개념과 주제를 나타냅니다. 제품 지식 질문은 다음 하위 그룹에 추가로 지정할 수 있습니다.

| 제품 지식 | 예시 |
| --- | --- |
| 뾰족한 학습 | <li>구매 그룹이란 무엇입니까? <li> 구매 그룹 역할 템플릿의 예를 보여 주시겠습니까? |
| 검색 열기 | <li>구매 그룹을 만드는 단계는 무엇입니까? <li>구매 그룹 역할 템플릿에서 사용자 정의 필드를 사용하는 방법은 무엇입니까? |
| 문제 해결 | <li>내 여정에 사용할 그룹을 만들지 않은 이유는 무엇입니까? <li>여정에서 수신할 경험 이벤트를 찾을 수 없는 이유는 무엇입니까? |

### Operational insights

_운영 인사이트_&#x200B;는 AI Assistant가 메타데이터 개체(특성, 계정 대상, 데이터 흐름, 데이터 세트, 대상, 계정 여정, 스키마, 소스, 구매 그룹 템플릿 및 솔루션 관심 분야)에 대해 생성하는 답변을 의미합니다. 이러한 통찰력에는 카운트, 조회 및 계보 영향이 포함됩니다. 샌드박스 내의 데이터는 보지 않습니다.

* 대상자 규모가 가장 큰 계정 대상자는 무엇이며 해당 규모는 무엇입니까?
* 여정에서 한 번도 사용한 적이 없는 계정 대상은 몇 명입니까?
* 솔루션 관심사 _x_&#x200B;을(를) 사용하는 활성 여정은 무엇입니까?

다음 도메인에서 운영 통찰력에 대해 AI Assistant에 질문할 수 있습니다.

| 도메인 | 지원되는 메타데이터 | 지원되지 않는 메타데이터 |
| --- | --- | --- |
| 속성/필드 | <li>속성 이름 검색 <li>속성 - 스키마 관계 <li>속성 - 데이터 세트 관계 <li>속성 - 대상 관계 <li>속성 - 대상 관계 | <li>Attribute 클래스 <li>감사 <li>사용 중단 상태 <li>레이블 <li>속성에 저장된 값 |
| 계정 대상 <br><br>**_참고:_**AJO B2B AI Assistant는 계정 대상에 대한 대상 질문에만 답할 수 있으며 Experience Platform AI Assistant는 개인 대상에 대한 질문에만 답할 수 있습니다 | <li>대상자 수 <li>대상자 유형(스트리밍 또는 일괄 처리) <li>생성/수정 날짜 <li>활성화 상태 <li>구성원 수 <li>중복 대상자 <li>이름 및 ID 검색 | <li>대상자 중복 <li>대상자 활성화 <li>감사 <li>만들기/수정 <li>레이블 <li>멤버 자격 트렌드 |
| 데이터 흐름 | <li>데이터 흐름 카운트 <li>데이터 흐름 상태 <li>데이터 흐름 - 데이터 세트 관계 <li>데이터 흐름 - 원본 관계 | <li>생성/수정 <li>데이터 흐름 일괄 처리 관계 <li>프로필 개수 수집 |
| 데이터 세트 | <li>데이터 세트 수 <li>프로필 활성화 상태 <li>생성/수정 날짜 <li>데이터 세트 - 스키마 관계 <li>데이터 세트 - 대상 관계 <li>데이터 세트 - 속성 관계 <li>데이터 세트 - 데이터 흐름 관계 <li>이름 검색 <li>이름 및 ID 검색 | <li>감사 <li>제작자 <li>데이터 세트 - 일괄 처리 관계 <li>데이터 세트 생성/수정 <li>데이터 세트 크기 <li>프로필 수 <li>행 수 <li>값 검색 |
| 대상 | <li>구성된 대상 카운트 <li>대상 - 대상 관계 <li>대상 속성 관계 | <li>계정 설정 <li>계정 자격 증명 정보 <li>고유 프로필 활성화됨 |
| 여정(계정 여정) | <li>계수 <li>이름 및 ID 검색 <li>여정 상태 <li>생성/수정 날짜 | <li>속성 - 여정 관계 감사 <li>생성/수정 <li>제작자 |
| 스키마 | <li>스키마 카운트 <li>생성/수정 날짜 <li>스키마 - 속성 관계 <li>스키마 - 데이터 세트 관계 <li>스키마 - 대상 관계 <li>프로필 활성화 상태 <li>이름 검색 <li>이름 및 ID 검색 | <li>감사 <li>생성/수정 <li>제작자 <li>필드 그룹 <li>ID <li>ID 네임스페이스 <li>레이블 <li>프로필 수 |
| 소스 | <li>계정 수 <li>계정 상태 <li>각 계정에 대한 활성/비활성 데이터 흐름 <li>Source 커넥터 - 데이터 흐름 관계 <li>Source 계정 - 데이터 흐름 관계 | <li>계정 자격 증명 정보 <li>계정 설정데이터 수집 지표 <li>프로필 수소스 - 배치 관계 |
| 구매 그룹 템플릿 | <li>카운트 <li>상태 <li>역할 <li>이름 및 ID 검색 | <li>역할 규칙 |
| 솔루션 관심 분야 | <li>카운트 <li>상태 <li>솔루션 관심사 - 구매 그룹 템플릿 관계 <li>이름 및 ID 검색 | <li>솔루션 관심사 - 구매 그룹 관계 |

{style=&quot;table-layout:fixed&quot;}

운영 통찰력 질문에 대한 답변이 UI의 현재 상태를 반영하지 않을 수 있습니다. 이러한 질문을 뒷받침하는 데이터는 24시간마다 한 번씩 업데이트됩니다. 예를 들어 사용자가 낮에 Real-Time CDP에서 수행하는 변경 사항은 밤에 데이터 스토어와 동기화된 다음 아침에 사용자 질문에 대해 사용할 수 있게 됩니다. 샌드박스에 로그인하여 객체와 관련된 특정 데이터를 조회합니다.

### 기능 범위

현재 AI Assistant의 범위는 다음과 같습니다.

* [제품 지식](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#product-knowledge): AI Assistant는 Real-Time Customer Data Platform 및 Adobe Journey Optimizer B2B edition에 대한 제품 지식 질문에 답변할 수 있습니다.

* [운영 인사이트](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#operational-insights): 특성, 계정 대상, 데이터 흐름, 데이터 세트, 대상, 계정 여정, 스키마, 소스, 구매 그룹 템플릿 및 솔루션 관심 사항과 같은 데이터 개체에 대한 운영 인사이트에 대해 AI Assistant에 질문할 수 있습니다.

### 개인 정보, 보안 및 거버넌스

Journey Optimizer B2B edition의 AI Assistant는 개인정보 보호, 보안 및 거버넌스를 전면에 두고 구축됩니다. 다음 정보를 검토하여 AI Assistant에서 기대할 수 있는 고객 신뢰 중심 기능에 대해 알아보십시오.

* 현재 AI Assistant는 교육 목적으로도 개인 데이터를 사용하지 않습니다.

* AI Assistant는 사람, 계정, 기회 및 구매 그룹과 같은 고객 데이터를 인식하지 못합니다.

* AI Assistant와 상호 작용하려면 명시적인 권한이 있어야 합니다.

   * 관리자는 [권한 UI](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) 및 [Admin Console](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/browse)을 사용하여 권한을 설정할 수 있습니다.

   * 권한은 세분화되며 샌드박스 관리자는 다양한 질문 카테고리(AI Assistant를 통한 제품 지식 기반 질문 또는 운영 통찰력에 대한 질문)를 물을 수 있는 사용자를 구성할 수 있습니다.

* 30일 보존 정책으로 AI Assistant와의 이전 상호 작용 로그를 볼 수 있습니다.

* AI Assistant는 사용자 프롬프트에 응답할 때 샌드박스 특정 데이터 및 공개 Adobe 설명서에 기반합니다. 데이터는 샌드박스 간에 공유되지 않습니다.

* AI Assistant에 제공하는 프롬프트는 다른 고객에게 공유되지 않습니다.

### 자주 묻는 질문

다음은 Journey Optimizer B2B edition의 AI Assistant에 대한 FAQ 답변 목록입니다.

**AI Assistant의 정보가 실시간으로 제공됩니까?**

AI 비서 응답에 제시된 데이터는 매일 업데이트됩니다. 이 주기는 응답에 포함된 데이터가 응답 시 사용자 인터페이스에 표시된 데이터보다 최대 24시간 이전일 수 있음을 의미합니다.

**AI Assistant의 기능은 무엇입니까?**

AI Assistant는 Adobe 제품 지식 쿼리를 처리할 수 있으며 운영 객체의 운영 통찰력과 관련된 질문에 답변할 수 있습니다.

**AI 관리자가 고객 데이터에 대한 정보를 제공할 수 있습니까?**

아니요. AI Assistant는 고객 데이터에 액세스할 수 없으므로 AI Assistant에서 보거나 사용하지 않습니다.

**AI Assistant의 교육 데이터에 내 개인 정보가 사용됩니까?**

AI 어시스턴트는 개인정보를 교육 목적으로 활용하지 않습니다. 본인(이름 또는 연락처 정보 포함) 또는 다른 당사자에 대한 개인 정보를 AI Assistant에 제공하지 마십시오.

## 다음 단계

AI Assistant에 대한 일반적인 이해로 워크플로우 동안 AI Assistant를 활성화하고 사용하십시오. 자세한 내용은 다음 설명서를 참조하십시오.

* [AI Assistant 액세스 활성화](./enable-ai-assistant-access.md)
* [질문 지침](./question-guidance.md)
* [AI 어시스턴트 사용](./use-ai-assistant.md)
