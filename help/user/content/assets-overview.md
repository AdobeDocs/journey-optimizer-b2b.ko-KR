---
title: 자산
description: Journey Optimizer B2B edition의 에셋 관리에 대해 알아봅니다.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 23fb478712f3c6df59e94432bdf16883e6acf70b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# 자산

Adobe Journey Optimizer B2B edition에서 에셋은 일반적으로 여정 콘텐츠를 만드는 데 사용되는 이미지입니다. 자산 선택기 또는 시각적 컨텐츠 편집기 내의 간단한 드래그 앤 드롭 인터페이스를 통해 Journey Optimizer B2B edition에서 작성된 이메일, 이메일 템플릿 및 조각에서 이러한 이미지를 사용할 수 있습니다.

Adobe Journey Optimizer B2B edition은 마케터에게 Adobe Marketo Engage Design Studio와 Adobe Experience Manager Assets as a Cloud Service 의 두 가지 유형의 자산 라이브러리에 대한 액세스를 제공합니다. Adobe Marketo Engage Design Studio만 사용하거나 보유하고 있는 AEM Assets 라이선스에 따라 구성된 두 라이브러리를 동시에 사용할 수 있습니다.

## 자산 관리

Marketo Engage 계정과 Cloud Service으로서의 Adobe Experience Manager을 사용하여 프로비저닝된 경우, 사용자 계정에 필요한 권한이 있을 때 Marketo Engage DAM 및 Adobe Experience Manager Assets as a Cloud Service 모두에 대한 저장소에 액세스할 수 있습니다. 이러한 저장소는 분리되어 있으며 동기화되지 않습니다. 두 소스 중 하나에서 이미지를 사용할 수 있지만 콘텐츠 편집기에서 한 번에 하나만 활성화할 수 있습니다. 관리자는 Marketo Engage DAM에서 Adobe Experience Manager Assetsas a Cloud Service 로 전환할 수 있습니다. 왼쪽 탐색의 _[!UICONTROL Assets]_ 항목에는 현재 설정된 저장소가 표시됩니다.

### Adobe Marketo Engage assets

Adobe Marketo Engage Design Studio 에셋 저장소는 모든 Journey Optimizer B2B edition 구독과 함께 기본적으로 제공됩니다. 즉, Adobe Marketo Engage > [!UICONTROL Design Studio] > [!UICONTROL 이미지 및 파일]에 저장된 이미지 자산에 액세스할 수 있습니다. 에셋 업로드 및 다운로드 기능을 포함하여 이 저장소를 로컬 에셋 라이브러리로 사용할 수 있습니다. 여정 컨텐츠 내에서 이러한 자산을 사용할 수도 있습니다.

Journey Optimizer B2B edition의 Marketo Engage 에셋을 편집하고 작업을 삭제 및 이동할 수 없는 내장 보호 기능이 있습니다. 이러한 보호를 통해 소스 에셋(Marketo Engage Design Studio)을 유지 관리하는 동시에 Journey Optimizer B2B edition에서 원활한 읽기 및 재사용이 가능합니다.

지원되는 파일 형식: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Adobe Experience Manager Assets을 사용하여 마케팅 및 크리에이티브 워크플로우를 결합합니다. Adobe Journey Optimizer B2B edition과 기본적으로 통합되어 있으므로 Assetsas a Cloud Service 에 쉽게 액세스하여 디지털 에셋을 검색하고 사용할 수 있습니다. 메시지를 채우는 데 사용할 수 있는 에셋에 대한 Assets 저장소에 대한 액세스 권한을 제공합니다.

Adobe Experience Manager Assets은 크리에이티브 시스템을 확장하고 경험 전달을 위해 디지털 에셋을 통합하는 중앙 집중식 에셋 작업 공간을 위해 Adobe Experience Manager Assetsas a Cloud Service 에 연결할 수 있습니다. 효율적인 디지털 에셋 관리 및 Dynamic Media 운영을 위한 Adobe Experience Manager Assets as a Cloud Service 클라우드 솔루션입니다. 인공 지능과 머신 러닝을 포함한 고급 기능을 매끄럽게 통합합니다.

자세한 내용은 [Adobe Experience Manager as a Cloud Service 설명서](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/overview)를 참조하세요.

Adobe Experience Manager Assets은 왼쪽 탐색 메뉴의 **[!UICONTROL Assets]** 항목에서 Adobe Journey Optimizer B2B edition 내에서 직접 액세스할 수 있습니다. 이메일 콘텐츠를 디자인할 때 에셋 및 폴더에 액세스할 수도 있습니다.

