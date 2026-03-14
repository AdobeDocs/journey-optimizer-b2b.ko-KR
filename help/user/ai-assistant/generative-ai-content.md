---
title: 콘텐츠용 생성형 AI
description: 모범 사례를 확인하는 등  [!DNL Journey Optimizer B2B Edition]에서 생성 AI를 사용하여 개인화된 전자 메일 및 랜딩 페이지를 만드는 방법을 알아봅니다.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
exl-id: 36baf7f9-2fff-4c33-bca0-7d43ec48e74a
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 7%

---

# 콘텐츠용 생성형 AI {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="AI 콘텐츠 생성"
>abstract="레이아웃을 만든 후에는 [!DNL Journey Optimizer B2B Edition]에서 생성형 AI 도구를 사용하여 콘텐츠를 개선시킬 수 있습니다. 이 기능은 설명 프롬프트에 따라 콘텐츠를 미세 조정하여 개인화 및 콘텐츠 개선 프로세스를 간소화합니다."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="참조 콘텐츠"
>abstract="_참조 콘텐츠_&#x200B;를 사용하여 [!DNL Journey Optimizer B2B Edition]에서 생성형 AI에 추가 컨텍스트를 제공하는 콘텐츠가 포함된 에셋 파일을 업로드하거나 이전에 업로드한 파일을 선택합니다. 이 옵션을 사용하면 생성된 콘텐츠의 품질과 관련성을 향상시키기 위해 필요한 모든 자료를 사용할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Adobe 생성형 AI 약관"
>abstract="이 기능의 이용에는 Adobe Experience Cloud 생성형 AI 사용자 가이드라인에 대한 계약이 적용됩니다. 이 기능을 통한 모든 출력 내용이 정확한지 검토하고 사용 사례에 적합한지 확인해 보시기 바랍니다."
>additional-url="https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe 생성형 AI 사용자 가이드라인"

Microsoft Azure OpenAI 및 Adobe Firefly에서 제공하는 [!DNL Adobe Journey Optimizer B2B Edition]의 콘텐츠에 대한 생성 AI는 텍스트 및 이미지에 대한 사전 예방적 콘텐츠 변형 제안을 제공합니다. 다양한 주요 제목과 이미지를 테스트하여 콘텐츠에 미치는 영향을 최적화합니다.

