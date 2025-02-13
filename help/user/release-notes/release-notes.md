---
title: 릴리스 정보
description: Adobe Journey Optimizer B2B 에디션 최신 릴리스 정보
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 24e39a532903ae2ca389f7c1a761ec7b5e03157d
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 9%

---

# Journey Optimizer B2B edition 릴리스 노트

Adobe Journey Optimizer B2B edition은 새로운 기능, 기존 기능 개선 사항 및 버그 수정 사항을 지속적으로 제공합니다.

Journey Optimizer B2B edition은 기본적으로 [!DNL Adobe Experience Platform]을(를) 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/latest){target="_blank"}를 참조하십시오.

자격, 성능 보호 및 제한 사항에 대한 자세한 내용은 [제품 설명](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}을 검토하십시오.

## 2025년 1월 릴리스 정보 {#Jan-2025}

**릴리스 날짜**: 2025년 2월 6일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 새로운 기능 | 경험 이벤트 전달 | 관리자는 Adobe Experience Platform(AEP) 기반 이벤트 정의를 구성할 수 있습니다. 이러한 구성을 통해 마케터는 AEP 경험 이벤트에 반응하는 계정 여정을 만들 수 있습니다.  <a href="../admin/configure-aep-events.md">자세히 알아보기</a> |
| 새로운 기능 | 유료 미디어 대상 | LinkedIn과 같은 광고 플랫폼에서 더 많이 참여할 수 있도록 계정 여정에서 알려진 사람에게 유료 미디어 캠페인을 검증합니다. 계정 여정의 분할된 경로 노드를 사용하여 특정 동작에 따라 계정 대상을 세그먼트화하고 추가 참여를 보장하는 계정을 식별합니다. 그런 다음 지원되는 유료 미디어 대상에 Real-Time CDP를 통해 이러한 계정의 사용자를 외부 고객 대상에 추가합니다. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">자세히 알아보기</a> |
| 새로운 기능 | 지능형 대시보드 | 보다 지능적인 분석과 정확한 계정 우선 순위를 위해 AI가 생성한 인사이트를 포함하여 계정 여정을 통해 구매 그룹의 진행 상황을 볼 수 있습니다. <a href="../dashboards/intelligent-dashboard.md">자세히 알아보기</a> |
| 새로운 기능 | 구매 그룹 및 계정 세부 정보 | 고객과 관계를 시작할 때 더 많은 컨텍스트 및 내역 데이터를 갖도록 구매 그룹 및 계정 수준에서 인사이트를 봅니다.<p>구매 그룹 세부 사항에는 감지된 모든 자사 의도가 포함됩니다. <a href="../buying-groups/buying-group-details.md">자세히 알아보기</a><p>계정 세부 정보 계정은 감지된 참여 급증을 강조하므로 사용자 지정된 판매 중심의 참여를 수행할 준비가 된 계정에 대해 영업을 경고할 수 있습니다.  <a href="../accounts/account-details.md">자세히 알아보기</a> |
| 새로운 기능 | 여정 개요 | 계정 여정에 액세스하면 개요 탭에서는 활성 계정 여정에 대한 포괄적인 스냅숏을 제공하며, 완료를 범주화하고 수량화하는 원 및 막대 차트, 참여 활동을 사용하여 계정 진행 상황을 자세히 설명합니다.  <a href="../dashboards/journeys-dashboard.md">자세히 알아보기</a> |
| 새로운 기능 | Adobe Express 이미지 편집 | Adobe Express 빠른 작업 을 사용하면 이미지를 간단하게 편집(자르기 및 크기 조정 등)하여 콘텐츠를 보다 세련되게 볼 수 있습니다. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">자세히 알아보기</a>  <p>보다 포괄적인 디자인 도구 세트의 경우, 이 통합을 통해 Journey Optimizer B2B edition에 전체 Adobe Express 라이선스를 제공할 수 있습니다. 이 설정을 사용하면 로컬 자산 작업 영역 내에서 전체 Adobe Express 사용자 인터페이스에 액세스할 수 있습니다. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">자세히 알아보기</a> |
| 새로운 기능 | 그룹 역할 구매를 위한 인텐트 필터 | 의도 키워드를 제출하면 의도 감지 모델은 리드의 활동을 기반으로 충분히 높은 신뢰도로 관심 있는 솔루션/제품을 예측합니다. <a href="../admin/intent-data.md">자세히 알아보기</a> <p>이 의도 데이터는 구매 그룹 역할 조건을 정의하는 데 사용할 수 있습니다. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">자세히 알아보기</a> |
| 개선 사항 | 여정의 Marketo Engage 이벤트 지원 | 이제 _이벤트 수신_ 여정 노드에서 사용자 수준의 두 개의 Marketo Engage 이벤트를 지원합니다. _웹 페이지 방문_ 및 _양식 작성_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">자세히 알아보기</a> |
| 개선 사항 | Marketo Engage 스마트 목록용 그룹 필터 구매 | Marketo Engage에서 구매 그룹 필터를 사용하여 스마트 목록을 보고 만들 수 있습니다. 이렇게 추가된 필터를 사용하면 Journey Optimizer B2B edition 내의 계정 여정에서 Marketo Engage 캠페인 및 프로그램 전반의 구매 그룹 구성원을 억제하고 포함할 수 있습니다. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">자세히 알아보기</a> |
| 개선 사항 | 여정 및 역할에 대한 Marketo Engage 목록 멤버십 필터 | Journey Optimizer B2B에서 여정 활동에서 중복을 제거하는 데 도움이 되도록 _사람별 분할 경로_ 노드에 대한 조건으로 Marketo Engage 목록 멤버십을 확인합니다. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">자세히 알아보기</a> <p> 그룹 역할 템플릿을 구매하려면 목록 멤버십을 역할 조건으로 사용하십시오. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">자세히 알아보기</a> |
| 개선 사항 | 참여 개요 대시보드 | 이 대시보드는 참여에 대한 포괄적인 보기를 제공하도록 업데이트됩니다. 스냅샷 원 차트 및 트렌드 표시 선 차트를 통해 계정 및 개별 상호 작용에 대한 실시간 지표를 보여줍니다. <a href="../dashboards/engagement-dashboard.md">자세히 알아보기</a> |


