---
title: 조각 작성
description: 시각적 디자인 도구를 통해 재사용 가능한 콘텐츠 조각을 작성 - Journey Optimizer B2B edition의 이메일 및 템플릿에 대한 구성 요소, 개인화, 조건부 콘텐츠 및 사용자 지정 가능한 필드를 추가합니다.
feature: Fragments, Content Design Tools
role: User
exl-id: d29754cf-6721-489c-bff8-cde034456db2
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 6%

---

# 조각 작성

[조각을 만들고](./fragments.md#create-fragments) 나면 시각적 디자인 공간을 사용하여 조각의 구조 및 콘텐츠 구성 요소를 작성합니다.

## 구조 및 콘텐츠 추가 {#design-fragment}

{{$include /help/_includes/content-design-components.md}}

## 에셋 추가

{{$include /help/_includes/content-design-assets.md}}

## 레이어, 설정 및 스타일 탐색

{{$include /help/_includes/content-design-navigation.md}}

## 콘텐츠 개인화

{{$include /help/_includes/content-design-personalization.md}}

## 조건부 콘텐츠

규칙에 따라 타겟팅된 프로필에 콘텐츠를 적용하는 조건부 콘텐츠를 추가하려면 콘텐츠 구성 요소를 선택하고 구성 요소 도구 모음에서 **[!UICONTROL 조건부 콘텐츠 사용]** 단추를 클릭하십시오. 게시된 조각이 이메일 메시지에 포함된 경우, 조건부 규칙은 이메일 메시지에 렌더링되는 조건부 구성 요소의 변형을 결정합니다.

자세한 내용은 [_조건부 콘텐츠_](./conditional-content.md)&#x200B;를 참조하세요.

## 조각 사용자 지정 활성화

작성자가 [이메일](./email-authoring.md#content-authoring---use-visual-fragments) 또는 [이메일 템플릿](./email-template-authoring.md#content-authoring---use-visual-fragments)에 조각을 추가하면 조각 콘텐츠가 기본적으로 잠깁니다. 게시된 조각에 대한 모든 변경 사항은 조각이 사용되는 모든 컨텐츠 자산에 자동으로 전파됩니다. 조각의 구성 요소에 대한 매개 변수를 편집 가능한 것으로 지정하면 이메일 또는 템플릿 작성자가 해당 요구 사항에 맞는 사용자 지정 필드 값을 지정할 수 있습니다. 이 사용자 정의 플래그는 이미지, 텍스트 및 버튼 시각적 구성 요소로 제한됩니다.

예를 들어 클릭 가능한 버튼이 포함된 재사용 가능한 배너를 디자인하는 경우 버튼의 URL 매개 변수를 편집 가능한 것으로 지정할 수 있습니다. 그러면 이메일 작성자는 이메일 캠페인에 더 구체적인 URL을 사용할 수 있습니다. 마케터는 이러한 사용자 정의 가능 필드를 통해 완전히 새로운 콘텐츠 블록을 만들거나 원래 조각에서 상속된 업데이트를 중단하지 않고도 재사용 가능한 콘텐츠를 관리하고 개인화할 수 있습니다.

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
