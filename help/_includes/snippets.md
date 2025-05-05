---
title: 스니펫
description: 특정 에디션에 적용되는 기능이나 페이지를 참고하기 위해 노트 및 시각적 요소를 재사용함
source-git-commit: d0b2f91754ce3c5e38c6aa2c49c816fd46510403
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# 스니펫

<!-- Content authoring steps for reuse -->

## 의도 데이터 구성 {#intent-data-note}

>[!NOTE]
>
>의도 데이터는 Journey Optimizer B2B edition 인스턴스에 대해 구성될 때 포함됩니다. 또한 하나 이상의 게시된 여정 **또는**&#x200B;이(가) 구매 그룹을 만들어야 합니다. Intent Detection 모델 및 키워드, 제품 및 범주를 제출하는 방법에 대한 자세한 내용은 [Intent Data](../user/admin/intent-data.md)를 참조하십시오.

## AEM assets 라이선싱 참고 {#aem-assets-licensing-note}

>[!NOTE]
>
>AEM Assets as a Cloud Service 및 Dynamic Media 라이선스는 통합을 위한 필수 요건입니다. [Dynamic Media withOpen API](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"}이(가) 활성화되어 있는지 확인해야 합니다.<br/>
>계약 및 구성에 따라 시각적 컨텐츠를 디자인할 때 Adobe Experience Manager Assets as a Cloud Service에서 Adobe Journey Optimizer B2B edition에 직접 액세스할 수 있습니다.

## 콘텐츠 작성 - 구성 요소 - 구조 단계 {#structures-step}

1. 콘텐츠 디자인을 시작하려면 **[!UICONTROL Structures]**&#x200B;에서 항목을 드래그하여 캔버스에 놓습니다.

   _[!UICONTROL 구조]_&#x200B;에서 필요한 만큼 항목을 추가하고 오른쪽 창에서 각 항목의 설정을 편집합니다.

   >[!TIP]
   >
   >_[!UICONTROL n:n 열]_ 구성 요소를 선택하여 선택한 열 수(3개에서 10개 사이)를 정의합니다. 열 아래로 화살표를 이동하여 각 열의 너비를 정의할 수도 있습니다.

   ![구조를 캔버스로 드래그하고 설정을 조정하십시오](../assets/content-design-shared/content-design-add-structure.png){width="800" zoomable="yes"}

   각 열 크기는 구조 구성 요소의 전체 너비의 10%보다 작을 수 없습니다. 빈 열만 제거할 수 있습니다.

## 컨텐츠 작성 - 구성 요소 - 컨텐츠 단계 {#contents-step}

1. **[!UICONTROL 내용]** 섹션을 확장하고 하나 이상의 구조 구성 요소에 필요한 만큼 요소를 추가합니다.

   ![콘텐츠 요소를 캔버스로 드래그하고 설정을 조정하십시오](../assets/content-design-shared/content-design-add-content.png){width="800" zoomable="yes"}
   <!--
   reference to the contents elements--->

## 컨텐츠 작성 - 구성 요소 - 설정 단계 {#settings-step}

1. 필요한 경우 _[!UICONTROL 설정]_ 또는 _[!UICONTROL 스타일]_ 탭에서 각 구성 요소를 추가로 사용자 지정할 수 있습니다.

   예를 들어 각 구성 요소의 텍스트 스타일, 패딩 또는 여백을 변경할 수 있습니다.

## 콘텐츠 작성 - 에셋 단계 {#assets-step}

1. _자산_ 선택기에서 자산 라이브러리에 저장된 자산을 직접 선택할 수 있습니다.

   에셋이 포함된 폴더를 두 번 클릭합니다. 항목을 구조 구성 요소로 끌어다 놓습니다.

   소스 유형의 자산을 사용하는 방법에 대한 자세한 내용은 [콘텐츠에 자산 추가](../user/content/assets-overview.md#use-assets-for-content-authoring)를 참조하십시오.

   ![Marketo Engage 에셋을 캔버스로 드래그하고 설정을 조정하십시오](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## 콘텐츠 작성 - 개인화 단계 {#personalization-step}

1. 개인화 필드를 삽입하여 프로필 속성, 대상자 멤버십, 컨텍스트 속성 등에서 콘텐츠를 사용자 지정합니다.

## 컨텐츠 작성 - 조건 컨텐츠 단계 활성화 {#dynamic-content-step}

1. 조건부 규칙에 따라 다이내믹 콘텐츠를 추가하고 타겟팅된 프로필에 콘텐츠를 적용하려면 **[!UICONTROL 조건 콘텐츠 사용]**&#x200B;을 클릭하십시오.

## 컨텐츠 작성 - 링크 추적 단계 {#links-tracking-step}

1. 추적되는 콘텐츠의 모든 URL을 표시하려면 왼쪽 창에서 **[!UICONTROL 링크]** 탭을 선택하십시오.

   _추적 유형_ 또는 _레이블_&#x200B;을 수정하고 필요한 경우 태그를 추가할 수 있습니다.
