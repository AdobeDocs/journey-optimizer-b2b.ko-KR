---
title: B2B 계정 및 사람에 대한 대상 기술
description: B2B 계정 및 피플에 대한 대상 기술에 대해 알아봅니다. 제품 의도를 탐색하고, 가상 사용자를 식별하고, 역할 범위를 평가하고, 구매 그룹 템플릿을 만듭니다.
feature: Agentic AI, Audiences
role: User
exl-id: c1210912-66ba-4b5f-8f3b-96eb6280c926
autotag-review: '2026-06-05T16:43:42.459Z'
TQID: 'https://experienceleague.adobe.com/d7KMYbH0NpoYGnBdTCmCpzLgpGIYfNP-YIFCQUjZpIg'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: afadf741-c5fe-42cd-8013-23bb6ff2d1bc
    internal-label: Buying Groups
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: bef5003b-cad2-4f40-bdb2-a80426d52ef5
    internal-label: AI Assistant
subfeature_v2:
  - id: ff10f619-348f-47e3-99bf-3ce4c817cf2c
    internal-label: Agentic AI
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
    internal-label: Taxonomy
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 1%
---
# B2B 계정 및 사용자를 위한 대상 기술

[!DNL CX Coworker] 인터페이스에서 B2B에 대상 기술을 사용하십시오. 계정 및 사용자 간의 제품 의도를 탐색합니다. 관련 담당자를 식별하고, 구매 그룹 범위를 평가하고, 구매 그룹 역할 템플릿을 만듭니다.

* 특정 제품에 대한 고객의 관심을 평가하고 의도 트렌드를 비교합니다.
* 제품 관심사와 관련된 사용자 및 가상 사용자를 식별합니다.
* 구매 그룹 역할을 검토하고 적용 범위 차이를 식별합니다.
* 구매 그룹 역할 템플릿을 생성하고 구체화합니다.

