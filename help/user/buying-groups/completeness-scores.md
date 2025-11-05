---
title: 구매 그룹에 대한 완성도 점수
description: Journey Optimizer B2B edition의 역할 기반 임계값, 사용자 정의 가능한 멤버 요구 사항 및 완전성 설정을 사용하여 구매 그룹 완전성 점수를 계산합니다.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 3%

---


# 완성도 점수 {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="완성도 점수"
>abstract="완전성 점수는 구매 그룹 멤버십이 판매 준비가 된 구매 그룹에 대해 얼마나 잘 일치하는지를 반영합니다."

완전성 점수는 정의된 역할에서 구매 그룹이 필수 구성원으로 얼마나 잘 채워지는지를 나타내는 백분율입니다. 이러한 점수는 역할 템플릿에서 구성한 역할 멤버 임계값과 구매 그룹의 각 역할에 할당된 실제 멤버 수를 기반으로 합니다. 결과 점수는 마케터가 판매 준비도를 평가하고 구매 그룹 구성의 차이를 식별하는 데 도움이 됩니다. 구매 그룹 멤버십이 변경될 때 자동으로 점수 계산이 발생합니다.

![그룹 완성도 점수를 구입하는 중](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

완성도 점수에는 두 가지 유형이 있습니다.

* **구매 그룹 완전성 점수** - 구매 그룹 완전성 점수는 0%에서 100% 사이의 백분율이며 역할 수준 완전성 계산에 따라 구매 그룹의 전체 완전성을 나타냅니다.

  구매 그룹 완성도 점수가 [구매 그룹 세부 정보](./buying-group-details.md) 페이지에 표시됩니다. 이 점수는 구매 그룹에 판매 참여를 위한 필수 이해 관계자가 있는지 한 눈에 볼 수 있는 보기를 제공합니다.

* **역할 완성도 점수** - 역할 완성도 점수는 해당 역할에 할당된 구성원 수를 기준으로 한 구매 그룹 내의 각 개별 역할에 대한 백분율입니다.

  역할을 편집하고 완결성 설정을 조정하면 구매 그룹 상세내역 페이지에 각 역할에 대한 역할 완결성 점수가 표시됩니다. 이러한 점수를 통해 판매 준비 임계값에 도달하기 위해 추가 구성원이 필요한 특정 역할을 식별할 수 있습니다.

  세부 정보 페이지에는 추가 역할에 대한 n_+ 링크가 있는 처음 두 개의 역할 완성도 점수가 표시됩니다. 링크를 클릭하여 추가 역할 완성도 점수를 확인합니다.

완전성 점수는 구매 그룹 멤버십의 현재 상태를 반영하며 멤버가 추가되거나 삭제되면 자동으로 업데이트됩니다. 표시된 점수는 전체 백분율로 표시됩니다(예: 66.67%의 점수가 67%로 표시됨).

## 영업 준비 상태 평가

Adobe Journey Optimizer B2B edition은 마케터에게 구매 그룹이 실제 의사 결정 프로세스에 맞게 조정되도록 하는 도구를 제공합니다. 조직의 영업 방식을 반영하는 사용자 정의 가능한 역할 구성원 임계값을 사용하여 전체 구매 그룹을 정의할 수 있습니다. 각 역할에 대해 최소 및 최대 구성원 요구 사항을 설정하여 판매 준비 구매 그룹을 구성하는 항목에 대한 명확한 기준을 설정합니다.

구매 그룹 완결성 점수는 그룹에 대한 판매 준비도를 정확하게 측정합니다. 예를 들어 특정 솔루션에 대한 기회를 완료하려면 최소 두 명의 의사 결정권자, 한 명의 영향력 행사자, 그리고 최소 한 명의 전문가가 필요할 수 있습니다. 완결성 점수 계산은 이러한 역할별 요구 사항 각각을 계산하며 전체 구매 그룹 준비에 대한 보기를 제공합니다.

## 여정 효율성 측정

구매 그룹 완전성은 여정 효과에 대한 핵심적인 성과 지표(KPI) 역할을 한다. 특정 여정의 목표는 판매 준비 경고를 트리거하기 전에 구매 그룹 완전성을 특정 퍼센트만큼 늘리거나 최소 임계값을 달성하는 것입니다.

대기업에서는 역할당 한 명을 식별할 수 있습니다. 단, 해당 영업 담당자는 영업 담당자에 적합하지 않거나 중요한 역할의 여러 담당자가 필요할 수 있습니다. 예를 들어, 대규모 조직에는 여러 부서나 사업부에 분산된 여러 IT(정보 기술) 의사 결정자가 있을 수 있습니다. 하나의 의사 결정자를 식별하는 것만으로는 복잡한 기업 판매를 위해 충분하지 않을 수 있습니다.

현재 구매 그룹 완성도를 분석한 후 역할 템플릿의 각 역할에 대해 필요한 연락처 수를 조정할 수 있습니다. 이러한 조정을 통해 실제 패턴 및 판매 결과에 따라 구매 그룹 전략을 조정할 수 있습니다.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## 역할 완성도 계산 {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="역할 완성도 계산"
>abstract="역할 완성도 점수는 역할에 할당된 멤버 수를 기반으로 백분율로 계산됩니다."

Journey Optimizer B2B edition은 각 개별 구매 그룹 역할에 대한 완성도 점수를 백분율로 계산합니다. 이 점수는 완료에 필요한 [역할 템플릿에 필요한 수](./buying-groups-role-templates.md#change-the-completeness-score-settings)와(과) 비교하여 역할에 할당된 구성원 수를 기반으로 합니다.

역할 완전성 계산은 0과 지정된 임계값(필수 멤버) 사이의 선형 백분율입니다.

* 할당된 구성원 수가 **0**&#x200B;인 경우 역할 완성도는 **0%**&#x200B;입니다.
* 할당된 구성원 수가 **임계값 이상**&#x200B;인 경우 역할 완성도는 **100%**&#x200B;입니다.
* 할당된 구성원 수가 **과(와) 임계값 사이**&#x200B;인 경우 완전성이 비례적으로 계산됩니다.

### 역할 완전성 공식

역할 완전성 비율은 다음 공식을 사용하여 계산됩니다.

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

위치:

* `Assigned Members` = 역할의 현재 구성원 수
* `Threshold` = 역할 템플릿에 설정된 멤버 필수 값

### 역할 완성도 예

다음 예는 서로 다른 임계값 구성을 사용하는 역할 완전성 계산을 보여 줍니다.

| 역할 | 멤버 필요 | 할당된 구성원 | 계산 | 역할 완성도 |
|------|------------------|------------------|-------------|-------------------|
| 의사 결정자 | 3 | 0 | None | 0% |
|  |  | 1 | 1/3 × 100 | 33% |
|  |  | 2 | 2/3 × 100 | 66% |
|  |  | 3 | 임계값 | 100% |
|  |  | 4 | 임계값 초과 | 100% |
| 영향력 있는 사용자 | 5 | 0 | None | 0% |
|  |   | 1 | 1/5 × 100 | 20% |
|  |   | 2 | 2/5 × 100 | 40% |
|  |   | 3 | 3/5 × 100 | 60% |
|  |   | 4 | 4/5 × 100 | 80% |
|  |   | 5 | 임계값 | 100% |
|  |   | 6 | 임계값 초과 | 100% |

## 구매 그룹 완전성 계산 {#buying-group-completeness-calculation}

구매 그룹 완성도 점수는 개별 역할 완성도 점수를 집계합니다. 이 계산은 정의된 모든 역할에 대해 구매 그룹 준비에 대한 전체적인 뷰를 제공합니다.

### 구매 그룹 완전성 공식

구매 그룹 완전성 퍼센트는 다음 공식을 사용하여 계산됩니다.

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

위치:

* `Role Completeness %` = 개별 역할 완전성 백분율(0-100%)
* `Σ` = 구매 그룹의 모든 역할에 대한 합계

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->