[!DNL Journey Optimizer B2B Edition]에서 콘텐츠를 만들 때 생성 AI 기능을 사용하여 Adobe의 생성 AI 기능을 활용하십시오. 이메일, SMS 메시지, 랜딩 페이지 등에 대한 개인화된 텍스트 및 시각화를 제작합니다. 전체 캠페인을 구축하거나 특정 자산을 세분화하는 경우 이러한 기능을 사용하면 귀중한 시간을 절약하면서 콘텐츠를 브랜드 지침에 원활하게 맞출 수 있습니다.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>[!DNL Journey Optimizer B2B Edition]에서 이러한 기능에 액세스하려면 _[!UICONTROL AI Assistant]_ > _[!UICONTROL 콘텐츠 생성]_ 권한이 있어야 합니다. 제품 관리자가 기능 권한을 부여하는 방법에 대한 자세한 내용은 [제품 권한에 대한 역할 편집](../admin/user-management.md#edit-roles-for-product-permissions)을 참조하십시오.

콘텐츠 생성을 위한 AI Assistant 도구는 다음 에셋 유형으로 지원됩니다.

* [이메일](../content/ai-assistant-emails.md)
* [!BADGE Beta] [랜딩 페이지](../content/ai-assistant-landing-pages.md)

## 일반 지침 및 제한 사항 {#general-guidelines-and-limitations}

생성 AI 기능의 사용은 [Adobe Experience Cloud 생성 AI 사용자 지침](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}의 적용을 받습니다. 미디어 생성을 위한 생성 AI 도구 사용에 대한 Adobe의 노력으로 Adobe은 [!DNL Firefly]에서 생성한 에셋을 포함하는 모든 콘텐츠 또는 프로젝트에 대해 [콘텐츠 자격 증명](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"}을(를) 다운로드하거나 내보낼 때 적용합니다.

[!DNL Journey Optimizer B2B Edition]의 콘텐츠에 생성 AI를 사용하는 방법에 대한 일반 지침을 검토하십시오.

* 생성 AI 모델이 정확하게 해석되도록 잘 정의된 프롬프트를 사용합니다. 제공하는 마케팅 목표 또는 프롬프트는 생성된 콘텐츠의 품질에 큰 영향을 줍니다.

* 정확한 브랜드 내 콘텐츠를 갖도록 콘텐츠 참조 파일을 업로드합니다. 그렇지 않으면 콘텐츠는 공개적으로 사용 가능한 정보를 기반으로 합니다. 업로드된 콘텐츠는 PDF, JPEG, PNG 또는 ZIP(지원되는 파일 형식 포함) 파일 형식일 수 있습니다. 업로드된 파일의 최대 크기는 50MB입니다. 파일이 크거나 이미지가 많으면 작동할 수 있지만, 이렇게 하면 처리 시간이 늘어납니다.

* 브랜드별 또는 사용자 지정 템플릿을 사용하여 이메일 콘텐츠를 만듭니다. 최대 8~10개의 이미지가 포함된 이메일 템플릿이 권장됩니다.

* 변형을 선택할 때 썸네일 업, 썸네일 다운 또는 플래그 아이콘을 사용하여 문제가 있는 출력을 보고해야 합니다.

## 생성형 AI에 대한 프롬프트 모범 사례 {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="프롬프트 지침"
>abstract="[!DNL Journey Optimizer B2B Edition] 설명서에서 전환율이 높고 브랜드에 맞는 마케팅 콘텐츠를 생성하는 효과적인 프롬프트를 만드는 방법을 알아보십시오."

이 안내서는 요청을 구조화하고, 의도를 명확하게 전달하며, AI가 브랜드 지침, 대상 요구 사항 및 캠페인 목표에 맞는 메시지를 생성하는지 확인하는 데 도움이 됩니다.

AI Assistant를 통해 목표에 맞는 고품질의 온-브랜드 마케팅 콘텐츠를 생성할 수 있는 효과적인 프롬프트를 작성하는 방법을 알아봅니다.

### CO-STAR 프레임워크 사용 {#costar-framework}

생성된 콘텐츠에서 최상의 결과를 얻으려면 CO-STAR 프레임워크를 사용하여 프롬프트를 구성하십시오. 이 구조화된 접근 방식은 필요한 사항을 정확하게 파악할 수 있도록 해 줍니다.

| 구성 요소 | 의미 | 이것이 중요한 이유 |
| --- | ---- | ------ |
| **C - 컨텍스트** | 캠페인, 제품 또는 상황에 대한 배경 정보 | 더 큰 그림을 이해할 수 있습니다. |
| **O - 목표** | 구체적인 마케팅 목표 | 컨텐츠가 달성해야 하는 목표 달성 |
| **초 - 스타일** | 커뮤니케이션할 방법 | 접근 방식 설정 |
| **T - 색조** | 감성적인 스타일과 목소리 | 메시지 느낌을 표시합니다. |
| **A - 대상** | 타깃팅하는 대상자 | 메시지가 적합한 사람에게 공명하는지 확인합니다. |
| **R - 요구 사항** | 특정 제한 또는 필수 포함 | 경계 및 한계 요소 정의 |

{style="table-layout:fixed"}

### 필수 메시지 표시 {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>실행</th>
<th>안 함</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>구조에 CO-STAR 프레임워크 사용
<li>새 컨텐츠와 기존 컨텐츠에 대해 명확하게 표시
<li>특정 추출 지침을 통해 문서 사용에 대한 포커스 제공
<li>톤, 전략 및 로케일을 선택합니다.
<li>마케팅 목표와 콘텐츠 유형 기능 일치
<li>A/B 테스트를 위해 여러 변형 생성</ul>
</td>
<td>
<ul><li>프롬프트에서 구조 변경, 스타일 지정 또는 이미지 편집을 요청합니다
<li>옵션에서 사용 가능한 경우 프롬프트의 언급 톤/전략
<li>제품 홍보 등 모호한 목표 사용_
<li>조건부 요소 선택 요청
<li>프롬프트를 통한 레이아웃 수정 예상</ul>
</td>
</tr>
</tbody>
</table>

### 프롬프트에서 지원되지 않는 콘텐츠

>[!TIP]
>
>디자인 도구 또는 [!DNL Adobe Express]을(를) 사용하여 시각적/이미지를 수정하십시오.

다음 요청은 **_지원되지 않음_**&#x200B;이며 다른 도구를 통해 처리해야 합니다.

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="레드 크로스 아웃">  이메일 구조 수정</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="레드 크로스 아웃">  시각적 스타일 변경</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="레드 크로스 아웃">  이미지 편집 작업</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>변경할 특정 섹션 선택</li>
<li>요소 삭제 또는 복제</li>
<li>조건부 선택</li>
<li>레이아웃 섹션 추가 또는 제거</li>
</ul>
</td>
<td>
<ul>
<li>텍스트 서식(굵게, 기울임체, 글꼴 크기)</li>
<li>색상 수정</li>
<li>레이아웃 스타일(테두리, 패딩, 여백)</li>
<li>시각 효과(그림자)</li>
</ul>
</td>
<td>
<ul>
<li>배경 변경 사항</li>
<li>텍스트 오버레이 또는 로고 추가</li>
<li>이미지 자르기 또는 크기 조정</li>
<li>색상 조정</li>
<li>이미지 대체</li>
</ul>
</td>
</tr>
</tbody>
</table>

### 품질 검사 목록 {#quality-checklist}

컨텐츠를 생성하기 전에 다음 사항을 확인하십시오.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **목표 지우기**: 작업, 제품/서비스, 값 및 컨텍스트를 명확하게 기술합니다.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **정의된 대상 대상**: 인구 통계학적, 역할 또는 세그먼트를 지정합니다.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **콘텐츠 형식 정렬**: 목표가 선택한 채널 또는 형식과 일치합니다.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **선택 항목 검토**: 톤, 전략 및 로케일을 선택했습니다. 프롬프트에 이 항목을 포함하지 마십시오.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **문서 포커스가 지정되었습니다**: 참조할 콘텐츠 또는 섹션을 강조 표시합니다.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **브랜드 적용**: 적절한 브랜드 지침이 선택되어 있습니다.

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} **실제 범위**: 레이아웃 변경, 스타일 또는 구조적 편집에 대한 요청을 방지합니다.

### 효과적인 마케팅 목표 {#marketing-objectives}

마케팅 목표를 작성할 때 명확하고, 실행 가능하며, 측정 가능해야 합니다. 모호하거나 일반적인 문을 사용하지 마십시오.

**좋은 목표의 예:**

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;새 AI 기반 분석 대시보드의 30일 무료 평가판 등록 유도&quot;

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;3월 15일에 발생한 &#39;클라우드 비용 40% 절감&#39;에 대한 B2B 웨비나에 대한 잠재 고객 생성&quot;

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;12월 25일에 종료되는 프리미엄 구독에 대한 25% 할인 혜택을 한시적으로 홍보합니다.&quot;

**피해야 할 예:**

![빨간색 십자 표시](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;제품 홍보&quot;(너무 모호함)

![빨간 십자 표시](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;사람들이 거래에 서명하도록 설정&quot;(불명확한 값)

![적십자선](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;새 기능에 대한 전자 메일&quot;(목적 부족)

#### 목표 구성

항상 관련 콘텐츠를 제작하기 위한 컨텍스트와 가치 제안을 제공하십시오. 다음 수식을 사용하여 효과적인 목표를 작성하십시오. **작업 + 제품/서비스 + 가치/이익 + 긴급도/컨텍스트**

**좋은 목표의 예:**

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;사용자가 개인화된 환경 친화적인 추천을 통해 지속 가능한 생활 습관을 추적하는 데 도움이 되는 새로운 모바일 앱의 다운로드를 장려합니다.&quot;

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;마케팅 전문가를 위한 고급 데이터 시각화 기술에 대한 단독 워크샵에 등록 홍보&quot;

![녹색 확인 표시](../../assets/do-not-localize/check-box-green.svg){width="20"} &quot;매주 5시간 이상 절약되는 혁신적인 AI 쓰기 도우미를 보여 주는 제품 출시 이벤트에 대한 참석 유도&quot;

**피해야 할 예:**

![빨간색 교차 ](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;새 앱 발표&quot;(값 제안 및 컨텍스트 누락)

![적십자 외부](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;워크샵에 등록하도록 사용자 지정&quot;(대상 및 혜택에 대한 구체성이 결여)

![빨간색 교차](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;승격 이벤트&quot;(명확한 작업, 값 또는 긴급성 없음)

#### 채널 유형별 프롬프트 예 {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>채널</th>
<th>예</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>이메일</strong></td>
<td>"세 가지 고객 성공 사례와 세부 ROI 지표를 제시하여 기업 잠재 고객을 육성합니다(Oracle: 45% 비용 절감, Accenture: 200% 리드 증가, Microsoft: 60% 시간 절약). 직원 수가 1,000명 이상인 기업의 IT 책임자 대상"</td>
</tr>
<tr>
<td><strong>랜딩 페이지</strong></td>
<td>"Fortune 500 추천서와 무료 보안 감사를 통해 엔터프라이즈 보안 솔루션이 사이버 공격의 99.9%를 방지하는 방법을 시연하여 B2B 방문자를 적격 리드로 전환하십시오."</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### 새 컨텐츠와 기존 컨텐츠 수정 비교 {#new-vs-modify}

요청에 새 콘텐츠 생성이 포함되는지 또는 기존 자료를 업데이트하는 것이 포함되는지 명확하게 표시합니다. 이러한 구분이 중요한 이유는 AI가 적절한 접근 방식을 선택할 수 있도록 안내하고 보다 정확하고 유용한 결과를 보장하기 때문입니다.

#### 새 콘텐츠 만들기

마케팅 캠페인을 시작하거나, 새 솔루션을 공개하거나, 업데이트/새로 고친 커뮤니케이션을 시작할 때 이 전략을 적용합니다. 이렇게 하면 메시지가 강력하게 시작되고 목표에 맞게 조정됩니다.

**메시지를 표시하는 방법** ➤ 새 콘텐츠를 만들 때 기존 콘텐츠를 참조하지 않고 마케팅 목표에 집중하십시오.

>[!BEGINSHADEBOX &quot;예&quot;]

* **SaaS 평가판**: &quot;소규모 비즈니스 소유자에게 새로운 CRM 소프트웨어를 출시하여 50% 시간 절약, 90% 빠른 리드 자격을 강조하고 맞춤형 온보딩을 통한 30일 무료 평가판을 제공합니다.&quot;
* **기능 발표**: &quot;기술 의사 결정자를 대상으로 기업 고객의 개발 시간을 60% 단축하는 새로운 API 통합 기능을 발표하십시오.&quot;
* **이벤트 프로모션**: &quot;실행 가능한 통찰력과 제한된 시트(최대 500개)를 강조하며 Google, Meta 및 Adobe의 전문가가 참여하는 &#39;디지털 마케팅 트렌드 2024&#39;에 대한 웨비나 등록을 촉진합니다.&quot;

>[!ENDSHADEBOX]

#### 기존 콘텐츠 수정

>[!TIP]
>
>정교함, 요약 또는 단순화와 같은 표준 수정 사항의 경우 사용자 지정 프롬프트를 작성하는 대신 **_세분화_**&#x200B;을(를) 선택하십시오.

현재 마케팅 캠페인을 업데이트, 새로 고침 또는 조정해야 하는 경우 수정 프롬프트를 사용하십시오. 이 방법은 증분 개선을 지원하므로 처음부터 새로 시작하지 않고도 메시징의 관련성을 유지할 수 있습니다.

**확인하는 방법** ➤ 기존 콘텐츠를 수정할 때는 변경할 내용과 변경하는 방법을 명확히 지정하십시오.

>[!BEGINSHADEBOX &quot;예&quot;]

* **캠페인 새로 고침**: &quot;일반적인 생산성 혜택 대신 엔터프라이즈 보안 기능에 집중하도록 프로그램 시작 이메일을 수정하여 규정 준수 인증을 보유한 IT 의사 결정자를 대상으로 함&quot;
* **대상 피벗**: &quot;특별히 대상 의료 서비스에 소프트웨어 데모 초대를 조정하여 일반 예제를 의료 사용 사례 및 HIPAA 준수 혜택으로 바꾸기&quot;
* **계절별 업데이트**: &quot;4분기 휴일 쇼핑을 위한 3분기 홍보 캠페인을 업데이트하여 초중고 학교에서 휴일 선물 제공으로 초점을 빠르게 전환합니다.&quot;

>[!ENDSHADEBOX]

## 고급 텍스트 설정 {#text-settings}

AI Assistant 콘텐츠 도구의 텍스트 설정에는 명확하고 형식이 잘 지켜진 프롬프트를 사용할 수 있을 뿐만 아니라 생성된 출력을 최적화하는 데 사용할 수 있는 텍스트 설정이 포함되어 있습니다.

>[!TIP]
>
>프롬프트에서 이러한 특성을 언급하는 대신 _[!UICONTROL 텍스트 설정]_&#x200B;에서 _[!UICONTROL 통신 전략]_ 및 _[!UICONTROL 색조]_ 옵션을 사용하십시오.

### 커뮤니케이션 전략 유형

커뮤니케이션 전략에 따라 메시지 표시 방법이 결정되어 효과를 극대화합니다. 긴급성을 구축하든, 신뢰를 구축하든, 즉각적인 조치를 취하든 다양한 전략이 다양한 목표에 더 적합합니다. 캠페인 목표와 대상자의 사고방식에 가장 적합한 전략을 선택합니다.

| **전략** | **추천 항목** | **메시징 스타일** | **예** |
| ------------ | ------------ | ------------------- | ------------ |
| **긴급** | 시간에 민감한 오퍼, 기한, 즉각적인 조치 | 시간 기반 언어로 즉각적인 압력 발생 | <li>&quot;지금 실행: 오퍼가 자정에 만료됨&quot; <li>&quot;얼룩이 차기 전에 오늘 등록&quot; <li>&quot;48시간 플래시 세일이 지금 시작&quot; |
| **FOMO(누락될 우려)** | 제한된 오퍼, 이벤트, 독점 액세스 | 긴급성, 희소성 및 시간 압력 신호를 사용합니다. | <li>&quot;24시간밖에 안 남았어요! 40% 할인된 한정 주식&quot; <li>&quot;마지막 기회: 조기 가격은 내일 종료됩니다.&quot; <li>&quot;100개의 베타 스팟만 남음&quot; |
| **소셜 증명** | 신뢰 구축, 사용 후기, 인기 제품 | 다른 사용자의 경험과 유효성 검사 활용 | <li>&quot;50,000명 이상의 만족한 고객 가입&quot; <li>&quot;업계 전문가로부터 별 4.9/5개 평가&quot; <li>&quot;Fortune지 선정 500대 기업에 신뢰&quot; |
| **부족** | 재고, 독점 릴리즈, 고수요 품목 제한 | 제한된 가용성과 독점성을 강조합니다. | <li>&quot;재고가 5개만 남음&quot; <li>&quot;한정판: 100개 제공&quot; <li>&quot;독점 릴리스: 선착순, 선착순&quot; |
| **인센티브** | 프로모션, 보상 프로그램, 특별 제공 | 실질적인 이점 및 보상 강조 | <li>&quot;첫 번째 주문에서 20% 할인&quot; <li>&quot;이번 주말에 2배 포인트 적립&quot; <li>&quot;50달러 이상 주문 시 무료 배송&quot; |
| **배타성** | Premium 제품, VIP 경험, 멤버 전용 오퍼 | 프리미엄 포지셔닝 및 특수 액세스 언어 사용 | <li>&quot;비공개 미리 보기에 대한 단독 초대&quot; <li>&quot;엘리트 멤버십으로 고급 분석 잠금 해제&quot; <li>&quot;Fortune지 선정 500대 기업에 가입하십시오. 이미 당사를 사용하고 있습니다.&quot; |
| **Gamification** | 참여 캠페인, 충성도 프로그램, 대화형 콘텐츠 | 게임 역학 및 성취 언어 사용 | <li>&quot;다음 보상 수준 잠금 해제&quot; <li>&quot;배지를 획득하려면 완벽한 도전&quot; <li>&quot;특별 경품을 위한 순위표에 오르기&quot; |
| **정보** | 교육, 연구, 복잡한 제품, 사고 리더십 | 팩트, 데이터, 통찰력 및 설명 사용 | <li>&quot;10,000개 이상의 상호 작용 분석을 통한 5가지 인사이트&quot; <li>&quot;새로운 연구는 3가지 혁신적인 접근 방식을 보여줍니다.&quot; <li>&quot;마케팅에서의 AI 구현에 대한 완전한 안내서&quot; |
| **교육 및 통찰력** | 학습 콘텐츠, 업계 동향, 모범 사례 | 귀중한 지식과 실행 가능한 방법 제공 | <li>&quot;전문가 안내서를 통해 고급 기법 학습&quot; <li>&quot;최고의 마케터가 사용하는 7가지 전략 살펴보기&quot; <li>&quot;5단계로 워크플로우를 최적화하는 방법을 알아봅니다.&quot; |

### 적절한 톤 설정 {#tone}

색조 셰이프는 대상자가 메시지를 인지하고 응답하는 방식을 나타냅니다. 항상 브랜드 음성 및 프로필 여정 단계에 맞는 톤을 선택합니다.

각 기능이 가장 잘 작동하는 시기 및 각 스타일에 맞는 콘텐츠 예제를 포함하여 사용 가능한 톤 옵션을 검토하십시오.

| 조음 | 다음에 최적 | 콘텐츠 예 |
| ---- | ----- | ----- |
| 전문가 | B2B 커뮤니케이션, 공식 발표 | &quot;우리의 전략적 파트너십을 발표하게 되어 기쁩니다...&quot; |
| 공감 가능하 | 고객 지원, 민감한 항목 | &quot;우리는 이 문제가 당신에게 얼마나 좌절감을 줄 수 있는지 이해합니다...&quot; |
| 해학적이어 | 캠페인 참여, 가벼운 콘텐츠 | &quot;경고: 심각한 생산성 향상을 초래할 수 있습니다!&quot; |
| 흥미진진 | 제품 출시, 이벤트 프로모션 | &quot;바로 지금이 바로 당신이 기다리던 순간이다!&quot; |
| 영감을 주는 | 동기부여 캠페인, 브랜드 목적 | &quot;함께, 우리는 세상에 변화를 만들 수 있습니다...&quot; |
| 설득력 있음 | 판매 캠페인, 전환 | &quot;...할 수 있는 이 제한된 시간 기회를 놓치지 마십시오.&quot; |
| 친숙해 | 고객 참여, 환영 메시지 | &quot;우리와 함께 있어서 기쁘다!&quot; |
| 공식 | 법적 커뮤니케이션, 공식 공지 | &quot;다음 변경 사항에 대한 알림입니다...&quot; |
| 변명 | 서비스 복구, 문제 해결 | &quot;보데아는 ...로 인한 불편에 대해 진심으로 사과한다.&quot; |
| 단호해 | 리더십 콘텐츠, 신뢰할 수 있는 메시징 | &quot;지금 당장 해야 할 일이 있습니다...&quot; |
| Storytelling | 브랜드 서사, 감정적 연결 | &quot;이 모든 것은 간단한 질문으로 시작되었습니다...&quot; |
| 대화형 | 캠페인 육성, 관계 구축 | &quot;이 프로그램이 어떤 도움을 줄 수 있는지에 대해 이야기해 보겠습니다.&quot; |

## 최적화된 참조 콘텐츠 {#reference-content}

>[!TIP]
>
>**[!UICONTROL 콘텐츠 참조]** 메뉴를 통해 에셋을 이미 업로드한 경우 프롬프트에서 참조할 필요가 없습니다. 시스템은 선택한 문서를 자동으로 사용합니다.

참조 콘텐츠 파일은 구체적이고 정확한 세부 정보로 생성된 콘텐츠를 보강하는 실제 정보를 제공합니다. 제품 브로셔나 백서 등의 문서를 업로드할 때 포커스가 있는 부품을 포함하도록 프롬프트를 변경합니다.

* **제품 브로셔를 사용합니다.** _대신&quot;_ **** _&quot;고급 보안 기능 및 규정 준수 인증, 특히 SOC 2 규정 준수 및 데이터 암호화에 집중&quot;_

* **대신** _&quot;사례 연구를 참조&quot;_ **사용해야 함** _&quot;의료 클라이언트의 ROI 결과 강조 표시, 특히 지역 의료 센터의 40% 비용 절감&quot;_

* **대신** _&quot;기술 세부 정보를 포함&quot;_ **사용해야 함** _&quot;REST API 끝점 및 99.9% 가동 시간 SLA에 중점을 두고 API 통합 기능 및 개발자 이점 강조&quot;_

### 콘텐츠 세분화

콘텐츠가 생성되면 **_[!UICONTROL Refine]_** 기능을 사용하여 다음 옵션을 사용하여 반복하고 개선합니다.

* **[!UICONTROL 자세히]** - AI Assistant를 통해 특정 주제를 확장하고 더 나은 이해와 참여를 위해 추가 세부 정보를 제공할 수 있습니다.

* **[!UICONTROL 요약]** - 정보가 길면 페이지 뷰어가 오버로드될 수 있습니다. AI Assistant를 사용하여 주요 사항을 명확하고 간결한 요약으로 요약하여 주목 받고 더 자세히 읽을 수 있도록 장려합니다.

* **[!UICONTROL 구문 변경]** - 의미를 유지하면서 메시지를 다시 작성합니다. 이 옵션은 핵심 메시지를 변경하지 않고 대체 단어를 생성하거나, 흐름을 개선하거나, 구문 조정을 하는 데 도움이 됩니다.

* **[!UICONTROL 더 간단한 언어 사용]** - 언어를 단순화하여 더 많은 대상자가 명확하고 쉽게 사용할 수 있도록 합니다.

* **[!UICONTROL 번역]** - 텍스트를 다른 언어로 번역합니다. (현재 지원되는 언어는 영어뿐입니다.)

* **[!UICONTROL 색조 변경]** - 메시지 색조를 조정하여 친숙하거나, 전문적이거나, 긴급하거나, 영감을 주는 등 사용자의 커뮤니케이션 스타일에 맞게 조정하십시오.

* **[!UICONTROL 통신 전략 변경]** - 긴급성을 만들거나 흥미로운 어필을 강조하는 등 목표에 따라 메시징 접근 방식을 수정합니다.
