---
title: 자산
description: Journey Optimizer B2B 에디션의 자산 관리에 대해 알아봅니다.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 100%

---

# 자산

Adobe Journey Optimizer B2B 에디션에서 자산은 일반적으로 계정 여정을 지원하는 콘텐츠를 디자인할 때 사용되는 이미지입니다. 이러한 이미지는 시각적 콘텐츠 편집기 내의 자산 선택기나 간단한 드래그 앤 드롭 인터페이스를 통해 이메일, 이메일 템플릿 및 조각 내에서 사용할 수 있습니다.

Adobe Journey Optimizer B2B 에디션에서 마케터는 두 가지 유형의 자산 라이브러리, 즉 Adobe Marketo Engage Design Studio와 Adobe Experience Manager Assets as a Cloud Service에 액세스할 수 있습니다. Adobe Marketo Engage Design Studio만 사용할 수도 있고, 동시에 구성된 두 라이브러리를 사용할 수도 있습니다(보유한 AEM Assets 라이선스에 따라 다름).

## 자산 관리

Adobe Experience Manager as a Cloud Services가 프로비저닝된 경우 사용자 계정에 필요한 권한이 있는 경우 Marketo Engage Design Studio와 Adobe Experience Manager Assets as a Cloud Service의 저장소에 액세스할 수 있습니다. 이들 저장소는 분리되어 있으며 동기화되지 않습니다. 두 소스의 이미지를 모두 사용할 수 있습니다.

### Adobe Marketo Engage 자산

Adobe Marketo Engage Design Studio 자산 저장소는 모든 Journey Optimizer B2B 에디션 구독에 기본적으로 제공됩니다. 즉, Adobe Marketo Engage([!UICONTROL Design Studio] > [!UICONTROL 이미지 및 파일])에 저장된 모든 이미지 자산에 액세스할 수 있습니다. 이 저장소를 로컬 자산 라이브러리로 사용할 수 있으며, 자산 업로드 및 다운로드 기능도 제공됩니다. 이들 자산을 여정 콘텐츠에도 사용할 수 있습니다.

Journey Optimizer B2B 에디션에는 Marketo Engage 자산의 편집 작업과 삭제 및 이동 작업을 방지하는 기본 제공 가드레일이 있습니다. 이러한 보호 장치를 통해 Marketo Engage Design Studio의 소스 자산이 유지되는 동시에 Journey Optimizer B2B 에디션에서 원활하게 읽고 재사용할 수 있습니다.

지원되는 파일 형식: JPG, JPEG, GIF, PNG, EPS, SVG 및 RGB

### Adobe Experience Manager Assets as a Cloud Service

Adobe Experience Manager Assets를 사용하여 마케팅과 크리에이티브 워크플로를 통합할 수 있습니다. Adobe Journey Optimizer B2B 에디션과 기본적으로 통합되어 있으므로 Assets as a Cloud Service에 쉽게 액세스하여 디지털 자산을 검색하고 사용할 수 있습니다. 메시지를 작성하는 데 사용할 수 있는 자산의 자산 저장소에도 액세스할 수 있습니다.

Adobe Journey Optimizer B2B 에디션은 Adobe Experience Manager Assets as a Cloud Service에 연결하여 중앙 집중식으로 자산을 관리하고, 이를 통해 크리에이티브 시스템을 확장하며 디지털 자산을 통합하여 경험을 제공할 수 있습니다. Adobe Experience Manager Assets as a Cloud Service는 효율적인 디지털 자산 관리 및 Dynamic Media 작업을 위한 사용하기 쉬운 클라우드 솔루션을 제공합니다. 여기에는 인공 지능과 머신 러닝을 비롯한 고급 기능이 완벽하게 통합되어 있습니다.

