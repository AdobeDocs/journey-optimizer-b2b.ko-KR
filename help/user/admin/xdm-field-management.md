---
title: XDM 필드 관리
description: XDM 필드 관리를 사용하여 Journey Optimizer B2B edition에서 사용할 수 있는 데이터를 제어합니다.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
source-git-commit: 0497f44336cdd6bfed5bac9f6f579a97f6be585a
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 1%

---


# XDM 필드 관리

XDM(경험 데이터 모델) 필드는 [!DNL Journey Optimizer B2B Edition] 응용 프로그램에 데이터를 제공하는 스키마 요소입니다. XDM 필드를 여정, 구매 그룹 및 이메일 개인화 및 조건부 콘텐츠와 같은 기능에서 필터 및 제약 조건으로 사용합니다.

스키마는 표준 XDM 클래스를 기반으로 필드를 정의합니다. 표준 XDM 클래스에는 개인 프로필, 비즈니스 계정 및 경험 이벤트가 포함됩니다. 또한 관계형 스키마는 기존의 관계형 데이터베이스와 유사하게 구조화된 데이터를 모델링할 수 있는 필드를 정의합니다.

Adobe Experience Platform(AEP) 스키마에는 일반적으로 복잡한 계층의 많은 필드가 포함됩니다. XDM 스키마 트리 트래버스에는 시간이 소요됩니다. XDM 필드 관리에서는 각 여정과 관련된 필드만 표시하여 필드 선택을 간소화합니다. 관리자는 여정 작성자에 대해 표시되는 필드를 제어합니다. 또한 관리자는 필드를 읽기 전용 또는 편집 가능으로 설정합니다. 이러한 작업은 여정 설계 중 효율성을 개선합니다.

XDM을 이해하고 데이터 엔지니어 또는 B2B 고객 데이터 플랫폼(CDP) 데이터 모델링 이해 당사자와 공동 작업하는 관리자는 이 페이지의 절차를 사용해야 합니다.

>[!NOTE]
>[관계형 스키마](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#)를 [!DNL Journey Optimizer B2B Edition]에서 제한된 가용성 릴리스로 사용할 수 있습니다. Journey Optimizer Orchestrated campaigns 라이선스 소유자는 Data Mirror 및 관계형 스키마를 사용할 수 있습니다. 라이선스 및 기능 활성화에 따라 Customer Journey Analytics 사용자를 위한 제한된 릴리스로도 관계형 스키마를 사용할 수 있습니다. 액세스하려면 Adobe 담당자에게 문의하십시오.

## XDM 클래스 액세스

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 구성]**&#x200B;을 선택합니다.

1. 중간 패널에서 **[!UICONTROL XDM 클래스]**&#x200B;를 클릭합니다.

   * **[!UICONTROL 표준]** 및 **[!UICONTROL 관계형]** 탭을 사용하여 새 필드를 추가하고 Journey Optimizer B2B edition에서 사용할 수 있도록 설정하십시오.

   * **이벤트** 탭을 사용하여 [특정 AEP Experience 이벤트 및 관련 필드를 선택](./configure-aep-events.md)하여 여정 이벤트 노드에 사용하십시오.

## 필드 선택

>[!IMPORTANT]
>
>언제든지 새 필드를 선택하거나 더 이상 필요하지 않은 필드를 선택 취소하여 필드 선택을 업데이트할 수 있습니다. 이 스키마를 사용하여 여정을 게시하면 스키마 구조를 잠급니다. 스키마 삭제 또는 이름 변경, 새 필드 추가 또는 필드 유형 변경은 지원되지 않으며 여정 오류가 발생할 수 있습니다.

필드를 선택하려면 다음 지침을 사용하십시오.

* 스키마가 여정에서 활발하게 사용된 후에만 새 필드를 추가할 수 있습니다.
* 필드 유형을 삭제, 이름 변경 또는 변경하면 여정 기능에 문제가 발생할 수 있습니다. 스키마를 조작할 때 주의하십시오.
* 스키마 이름을 바꾸거나 삭제하거나 관계형 스키마의 키를 수정하지 마십시오.

### 표준 클래스

_[!UICONTROL 표준]_ 탭에서 표준 클래스에 대한 _관리되는 필드_ 및 _업데이트할 수 있는 필드_&#x200B;를 편집할 수 있습니다.

* 관리 필드는 여정, 구매 그룹 및 개인화 기능에 표시됩니다.
* 업데이트할 수 있는 필드는 _계정 프로필 업데이트_ 및 _개인 프로필 업데이트_ 여정 노드에 대한 제약 조건 역할을 합니다.

![XDM 클래스 구성을 표시하는 표준 클래스 탭](assets/xdm-standard.png){width="600" zoomable="yes"}

이 목록에는 두 개의 클래스가 포함됩니다.

* **[!UICONTROL XDM 개별 프로필]**
* **[!UICONTROL XDM 비즈니스 계정]**

표시되는 클래스 정보는 다음과 같습니다.

* 관리되는 필드 수
* 업데이트할 수 있는 필드 수
* 마지막 업데이트 시간

표준 XDM 클래스의 유니온 스키마에서 필드를 선택하려면 클래스 이름을 클릭하여 _관리되는 필드_ 선택 대화 상자를 열거나 _추가 메뉴_(**...** ) 아이콘을 클릭하여 _[!UICONTROL 관리되는 필드]_&#x200B;와 _[!UICONTROL 업데이트할 수 있는 필드]_ 중에서 선택하십시오.

