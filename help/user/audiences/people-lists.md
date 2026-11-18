---
title: 사용자 목록
description: Journey Optimizer B2B Edition에서 사용자 목록과 사용자 목록을 탐색, 보기, 편집, 삭제 및 사용하는 방법을 알아봅니다.
feature: Audiences
role: User
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
    internal-label: Audience segmentation
source-git-commit: d713d57bddf2ac6f8cf7e7a7d163281f607d729c
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%
---

# 사용자 목록

[!DNL Journey Optimizer B2B Edition]에서 사용자 목록은 여정 간에 다시 사용할 수 있는 사용자 프로필의 명명된 컬렉션입니다. 모든 여정에서 동일한 필터 세트를 다시 만드는 대신 한 번 사용자 그룹을 정의하고 필요한 모든 위치에서 참조합니다. 예를 들어, 직원 목록을 사용하여 내부 직원이나 기존 고객을 육성 여정에서 제외시키거나, 한 여정에서 단계를 완료한 직원을 추적하여 다른 여정이 이를 처리할 수 있도록 할 수 있습니다.

사람 목록에는 두 가지 유형이 있습니다.

* **[!UICONTROL 정적]** - 명시적으로 사용자를 추가하거나 제거하는 경우에만 구성원 자격이 변경됩니다. 필터 세트를 적용하여 현재 개인 데이터를 기반으로 목록을 채워 사용자를 추가하거나, 계정 또는 개인 여정을 통해 사용자를 추가 및 제거할 수 있습니다. [정적 사용자 목록](./people-lists-static.md)을 참조하세요.
* **[!UICONTROL 동적]** - 목록을 자동으로 조정하기 위해 규칙 집합(필터)을 정의합니다. 규칙 정의에 대해 자격이 되거나 자격을 상실하면 목록이 동적으로 새로 고쳐집니다. [동적 사용자 목록](./people-lists-dynamic.md)을 참조하세요.

[계정 여정 및 개인 여정의 사용자 목록을 사용](./people-lists-journeys.md)하여 목록 멤버십에 따라 경로를 분할하고 정적 목록에 사용자를 추가하거나 정적 목록에서 사용자를 제거할 수 있습니다.

>[!NOTE]
>
>사용자 목록에는 이미 동기화되어 [!DNL Journey Optimizer B2B Edition]에서 사용할 수 있는 사용자 프로필이 포함되어 있습니다. 목록을 평가할 때 [!DNL Adobe Experience Platform] 대상에서 프로필을 직접 읽지 않습니다.

## 직원 목록 액세스 및 찾아보기 {#access-browse}

왼쪽 탐색에서 사람 목록에 액세스하여 목록 멤버십을 보고, 만들고, 관리합니다.

