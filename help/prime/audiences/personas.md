---
title: 파생 가상 사용자
description: Journey Optimizer B2B Prime에서 파생된 가상 사용자를 사용하여 사용자 목록 및 여정 경로를 타깃팅합니다. 기본 담당자 매핑 및 파생된 담당자 필터에 대해 알아봅니다.
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
autotag-review: '2026-06-23T22:01:21.605Z'
TQID: 'https://experienceleague.adobe.com/OZ4GDkaqg9a5Aikic-m-f0MtHSpc3BO0h41fTAL1Rww'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c3d6e661-d372-4e98-9fd9-eac771e7e4ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6ba70fe8d56bc35829649948c89356327042bf3f
workflow-type: tm+mt
source-wordcount: 650
ht-degree: 2%

---

# 파생 가상 사용자

개인 분류는 원시 고객 데이터를 AI가 컨텍스트를 생성하고 모든 채널 및 여정에서 개인화된 결정을 내리는 데 사용할 수 있는 의미론적 구매자 이해로 변환합니다. 이 통합 프로필은 다음 기능을 제공합니다.

* _여정 분기_ - 개인, 참여 깊이 및 역할별로 경로 분할
* _여정 중재_ - 동시 프로그램 간 메시지 충돌을 피하여 현재 어떤 육성 리드가 속해 있는지 결정합니다.
* _콘텐츠 개인화_ - 역할별 설명(&quot;경영진&quot;과 &quot;실무자&quot;용) 콘텐츠
* _영업 한정자 컨텍스트_ - BDR은 &quot;이 사람이 누구이며, 어떤 점에 관심이 있으며, 구매자 여정에서 어디에 있는지&quot;를 보여주는 한 화면 간단한 설명을 받습니다.

## 기본 가상 사용자 {#default-ersonas}

Journey Optimizer B2B Prime의 Beta 릴리스의 경우 직책 속성에 따라 다음과 같은 기본 가상 사용자가 정의됩니다.

| 담당자 | 직함 |
| ------- | ---------- |
| [!UICONTROL CXO / EVP] | CEO, CIO, CTO, CMO, CFO, 전략 담당 수석 부사장 |
| [!UICONTROL SVP/VP] | 마케팅 담당 SVP, 영업 담당 VP, 운영 담당 SVP, 제품 담당 VP, IT 담당 VP |
| [!UICONTROL 선임 관리자/관리자] | 수석 마케팅 관리자, IT 관리자, 운영 관리자, 영업 관리자, HR 관리자 |
| [!UICONTROL 개별 참여자] | 고객 담당자, 소프트웨어 엔지니어, 마케팅 전문가, 고객 성공 담당자 |
| [!UICONTROL 분석가] | 비즈니스 분석가, 데이터 분석가, 시장 조사 분석가, 재무 분석가, 운영 분석가 |
| [!UICONTROL Developer] | 프론트엔드 개발자, 백엔드 개발자, 전체 스택 개발자, 모바일 앱 개발자, DevOps 엔지니어 |
| [!UICONTROL 전문 직원] | HR 전문가, 법률 자문, 규정 준수 책임자, 프로젝트 관리자, 조달 전문가 |
| [!UICONTROL 컨설턴트] | 관리 컨설턴트, IT 컨설턴트, 비즈니스 프로세스 컨설턴트, 마케팅 컨설턴트 |
| [!UICONTROL 기타] | 산업 전문가, 독립 고문, 프리랜서 컨설턴트, 주제전문가 |

>[!NOTE]
>
>일반 가용성 릴리스에서는 조직의 필요에 따라 이러한 기본 가상 사용자를 편집할 수 있습니다. 또한 사용자 정의 사용자 정의 정의 및 매핑을 지원합니다.

## 파생 성향으로 필터링 {#derived-persona-filter}

Journey Optimizer B2B Prime은 정의된 담당자에게 레코드의 속성을 평가하여 각 개인 레코드에 대한 담당자를 파생합니다. 사용자 목록에 대한 대상자를 정의하거나 사용자 여정에서 세그먼트화할 때 추론된 결과(_파생된 사용자_)를 필터로 사용할 수 있습니다.

_[!UICONTROL 파생 사용자]_ 필터는 **[!UICONTROL 개인 특성]** 범주 아래의 필터 패널에 표시됩니다.

### 사용자 목록 {#people-lists}

[정적 사용자 목록](./people-lists.md#static-list)에서 구성원을 추가하거나 제거할 때 또는 [동적 사용자 목록](./people-lists.md#dynamic-lists)에 대한 구성원 규칙을 정의할 때, 파생된 성향별로 필터링하여 특성이 구성된 특정 성향과 일치하는 모든 사람을 대상으로 할 수 있습니다.

![사람 목록에 대해 파생된 사용자 필터링](./assets/derived-persona-filter-people-list.png){width="700" zoomable="yes"}

**정적 목록 — 구성원 추가**

1. 정적 목록을 열고 오른쪽 상단에서 **[!UICONTROL 사람 추가]**&#x200B;를 클릭합니다.

1. 필터 대화 상자에서 **[!UICONTROL 사람 특성]**&#x200B;을 확장하고 **[!UICONTROL 파생 사용자]**&#x200B;를 캔버스로 드래그합니다.

1. 필터 조건에서 **[!UICONTROL is]**&#x200B;을(를) 선택하고 목록에서 가상 사용자를 하나 이상 선택합니다.

1. 필터를 적용하고 일치하는 사람을 목록에 추가하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하십시오.

**동적 목록 — 구성원 규칙을 설정합니다**

1. 동적 목록을 열고 **[!UICONTROL 규칙]** 탭을 선택합니다.

1. **[!UICONTROL 규칙 편집]**&#x200B;을 클릭합니다.

1. 필터 대화 상자에서 **[!UICONTROL 사람 특성]**&#x200B;을 확장하고 **[!UICONTROL 파생 사용자]**&#x200B;를 캔버스로 드래그합니다.

1. 필터 조건에서 **[!UICONTROL is]**&#x200B;을(를) 선택하고 목록에서 가상 사용자를 하나 이상 선택합니다.

1. 규칙을 저장하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하십시오.

   개인 레코드가 규칙에 대해 평가되면 멤버십이 자동으로 업데이트됩니다.

### 개인 여정 {#person-journeys}

[_분할 경로_ 여정](../marketing/split-merge-paths-nodes.md)에서 개인 여정에 대한 세분화를 구성할 때 파생된 담당자를 개인 프로필 필터로 사용하여 경로를 입력하는 사용자를 제어할 수 있습니다.

![분할 경로 조건에 대해 파생된 사용자 필터링](./assets/derived-persona-filter-split-path.png){width="700" zoomable="yes"}

1. 여정 캔버스에서 **[!UICONTROL 경로 분할]** 노드를 클릭합니다.

1. 오른쪽의 노드 속성 패널에서 경로에 대해 **[!UICONTROL 조건 적용]** 또는 **[!UICONTROL 조건 편집]**&#x200B;을 클릭합니다.

1. 필터 대화 상자에서 **[!UICONTROL 사람 특성]**&#x200B;을 확장하고 **[!UICONTROL 파생 사용자]**&#x200B;를 캔버스로 드래그합니다.

1. 필터 조건에서 **[!UICONTROL is]**&#x200B;을(를) 선택하고 목록에서 가상 사용자를 하나 이상 선택합니다.

1. **[!UICONTROL 완료]**&#x200B;를 클릭하여 경로에 대한 필터를 저장합니다.
