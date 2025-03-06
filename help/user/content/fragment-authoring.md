---
title: 조각 작성
description: 이메일 및 템플릿 디자인에 재사용할 수 있는 콘텐츠 조각을 작성하여 효율성을 높이고 디자인 및 브랜딩 표준을 유지 관리하는 방법에 대해 알아봅니다.
feature: Content
source-git-commit: 1f551b636ef347fd65aa39a809dedba8372c3ac4
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 14%

---

# 조각 작성

[조각을 만들고](./fragments.md#create-fragments) 나면 시각적 편집기를 사용하여 조각의 구조적 구성 요소와 콘텐츠 구성 요소를 작성합니다.

## 구조 및 콘텐츠 추가 {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="구조 구성 요소 추가"
>abstract="구조 구성 요소는 조각 레이아웃을 정의합니다. **구조** 구성 요소를 캔버스로 드래그 앤 드롭하여 조각의 콘텐츠 디자인을 시작할 수 있습니다."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="콘텐츠 구성 요소 정보"
>abstract="콘텐츠 구성 요소는 조각 레이아웃 제작에 사용할 수 있는 빈 콘텐츠 플레이스홀더입니다."

{{$include /help/_includes/content-design-components.md}}

## 에셋 추가

{{$include /help/_includes/content-design-assets.md}}

## 레이어, 설정 및 스타일 탐색

{{$include /help/_includes/content-design-navigation.md}}

## 콘텐츠 개인화

{{$include /help/_includes/content-design-personalization.md}}

## 사용자 정의 필드 활성화

이메일 또는 이메일 템플릿 작성자가 조각을 추가하면 조각 콘텐츠가 기본적으로 잠깁니다. 게시된 조각에 대한 모든 변경 사항은 조각이 사용되는 모든 컨텐츠 자산에 자동으로 전파됩니다. 조각의 구성 요소에 대한 매개 변수를 편집 가능한 것으로 지정하면 이메일 또는 템플릿 작성자가 해당 요구 사항에 맞는 사용자 지정 필드 값을 지정할 수 있습니다. 이 사용자 지정 플래그는 이미지, 텍스트 및 단추 시각적 구성 요소로 제한됩니다.

예를 들어 클릭 가능한 버튼이 포함된 재사용 가능한 배너를 디자인하는 경우 버튼의 URL 매개 변수를 편집 가능한 것으로 지정할 수 있습니다. 그러면 이메일 작성자는 이메일 캠페인에 더 구체적인 URL을 사용할 수 있습니다. 마케터는 이러한 사용자 정의 가능 필드를 통해 완전히 새로운 콘텐츠 블록을 만들거나 원래 조각에서 상속된 업데이트를 중단하지 않고도 콘텐츠를 관리하고 개인화할 수 있습니다.

1. 시각적 콘텐츠 편집기에서 사용자 지정을 활성화할 이미지, 텍스트 또는 단추 요소를 선택합니다.

1. 오른쪽의 구성 요소 세부 정보에서 **[!UICONTROL 편집 가능한 필드]** 탭을 선택합니다.

1. **[!UICONTROL 편집 사용]** 옵션 토글을 클릭하고 편집 가능한 필드를 설정합니다.

   ![조각 이미지 구성 요소에 대해 편집 가능한 필드를 사용하도록 설정](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   구성 요소 유형 및 조각에 정의된 매개 변수에 따라 표시된 필드를 사용자 지정할 수 있습니다.

   맞춤화를 허용할 각 필드의 활성화 상태로 전환을 변경합니다.

1. 편집 가능한 모든 필드와 해당 기본값을 검토하려면 **[!UICONTROL 개요]**&#x200B;를 클릭하십시오.

   ![편집 가능한 필드와 해당 기본값을 검토합니다](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. 변경 내용을 저장합니다.

## 연결된 URL 추적 편집

{{$include /help/_includes/content-design-links.md}}
