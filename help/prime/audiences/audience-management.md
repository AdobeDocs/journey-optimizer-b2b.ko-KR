---
title: 고객 관리
description: 대상자를 위한 자리 표시자 페이지입니다.
source-git-commit: 6d91218d904406a7b398e3e998fde47e8d670fee
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 4%

---

# 대상자 관리

대상은 AJO B2B Prime에서 어떻게 재생됩니까?

마케팅 관리 허브에서 오른쪽 탐색에 있는 **[!UICONTROL 사람 목록]**&#x200B;을 클릭합니다.

![대상자 목록을 관리하도록 액세스](./assets/people-lists.png){width="800" zoomable="yes"}

**[!UICONTROL 동적 목록]** 및 **[!UICONTROL 정적 목록]**&#x200B;을 보고 관리할 수 있는 두 가지 탭이 있습니다. 탭을 클릭하여 각 유형 간에 목록 보기를 전환합니다.

이 페이지에서 다음 작업을 수행할 수 있습니다.

* 새 동적 및 정적 목록 만들기
* 기존 목록 검색
* 에셋 정보 보기
* 목록에 액세스하여 멤버십 검토

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across AJO B2B. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## 사람 목록 만들기


새 동적 또는 정적 목록을 만들려면 다음 작업을 수행하십시오.

1. _[!UICONTROL 사람 목록]_ 페이지의 오른쪽 상단에 있는 **목록 만들기**&#x200B;를 클릭합니다.
1. 목록의 **[!UICONTROL 상위]**(으)로 프로그램을 선택하십시오.
1. **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]** 목록을 입력하십시오(선택 사항).
1. **[!UICONTROL Type]**&#x200B;을(를) 나열하려면 선택하십시오.

   * **[!UICONTROL 정적]** - 구성원 자격은 목록을 만들 때 평가되는 자격 부여 필터에 의해 결정됩니다. 수동으로 레코드를 한정하거나 한정하지 않으면 목록 멤버십이 업데이트되지 않습니다.
***[!UICONTROL Dynamic]** - 멤버십은 자격을 갖춘 필터에 의해 동적으로 결정됩니다. 목록 멤버십이 자동으로 새로 고쳐집니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

>[!NOTE]
>
>이 Beta 릴리스의 사용자 목록에 대해서는 현재 삭제 및 중복이 지원되지 않습니다.

## 정적 목록

정적 목록 멤버십은 사용자 특성 및 활동을 참조하는 간단한 필터로 정의됩니다. 구성원이 자격을 수동으로 부여하거나 자격을 박탈하지 않는 한 멤버십은 변경되지 않습니다.

### 구성원 추가

1. 정적 목록을 열고 오른쪽 상단에서 **[!UICONTROL 사람 추가]**&#x200B;를 클릭합니다.

1. 대화 상자에서 왼쪽에서 필터를 드래그 앤 드롭하여 잠재 고객을 선별하는 규칙을 정의합니다.

   다음을 조합하여 사람을 필터링할 수 있습니다.

   * 활동 기록
   * 회사 속성
   * 개인 속성
   * 여정 멤버십과 같은 특수 필터

1. 변경 내용을 저장하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하세요.

1. **[!UICONTROL 구성원]** 탭을 선택합니다.

   잠시 후 자격을 갖춘 멤버가 목록에 나타납니다.

### 멤버 제거

1. 정적 목록을 열고 오른쪽 상단에서 **[!UICONTROL 사람 제거]**&#x200B;를 클릭합니다.

1. 대화 상자에서 자격을 취소할 멤버에 해당하는 필터를 추가합니다.

1. 변경 내용을 저장하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하세요.

1. **[!UICONTROL 구성원]** 탭을 선택합니다.

   짧은 시간이 지나면 실격된 구성원들이 명단에서 빠집니다.

## 동적 목록

동적 목록 멤버십은 사용자 특성 및 활동을 참조하는 간단한 필터를 사용하여 정의됩니다. 필터 논리에 따라 자격 및 자격 취소 리드에 의해 멤버십이 자동으로 유지됩니다.

### 멤버십 논리 정의

1. 정적 목록을 열고 규칙 탭을 선택합니다.

1. 규칙 편집을 클릭합니다.

1. 대화 상자에서 왼쪽에서 필터를 드래그 앤 드롭하여 잠재 고객을 선별하는 규칙을 정의합니다.

   다음 조합을 사용하여 목록에 대한 잠재 고객을 우량으로 선별할 수 있습니다.

   * 활동 기록
   * 회사 속성
   * 개인 속성
   * 여정 멤버십과 같은 특수 필터

1. 변경 내용을 저장하려면 **[!UICONTROL 완료]**&#x200B;를 클릭하세요.

1. **[!UICONTROL 구성원]** 탭을 선택합니다.

   잠시 후 자격을 갖춘 멤버가 목록에 나타납니다.

요약 및 최근 활동을 볼 수 있는 가망 고객 프로필 세부 정보 페이지를 열려면 목록에서 개인명을 누릅니다.