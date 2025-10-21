---
title: 사용자 매핑
description: 개인 속성을 매핑하여 구매 그룹을 위한 간소화된 역할 템플릿을 만들어 계정 기반 마케팅을 위한 담당자를 구성하는 방법에 대해 알아봅니다.
feature: Setup, Buying Groups
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
role: Admin
source-git-commit: e301dfd5ac1421eb73e80b1d772d1b17f9ef3a1e
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# 사용자 매핑

성향은 마케터가 목표 계정 내에서 개인의 특정 요구 사항, 선호도 및 해결 과제에 맞게 전략을 조정할 수 있도록 돕기 때문에 계정 기반 마케팅(ABM) 접근법의 핵심 측면입니다. 마케터는 배경, 책임, 불만 사항 및 선호하는 커뮤니케이션 채널을 포함하여 각 담당자에 대한 세부 프로필을 만들 수 있습니다. 이러한 정의를 통해 관리자는 Journey Optimizer B2B edition의 개인 속성에 따라 가상 사용자를 구성할 수 있으므로 역할 템플릿은 이러한 가상 사용자를 캡처하는 간소화되고 일관된 역할 조건을 사용할 수 있습니다.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
사용자 정의 및 사용 제한 사항:

* _[!UICONTROL 사용자 매핑]_ 목록에 최대 20개의 사용자를 정의할 수 있습니다.
* 각 담당자는 정의에 최대 5개의 특성을 포함할 수 있습니다.
* 정의된 모든 가상 사용자에서 최대 10개의 다른 개인 속성을 사용할 수 있습니다.

>[!BEGINSHADEBOX]

**사용 사례: 직책 변형**

많은 마케팅 및 영업 팀은 계정 내에서 서로 다른 담당자를 식별하는 방법으로 직함을 사용합니다. 그러나 연락처의 제목은 일관되지 않을 수 있으며 유사한 역할에 수많은 변형을 사용할 수 있습니다. 구매 그룹 역할 템플릿을 작성할 때 주어진 역할에 대해 가능한 모든 관련 직책을 정의해야 할 수 있습니다. 이러한 정의를 단순화하고 유사한 직책을 가진 사람들을 하나의 유추된 성향으로 데려올 수 있으며, 그런 다음 구매 그룹을 위해 다양한 역할 템플리트에 활용할 수 있습니다.

예를 들어, _제품 관리_&#x200B;라는 담당자를 구성하고 _제품 관리자_, _Sr 값에 대한 직책 특성을 사용하여 정의할 수 있습니다. 제품 관리자_, _고급 제품 관리자_, _오후_, _Sr. PM_, _사용자 PM_ 및 _사용자 제품 관리자_. 그런 다음 조건이 _제품 관리_&#x200B;와 일치하는 역할 템플릿에서 이 담당자를 사용합니다. 구성된 담당자를 사용하면 각 역할 템플릿을 간편하게 만들 수 있으며, 가능한 모든 직책에 대해 일치할 수 있는 복잡한 조건을 필요로 하지 않습니다.

>[!ENDSHADEBOX]

## 구성된 가상 사용자에 액세스

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 구성]**&#x200B;을 선택합니다.