[Adobe Experience Manager as a Cloud Service 설명서](https://experienceleague.adobe.com/ko/docs/ experience-manager-cloud-service/content/assets/overview){target="_blank"}에서 자세히 알아보십시오.

{{aem-assets-licensing-note}}

Journey Optimizer B2B 에디션에서 콘텐츠 디자인 왼쪽 탐색 영역의 **[!UICONTROL Experience Manager Assets]** 항목을 통해 Adobe Experience Manager Assets에 직접 액세스할 수 있습니다. 이메일, 이메일 템플릿 및 시각적 조각 콘텐츠를 디자인할 때 자산과 폴더에 액세스할 수도 있습니다.

현재 Adobe Journey Optimizer B2B 에디션에서는 Adobe Experience Manager Assets의 이미지만 사용할 수 있습니다.

## 자산을 사용하여 콘텐츠 작성

자산을 사용하여 이메일, 이메일 템플릿 및 시각적 조각을 작성할 수 있습니다. 시각적 콘텐츠 편집기에서 연결된 자산 저장소의 이미지에 액세스할 수 있습니다. Adobe Marketo Engage Design Studio와 함께(기본값) Experience Manager Assets as a Cloud Service를 구독한 경우 두 소스 중 하나에서 이미지 자산을 선택할 수 있습니다. 이미지 자산을 업로드하여 연결된 Marketo Engage Design Studio 저장소의 Journey Optimizer B2B 에디션 작업 영역에 저장할 수도 있습니다.

이미지 구성 요소의 설정을 편집할 때 이미지 소스를 선택할 수도 있고, 캔버스에서 직접 이미지 소스를 선택할 수도 있습니다.

* **_이미지 구성 요소 설정_** - 시각적 디자이너에서 이미지 구성 요소를 선택하면 오른쪽 패널에서 설정을 보고 편집할 수 있습니다. 구성 요소에 표시되는 이미지 파일을 추가하거나 변경하려면 소스 유형을 선택하고 이미지 파일을 선택합니다.

  ![오른쪽 패널에서 이미지 구성 요소 설정 편집](./assets/content-assets-image-settings.png){width="350"}

* **_빈 구성 요소_** - 시각적 디자이너에 이미지 구성 요소를 추가하면 해당 구성 요소가 비어 있어 소스를 선택하고 이미지 파일을 쉽게 선택할 수 있습니다.

  ![소스를 선택하여 빈 이미지 구성 요소에 대한 이미지 파일 선택](./assets/content-assets-image-component-empty.png){width="500"}

* **_이미지 구성 요소 도구 모음_** - 시각적 디자이너에서 이미지 구성 요소를 선택하면 도구 모음을 통해 소스를 쉽게 선택하고 이미지 파일을 선택할 수 있습니다.

  ![도구 모음을 사용하여 이미지 구성 요소에 대한 이미지 파일을 선택할 소스 선택](./assets/content-assets-image-toolbar-settings.png){width="500"}

콘텐츠를 작성할 때 이미지 자산 소스에 따라 이미지 자산을 추가할 수 있습니다.

>[!BEGINTABS]

>[!TAB Marketo Engage 자산]

**[!UICONTROL Marketo Engage 자산]**&#x200B;를 클릭하면 자산 선택기가 열리고, Marketo Engage 작업 영역 또는 Journey Optimizer B2B 에디션 작업 영역에서 이미지를 선택할 수 있습니다.

![작업 영역에서 이미지 자산 선택](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

검색어와 필터를 사용하여 원하는 이미지 자산을 찾을 수 있습니다. 자산을 선택하고 **[!UICONTROL 선택]**&#x200B;을 클릭하여 이미지 구성 요소에 사용합니다.

Marketo Engage 이미지 자산 사용에 대한 자세한 내용은 [콘텐츠에 자산 사용](./marketo-engage-design-studio.md#use-assets-in-your-content)을 참조하십시오.

>[!TAB Experience Manager Assets]

**[!UICONTROL Experience Manager Assets]**&#x200B;를 클릭하여 자산 선택기를 열면 Experience Manage Assets 저장소에서 이미지를 선택할 수 있습니다.

![AEM Assets 저장소에서 이미지 자산 선택](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

검색어와 필터를 사용하여 원하는 이미지 자산을 찾을 수 있습니다. 자산을 선택하고 **[!UICONTROL 선택]**&#x200B;을 클릭하여 이미지 구성 요소에 사용합니다.

Experience Manager Assets의 이미지 파일 사용에 대한 자세한 내용은 [AEM Assets 이미지 액세스](./aem-assets.md#access-aem-assets-images)를 참조하십시오.

>[!TAB 미디어 가져오기]

**[!UICONTROL 미디어 가져오기]**&#x200B;를 클릭하여 이미지 파일을 선택하고 Journey Optimizer B2B 에디션 콘텐츠에 사용할 수 있는 자산으로 가져옵니다.

![자산으로 가져올 고유한 이미지 파일 선택](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

파일을 드래그 앤 드롭하거나 파일 시스템에서 선택한 후 **[!UICONTROL 가져오기]**&#x200B;를 클릭합니다. 가져온 자산은 Adobe Marketo Engage Design Studio 저장소의 Journey Optimizer B2B 에디션 작업 영역에 저장됩니다.

>[!ENDTABS]