>[!PREREQUISITES]
>
>B2B 계정 및 사용자에 대해 대상 기술을 사용하기 전에 다음 데이터 정의 및 매핑을 구성합니다.
>
>* [의도 데이터 분류 및 매핑](../admin/intent-data.md)
>* [XDM 필드 매핑](#xdm-data-prerequisites)

[!DNL Coworker] 응용 프로그램을 열려면 응용 프로그램 상단의 _묻기[!DNL Coworker]_( ![묻기 [!DNL Coworker]](../assets/do-not-localize/icon-ask-coworker.svg)) 아이콘을 클릭합니다. 채팅 인터페이스에 자연어 프롬프트를 입력하십시오.

[!DNL CX Coworker]![&#128279;](./assets/audience-skills-prompt.png){width="800" zoomable="yes"}의 대상 프롬프트

## 대상자 스킬 포커스 영역

대상자 스킬 포커스 영역을 사용하여 계정 의도를 탐색하고, 사람 및 가상 사용자를 이해하고, 그룹 템플릿 구매를 준비합니다.

| 포커스 | 작업 |
| ----- | ----- |
| 계정 의도 | 낮음, 중간, 높음 의도 수준을 사용하여 특정 제품에 대한 계정 의도를 평가합니다. 시간 경과에 따른 제품 관심 트렌드를 비교하고 특정 제품에 관심을 보이는 계정을 식별합니다. 사용자 범위와 함께 참여 패턴을 검토합니다. |
| 사람 및 가상 사용자 | 하나 이상의 제품에서 제품 의도에 따라 가상 사용자를 식별하고 등급을 지정합니다. 승률, 멤버십 비율 및 카운트를 포함한 영업 기회 지표를 검토합니다. 가상 사용자를 _챔피언_, _의사 결정자_, _영향력 있는 사용자_ 등의 역할에 매핑하고 역할 할당에 대한 설명을 검토하십시오. |
| 구매 그룹 범위 | 거래처 간 구매 그룹 규모 및 개인 범위를 평가합니다. 역할 배포를 검토하고 누락된 담당자 또는 역할을 식별합니다. 최근 거래에서 식별된 챔피언의 계정을 찾습니다. |
| 구매 그룹 템플릿 | 특정 제품에 대한 구매 그룹 역할 템플릿을 생성하고 권장 사용자 매핑을 검토하십시오. 가상 사용자 및 역할을 포함하거나 제외하여 템플릿을 구체화합니다. 구매 그룹을 만들기 전에 필요한 역할을 확인하십시오. |

## 제한 사항

Audience Insights는 구성된 의도 분류법, XDM 필드 매핑 및 경험 이벤트 데이터에 따라 다릅니다. 불완전한 영업 기회 데이터, 누락되었거나 오래된 분류법 또는 누락된 프로필 및 계정 식별자로 인해 insight 신뢰성이 저하될 수 있습니다.

의도 계산에서는 `directMarketing.emailClicked`, `directMarketing.emailOpened`, `directMarketing.emailUnsubscribed` 및 `web.webpagedetails.pageViews` 경험 이벤트만 사용합니다.

## 프롬프트 예제

[!DNL CX Coworker] 인터페이스에 다음 프롬프트를 입력하여 계정 의도를 탐색하고, 사람 및 가상 사용자를 이해하고, 그룹 템플릿 구매를 준비하십시오.

### 계정 의도

제품에 대한 계정 관심도를 살펴보고 의도 변경 사항을 검토하십시오.

* 제품당 계정 제품 의도에 대한 가장 빠른 업데이트 및 최신 업데이트와 같은 트렌드 창을 표시합니다.
* 제품에 대한 의도는 낮지만 여전히 열려 있는(육성할 가치가 있는) 계정은 무엇입니까?
* 이번 주에 `<account_name>`에 대해 기록된 새로운 의도 신호는 무엇입니까?

### 사람 및 가상 사용자

제품 관심사와 관련된 담당자를 식별하고 권장 구매 그룹 역할을 검토하십시오.

* `<product>`과(와) 관련된 가상 사용자를 표시합니다.
* `<product>`에 대한 역할-사용자 매핑 추천을 표시합니다.
* `<product>`의 경우 영업 기회 지표(성공률, 멤버십 비율, 카운트)와 함께 가상 사용자 및 역할을 나열합니다.

### 구매 그룹 및 템플릿

구매 그룹 의도 및 적용 범위를 검토한 다음 템플릿을 생성하거나 세분화합니다.

* `<product>`의 경우 제품 의도와 점수가 있는 구매 그룹을 나열합니다.
* `<industry>`에 있는 계정의 경우 `<product>`의 평균 계정 사용자 적용 범위는 얼마입니까?
* `<product>`에 대한 구매 그룹 템플릿을 만듭니다.
* `<persona>` 사용자 없이 `<product>`의 구매 그룹 템플릿을 만들고 `<role>` 역할을 제거하십시오.

## 개념

이 개념을 사용하여 계정 의도, 사용자 등급 및 구매 그룹 추천을 해석합니다.

| 개념 | 설명 |
| ------- | ----------- |
| 대상 감지 | 계정 내 사람들 간의 자사 참여 신호를 분석하여 제품 관심사 및 관련 담당자를 식별합니다. 분석은 기회 종료 전의 활동을 포함하여 이전 18개월의 활동을 고려한다. 영업 기회 데이터가 불완전할 때 참여 패턴이 제품 의도를 나타낼 수 있지만, 데이터가 누락되면 insight 신뢰성이 저하될 수 있습니다. |
| 담당자 | 성향 은 정규화된 직책, 기능 및 연공서열에 따라 사람을 그룹화합니다. 의사 결정자, 영향력 있는 사용자 및 지원 역할을 포함하여 계정 내에서 누가 참여하는지를 이해하려면 가상 사용자를 사용하십시오. |
| 구매 그룹 역할 매핑 | 직책, 기능, 연공 순위 및 구성된 속성을 기반으로 가상 사용자를 제품별 구매 그룹 역할에 매핑합니다. 이러한 역할은 구매에 영향을 주거나 구매를 결정하는 계정 내 사용자를 나타냅니다. 범위를 검토하여 누락된 역할을 식별하십시오. |
| 사용자 등급에 대한 영업 기회 데이터 | 영업 기회 단계, 종료 날짜 및 영업 기회-제품 간 매핑은 각 제품에 대한 담당자 등급을 지원합니다. 기회 데이터가 불완전할 때 순위는 활동 양과 시간 감소를 사용하여 최근 활동에 더 많은 가중치를 부여합니다.<br/><br/>가능한 경우 제품 연결에서 제공된 또는 생성된 제품 간 매핑 테이블을 사용합니다. 그렇지 않으면 유사 항목 일치는 제품 기회를 연결합니다. 연결할 수 없는 경우 제품 의도는 영업 기회 종료 날짜 이전의 최근 활동에서 추론됩니다. 이러한 대체 방법은 불완전한 데이터의 신뢰성 제한을 없애지는 않습니다. |
| 영업 기회 분석 | 과거 영업 기회 분석은 세 가지 차원을 사용하여 구매 결과와 관련된 성향 패턴을 식별합니다.<ul><li>승률: 특정 사용자가 참여했을 때 기회가 이기는 빈도를 측정합니다. 더 높은 승률과 연관된 페르소나 패턴은 더 많은 가중치를 받습니다.</li><li>멤버십 비율: 특정 제품에 대한 기회에 개인이 표시되는 빈도를 측정합니다.</li><li>성향 영향: 성향이 존재하는지 여부를 넘어 성향 참여 또는 활동이 성패와 어떻게 상관되는지 측정합니다.</li></ul>이러한 신호는 계정 의도, 담당자 매핑 및 구매 그룹 추천을 알려줍니다. |
| 의도 | 인텐트는 웹 페이지 방문 또는 이메일 링크 클릭과 같은 참여를 통한 제품 관심을 나타냅니다. 제품 분류는 참여 활동을 키워드, 제품 및 제품 범주에 연결합니다. 참여 깊이 및 빈도는 각 키워드, 제품 또는 제품 카테고리에 대한 개별 의도 점수를 결정합니다.<br/><br/>점수는 관심 강도를 나타냅니다. 낮은 의도: `<=0.2`, Medium 의도: `0.2 < score <= 0.6`, 높은 의도: `0.6 < score <= 1`.<br/><br/>계정 의도를 파악하기 위해 동일한 계정의 사람들 간에 개별 의도 점수를 집계합니다. |
| 구매 그룹에 영향을 주는 역할 | 구매 그룹 역할은 구매 결정에 대한 다양한 기여를 나타냅니다. _의사 결정자_&#x200B;는 일반적으로 예산 승인을 제어합니다. _영향력 있는 사용자_ 셰이프 평가 및 권장 사항입니다. _챔피언_ 내부 합의를 만듭니다. _최종 사용자_&#x200B;가 제품 적합성을 확인합니다.<br/><br/>역할 할당 및 적용 범위를 검토하여 결정에 영향을 미치는 사람과 참여 간격이 남아 있는 위치를 파악합니다. |
| 사용자 또는 역할 범위 | 적용 범위는 예상 담당자 또는 역할이 계정 내에 최소 한 명의 담당자가 있는 수를 측정합니다. _N_&#x200B;개의 예상 담당자 또는 역할이 있는 제품의 경우 전체 적용 범위는 모든 _N_&#x200B;이(가) 표시됨을 의미합니다. 부분 적용은 일부가 누락되었음을 의미합니다. 범위를 사용하여 구매 그룹의 완전성을 평가하고 차이를 식별합니다. |

## XDM 데이터 사전 요구 사항

계정 의도 분석, 개인 식별 및 구매 그룹 역할 매핑을 지원하도록 다음 XDM 필드 매핑을 구성합니다.

### XDM 필드 매핑

<table>
  <tbody>
    <tr>
      <th>XDM 필드</th>
      <th>엔티티</th>
      <th>비즈니스 정의</th>
      <th>추가 세부 정보</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>프로필</span>
        </p>
      </td>
      <td>영업 기회, 이벤트 및 의도 데이터에 대한 조인에 사용되는 계정 식별자</td>
      <td rowspan="2">영업 기회 분석<br/>계정 탐색<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>프로필</span>
        </p>
      </td>
      <td>프로필 데이터에 이벤트 데이터를 포함하는 조인에 사용되는 개인 식별자</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.departments</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 프로필</span>
        </p>
      </td>
      <td>프로필/개인의 작업 부서</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>사용자 매핑</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 프로필</span>
        </p>
      </td>
      <td>사용자 계산에 사용된 프로필/사용자의 직함</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>person.name.firstName</span>
        </p>
      </td>
      <td>
        <p>
          <span >프로필</span>
        </p>
      </td>
      <td>쿼리와 일치하는 결과에 개인의 이름을 표시합니다.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 프로필</span>
        </p>
      </td>
      <td>쿼리와 일치하는 결과에 개인의 전체 이름을 표시합니다.</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.lastName</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 프로필</span>
        </p>
      </td>
      <td>사용자의 쿼리와 일치하는 결과에 사용자의 성을 표시합니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 계정</span>
        </p>
      </td>
      <td>영업 기회, 이벤트 및 의도 데이터에 대한 조인에 사용되는 계정 식별자</td>
      <td>영업 기회 분석<br/>계정 탐색</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountName</span>
        </p>
      </td>
      <td>
        <p>
          <span>계정</span>
        </p>
      </td>
      <td>쿼리와 일치하는 결과에 계정 이름을 표시합니다.</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>계정 탐색</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>계정</span>
        </p>
      </td>
      <td>쿼리를 기반으로 계정 설명에 의한 계정 필터링을 지원합니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 계정</span>
        </p>
      </td>
      <td>쿼리를 기반으로 산업별 계정 필터링을 지원합니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span>개 계정</span>
        </p>
      </td>
      <td>쿼리를 기반으로 청구 주소 영역별 계정 필터링을 지원합니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>영업 기회, 이벤트 및 의도 데이터에 대한 조인에 사용되는 계정 식별자</td>
      <td rowspan="2">
        <p>영업 기회 분석<br/>계정 탐색</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>계정 데이터에 대한 조인에 사용되는 영업 기회 식별자</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityName</span>
        </p>
      </td>
      <td>
        <p>
          <span>개의 영업 기회</span>
        </p>
      </td>
      <td>영업 기회 분석에 사용된 영업 기회 이름.</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>영업 기회 분석</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>영업 기회 성공 여부(바이너리)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>영업 기회 분석에 사용되는 영업 기회 설명.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityMount</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>영업 기회와 관련된 $ 금액</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>opportunityType</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>영업 기회 유형</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>opportunityStage</span>
        </p>
      </td>
      <td>
        <p>
          <span>개의 영업 기회</span>
        </p>
      </td>
      <td>영업 기회 단계(마감된 원화나 마감된 손실 또는 중간 단계) </td>
      <td rowspan="4">
        <p>영업 기회 분석<br/>계정 탐색</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>실제 종료 날짜</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>영업 기회의 실제 종료일</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>개의 영업 기회</span>
        </p>
      </td>
      <td>영업 기회의 예상 종료일</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>기회</span>
        </p>
      </td>
      <td>이 영업 기회의 생성일</td>
    </tr>
  </tbody>
</table>

### 분류 데이터

대상 기술은 [!DNL Adobe Journey Optimizer B2B Edition]의 자사 의도 데이터를 사용합니다. 의도 계산은 제품 분류법을 참여 활동과 연결하고 계정 수준에서 개별 점수를 집계합니다.

1. 의도 계산에는 고객 > 분류법의 분류 데이터(고객 제품 및 해당 키워드)가 필요합니다
1. 분류 데이터는 이벤트 데이터(자산 레이블 지정)에 레이블을 지정하는 데 사용됩니다. 이 데이터는 이벤트 데이터 > 자산 레이블 지정을 기반으로 방문자가 관심을 갖는 키워드 및 제품에 대한 인사이트를 제공합니다 
1. 레이블이 지정된 에셋(이벤트 데이터)은 방문자 행동(방문한 페이지 수)과 결합하여 키워드, 제품 및 제품 범주 수준에서 방문자 의도→ 의도 계산을 결정합니다
1. 방문자 프로필 수준의 의도 점수는 계정 수준에서 집계되어 주어진 키워드, 제품 및 제품 카테고리 > 의도 계정 집계에서 계정 의도를 파악합니다

[의도 분류법을 구성](../admin/intent-data.md)하는 것 외에 다음 필드가 필요합니다.

<table>
  <tbody>
    <tr>
      <th>XDM 필드</th>
      <th>엔티티</th>
      <th>비즈니스 정의</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>개인 프로필</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>프로필</span>
        </p>
      </td>
      <td>개인(이메일 또는 b2b_person) 식별자를 식별하는 데 도움이 됩니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>프로필</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>keyword_id</li>
          <li>keyword_name</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>자산에 레이블을 지정하는 분류법으로 사용됩니다(클릭한 이메일, 방문한 웹 페이지 등 경험 이벤트).</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>타임스탬프</span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>채우기 및 증분 실행을 가져오는 데 사용됩니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>이벤트 유형을 식별합니다. 의도 계산에서는 <code>directMarketing.emailClicked</code>, <code>directMarketing.emailOpened</code>, <code>directMarketing.emailUnsubscribed</code> 및 <code>web.webpagedetails.pageViews</code>만 사용합니다.
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/부기에만 해당, 캠페인 이름에 대한 정보</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/예약 기능만 해당; 이메일이 타겟팅된 소스 ID에 대한 정보</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/예약 기능만 해당, 이메일이 타겟팅된 소스 인스턴스 정보</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>[!DNL Adobe Marketo Engage] 데이터 센터에서 전자 메일 콘텐츠를 가져오는 데 사용됩니다. (SourceID@SourceInstanceID.SourceType)로 구성됩니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/부기용으로만 사용됩니다. 소스의 유형 또는 소스가 시작된 위치에 대한 정보 </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>웹 페이지 방문 원본 정보</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>콘텐츠 가져오기에 사용되는 실제 URL</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>타깃팅된 컨텐츠를 가져오는 데 사용되는 URL에 대한 추가 쿼리 매개 변수 </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/부기만을 위한 것</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/예약 기능만 해당; 이메일이 타겟팅된 소스 ID에 대한 정보</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>경험 이벤트</span>
        </p>
      </td>
      <td>참조/예약 기능만 해당, 이메일이 타겟팅된 소스 인스턴스에 대한 정보</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>경험 이벤트</span>
      </td>
      <td>참조/부기 전용이며 (SourceID@SourceInstanceID.SourceType)로 구성됩니다.</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>경험 이벤트</span>
      </td>
      <td>참조/부기용으로만 사용됩니다. 소스의 유형 또는 소스가 시작된 위치에 대한 정보</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>경험 이벤트</span>
      </td>
      <td>web.webPageDetails.name에 없는 경우 실제 URL을 가져오는 데 사용됩니다.</td>
    </tr>
  </tbody>
</table>
