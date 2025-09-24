---
title: Journey Optimizer B2B Edition 릴리스 정보
description: Adobe Journey Optimizer B2B Edition의 최신 기능, 개선 사항 및 버그 수정 내용 살펴보기 - 새로운 기능 및 제품 개선 사항에 대한 최신 업데이트를 받아 보십시오.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: ac67766c80394b3f00fa8ce713b441a34574b583
workflow-type: tm+mt
source-wordcount: '3016'
ht-degree: 94%

---

# Journey Optimizer B2B Edition 릴리스 정보

Adobe Journey Optimizer B2B Edition은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다.

Journey Optimizer B2B Edition은 기본적으로 [!DNL Adobe Experience Platform]기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-platform/release-notes/latest){target="_blank"}를 참조하십시오.

권한, 성능 가드레일 및 제한 사항에 대한 정보는 [제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}을 검토하십시오.

<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## 2025.9 릴리스 정보

**배포 일자**: 2025년 9월 30일 수요일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 이메일 콘텐츠 공동 작업 | 이제 이메일 에셋의 컨텍스트에서 동료 Journey Optimizer B2B edition 사용자와 공동 작업에 대해 댓글을 달 수 있습니다. 팀 구성원이 주석의 세부 정보가 포함된 이메일 알림을 받을 수 있도록 태그를 지정할 수 있습니다. 알림은 펄스 알림으로도 사용할 수 있습니다. <!-- [Learn more](../admin/engagement-score-weighting.md) --> |
| 기능 | 이메일 디자인을 위한 다크 모드 | 이제 이메일 디자인 공간에 _어두운 모드_(으)로 전환하는 기능이 포함됩니다. 다크 모드에서는 이메일 콘텐츠를 미리 볼 수 있으며, 다크 모드에서 이메일을 보는 수신자를 위해 특히 표시될 사용자 지정 설정을 정의할 수 있습니다. <!-- [Learn more](../content/email-dark-mode.md) --> |
| 개선 사항 | 여정 - 역할에 있는 사람 수별로 경로 분할 | 계정 노드별 분할 경로를 사용하여 하나 이상의 구매 그룹 역할에 있는 사람 수가 있는 계정을 타겟팅합니다. 경로에서 역할 깊이를 기반으로 영업 경고 및 기타 참여에 대한 구매 그룹 준비 상태를 평가할 수 있습니다. <!-- [Learn more](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) --> |
| 개선 사항 | 여정 - 이벤트에 대한 개인 필터 | 사람 필터를 사용하여 사람 이벤트를 수신합니다. 이러한 필터에는 일치하는 구매 그룹에 대한 특정 역할을 타깃팅하는 기능이 포함됩니다. <!-- [Learn more](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) --> |

>[!NOTE]
>
>릴리스 변경 사항은 2025년 9월 30일 수요일에 배포가 시작되며, 각 기능은 단계적으로 롤아웃됩니다. 기능 및 개선 사항의 릴리스 일자는 변경될 수 있습니다.

## 2025.8 릴리스 정보

**배포 일자**: 2025년 8월 26일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 역할 템플릿 및 여정에 대한 사용자 참여 점수 필터 | 이제 구매 그룹을 만들 때와 경로 분할 여정 노드에서 사용하는 역할 템플릿에서 _사용자 참여 점수_&#x200B;를 필터로 사용할 수 있습니다. [자세히 알아보기](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| 기능 | 구매 그룹 사용자 정의 역할 구성 | 이제 구매 그룹에 대한 사용자 정의 역할을 유연하게 구성할 수 있게 되어 사용 사례에 맞도록 역할을 정의할 수 있습니다. [자세히 알아보기](../buying-groups/default-custom-roles.md) |
| 기능 | 참여 점수 가중치 구성 | 이제 구매 그룹 참여 점수에 영향을 주는 활동에 가중치를 할당할 수 있습니다. 이 기능은 사용자 정의 점수 모델을 정의하고 참여 점수 계산에 영향을 주는 활성 모델을 변경하는 기능을 포함합니다. [자세히 알아보기](../admin/engagement-score-weighting.md) |
| 개선 사항 | 조각용 조건부 콘텐츠 | 시각적 조각 디자인에 대해 이제 조건부 콘텐츠 도구를 사용할 수 있습니다. [자세히 알아보기](../content/conditional-content.md) |
| 개선 사항 | 참여 점수 업데이트 | 점수 정규화를 위해 구매 그룹 참여 점수 논리가 업데이트되었습니다. 또한 멤버 수준 참여 점수와 더불어 전체 구매 그룹에 대한 집단적 참여 점수도 활용할 수 있습니다. [자세히 알아보기](../buying-groups/engagement-scores.md) |
| 개선 사항 | 활성 여정 가시성 - 각 노드의 계정 | 활성 계정 여정의 경우 여정에서 각 계정 노드에 도달한 계정 목록을 활용할 수 있습니다. |

