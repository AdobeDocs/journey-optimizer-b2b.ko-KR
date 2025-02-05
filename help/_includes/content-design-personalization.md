---
title: 콘텐츠 작성 - 개인화
description: 콘텐츠 작성을 위한 개인화 사용에 대한 재사용 섹션
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# 콘텐츠 작성 - 개인화

Journey Optimizer B2B edition에서는 중괄호 `{}`로 묶은 개인 맞춤화된 콘텐츠로 식을 만들 수 있는 인라인 단순 구문을 사용합니다. 동일한 콘텐츠 또는 필드에 제한 없이 여러 표현식을 추가할 수 있습니다.

예:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

콘텐츠를 처리할 때 Journey Optimizer B2B edition은 표현식을 Experience Platform 데이터베이스에 포함된 데이터로 대체합니다. 첫 번째 예제는 _Hello John Doe_&#x200B;입니다.

다음 예제에서는 리드/계정 속성과 시스템 토큰을 사용하여 콘텐츠를 개인화하는 단계를 간략하게 설명합니다.

1. 텍스트 구성 요소를 선택하고 도구 모음에서 _개인화 추가_ 아이콘을 클릭합니다.

   ![개인 설정 아이콘을 클릭합니다](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   이 작업은 _Personalization 편집_ 대화 상자를 엽니다.

1. **+** 또는 **...**&#x200B;을(를) 클릭하여 빈 공간에 토큰을 추가합니다.

   ![토큰을 사용하여 개인화된 텍스트 만들기](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