## 2024년 10월 릴리스 정보 {#Oct-2024}

**릴리스 날짜**: 2024년 10월 29일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 새로운 기능 | 이메일 템플릿의 조건부 콘텐츠 | 계정 및 리드 수준에서 수신자 행동 및 프로필 특성을 기반으로 이메일 콘텐츠를 개인화합니다. <p>이메일 디자이너에서 계정 여정에 대한 이메일을 작성할 때 조건부 규칙을 사용하여 콘텐츠 구성 요소에 대한 여러 변형을 정의합니다. <a href="../content/conditional-content.md">자세히 알아보기</a> |
| 새로운 기능 | _목록에 추가_ 및 _목록에서 제거_&#x200B;여정의 사람 작업 | 계정 및 리드 수준에서 수신자 행동 및 프로필 특성을 기반으로 이메일 콘텐츠를 개인화합니다. <a href="../journeys/action-nodes.md">자세히 알아보기</a> |
| 새로운 기능 | 콘텐츠 거버넌스 및 구성 요소 잠금 | 승인된 콘텐츠 디자인을 준수하려면 콘텐츠 거버넌스 기능을 사용하여 이메일 템플릿 콘텐츠 구성 요소를 잠급니다. 이메일 템플릿에서 콘텐츠 거버넌스를 활성화하면 마케터는 허용된 요소만 변경하여 콘텐츠 전략에 맞게 콘텐츠를 조정할 수 있습니다. <a href="../content/template-content-governance.md">자세히 알아보기</a> |
| 새로운 기능 | 구매 그룹 단계 | 사용자 정의 구매 그룹 스테이징 모델을 정의하고 게시하면 구매 그룹 라이프사이클 단계 간의 구매 그룹 진행률을 추적할 수 있습니다. 구매 그룹 구성원을 위한 다음 최적 작업을 식별하려면 다음 단계를 사용하십시오. 단계 진행률을 결정하고 변경 사항을 기반으로 작업을 트리거하는 전환 규칙 및 여정 노드를 구성합니다. <a href="../buying-groups/buying-group-stages.md">자세히 알아보기</a> |
| 개선 사항 | 새로운 기본 이메일 템플릿 | 이제 샘플 템플릿 라이브러리에는 B2B 마케터용으로 설계된 추가 이메일 템플릿이 포함되어 있습니다. 이러한 샘플 템플릿을 시작점으로 사용하고 고유한 브랜딩 및 메시지를 추가합니다. <a href="../content/email-templates.md#select-a-design-template">자세히 알아보기</a> |
| 개선 사항 | 사용자 특성으로서의 사용자 정의 필드 | Experience Platform의 계정 대상 스키마에 사용자 정의 개인 필드가 정의된 경우 해당 필드를 조건에서 개인 속성으로 사용할 수도 있습니다. 에서 이러한 사용자 지정 특성을 사용합니다. <li>역할 템플릿 <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">자세히 알아보기</a></li><li>사람 여정 노드로 경로 분할 <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">자세히 알아보기</a></li> |
| 개선 사항 | 이메일 채널 설정 | 이제 이메일 설정이 Journey Optimizer B2B edition 인터페이스에 표시됩니다. 현재 구성을 빠르게 검토할 수 있으며 관리자는 _[!UICONTROL 설정 편집]_&#x200B;을 클릭하여 Marketo Engage의 설정으로 바로 이동하여 조직의 요구 사항에 따라 업데이트할 수 있습니다. <a href="../admin/configure-channels-emails.md">자세히 알아보기</a> |