1. 중간 패널에서 **[!UICONTROL 담당자 매핑]**&#x200B;을 클릭하여 담당자 목록을 표시합니다.

   ![구성된 가상 사용자에 액세스](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   이 페이지에서 [만들기](#create-an-engagement-score-model), [편집](#change-the-engagement-weighting-settings) 또는 [삭제](#delete-a-persona)할 수 있습니다.

   사용자 매핑 목록입니다. 은(는) 표로 구성되며 맨 위에 가장 최근에 업데이트된 가상 사용자를 표시합니다(_[!UICONTROL 마지막 업데이트]_&#x200B;별로 정렬됨). 오른쪽 상단의 _열 설정_( ![열 설정](../assets/do-not-localize/icon-column-settings.svg) ) 아이콘을 클릭하고 열 확인란을 선택하거나 선택을 취소하여 표시된 테이블을 사용자 지정할 수 있습니다.

![사용자 매핑 목록에 표시할 열](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. 담당자의 세부 정보에 액세스하려면 이름을 클릭합니다.

### 기본 가상 사용자

_담당자 매핑_ 목록에는 작업 제목 특성에 따라 정의된 5개의 기본 담당자가 포함되어 있습니다. 조직의 필요에 따라 이러한 기본 가상 사용자를 편집할 수 있습니다.

| 담당자 | 직함 |
| ------- | ---------- |
| CXO / EVP - CXO / 수석 부사장 | CEO, CIO, CTO, CMO, CFO, 전략 담당 수석 부사장 |
| SVP/VP - 수석 부사장/부사장 | 마케팅 담당 SVP, 영업 담당 VP, 운영 담당 SVP, 제품 담당 VP, IT 담당 VP |
| 선임 이사 / 이사 - 선임 이사 / 이사 | 엔지니어링 이사, 제품 담당 수석 이사, 재무 이사, 고객 성공 이사 |
| 선임 관리자/관리자 - 선임 관리자/관리자 | 수석 마케팅 관리자, IT 관리자, 운영 관리자, 영업 관리자, HR 관리자 |
| 개별 참여자 - 개별 참여자 | 고객 담당자, 소프트웨어 엔지니어, 마케팅 전문가, 고객 성공 담당자 |
| 분석가 - 분석가 | 비즈니스 분석가, 데이터 분석가, 시장 조사 분석가, 재무 분석가, 운영 분석가 |
| 개발자 - 개발자 | 프론트엔드 개발자, 백엔드 개발자, 전체 스택 개발자, 모바일 앱 개발자, DevOps 엔지니어 |
| 전문 직원 - 전문 직원 | HR 전문가, 법률 자문, 규정 준수 책임자, 프로젝트 관리자, 조달 전문가 |
| 컨설턴트 - 컨설턴트 | 관리 컨설턴트, IT 컨설턴트, 비즈니스 프로세스 컨설턴트, 마케팅 컨설턴트 |
| 기타 - 기타 | 산업 전문가, 독립 고문, 프리랜서 컨설턴트, 주제전문가 |

### 목록 필터링

원하는 담당자를 찾으려면 검색 및 필터 도구를 사용합니다.

* 이름별로 성향을 일치시키려면 검색 창에 텍스트 문자열을 입력합니다.

  ![표시된 이벤트 정의를 필터링합니다](./assets/configuration-events-defs-list-filtered.png){width="700" zoomable="yes"}

* 다음 특성을 사용하여 표시된 목록을 필터링하려면 왼쪽 상단의 _필터_( ![필터 아이콘](../assets/do-not-localize/icon-filter.svg)) 아이콘을 클릭하십시오.

   * ?
   * ?

## 사용자 만들기

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 구성]**&#x200B;을 선택합니다.

1. 중간 패널에서 **[!UICONTROL 사용자 매핑]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 사용자 만들기]**&#x200B;를 클릭합니다.

1. 담당자의 고유한 **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

1. 성향 일치에 사용할 특성을 선택합니다.

   * **[!UICONTROL 사용자 특성 선택]**&#x200B;을 클릭합니다.

   * _[!UICONTROL 개인 특성 선택]_ 대화 상자에서 매핑할 각 특성(최대 5개)에 대한 확인란을 선택합니다.

     오른쪽 상단의 _열 설정_( ![열 설정](../assets/do-not-localize/icon-column-settings.svg) ) 아이콘을 클릭하여 표시된 테이블을 사용자 지정할 수 있습니다.

     이름별로 속성 목록을 필터링하려면 검색 막대에 텍스트 문자열을 입력합니다. 왼쪽 상단의 _필터_( ![필터 아이콘](../assets/do-not-localize/icon-filter.svg)) 아이콘을 클릭하여 표시된 목록을 유형, _표준_ 또는 _사용자 지정_&#x200B;별로 필터링할 수도 있습니다.

   * **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

     선택한 특성은 _[!UICONTROL 사용자 특성]_ 섹션에 채워집니다.

1. 각 속성에 대해 속성에 대해 일치시킬 쉼표로 구분된 값을 입력합니다.

   값 대신 일치 항목을 식별하는 데 사용할 수 있는 프롬프트를 추가할 수도 있습니다. 예를 들어 다음을 입력할 수 있습니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

## 사용자 편집

1. 담당자의 세부 정보에 액세스하려면 이름을 클릭합니다.


## 사용자 삭제

담당자를 삭제하면 _담당자 매핑_ 목록에서 담당자가 제거되며 더 이상 역할 템플릿에서 사용할 수 없습니다.

1. _[!UICONTROL 사용자 매핑]_ 페이지에서 삭제할 사용자를 찾습니다.

1. 이름 옆에 있는 의 줄임표(**...**) 아이콘을 클릭하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.

1. 확인 대화 상자에서 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.
