---
title: Experience Manager Assets 작업
description: Adobe Journey Optimizer B2B Edition에서 콘텐츠를 작성할 때 연결된 AEM Assets 저장소에서 이미지 에셋을 사용하는 방법을 알아봅니다.
feature: Assets, Content
source-git-commit: 0bdf0da4db0cbfc781d16f1c50716b1fc8ea4db9
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Experience Manager 에셋으로 작업

Adobe Experience Manager Assets as a Cloud Service B를 Adobe Journey Optimizer B2Edition과 통합하면 마케팅 콘텐츠에서 디지털 에셋을 쉽게 검색하고 액세스할 수 있습니다. 콘텐츠를 작성할 때 왼쪽 탐색 메뉴의 _[!UICONTROL Assets]_ 항목에서 에셋에 액세스할 수 있으며 계정 여정에 대한 이메일 콘텐츠를 작성할 때 액세스할 수 있습니다. Adobe Journey Optimizer B2B 에디션에서 직접 연결된 AEM Assets as a Cloud Service 저장소에 에셋을 업로드할 수도 있습니다.

>[!NOTE]
>
>현재 Adobe Journey Optimizer B2B 에디션에서는 Adobe Experience Manager Assets의 이미지 에셋만 지원됩니다. 에셋에 대한 변경은 Adobe Experience Manager Assets 중앙 저장소에서 수행해야 합니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets)

이러한 디지털 에셋을 사용하는 경우 Assetsas a Cloud Service 의 최신 변경 사항이 연결된 참조를 통해 라이브 이메일 캠페인에 자동으로 전파됩니다. Adobe Experience Manager Assetsas a Cloud Service 에서 이미지가 삭제되면 이메일에 이미지가 깨진 참조로 나타납니다. 현재 계정 여정 내에서 사용되는 에셋이 수정되거나 삭제되면 여정 작성자에게 이미지 변경 사항과 이미지를 사용하는 여정 목록에 대한 알림이 표시됩니다. 에셋에 대한 모든 변경 작업은 Adobe Experience Manager Assets 중앙 저장소에서 수행해야 합니다.

## AEM Assets을 이미지 소스로 사용

환경에 [Assets 저장소 연결](../admin/configure-aem-repositories.md)이 하나 이상 있는 경우 전자 메일, 전자 메일 템플릿 또는 시각적 조각에 대한 세부 정보를 만들거나 볼 때 AEM Assets을 에셋의 소스로 지정할 수 있습니다.

* 새 콘텐츠를 만들 때는 대화 상자에서 `AEM Assets`을(를) **[!UICONTROL Image Source]** 항목으로 선택하십시오.

  ![만들기 대화 상자에서 이미지 소스로 AEM Assets 선택](./assets/create-dialog-aem-assets.png){width="500"}

* 기존 콘텐츠 리소스를 여는 경우 오른쪽의 _[!UICONTROL 본문]_ 패널에서 `AEM Assets`을(를) 선택합니다.

  ![속성에서 이미지 소스로 AEM Assets 선택](./assets/content-source-aem-assets.png){width="700" zoomable="yes"}

## 작성을 위해 에셋에 액세스

>[!IMPORTANT]
>
>관리자는 Assets에 액세스해야 하는 사용자를 Assets 소비자 사용자 또는/및 Assets 사용자 제품 프로필에 추가해야 합니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console)

시각적 콘텐츠 편집기에서 왼쪽 사이드바의 _자산 선택기_ 아이콘을 클릭합니다. 이렇게 하면 도구 패널이 선택한 저장소에서 사용 가능한 에셋 목록으로 변경됩니다.

![Assets 선택기 아이콘을 클릭하여 이미지 자산에 액세스합니다](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

연결된 AEM 저장소가 두 개 이상 있는 경우 **[!UICONTROL 저장소]**&#x200B;의 메뉴 화살표를 클릭하여 사용할 저장소를 선택합니다.

![이미지 자산에 액세스할 AEM Assets 저장소를 선택하십시오](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

이미지 에셋을 시각적 캔버스에 추가하는 방법에는 여러 가지가 있습니다.

* 왼쪽 탐색에서 이미지 썸네일을 끌어서 놓습니다.

  ![이미지 자산에 액세스할 AEM Assets 저장소를 선택하십시오](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

* 캔버스에 이미지 구성 요소를 추가하고 **[!UICONTROL 찾아보기]**&#x200B;를 클릭하여 _[!UICONTROL Assets 선택]_ 대화 상자를 엽니다.

  대화 상자에서 선택한 저장소에서 이미지를 선택할 수 있습니다.

  필요한 에셋을 찾는 데 도움이 되는 여러 가지 도구가 있습니다.

  ![Assets 선택 대화 상자에서 도구를 사용하여 이미지 자산을 찾아 선택합니다](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * 오른쪽 상단에서 **[!UICONTROL 저장소]**&#x200B;를 변경합니다.

   * 오른쪽 상단의 **[!UICONTROL 자산 관리]**&#x200B;를 클릭하여 다른 브라우저 탭에서 Assets 저장소를 열고 AEM Assets 관리 도구를 사용합니다.

   * 표시를 **[!UICONTROL 목록 보기]**, **[!UICONTROL 눈금 보기]**, **[!UICONTROL 갤러리 보기]** 또는 **[!UICONTROL 폭포 보기]**(으)로 변경하려면 오른쪽 상단의 _보기 유형_ 선택기를 클릭하십시오.

   * 오름차순과 내림차순 사이의 정렬 순서를 변경하려면 _정렬 순서_ 아이콘을 클릭하십시오.

   * **[!UICONTROL 정렬 기준]** 메뉴 화살표를 클릭하여 정렬 기준을 **[!UICONTROL 이름]**, **[!UICONTROL 크기]** 또는 **[!UICONTROL 수정됨]**(으)로 변경합니다.

   * 조건에 따라 표시된 항목을 필터링하려면 왼쪽 상단의 _필터_ 아이콘을 클릭하십시오.

   * 표시된 항목을 자산 이름과 일치하도록 필터링하려면 검색 필드에 텍스트를 입력합니다.

  ![필터 및 검색 필드를 사용하여 자산을 찾습니다](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

<!-- 
## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.

-->