>[!AVAILABILITY]
>
>다음 제품 권한은 사용자 목록에 대한 액세스를 제어합니다.
>
>* [!UICONTROL B2B 사용자 목록 관리] - 사용자 목록을 보고, 만들고, 편집하고, 삭제합니다.
>* [!UICONTROL B2B 사용자 목록 보기] - 사용자 목록 및 해당 구성원 보기(읽기 전용).
>
>권한 할당에 대한 자세한 내용은 [사용자 액세스 및 권한](../admin/user-management.md#b2b-product-permissions)을 참조하세요.

* 왼쪽 탐색에서 **[!UICONTROL 계정]**&#x200B;을 확장하고 **[!UICONTROL 사람 목록]**&#x200B;을 선택합니다.

* **[!UICONTROL 동적 목록]** 또는 **[!UICONTROL 정적 목록]**&#x200B;을 선택하여 두 목록 형식 간에 전환합니다.

* 목록 상단의 _검색_ 필드에 텍스트를 입력하여 표시된 목록을 이름별로 필터링합니다.

  ![사람 목록에 액세스하여 사용자 수준의 대상자를 관리할 수 있습니다](./assets/people-lists-browse-search.png){width="800" zoomable="yes"}

* 오른쪽 상단의 _열 설정_( ![열 설정 아이콘](../assets/do-not-localize/icon-column-settings-new.svg) ) 아이콘을 클릭하여 표시된 열을 선택하거나 지웁니다.

* 열의 너비를 변경하려면 열 머리글 사이의 구분선을 끕니다.

각 탭에는 **[!UICONTROL 이름]**, **[!UICONTROL 마지막 업데이트]**, **[!UICONTROL 업데이트한 사람]**, **[!UICONTROL 만든 날짜]** 및 **[!UICONTROL 만든 사람]** 열이 포함되어 있습니다. 세부 정보를 보려면 사람 목록 이름을 클릭합니다.

이 페이지에서는 다음 작업도 수행할 수 있습니다.

* 새 동적 및 정적 목록을 만듭니다.
* 목록을 열고 [현재 구성원을 검토](#view-list-members)합니다.
* 목록에 대한 _추가 작업_( **...** ) 아이콘을 클릭하고 [편집](#edit-list-properties) 또는 [삭제](#delete-people-list)을 선택합니다.

## 사람 목록 만들기 {#create-people-list}

1. _[!UICONTROL 사람 목록]_ 페이지의 오른쪽 상단에 있는 **[!UICONTROL 목록 만들기]**&#x200B;를 클릭합니다.

   ![사람 목록 만들기 대화 상자](./assets/people-list-create-dialog.png){width="450"}

1. 목록에 **[!UICONTROL 이름]**(필수)과 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   이름은 최대 180자를 포함할 수 있으며 동일한 유형의 목록에서 고유해야 합니다. 설명에는 최대 2,000자가 포함될 수 있습니다.

1. **[!UICONTROL 유형]** 목록 선택:

   * [**[!UICONTROL 정적]**](./people-lists-static.md) - 자격 필터는 목록에 적용할 때 구성원 자격을 결정합니다. 수동으로 사람을 추가하거나 여정이 추가하거나 제거하는 경우에만 멤버십이 업데이트됩니다.
   * [**[!UICONTROL 동적]**](./people-lists-dynamic.md) - 자격 필터는 구성원 자격을 동적으로 결정합니다. 멤버십이 자동으로 새로 고쳐집니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

   새 사람 목록이 세부 정보 페이지에 열리고, 필터 편집기가 열려 목록의 사람을 정의할 수 있습니다. 정적 목록에 사용자를 추가하려면 하나 이상의 필터를 적용합니다. 동적 목록의 경우 목록 멤버십에 대한 규칙을 정의합니다.

## 목록 구성원 보기 {#view-list-members}

직원 목록의 세부 정보 페이지에서 **[!UICONTROL 구성원]** 목록에 목록에 있는 사람이 표시됩니다. 목록의 총 인원수가 테이블 맨 위에 표시됩니다.

멤버 테이블에는 다음 열이 포함되어 있습니다.

* **[!UICONTROL 이름]**
* **[!UICONTROL 전자 메일 주소]**
* **[!UICONTROL 직책]**
* **[!UICONTROL 회사]**
* **[!UICONTROL 구독 취소됨]**
* **[!UICONTROL 만든 날짜]**
* **[!UICONTROL 마지막 수정일]**

기본적으로 구성원은 **[!UICONTROL 마지막 수정 날짜]**&#x200B;별로 정렬되며 가장 최근에 수정된 사람을 먼저 표시합니다. **[!UICONTROL 이름]**, **[!UICONTROL 전자 메일 주소]** 또는 **[!UICONTROL 만든 날짜]**&#x200B;별로 정렬할 수도 있습니다.

* 특정 구성원을 찾으려면 _검색_ 필드를 사용하십시오. 이름, 이메일 주소 또는 회사로 검색할 수 있습니다.
* 표시할 열을 선택하려면 _열 설정_ 아이콘을 클릭하고 확인란을 선택하거나 선택을 취소합니다. _[!UICONTROL 이름]_ 열은 항상 표시됩니다.
* 최신 멤버십을 보려면 _[!UICONTROL 기타]_ 메뉴를 사용하여 **[!UICONTROL 구성원 새로 고침]**&#x200B;을 선택하세요.
* 사용자에 대한 자세한 정보를 보려면 해당 사용자의 이름을 클릭하여 [개인 세부 정보](../accounts/person-details.md) 페이지를 엽니다. 이 페이지에서 해당 사용자의 요약 및 최근 활동을 볼 수 있습니다.

## 사람 목록 속성 편집 {#edit-list-properties}

정적 또는 동적 사람 목록의 이름과 설명을 변경할 수 있습니다.

1. 다음 방법 중 하나를 사용하여 _[!UICONTROL 목록 편집]_ 대화 상자를 엽니다.

   * _[!UICONTROL 인물 목록]_ 페이지에서 목록의 _추가 작업_(**...**) 아이콘을 클릭하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.
   * 목록의 세부 정보 페이지에서 **[!UICONTROL 목록 속성 편집]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 이름]** 또는 **[!UICONTROL 설명]**&#x200B;을(를) 업데이트합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 사람 목록 삭제 {#delete-people-list}

>[!IMPORTANT]
>
>사용자 목록 삭제는 영구적이며 실행 취소할 수 없습니다. 활성 여정이 사용 중인 사람 목록은 삭제할 수 없습니다.

1. 다음 방법 중 하나를 사용하여 목록을 삭제합니다.

   * _[!UICONTROL 사람 목록]_ 페이지에서 목록 이름 옆에 있는 _추가 작업_(**...**) 아이콘을 클릭하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.
   * 목록의 세부 정보 페이지에서 **[!UICONTROL 목록 삭제]**&#x200B;를 클릭합니다.

1. 확인 대화 상자에서 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.