## 2024년 9월 릴리스 정보 {#Sept-2024}

**릴리스 날짜**: 2024년 10월 7일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 개선 사항 | 중앙 자산 라이브러리 | 향상된 _중앙 자산 라이브러리_&#x200B;를 사용하면 Design Studio 작업 영역에서 Marketo Engage 인스턴스의 모든 이미지 자산을 사용할 수 있습니다. Journey Optimizer B2B edition에서 Marketo Engage 에셋을 편집하고 작업을 삭제 및 이동할 수 없는 내장 보호 기능이 있습니다. 이러한 보호를 통해 소스 에셋(Marketo Engage Design Studio)을 유지 관리하는 동시에 Journey Optimizer B2B edition에서 원활한 읽기 및 재사용이 가능합니다.<p>Journey Optimizer B2B edition에서만 사용되는 에셋의 경우 특정 작업 영역에서 전체 에셋 관리 기능을 제공합니다. <a href="../content/marketo-engage-design-studio.md">자세히 알아보기</a> |
| 새로운 기능 | 최근에 액세스한 자산 | 이제 Journey Optimizer B2B edition 앱의 홈 페이지에는 마케터 또는 관리자를 위해 가장 최근에 액세스한 에셋 목록을 제공하는 _[!UICONTROL 최근에 액세스함]_ 섹션이 포함됩니다. 이 목록을 사용하면 일련의 에셋 페이지를 탐색하고 검색하지 않고도 최근에 작업한 에셋으로 직접 이동할 수 있습니다. <p>이 목록에서는 마지막 세션에서 추가로 수정해야 하는 자산을 결정할 수 있도록 수정과 관련된 추가 정보를 제공합니다. 이메일 에셋의 경우 이메일 에셋이 사용되는 계정 여정을 표시합니다. <a href="../home-page.md">자세히 알아보기</a> |
| 개선 사항 | 여정 분할 노드 - 경로 순서 바꾸기 | 분할 경로 노드에서 경로 필터링은 하향식으로 평가됩니다. 각 개인 또는 계정은 일치하는 첫 번째 경로를 따라 진행됩니다. 각 경로 카드의 오른쪽 상단에 있는 위쪽 및 아래쪽 화살표를 클릭하여 정의된 경로를 목록에서 위나 아래로 이동하여 순서를 변경할 수 있습니다. <a href="../journeys/split-merge-paths-nodes.md#split-paths">자세히 알아보기</a> |
| 개선 사항 | 여정 분할 노드 - 추가 활동 기록 조건 속성 | 조건을 사용하여 사람이 분할한 노드에 대한 경로 필터링을 정의하는 경우 _열린 전자 메일_ 및 _배달된 전자 메일_&#x200B;의 두 가지 추가 특성이 있습니다. 이러한 추가 기능은 이메일 활동을 기반으로 여정 사용자를 필터링할 수 있는 더 큰 유연성을 제공합니다. <a href="../journeys/journey-nodes.md#split-paths">자세히 알아보기</a> |

## 2024년 8월 릴리스 정보 {#Aug-2024}

**릴리스 날짜**: 2024년 8월 29일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 새로운 기능 | LinkedIn 계정 일치 대상 | 계정 일치 대상을 통해 LinkedIn 광고 대상을 생성하여 구매 그룹에서 빈 역할을 채우는 데 도움이 됩니다. 구매 그룹 필터 세트를 정의하여 LinkedIn 일치 대상을 유지 관리하여 구매 그룹 매개 변수와 일치하는 잠재 고객을 타깃팅할 수 있습니다. <p>이 기능은 Experience Platform 대상 을 활용하여 통합의 몇 가지 측면을 관리합니다. <a href="../data/linkedin-account-matched-audiences.md">자세히 알아보기</a> |
| 개선 사항 | 시각적 컨텐츠 조각의 상태 라이프사이클 | 이제 상태 라이프사이클을 사용하여 시각적 조각을 관리합니다. 조각 상태는 이메일 또는 이메일 템플릿에서 사용할 수 있는 가용성과 해당 조각에 적용할 수 있는 변경 사항을 결정합니다. <p>이 향상된 워크플로우를 통해 홍보 및 커뮤니케이션 달력에 따라 재사용된 콘텐츠를 쉽게 관리할 수 있습니다. <a href="../content/fragments.md#fragment-status-and-lifecycle">자세히 알아보기</a> |
