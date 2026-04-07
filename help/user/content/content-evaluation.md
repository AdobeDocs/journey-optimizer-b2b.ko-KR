---
title: 콘텐츠 점수
description: 브랜드 정렬 점수로 이메일 콘텐츠를 평가합니다. Journey Optimizer B2B edition의 브랜드 지침에 따라 색상, 글꼴, 로고 및 작성 스타일을 확인합니다.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: 37e4a7976d716f24edf2c2e92cbfa4c149aa66ec
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 8%

---

# 컨텐츠 점수 책정 {#content-scoring}

콘텐츠 평가 및 채점을 통해 선택한 브랜드에서 [정의된 지침](./brands-manage-create.md#brand-definitions) 및 일반 품질 표준을 준수하는 콘텐츠를 만들고, 검토하고, 관리할 수 있습니다. 평가를 실행하면 이메일 캠페인 전반에서 톤, 메시징 및 시각적 ID의 일관성을 유지하는 동시에 콘텐츠가 라이브로 전환되기 전에 품질을 확인하는 역할을 합니다.

>[!AVAILABILITY]
>
>Adobe Journey Optimizer B2B edition에서 AI 기반 기능을 사용하려면 [사용자 동의](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}가 필요합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.
>
>제품 관리자가 이러한 기능을 사용할 수 있는 방법에 대한 자세한 내용은 [브랜드 관련 권한](./brands-overview.md#brand-related-permissions)을 참조하세요.

## 평가 실행

1. 이메일 콘텐츠를 만든 후 오른쪽의 _브랜드 정렬_( ![브랜드 정렬 아이콘](../assets/do-not-localize/icon-brand-compliance.svg)) 아이콘을 클릭하여 이메일 디자인 공간에서 _브랜드 정렬_ 오른쪽 패널을 엽니다.

   [기본 브랜드](./brands-manage-create.md#default-brand)이(가) 자동으로 선택됩니다.

   ![브랜드 정렬 도구 액세스](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   패널 맨 위에 있는 _전체 화면_( ![전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg) ) 아이콘을 클릭하여 브랜드 정렬 도구를 전체 화면 모드로 표시할 수 있습니다.

1. 필요한 경우 **[!UICONTROL 브랜드]** 메뉴 화살표(![아래쪽 화살표](../assets/do-not-localize/icon-down-menu.svg))를 클릭하여 게시된 다른 브랜드를 선택합니다.

1. 선택한 브랜드에 맞게 콘텐츠 정렬을 평가하려면 **[!UICONTROL 점수 평가]**&#x200B;를 클릭하십시오.

   시스템은 선택한 브랜드에 대한 지침에 따라 콘텐츠를 평가하고 결과 점수를 표시합니다.

   ![오른쪽 패널의 평가 점수](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## 브랜드 정렬 점수 {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="브랜드 선택"
>abstract="브랜드를 선택하여 콘텐츠가 브랜드의 특정 지침, 기준 및 정체성에 맞게 제작되도록 하여 일관성과 브랜드 무결성을 유지합니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="브랜드 정렬 점수"
>abstract="브랜드 정렬 점수는 색상, 글꼴, 로고, 이미지 및 작성 스타일의 일관성을 유지하기 위해 콘텐츠가 브랜드 지침을 얼마나 잘 준수하는지 측정합니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors_score"
>title="색상 점수"
>abstract="색상 점수"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts_score"
>title="글꼴 점수"
>abstract="글꼴 점수"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos_score"
>title="로고 점수"
>abstract="로고 점수"

>[!AVAILABILITY]
>
>이 기능은 현재 공개 베타로 사용할 수 있습니다.

브랜드가 잘 정의되고 게시되면 이메일 디자인 공간 내에서 직접 브랜드 정렬 점수를 평가하여 콘텐츠가 브랜드 지침에 부합하는지 확인합니다.

점수는 평가된 이메일 콘텐츠에서 식별된 위반에 따라 계산됩니다.

* 100 = 완료 - 위반을 찾을 수 없음
* 80-99 = 양호 - 경미한 위반만
* 60-79 = 보통 - 일부 중대한 위반
* 60 미만 = 부족 - 주요 위반 사항 주의 필요

평가 결과를 보다 자세히 검토하여 위반 사항을 식별하고 범주 정렬 점수(_높음_, _Medium_, _낮음_)를 개선하는 데 도움을 주고 세부 정보를 검토할 수 있습니다.

**[!UICONTROL 작성 스타일]** 또는 **[!UICONTROL 시각적 콘텐츠]**&#x200B;의 경우 _확장_( ![확장 화살표](../assets/do-not-localize/icon-expand-right.svg) ) 화살표를 클릭하여 평가에 대한 세부 정보를 표시합니다.

![브랜드 정렬 평가 세부 정보](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

각 점수 insight에 대한 세부 보기를 보려면 _전체 화면_( ![자세한 인사이트를 보려면 전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg)) 아이콘을 클릭하십시오.

특정 피드백 및 제안을 보려면 플래그가 지정된 지침을 선택하십시오.

![전체 화면 보기의 브랜드 정렬 평가 세부 정보](./assets/brands-alignment-evaluation-details-full-screen.png){width="700" zoomable="yes"}

콘텐츠를 변경하고 **[!UICONTROL 점수 다시 평가]**&#x200B;를 클릭하여 다른 평가를 실행하고 개선된 결과를 확인할 수 있습니다.

## 콘텐츠 품질 점수 {#quality-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_quality_score_overview"
>title="콘텐츠 품질"
>abstract="일반적인 콘텐츠 품질을 평가하여 가독성, 콘텐츠 응집성 및 효과성과 관련된 잠재적인 문제를 식별합니다. 품질 평가는 브랜드 지침과 독립적입니다."

>[!NOTE]
>
>콘텐츠 품질 평가는 브랜드 지침과 독립적입니다. 브랜드를 선택하더라도 품질 검사에는 해당 지침이 적용되지 않는다. 브랜드 선택은 브랜드 정렬 점수에만 관련이 있습니다.

브랜드 정렬뿐만 아니라 일반 콘텐츠 품질을 평가하여 브랜드 지침과 관계없이 가독성, 콘텐츠 응집성 및 효과성과 관련된 잠재적 문제를 식별할 수 있습니다.

**[!UICONTROL 콘텐츠 품질]** 섹션으로 스크롤하여 품질 인사이트 및 권장 사항을 검토하십시오.

![콘텐츠 품질 평가](./assets/content-scoring-quality-insights.png){width="600" zoomable="yes"}

특정 피드백 및 개선을 위해 실행 가능한 제안을 보려면 플래그가 지정된 항목을 선택하십시오. 점수는 다음 카테고리를 기반으로 합니다.

* **[!UICONTROL CTA 효율성]**: call-to-action이 독자에게 원하는 행동을 취하도록 동기를 부여하는 정도를 평가합니다.
* **[!UICONTROL 제목 줄]**: 명확성, 관련성 및 주의를 끄는 품질을 평가하여 이메일 열기를 유도합니다.
* **[!UICONTROL 가독성]**: 독자가 이해할 수 있는 컨텐츠의 용이성과 참여도를 측정합니다.
* **[!UICONTROL 스팸 확인]**: 전달성에 영향을 줄 수 있는 일반적인 스팸 트리거를 식별합니다.
* **[!UICONTROL 컨텐츠 응집력]**: 컨텐츠가 원활하게 흐르고 주제를 벗어나지 않도록 합니다.
* **[!UICONTROL 교정]**: 맞춤법, 문법 및 명확성 문제가 있는지 확인합니다.

품질 점수에 대한 자세한 보기를 보려면 _전체 화면_(![자세한 인사이트를 보려면 전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg)) 아이콘을 클릭하십시오.

![콘텐츠 품질 평가의 전체 화면 보기](./assets/content-scoring-quality-full-screen.png){width="700" zoomable="yes"}

권장 사항을 기반으로 콘텐츠를 편집하여 가독성, 콘텐츠 응집성 및 전체 품질을 향상시킬 수 있습니다. 품질 점수를 새로 고치려면 변경한 후 **[!UICONTROL 점수 다시 평가]**&#x200B;를 클릭하십시오.
