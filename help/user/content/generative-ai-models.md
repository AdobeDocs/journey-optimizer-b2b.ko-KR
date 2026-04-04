---
title: 생성 AI 모델
description: 마케터가 이메일 및 랜딩 페이지 콘텐츠에 대한 이미지를 생성하기 위해 선택할 수 있는 생성 AI 이미지 모델을 만들고 관리합니다.
topic: Artificial Intelligence
feature: Generative AI, Brand Identity, Content
role: User
level: Beginner, Intermediate
source-git-commit: 0612c3caa0673a7eb65a0aac0010edcf12c5d553
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# 브랜드 정렬을 위한 생성 AI 모델

내장된 모델, 맞춤형 Firefly 모델 및 서드파티 이미지 생성 공급자를 통해 AI 이미지 생성 기능을 확장하여 특정 요구 사항을 충족하고 브랜드 정렬을 개선합니다.

- Firefly Image Model 4에서 제공하는 **[!UICONTROL Adobe 모델]**&#x200B;은(는) 즉시 제공되며 추가 설정 없이 즉각적인 이미지 생성에 사용할 수 있습니다.
- Gemini 2.5 Flash에서 제공하는 **[!UICONTROL 파트너 모델]**&#x200B;은(는) 특정 사용 사례에 특화된 기능을 제공합니다.
- **[!UICONTROL 사용자 지정 모델]**&#x200B;은(는) 자신의 자산에 대해 교육되고 조직에서 추가한 브랜드별 모델입니다.

[Adobe Firefly 설명서](https://helpx.adobe.com/kr/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html){target="_blank"}에서 사용자 지정 모델에 대해 알아보세요.

마케터는 이메일 또는 랜딩 페이지 콘텐츠에 대한 이미지를 생성할 때 활성화된 생성 모델을 선택할 수 있습니다.

## 생성 모델 관리

중앙 위치에서 사용 가능한 모든 모델을 보고, 필터링 및 검색을 통해 특정 모델을 찾고, 브랜드에 대한 모델 설정을 구성할 수 있습니다.

1. 왼쪽 탐색에서 **[!UICONTROL 콘텐츠 관리]** > **[!UICONTROL 브랜드]**(으)로 이동합니다.

1. 페이지에서 **[!UICONTROL 생성 모델]** 탭을 선택합니다.

![생성 모델 목록에 액세스](./assets/brands-gen-models-list.png){width="800" zoomable="yes"}

### 목록 필터링 및 검색

_필터_ ![필터 아이콘](../../assets/do-not-localize/icon-react-filter.svg) 아이콘을 클릭하여 필터 메뉴에 액세스합니다. **[!UICONTROL 유형]** 또는 **[!UICONTROL 상태]**&#x200B;별로 모델을 필터링합니다.

![생성 모델 목록 필터링](./assets/brands-gen-models-filter.png){width="700" zoomable="yes"}

검색 창을 사용하여 이름별로 특정 생성 모델을 찾을 수도 있습니다.

### 모델 작업

목록에 있는 사용자 지정 모델의 경우 _추가 메뉴_ ![추가 메뉴 아이콘](../../assets/do-not-localize/icon-more-menu.svg) 아이콘을 클릭합니다. 모델의 가용성 상태를 변경하려면 **[!UICONTROL 활성화]** 또는 **[!UICONTROL 비활성화]**&#x200B;를 선택하거나 목록에서 모델을 제거하려면 **[!UICONTROL 삭제]**&#x200B;를 선택할 수 있습니다.

![생성 모델 목록의 추가 메뉴](./assets/brands-gen-models-more-menu.png){width="450"}

기본 제공 모델의 경우 _활성화_( ![활성화 아이콘](../../assets/do-not-localize/icon-enable.svg) ) 또는 _비활성화_( ![비활성화 아이콘](../../assets/do-not-localize/icon-disable.svg) ) 아이콘을 클릭하여 이미지 생성을 위한 모델 가용성을 변경합니다.

>[!NOTE]
>
>사용자 지정 모델만 삭제할 수 있습니다.

## 생성 모델 추가

맞춤형 Firefly 모델을 생성하거나 서드파티 이미지 생성 공급자를 연결하여 생성 AI 기능을 확장하십시오.

>[!NOTE]
>
>사용자 지정 Firefly 모델을 만들려면 Firefly ETLA 계약이 필요합니다.

1. _[!UICONTROL 생성 모델]_ 탭에서 **[!UICONTROL 모델 추가]**&#x200B;를 클릭합니다.

1. 모델의 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

<!-- 1. Select a **[!UICONTROL Model provider]**. future development -->

1. **[!UICONTROL 모델 ID]**&#x200B;을(를) 입력하십시오.

   모델 ID를 찾으려면 Firefly 웹 사이트에 액세스하여 훈련된 모델로 이동합니다. 고유 식별자는 모델이 게시된 후 모델의 관리 섹션에서 사용할 수 있습니다. 자세한 내용은 [Firefly 사용자 지정 모델 설명서](https://helpx.adobe.com/kr/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html){target="_blank"}를 참조하세요.

1. 필요한 경우 모델 및 해당 용도를 식별하는 데 도움이 되도록 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

   ![모델 추가 - 생성 모델](./assets/brands-gen-models-add-model.png){width="550" zoomable="yes"}

1. 모델 구성을 확인하려면 **[!UICONTROL 연결 테스트]**&#x200B;를 클릭하십시오.

1. 연결 테스트가 성공하면 **[!UICONTROL 저장]**&#x200B;을 클릭하여 모델 구성을 저장합니다.

   모델을 저장하면 마케팅 담당자가 사용할 수 있도록 활성화할 수 있는 생성 모델 목록에 모델이 추가됩니다. 언제든지 비활성화하거나 삭제할 수도 있습니다.

   ![이미지 생성을 위한 생성 모델 선택](./assets/gen-ai-model-selection.png){width="600" zoomable="yes"}
