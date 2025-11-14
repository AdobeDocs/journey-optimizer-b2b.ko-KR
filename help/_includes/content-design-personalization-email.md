---
title: 콘텐츠 작성 - 개인화
description: 콘텐츠 작성을 위한 개인화 사용에 대한 재사용 섹션
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 콘텐츠 작성 - 개인화

Journey Optimizer B2B edition에서는 중괄호 `{{}}`로 묶은 개인화된 콘텐츠로 식을 만들 수 있는 인라인 단순 구문을 사용합니다. 동일한 콘텐츠 또는 필드에 제한 없이 여러 표현식을 추가할 수 있습니다.

예를 들어 개인화 식을 `Hello {{lead.firstName}} {{lead.lastName}}`(으)로 추가할 수 있습니다. 콘텐츠를 처리할 때 Journey Optimizer B2B edition은 표현식을 Experience Platform 데이터베이스에 포함된 데이터로 대체합니다. 첫 번째 예제는 _Hello John Doe_&#x200B;입니다.

Journey Optimizer B2B edition의 개인화 도구 사용에 대한 자세한 내용은 [콘텐츠 개인화](../user/content/personalization.md)를 참조하십시오.

>[!NOTE]
>
>Journey Optimizer B2B edition은 일관된 경험을 위해 다른 Adobe Experience Platform 애플리케이션과 일치하도록 이메일의 개인화 토큰에 대한 _카멜 대/소문자_ 구문을 따릅니다. 이 토큰 형식은 [Handlebars 템플릿 언어](https://handlebarsjs.com/guide/#what-is-handlebars){target="_blank"}와(과) 완전히 호환됩니다. 이 변경 전에 추가된 모든 토큰은 자동으로 업데이트됩니다.

다음 예제에서는 사용자 및 시스템 토큰을 사용하여 콘텐츠를 개인화하는 단계를 간략하게 설명합니다. 이는 [간소화된 아키텍처](../user/simplified-architecture.md)에서 프로비저닝된 Journey Optimizer B2B edition 환경에서 사용할 수 있는 변경 사항을 반영합니다.

1. 텍스트 구성 요소를 선택하고 도구 모음에서 _개인화 추가_(![개인화 추가 아이콘](../assets/do-not-localize/icon-personalization-field.svg) ) 아이콘을 클릭합니다.

   ![개인 설정 아이콘을 클릭합니다](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   이 작업은 _Personalization 편집_ 대화 상자를 엽니다.

1. 토큰 옆에 있는 더하기(**+**) 기호를 클릭하여 토큰을 추가합니다.

   대체(잠재 고객에 대해 해당 필드를 사용할 수 없을 때 표시되는 기본 텍스트)를 사용하여 토큰을 추가하려면 _자세히_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 대체 텍스트를 사용하여 삽입]**&#x200B;을 선택합니다.

   ![토큰을 사용하여 개인화된 텍스트 만들기](../assets/content-design-shared/visual-designer-personalize-dialog-handlebar.png){width="700" zoomable="yes"}

1. 포함할 추가 토큰 또는 기타 정적 텍스트를 추가합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   개인화 스크립팅은 시각적 디자인 공간에 표시됩니다. 필요할 때 변경하려면 이 옵션을 선택할 수 있습니다.

   ![개인화 스크립트 선택](../assets/content-design-shared/visual-designer-select-personalization-script.png){width="600"}
