---
title: 의도 데이터
description: 키워드 매핑으로 의도 데이터를 구성하여 Journey Optimizer B2B edition에서 계정 기반 마케팅을 위한 고객의 관심사와 구매 신호를 예측합니다.
feature: Setup, Intent, Account Insights
roles: Admin
exl-id: c7f9f6fe-2275-42a4-af80-b5c3d1a82837
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 의도 데이터

Journey Optimizer B2B edition에서 의도 감지 모델은 리드의 활동을 기반으로 충분히 높은 신뢰도로 관심 있는 솔루션/제품을 예측합니다. 태그된 콘텐츠와 함께 다른 계정 공동 멤버의 활동도 활용합니다. 사람의 의도는 상품에 대한 관심을 가질 확률로 해석할 수 있다.

* 의도 레벨 - 알려진 리드, 계정 및 구매 그룹 레벨에서 사용할 수 있습니다.
* 의도 신호 유형 - 키워드, 제품 및 솔루션

의도 데이터는 [_지능형 대시보드_](../dashboards/intelligent-dashboard.md), [_계정 세부 정보_ 페이지](../accounts/account-details.md), [_구매 그룹 세부 정보_ 페이지](../buying-groups/buying-group-details.md) 및 [_개인 세부 정보_ 페이지](../accounts/person-details.md)에서 사용됩니다.

![의도 데이터 시각화](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

## 의도 매핑 데이터 준비

이 기능을 활성화하려면 탭을 사용하여 의도 분류법을 정의하여 Microsoft Excel 파일과 같은 스프레드시트를 만듭니다. 전체 스프레드시트는 여러 제품을 가질 수 있는 하나의 카테고리로 업로드되며 각 제품은 여러 키워드를 가질 수 있습니다. 정의하려는 각 범주에 대한 의도 매핑 스프레드시트에 다음 정의를 사용합니다.

* 스프레드시트 이름 = _범주 이름_
* 각 탭 = 제품 이름
* 각 탭에는 하나의 열 = 제품 키워드(최대 150개)가 포함됩니다.

Excel 파일을 다운로드하여 매핑 데이터를 준비하기 위한 템플릿으로 사용할 수 있습니다. 템플릿을 다운로드하려면 다음 작업을 수행하십시오.

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 구성]**&#x200B;을 선택합니다.

1. 중간 패널에서 **[!UICONTROL 의도 매핑]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 범주 만들기]**&#x200B;를 클릭합니다.

1. 대화 상자에서 **[!UICONTROL 파일 템플릿 다운로드]** 링크를 클릭합니다.

   ![의도 데이터 다운로드 템플릿 파일](./assets/intent-data-upload-files.png){width="500"}

1. **[!UICONTROL 취소]**&#x200B;를 클릭합니다.

   완료되면 다시 돌아와 준비된 파일을 업로드할 수 있습니다.

1. 템플릿을 사용하여 의도 매핑 데이터를 정의합니다.

   * 범주 이름을 반영하도록 파일 이름을 변경합니다(예: _규모에 맞는 Personalization_).
   * 제품 이름(예: _Journey Optimizer B2B_, _Marketo Engage_ 및 _Experience Manager_)에 따라 각 탭의 이름을 바꾸십시오.
   * _B2B 마케팅_, _브랜드 인식_, _리드 참여_ 등 각 탭에 대한 제품 키워드를 추가하십시오.

   ![범주 스프레드시트](./assets/intent-category-spreadsheet.png){width="600" zoomable="yes"}

## 범주 파일 업로드

스프레드시트가 준비되면 _[!UICONTROL 의도 매핑]_ 구성 페이지로 돌아가서 파일을 업로드하십시오.

1. **[!UICONTROL 범주 만들기]**&#x200B;를 클릭합니다.

1. 파일을 _[!UICONTROL 파일 업로드]_ 대화 상자로 끌어다 놓거나 **[!UICONTROL 파일 선택]**&#x200B;을 클릭하여 시스템에서 파일을 찾아 선택합니다.

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   사전 처리 작업은 유사한 키워드를 클러스터링하기 위해 실행되므로 의도 탐지가 향상되고 키워드 희석이 방지됩니다. 이 사전 처리가 완료되는 즉시 펄스 알림이 표시됩니다(데이터에 따라 최대 15분).

   ![펄스 알림](./assets/intent-data-upload-files-pre-process.png){width="500"}

   결과는 _의도 매핑_ 페이지에 표시됩니다.

   ![승인을 위해 업로드된 의도 범주](./assets/intent-data-category-approve.png){width="600" zoomable="yes"}

## 범주 승인 또는 거부

범주 목록을 검토하고 **[!UICONTROL 승인]**&#x200B;을 클릭하여 지능형 대시보드, 계정 세부 정보 페이지, 구매 그룹 세부 정보 페이지 및 개인 세부 정보 페이지에서 사용할 키워드를 활성화합니다. 각 제품에 대한 전체 목록을 표시하려면 **[!UICONTROL 모두 보기]**&#x200B;를 클릭하고, 전체 목록을 Excel 파일로 검토하려면 **[!UICONTROL 다운로드]**&#x200B;를 클릭하십시오.

목록에 만족하지 않으면 **[!UICONTROL 삭제]**&#x200B;를 클릭하여 범주를 제거할 수 있습니다. 그런 다음 업로드 프로세스를 다시 시작하기 전에 스프레드시트 파일을 조정하여 해당 범주를 정의할 수 있습니다.

>[!IMPORTANT]
>
>다른 범주를 추가하거나 범주를 편집하려면 먼저 새 범주를 승인 또는 거부(삭제)해야 합니다.

다른 범주를 추가하고 해당 분류법이 기존 범주에 영향을 주는 경우 경고가 표시됩니다. 카테고리를 승인하거나 거부하기로 결정할 때 이 영향을 고려하십시오. 제품을 둘 이상의 카테고리에 사용하는 경우 제품-키워드 매핑은 모든 카테고리에서 동일해야 합니다.

![기존 범주 영향 경고](./assets/intent-data-category-overlap.png){width="600" zoomable="yes"}