![관리 필드와 업데이트할 수 있는 필드 중에서 선택하려면 기타 메뉴 아이콘을 클릭하세요](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>필드는 먼저 _관리_&#x200B;되어야 _업데이트할 수 있음_&#x200B;이 됩니다. 선택한 _업데이트할 수 있는 필드_&#x200B;은(는) 사용자 제공 스키마에 있어야 합니다. 스키마에는 시스템 정의 필드를 제외한 필수 필드가 포함되지 않을 수 있습니다.

#### 관리되는 필드

**[!UICONTROL 관리되는 필드]**&#x200B;를 선택하면 _필드 선택_ 대화 상자에 구성 가능한 모든 필드가 나열됩니다.

1. 각 XDM 클래스에 대해 최대 100개의 필드를 선택합니다.

   _[!UICONTROL 검색]_ 필드를 사용하여 표시된 목록을 이름별로 필터링하십시오. **[!UICONTROL 선택한 필드만 표시]** 슬라이더를 사용하여 현재 선택 항목을 검토하십시오.

   구성 가능한 필드 옵션을 표시하는 표준 XDM 클래스에 대한 ![관리되는 필드 선택 대화 상자](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. 선택 내용을 확인하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

#### 업데이트할 수 있는 필드

업데이트할 수 있는 필드를 구성하려면 먼저 해당 필드가 사용자 지정 데이터 세트에 있어야 합니다. 사용자 지정 데이터 집합 워크플로에 대한 설명은 [데이터 집합 만들기 및 데이터 수집](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data#){target="_blank"}을 참조하고 **[!UICONTROL 스키마에서 데이터 집합 만들기]** 옵션을 사용하십시오. 이 데이터 세트는 업데이트할 수 있는 필드를 분리하는 데 사용됩니다. 업데이트할 수 있는 모든 필드는 이 데이터 세트에 있어야 합니다.

개별 프로필에 대한 데이터 세트를 만들고 비즈니스 계정에 대한 데이터 세트를 만듭니다. 구성 프로세스 중에 각 새 데이터 세트를 선택합니다.

1. **[!UICONTROL 데이터 세트]**&#x200B;에 대해 만든 새 데이터 원본을 선택하십시오.
1. 선택한 데이터 세트에서 필드를 선택합니다.

   ![XDM 스키마 구성의 데이터 세트에서 업데이트할 수 있는 필드를 선택하는 대화 상자](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. 변경 내용을 적용하려면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

### 관계형 스키마

관계형 스키마를 사용하면 사용자 정의 데이터 클래스를 생성할 수 있습니다. 여러 데이터 세트에 액세스하여 데이터 요구 사항에 맞게 클래스를 만들 수 있습니다. 여정 결정 및 이메일 개인화에서 구매, 라이선스 및 이벤트 등록과 같은 비즈니스 엔터티에 대해 관계형 스키마를 사용합니다. 스키마당 최대 50개의 스키마와 최대 100개의 필드를 선택할 수 있습니다.

선택한 필드를 고급 전자 메일 개인화에 사용하는 방법에 대한 자세한 내용은 [콘텐츠 개인화](../content/personalization.md#custom-datasets)를 참조하십시오.

>[!NOTE]
>
>이 기능은 현재 계정 관련 사용자 지정 개체 사용 사례를 지원하며, 향후 더 많은 기본 개체 사용 사례를 지원할 계획입니다.

스키마 편집기를 사용하여 관계형 스키마를 만들 수 있습니다(왼쪽 탐색 영역에서 **[!UICONTROL 데이터 관리]** > **[!UICONTROL 스키마]**(으)로 이동).

[!DNL Journey Optimizer B2B Edition]에 사용할 스키마를 만들 때 다음 구성 값이 필요합니다.

* 동작: 레코드
* 세그먼테이션: 활성화됨
* 관계 유형: 다대일
* 참조 스키마: B2B 계정
* 필수 필드: 기본 키, 외래 키 및 버전 설명자
* 관련 데이터 세트: 스키마에 정의 및 매핑됨

[!DNL Journey Optimizer B2B Edition]에서 사용할 관계형 스키마 필드를 선택하려면 다음을 수행하십시오.

1. 스키마를 보려면 **[!UICONTROL 관계형]** 탭을 선택하십시오.

   Adobe Journey Optimizer B2B edition에 대한 비즈니스 엔터티 필드를 표시하는 스키마 편집기의 ![관계형 스키마 탭](assets/xdm-relational.png){width="600" zoomable="yes"}

1. **[!UICONTROL 관계형 XDM 스키마 선택]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >이 Beta 기능 릴리스에서는 _다대일 사용자 지정 개체 계정_&#x200B;만 지원됩니다.

1. 관계형 스키마를 선택하고 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >이 Beta 기능 릴리스에서는 스키마를 선택한 후 목록에서 제거할 수 없습니다.

   ![대화 상자에서 관계형 스키마 선택](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. 네임스페이스를 입력하거나 기본 네임스페이스를 사용하십시오. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   네임스페이스는 한 번만 설정할 수 있으며 이 작업을 되돌릴 수 없습니다.

   ![네임스페이스 만들기 대화 상자의 기본 네임스페이스](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. 관계형 스키마 필드를 검토합니다.

   필드 메타데이터를 보려면 _정보_ ![정보 아이콘](../assets/do-not-localize/icon-info-light.svg) 아이콘을 클릭하십시오.

1. 여정 및 개인화에 대해 활성화할 필드를 선택합니다.

   플랫폼은 다음 필수 필드를 자동으로 선택합니다.

   * 외래 키
   * 기본 키
   * 버전 설명자

   _[!UICONTROL 검색]_ 필드를 사용하여 표시된 목록을 이름별로 필터링하십시오. **[!UICONTROL 선택한 필드만 표시]** 슬라이더를 사용하여 현재 선택 항목을 검토하십시오.

   ![대화 상자에서 관계형 스키마의 필드 선택](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