>[!NOTE]
>
>릴리스 변경 사항은 2025년 8월 26일에 배포가 시작되며, 각 기능은 단계적으로 롤아웃됩니다. 기능 및 개선 사항의 릴리스 일자는 변경될 수 있습니다.

## 2025.6 릴리스 정보

**배포 일자**: 2025년 7월 15일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | GenStudio for Performance Marketing과 통합 | (제한 공개) 이제 GenStudio for Performance Marketing 이메일 경험을 Journey Optimizer B2B Edition과 통합하여 마케팅 효율을 높이고 브랜드 일관성을 유지할 수 있습니다. 이 통합을 통해 GenStudio AI 기반 콘텐츠 생성과 Journey Optimizer B2B Edition의 고급 오케스트레이션 기능을 결합할 수 있습니다. [자세히 알아보기](../content/genstudio-email-workflow.md) |
| 기능 | 스팸 탐지 보고 | 스팸 필터를 피하고 메시지가 대상자의 받은 편지함으로 전달되도록 하려면 이메일 디자인 공간에서 바로 _스팸 보고서_&#x200B;를 생성할 수 있습니다. [자세히 알아보기](../content/email-spam-report.md) |
| 기능 | 개인 정보 페이지 | 이제 지능형 대시보드, 구매 그룹 세부 정보 페이지 및 계정 세부 정보 페이지에 하이퍼링크로 표시되는 이름을 클릭할 수 있습니다. 이 작업을 통해 연결된 개인 정보 페이지가 열리며, 이 페이지에는 연락처 정보, 활동 및 가장 많이 참여한 구매 그룹에 대한 정보가 표시됩니다. [자세히 알아보기](../accounts/person-details.md) |
| 기능 | 계정 및 구매 그룹 작업 | 계정 상세 정보 및 구매 그룹 상세 정보 페이지에서 바로 작업을 수행하여 시기적절하고 의도적인 참여를 유도할 수 있습니다. <li>_이메일 보내기_ 작업을 사용하여 승인된 Marketo Engage 이메일을 선택한 계정 연락처 또는 구매 그룹 멤버들에게 보낼 수 있습니다. [자세히 알아보기](../accounts/account-details.md#send-emails) <li>구매 그룹 세부 정보에서는 _새 멤버 할당_, _멤버 제거_, _역할 편집_ 등의 작업도 포함됩니다. [자세히 알아보기](../buying-groups/buying-group-details.md#members-tab) |
| 기능 | CRM 내에서 세부 정보 페이지에 액세스 | 이제 Salesforce 또는 Microsoft Dynamics와 같은 고객 관계 관리(CRM) 도구에서 계정, 연락처 및 리드에 대한 Journey Optimizer B2B Edition 세부 정보 페이지로 직접 연결되는 링크를 구성할 수 있습니다. [자세히 알아보기](../accounts/crm-linking.md) |
| 기능 | 콘텐츠 디자인을 위한 사용자 정의 CSS 지원 | 이제 디자인 공간에서 이메일 및 랜딩 페이지 콘텐츠를 작성할 때 사용자 정의 CSS를 추가할 수 있습니다. [자세히 알아보기](../content/design-custom-css.md) |
| 기능 | 의도 키워드 매핑 구성 | 의도 감지 모델을 활성화하고 관리하려면 이제 스프레드시트를 업로드하여 의도 데이터 매핑 카테고리를 정의할 수 있습니다. [자세히 알아보기](../admin/intent-data.md) |
| 개선 사항 | 이메일 요약에서 콘텐츠 시뮬레이션 | 이제 이메일 목록에서 이메일을 열 때 이메일 요약(세부 정보 및 속성)에서 _콘텐츠 시뮬레이션_ 도구에 액세스할 수 있습니다. 이러한 접근 방식은 이메일 디자인 공간에 추가됩니다. [자세히 알아보기](../content/email-simulate-content.md#display-the-email-preview) |
| 개선 사항 | 역할 템플릿 목록에 총 개수 표시 | _[!UICONTROL 역할 템플릿]_ 목록 페이지에 검색 창 옆에 총 개수 표시 기능이 추가되어 향상되었습니다. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## 2025.5 릴리스 정보

**배포 일자**: 2025년 6월 3일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | Litmus를 통한 이메일 테스트 | [Litmus Enterprise 계정](https://www.litmus.com/email-testing){target="_blank"}이 있으면 이제 Journey Optimizer B2B Edition의 인기 있는 이메일 클라이언트에서 이메일 렌더링을 미리 볼 수 있습니다. 이 통합 기능은 모든 이메일 받은 편지함에서 이메일 콘텐츠가 멋지게 보이고 디자인대로 작동하는지 확인하는 데 도움이 됩니다. [자세히 알아보기](../content/email-test-rendering.md) |
| 개선 사항 | 이메일 복사 | 이제 여정 노드에 이메일을 추가할 때 기존 이메일을 복사하여 쓸 수 있습니다. 복사된 이메일의 설정이나 내용을 수정하거나 그대로 둘 수 있습니다. [자세히 알아보기](../content/add-email.md#add-an-email-to-your-journey) |
| 개선 사항 | 이메일용 핸들바 토큰 형식 | 이메일 콘텐츠에 대한 개인화 토큰은 이제 핸들바 스크립팅과 완벽하게 호환되는 업데이트된 형식을 사용합니다. 이 형식은 공백을 제거하는 _카멜 표기법_ 또는 밑줄을 사용합니다. [자세히 알아보기](../content/email-authoring.md#content-authoring---personalization) |
| 개선 사항 | 목록의 총 개수 표시 | _[!UICONTROL 솔루션 관심 분야]_ 및 _[!UICONTROL 계정 여정]_ 목록 페이지에서 검색 창 옆에 총 개수가 표시되어 가시성이 더욱 향상되었습니다. |

## 2025.4 릴리스 정보

**배포 일자**: 2025년 4월 29일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 계정 목록 | 이제 업계, 위치 또는 회사 규모와 같은 정의된 기준에 따라 지정된 계정을 타기팅하기 위해 정적 또는 동적 계정 목록을 만들 수 있습니다. <a href="../accounts/account-lists.md">자세히 알아보기</a> |
| 기능 | 계정 목록 여정 오케스트레이션 | 여정 작업 노드를 사용하여 정적 계정 목록에 계정을 추가하거나 제거할 수 있습니다. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">자세히 알아보기</a> |
| 개선 사항 | Marketo Engage에서 여정 멤버십 필터링 | 여정 대상자에 Adobe Journey Optimizer B2B Edition 계정 목록을 사용한 다음 Marketo Engage 스마트 목록에서 _계정 목록 멤버_ 필터를 적용합니다. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">자세히 알아보기</a> |
| 기능 | 비활동 필터 | 이메일 비활동, 즐거운 순간, 데이터 가치 변화, 방문한 웹 페이지 등을 포함하여 Marketo Engage 캠페인과 프로그램 내의 비활동에 따라 조율되는 여정입니다. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">자세히 알아보기</a> |
| 개선 사항 | 방문한 웹 페이지 필터 | Marketo Engage 캠페인 및 프로그램과 관련된 방문한 웹 페이지의 활동을 기반으로 여정을 조율합니다. <a href="../journeys/split-merge-paths-nodes.md#people-path-conditions">자세히 알아보기</a> |
| 개선 사항 | 이메일 목록 | 활성 및 초안 이메일의 글로벌 목록을 조회하고, 연관된 계정 여정 전반에 걸쳐 이를 검색, 검토 및 업데이트합니다. <a href="../content/emails-list.md">자세히 알아보기</a> |

## 2025.3 릴리스 정보

**배포 일자**: 2025년 4월 1일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 중복 계정 여정 | 이제 계정 여정에 대한 복제 액션을 사용할 수 있습니다. 계정 여정의 세부 정보를 복제하거나 흐름 및 경로 구조에 대한 간단한 스켈레톤을 복제할 수 있습니다. <a href="../journeys/journey-overview.md#duplicate-journey">자세히 알아보기</a> |
| 기능 | 계정 여정을 위한 내 토큰 | 이제 계정 여정에 특정한 값을 가진 사용자 정의 토큰 세트를 정의할 수 있습니다. 이 사용자 정의 토큰 세트는 _내 토큰_&#x200B;이라고 하며, 이러한 사용자 정의 토큰은 여정 이메일을 작성할 때 개인화하는 데 사용됩니다. <a href="../content/personalization-my-tokens.md">자세히 알아보기</a> |
| 기능 | 구매 그룹 단계 삭제 | 구매 그룹 단계 모델이 초안 또는 게시된 상태일 때 삭제할 수 있습니다. 게시된(진행 중) 경우 솔루션 관심 분야와 연관되지 않은 경우에만 삭제할 수 있습니다. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">자세히 알아보기</a> |
| 개선 사항 | 여정 노드 수 | 노드 수준에서 게시된 여정 멤버십 수에 대한 가시성이 향상되었습니다. _여정 맵_&#x200B;에서 노드는 _[!UICONTROL 입력한 총 계정]_&#x200B;을 표시합니다. 노드를 선택하고 실행하면 오른쪽에 있는 세부 정보에는 _[!UICONTROL 아직 실행되지 않은 계정]_&#x200B;도 포함됩니다. _이벤트 수신_&#x200B;을 위한 자세한 내용에는 _[!UICONTROL 이 단계의 계정]_&#x200B;이 포함됩니다. 이 정보를 사용하여 진행 중인 여정, 완료된 여정, 중단된 여정의 계정 진행 상황을 확인합니다. |

## 2025.2 릴리스 정보

**배포 일자**: 2025년 3월 11일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 사용자 정의 가능 필드 - 콘텐츠 조각 | 시각적 조각 디자인 과정에서 해당 조각의 구성 요소에 대한 매개변수를 “편집 가능”으로 지정할 수 있습니다. 이 기능을 통해 이메일 또는 템플릿 작성자는 필요에 맞는 사용자 정의 필드 값을 지정할 수 있습니다. 이 사용자 정의 플래그는 이미지, 텍스트 및 버튼 시각적 구성 요소로 제한됩니다. <a href="../content/fragment-authoring.md#enable-fragment-customization">자세히 알아보기</a> |
| 기능 | 여정 복제 유형 | 계정 여정을 복제할 때 Journey Optimizer B2B Edition에서 생성된 이메일 및 SMS 메시지를 제외한 노드 세부 정보를 포함할 수 있습니다. 대안으로, 노드 세부 정보 및 설정 없이 구조와 경로 흐름의 스켈레톤 복사본을 만들 수 있습니다. <a href="../journeys/journey-overview.md#duplicate-journey">자세히 알아보기</a> |
| 개선 사항 | 4가지 추가 샘플 이메일 템플릿 | 이제 샘플 이메일 템플릿 라이브러리에는 재참여, 정보 제공, 육성 및 피드백 콘텐츠 예시를 위한 4가지 SecurFinancial 템플릿이 포함됩니다. |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## 2025.1 릴리스 정보 {#Jan-2025}

**배포 일자**: 2025년 2월 6일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 경험 이벤트 전달 | 관리자는 Adobe Experience Platform(AEP) 기반 이벤트 정의를 구성할 수 있습니다. 이러한 구성을 통해 마케터는 AEP 경험 이벤트에 반응하는 계정 여정을 만들 수 있습니다. <a href="../admin/configure-aep-events.md">자세히 알아보기</a> |
| 기능 | 유료 미디어 대상 | 계정 여정에서 알려진 사용자에게 유료 미디어 캠페인에 대한 자격을 제공하여 LinkedIn과 같은 광고 플랫폼에서 더 깊이 있게 참여할 수 있도록 합니다. 경로 분할 노드를 사용하여 특정 행동을 기준으로 계정 대상자를 세분화하고 추가 참여가 필요한 계정을 식별합니다. 그런 다음 지원되는 유료 미디어 대상에 대한 Real-Time CDP를 통해 해당 계정의 사용자를 외부 고객 대상자에 추가합니다. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">자세히 알아보기</a> |
| 기능 | 지능형 대시보드 | AI 생성 인사이트를 통한 보다 지능적인 분석과 정확한 계정 우선순위 지정을 포함하여 구매 그룹의 계정 여정 진행 상황을 확인합니다. <a href="../dashboards/intelligent-dashboard.md">자세히 알아보기</a> |
| 기능 | 구매 그룹 및 계정 세부 정보 | 구매 그룹 및 계정 수준에서 인사이트를 확인하여 고객과 소통을 시작할 때 더 많은 컨텍스트와 내역 데이터를 확보합니다.<p>구매 그룹 세부 정보에는 감지된 모든 자사 의도가 포함됩니다. <a href="../buying-groups/buying-group-details.md">자세히 알아보기</a><p>계정 세부 정보 계정은 참여 의도의 급증을 감지하여 강조 표시하므로 맞춤화된 판매 중심 참여가 준비된 계정에 대한 판매 알림을 보낼 수 있습니다. <a href="../accounts/account-details.md">자세히 알아보기</a> |
| 기능 | 여정 개요 | 계정 여정에 액세스하면 개요 탭에서 활성 계정 여정에 대한 포괄적인 스냅샷을 제공합니다. 이 탭에서는 완료율 및 참여 활동을 카테고리화하고 정량화하여 보여 주는 원형 차트와 막대 차트를 활용하여 계정 진행 상황을 자세히 알려 줍니다. <a href="../dashboards/journeys-dashboard.md">자세히 알아보기</a> |
| 기능 | Adobe Express 이미지 편집 | Adobe Express 빠른 작업을 사용하면 이미지를 간단히 편집(자르기, 크기 조정 등)하여 콘텐츠를 더욱 세련되게 만들 수 있습니다. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">자세히 알아보기</a>  <p>보다 포괄적인 디자인 도구 세트를 제공하기 위해, 이 통합을 통해 Journey Optimizer B2B Edition에서 전체 Adobe Express 라이선스를 사용할 수 있습니다. 이 설정을 사용하면 로컬 자산 작업 영역에서 전체 Adobe Express 사용자 인터페이스에 액세스할 수 있습니다. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">자세히 알아보기</a> |
| 기능 | 구매 그룹 역할을 위한 의도 필터 | 의도 키워드를 제출하면 의도 감지 모델이 리드의 활동을 기반으로 높은 신뢰도로 관심 있는 솔루션/제품을 예측합니다. <a href="../admin/intent-data.md">자세히 알아보기</a> <p>이 의도 데이터는 구매 그룹 역할 조건을 정의하는 데 사용할 수 있습니다. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">자세히 알아보기</a> |
| 개선 사항 | 여정에서 Marketo Engage 이벤트 지원 | _이벤트 수신_ 여정 노드는 이제 사용자 수준에서 두 가지 Marketo Engage 이벤트, 즉 _웹 페이지 방문_ 및 _양식 작성_&#x200B;을 지원합니다. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">자세히 알아보기</a> |
| 개선 사항 | Marketo Engage 스마트 목록을 위한 구매 그룹 필터 | Marketo Engage에서 구매 그룹 필터를 사용하여 스마트 목록을 보고 만들 수 있습니다. 이러한 추가 필터를 사용하면 Journey Optimizer B2B Edition의 계정 여정의 Marketo Engage 캠페인 및 프로그램에서 구매 그룹 멤버를 제외하거나 포함할 수 있습니다. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">자세히 알아보기</a> |
| 개선 사항 | 여정 및 역할을 위한 Marketo Engage 목록 멤버십 필터 | Journey Optimizer B2B에서는 Marketo Engage 목록 멤버십을 _사용자별 경로 분할_ 노드의 조건으로 설정하여 여정 활동에서 중복을 제거할 수 있습니다. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">자세히 알아보기</a> <p> 그룹 역할 템플릿의 경우 역할 조건으로 목록 멤버십을 사용합니다. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">자세히 알아보기</a> |
| 개선 사항 | 참여 개요 대시보드 | 이 대시보드는 참여에 대한 포괄적인 보기를 제공하도록 업데이트되었습니다. 여기에는 시간 경과에 따른 스냅샷 원형 차트와 추세를 보여 주는 선형 차트를 통해 계정 및 개별 상호 작용에 대한 실시간 지표가 표시됩니다. <a href="../dashboards/engagement-dashboard.md">자세히 알아보기</a> |

## 2024년 릴리스

2024년에 출시된 Journey Optimizer B2B Edition의 기능과 향상된 기능을 보려면 다음 목록을 펼치십시오.

+++2024년 10월 릴리스 정보

**배포 일자**: 2024년 10월 29일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | 이메일의 조건부 콘텐츠 | 수신자의 행동 및 프로필 특성에 따라 계정 및 리드 수준에서 이메일 콘텐츠를 개인화할 수 있습니다. <p>이메일 시각적 디자인 공간에서 계정 여정에 대한 이메일을 작성할 때 조건부 규칙을 사용하면 모든 콘텐츠 구성 요소에 대한 여러 개의 변형을 정의할 수 있습니다. <a href="../content/conditional-content.md">자세히 알아보기</a> |
| 기능 | _목록에 추가_ 및 _목록에서 제거_ 여정 사용자 액션 | 수신자의 행동 및 프로필 특성에 따라 계정 및 리드 수준에서 이메일 콘텐츠를 개인화할 수 있습니다. <a href="../journeys/action-nodes.md">자세히 알아보기</a> |
| 기능 | 콘텐츠 거버넌스 및 구성 요소 잠금 | 승인된 콘텐츠 디자인을 준수하기 위해 콘텐츠 거버넌스 기능을 사용하여 이메일 템플릿 콘텐츠 구성 요소를 잠글 수 있습니다. 이메일 템플릿에서 콘텐츠 거버넌스를 활성화하면 마케터가 콘텐츠 전략에 맞게 허용된 요소만 변경할 수 있습니다. <a href="../content/template-content-governance.md">자세히 알아보기</a> |
| 기능 | 구매 그룹 단계 | 사용자 정의 구매 그룹 스테이징 모델을 정의하고 게시하면 구매 그룹 라이프사이클 단계를 통해 구매 그룹 진행 상황을 추적할 수 있습니다. 이러한 단계를 사용하여 구매 그룹 멤버를 위해 다음으로 취할 가장 좋은 액션을 식별할 수 있습니다. 변경 사항에 따라 단계 진행을 결정하고 액션을 트리거하는 전환 규칙과 여정 노드를 구성하십시오. <a href="../buying-groups/buying-group-stages.md">자세히 알아보기</a> |
| 개선 사항 | 새로운 기본 이메일 템플릿 | 이제 샘플 템플릿 라이브러리에 B2B 마케터를 위해 디자인된 추가 이메일 템플릿이 포함됩니다. 이들 샘플 템플릿을 시작점으로 삼아 나만의 브랜딩과 메시지를 추가해 보십시오. <a href="../content/email-templates.md#select-a-design-template">자세히 알아보기</a> |
| 개선 사항 | 사용자 정의 필드를 개인 속성으로 사용 | Experience Platform의 계정 대상자 스키마에 사용자 정의 개인 필드를 정의한 경우 이들 필드를 조건에서 개인 속성으로 사용할 수도 있습니다. 다음에서 사용자 정의 속성을 사용할 수 있습니다. <li>역할 템플릿 <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">자세히 알아보기</a></li><li>사용자 여정별 경로 분할 노드 <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">자세히 알아보기</a></li> |
| 개선 사항 | 이메일 채널 설정 | 이제 Journey Optimizer B2B Edition 인터페이스에서 이메일 설정을 볼 수 있습니다. 빠르게 현재 구성을 검토할 수 있으며, 관리자는 _[!UICONTROL 설정 편집]_&#x200B;을 클릭하여 Marketo Engage의 설정으로 직접 이동한 다음 조직의 요구 사항에 맞게 업데이트할 수 있습니다. <a href="../admin/configure-channels-emails.md">자세히 알아보기</a> |

+++

+++2024년 9월 릴리스 정보

**배포 일자**: 2024년 10월 7일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 개선 사항 | 중앙 자산 라이브러리 | 강화된 _중앙 자산 라이브러리_&#x200B;를 통해 Design Studio 작업 영역 전반에서 Marketo Engage 인스턴스의 모든 이미지 자산을 사용할 수 있습니다. Journey Optimizer B2B Edition에는 Marketo Engage 자산의 편집 작업과 삭제 및 이동 작업을 방지하는 기본 제공 가드레일이 있습니다. 이러한 보호 장치를 통해 Marketo Engage Design Studio의 소스 자산이 유지되는 동시에 Journey Optimizer B2B Edition에서 원활하게 읽고 재사용할 수 있습니다.<p>Journey Optimizer B2B Edition에서만 사용되는 자산의 경우 자산을 완전히 제공할 수 있는 특정 작업 영역이 제공됩니다. <a href="../content/marketo-engage-design-studio.md">자세히 알아보기</a> |
| 기능 | 최근에 액세스한 자산 | 이제 Journey Optimizer B2B Edition 앱의 홈 페이지에는 _[!UICONTROL 최근 액세스한 항목]_ 섹션이 포함됩니다. 이 섹션에서는 마케터나 관리자가 가장 최근에 액세스한 자산 목록을 제공합니다. 이 목록을 사용하면 일련의 자산 페이지를 탐색하거나 검색하지 않고도 최근에 작업한 자산으로 바로 이동할 수 있습니다. <p>이 목록은 수정 사항에 대한 추가 정보를 제공하므로, 마지막 세션 이후 어떤 자산을 추가로 수정해야 할지 결정할 수 있습니다. 이메일 자산의 경우 이메일 자산이 사용된 계정 여정이 표시됩니다. <a href="../home-page.md">자세히 알아보기</a> |
| 개선 사항 | 여정 분할 노드 - 경로 재정렬 | 경로 분할 노드에서 경로 필터링은 하향식으로 평가됩니다. 각 개인 또는 계정은 일치하는 첫 번째 경로를 따라 진행합니다. 각 경로 카드의 오른쪽 상단에 있는 위쪽 및 아래쪽 화살표를 클릭하여 정의된 경로를 재정렬하고 목록에서 해당 경로를 위나 아래로 이동할 수 있습니다. <a href="../journeys/split-merge-paths-nodes.md#split-paths">자세히 알아보기</a> |
| 개선 사항 | 여정 분할 노드 - 추가 활동 내역 조건 속성 | 사용자별 분할 노드의 경로 필터링을 정의하기 위해 조건을 사용할 때 두 가지 추가 속성, 즉 _이메일을 열람함_&#x200B;과 _이메일을 전달함_&#x200B;을 사용할 수 있습니다. 이러한 추가 기능은 이메일 활동을 기반으로 여정에서 사람들을 보다 유연하게 필터링할 수 있도록 해 줍니다. <a href="../journeys/journey-nodes.md#split-paths">자세히 알아보기</a> |

+++

+++2024년 8월 릴리스 정보

**배포 일자**: 2024년 8월 29일

이번 릴리스에는 다음과 같은 새로운 기능 및 개선 사항이 포함되었습니다.

| 유형 | 항목 | 설명 |
| ---- | ---- | ----------- |
| 기능 | LinkedIn 계정 일치 대상자 | 구매 그룹에서 빈 역할을 채우는 데 도움이 되는 계정 일치 대상자를 통해 LinkedIn 광고 대상자를 생성합니다. 구매 그룹 필터 세트를 정의하면 LinkedIn 일치 대상자를 유지하여 구매 그룹 매개변수와 일치하는 잠재 고객을 타기팅할 수 있습니다. <p>이 기능은 Experience Platform 대상을 활용하여 통합의 일부 요소를 관리합니다. <a href="../data/linkedin-account-matched-audiences.md">자세히 알아보기</a> |
| 개선 사항 | 시각적 콘텐츠 조각을 위한 상태 라이프사이클 | 이제 시각적 조각은 상태 라이프사이클을 사용하여 관리됩니다. 조각 상태는 이메일이나 이메일 템플릿에서 조각을 사용할 수 있는지 여부와 조각에 적용할 수 있는 변경 사항을 결정합니다. <p>이 향상된 워크플로를 통해 홍보 및 커뮤니케이션 일정에 따라 재사용된 콘텐츠를 손쉽게 관리할 수 있습니다. <a href="../content/fragments.md#fragment-status-and-lifecycle">자세히 알아보기</a> |

+++