>[!NOTE]
>
>이 통합을 위해 AEM Assets as Cloud Service 및 Dynamic Media 라이선스가 전제 조건입니다.<br/>
>Adobe Experience Manager Assets as a Cloud Service 계약 및 구성에 따라 왼쪽 메뉴 Assets 섹션을 통해 Adobe Journey Optimizer B2B edition에 직접 액세스할 수 있습니다. 이메일 콘텐츠를 디자인할 때 에셋 및 폴더에 액세스할 수도 있습니다.

현재 Adobe Journey Optimizer B2B edition에서는 Adobe Experience Manager Assets 이미지만 사용할 수 있습니다.

## 컨텐츠 작성에 자산 사용

이메일, 이메일 템플릿 및 시각적 조각을 작성할 때 에셋을 사용합니다. 시각적 콘텐츠 편집기 UI는 연결된 자산 저장소의 이미지에 대한 액세스를 제공합니다.

### 자산 소스 선택

기본 Adobe Marketo Engage Design Studio와 함께 Experience Manager Assets as a Cloud Service에 대한 구독이 있는 경우 두 소스 중 하나에서 이미지 에셋을 선택할 수 있습니다. 이렇게 하려면 새 이메일, 이메일 템플릿 또는 시각적 조각을 만들 때 이미지 소스를 선택해야 합니다. 또는 콘텐츠를 편집할 때 이미지 소스를 선택할 수 있습니다. 선택 사항은 편집 경험에만 적용되며, 필요한 경우 이미지 소스를 변경하여 다른 라이브러리의 에셋에 액세스할 수 있습니다.

_**콘텐츠 리소스 만들기**_ - 전자 메일, 전자 메일 템플릿 또는 조각을 만들 때 이미지 소스를 선택하려면 대화 상자에서 **[!UICONTROL 이미지 소스]**&#x200B;를 설정하십시오.

_**콘텐츠 리소스 편집**_ - 시각적 미리 보기에서 이미지 에셋 소스를 선택하려면 오른쪽 패널의 **[!UICONTROL 이미지 소스]** 설정을 사용하십시오.

### 콘텐츠에 자산 추가

콘텐츠를 작성할 때 선택한 이미지 에셋 소스에 따라 이미지 에셋을 추가할 수 있습니다.

>[!BEGINTABS]

>[!TAB Marketo Engage 이미지 자산 추가]

다음 방법 중 하나를 사용하여 Marketo Engage 에셋을 추가할 수 있습니다.

* 구조 요소를 추가한 다음 왼쪽 탐색 메뉴에서 시각적 캔버스로 에셋을 드래그 앤 드롭합니다.
* 구조 요소를 추가한 다음 _이미지_ 콘텐츠 형식을 구조에 끌어다 놓습니다. 오른쪽의 속성 설정에서 이미지를 지정하는 두 가지 방법이 있습니다.
   * **[!UICONTROL 찾아보기]**&#x200B;를 클릭하여 자산 선택기를 엽니다. 이 선택기에서 Adobe Marketo Engage Design Studio 자산 라이브러리에서 이미지를 선택할 수 있습니다.
   * 로컬 시스템에서 에셋을 가져오려면 **[!UICONTROL 미디어 가져오기]**&#x200B;를 클릭하십시오. 가져온 자산은 Adobe Marketo Engage Design Studio 라이브러리의 Assets 루트 폴더 내에 저장됩니다.

자세한 내용은 [콘텐츠의 에셋 사용](./marketo-engage-design-studio.md#use-assets-in-your-content)을 참조하십시오.

이미지를 변경하려면 오른쪽의 속성에서 이미지에 대한 소스 URL을 업데이트할 수 있습니다.

>[!TAB Experience Manager Assets 이미지 추가]

1. 이메일 디자이너에서 이메일 콘텐츠를 작성하는 동안 이미지 요소를 캔버스로 드래그합니다.

   오른쪽의 속성은 이미지 요소 선택을 반영합니다.

1. **[!UICONTROL 에셋 선택]**&#x200B;을 클릭하여 Experience Manager 에셋 선택기를 엽니다.

   여기에서 원하는 컨텐츠 자산을 검색, 필터링 및 액세스하여 마케팅 자산에 추가할 수 있습니다. 선택기 사용 방법에 대한 자세한 내용은 이 페이지 를 참조하십시오.

   >[!NOTE]
   >
   >저장소가 두 개 이상 구성된 경우 에셋 선택기에서 저장소 전환기를 사용할 수 있습니다

1. 이메일에 삽입할 자산을 선택합니다.

>[!ENDTABS]
