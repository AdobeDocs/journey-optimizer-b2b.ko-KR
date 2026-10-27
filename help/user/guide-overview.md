---
title: Adobe Journey Optimizer B2B Edition 설명서
description: Journey Optimizer B2B Edition에 대한 전체 설명서 - 온보딩, 구매 그룹 만들기, 계정 여정 구축, 콘텐츠 관리에 사용할 수 있는 리소스를 살펴보십시오.
exl-id: 3d7b6c82-95c3-4d89-b3dc-7fd5b0aef615
autotag-review: 2026-03-27T22:18:45.397Z
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
    internal-label: Onboarding
TQID: https://experienceleague.adobe.com/BK-uFYGIZyqRNy4Gx-vJB-oy3q8zpjERIoJwBvgofUY
source-git-commit: ce5504e7a539c38b489fddc103358029edf1cfba
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 26%
---
# Adobe Journey Optimizer B2B Edition 설명서

[!DNL Adobe Journey Optimizer B2B Edition]은(는) 마케팅 및 영업 팀이 계정 기반 경험을 조정하고 전체 고객 라이프사이클에서 특정 제품에 대한 구매 그룹의 자격을 부여할 수 있는 최초의 애플리케이션입니다. AI를 사용하여 대상 고객 내에서 구매 그룹을 참여시키고 자격을 부여함으로써 팀이 더 높은 품질의 파이프라인을 생성하고 더 나은 획득, 확장 및 유지 전략을 설계할 수 있도록 지원합니다. 또한 영업 및 마케팅 팀 간에 공유된 통찰력을 사용할 수 있습니다.

이 설명서에서는 응용 프로그램 마스터링에 대한 정보를 제공합니다. 마케터, 비즈니스 개발 담당자, 데이터 분석가 및 운영 관리자를 위해 설계되었습니다.

## 새로운 기능

[!DNL Journey Optimizer B2B Edition] 응용 프로그램 및 설명서에서 최신 추가 기능 및 개선 사항의 샘플링을 검토하십시오.

>[!BEGINTABS]

>[!TAB 개인 여정]

[!DNL Adobe Experience Platform]개의 대상과 데이터를 사용하여 개별 사용자의 참여를 유도하는 잠재 고객 기반 마케팅을 사용자 여정으로 오케스트레이션하십시오. 이제 개인 여정이 _이벤트 수신_, 외부 작업 및 외부 분할 경로 노드 및 여정 재입력을 지원합니다. 계정 여정 및 구매 그룹과 함께 사용하여 전체 구매 여정을 조정합니다.

[!BADGE 자세히 알아보기]{type=Informative url="/help/user/journeys/journeys-overview.md" tooltip="개인 여정에 대해 알아보기"}

>[!TAB 변형 분할 경로]

정의한 백분율을 기준으로 계정이나 인력을 서로 다른 여정 여정에 할당하여 계정이나 개인 경로 내에서 변형을 테스트합니다. 인간 여정에서 할당은 결정론적이므로 각 사람은 항상 동일한 경로를 따르므로 통제된 실험을 지원한다.

[!BADGE 자세히 알아보기]{type=Informative url="/help/user/journeys/variant-split-paths-nodes.md" tooltip="변형 분할 경로에 대해 알아보기"}

>[!TAB WhatsApp 채널]

개발자와 제품 관리자가 Meta Business Manager 계정과의 통합을 구성할 때 마케터는 Meta Cloud API를 사용하여 계정 여정에서 WhatsApp 메시지를 컨텐츠 채널로 포함할 수 있습니다. WhatsApp은 계정 구성원에게 여정 콘텐츠를 직접 전달할 수 있는 사용 가능한 채널로 이메일 및 SMS에 가입합니다.

[!BADGE 자세히 알아보기]{type=Informative url="/help/user/admin/configure-channels-whatsapp.md" tooltip="WhatsApp 채널에 대해 알아보기"}

>[!TAB 생성 AI 모델]

이제 이메일 디자이너는 이메일 콘텐츠에 대한 이미지를 생성할 때 표준 [!DNL Firefly] 모델, 브랜드별 자산에 대해 교육된 사용자 지정 [!DNL Firefly] 모델 및 승인된 타사 이미지 모델 중에서 선택할 수 있습니다. 이 선택을 통해 팀은 일반적인 콘텐츠 요구 사항에서 브랜드 또는 특수 사용 사례에 이르기까지 특정 디자인 시나리오에 맞는 모델을 제어할 수 있습니다.

[!BADGE 자세히 알아보기]{type=Informative url="/help/user/content/generative-ai-models.md" tooltip="생성 AI 모델 선택에 대해 알아보기"}

>[!TAB 전송 시간 최적화]

_직접 여정에 이메일 보내기_ 작업 노드의 경우 이제 전송 시간 최적화를 사용하여 이메일 게재 타이밍을 개인화할 수 있습니다. 시스템은 모든 수신자에게 동시에 메시지를 보내는 대신 각 개인이 참여할 가능성이 가장 높고 그에 따라 게재를 예약하는 시기를 예측합니다.

[!BADGE 자세히 알아보기]{type=Informative url="/help/user/content/email-send-time-optimization.md" tooltip="전송 시간 최적화에 대해 알아보기"}

>[!TAB 여정 다시 입력]

이제 계정이나 사용자 여정을 통해 계정이나 사용자를 여러 번 보낼 수 있습니다. 재입력은 자격 기준의 재평가 및 재사용 가능한 육성 워크플로와 같은 여러 시나리오를 해결합니다. 계정이나 사용자가 제어된 방식으로 여정을 다시 확인할 수 있도록 기준, 제한 및 대기 시간을 설정하려면 재입력 설정을 사용하십시오.

[!BADGE 자세히 알아보기]{type=Informative url="/help/user/journeys/journey-re-entry.md" tooltip="여정 재입력에 대해 알아보기"}

>[!ENDTABS]

## 탐색 시작 {#section-explore}

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=ko)

최신 릴리스 정보

[!DNL Adobe Journey Optimizer B2B Edition]의 최신 릴리스 정보, 새로운 기능 및 향상된 기능을 계속 업데이트하세요.

[릴리스 정보 보기](./release-notes/release-notes.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=ko)

시작

관리자 및 마케터를 위한 [!DNL Journey Optimizer B2B Edition] 온보딩 지침을 검토하십시오.

[관리자](./setup-ultimate.md)
[사용자](./start/get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=ko)

데이터 관리

[!DNL Adobe Journey Optimizer B2B Edition]에서 사용할 XDM 스키마와 필드를 활성화하고 [!DNL Adobe Experience Platform]에서 해당 데이터가 작동하는 방식을 알아봅니다.

[XDM 필드 관리 보기](./admin/xdm-field-management.md)
[내보낸 데이터 세트](./data/aep-exported-datasets.md)
[데이터 세트 쿼리](./data/aep-query-examples.md)
[데이터 가용성 및 동기화 시간](./data/data-availability-timing.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=ko)

커뮤니케이션 채널

개인화된 고객 상호 작용을 위해 이메일, SMS, WhatsApp 및 기타 채널을 구성하고 관리합니다.

[전자 메일 채널 구성](./admin/configure-channels-emails.md)
[SMS 채널 구성](./admin/configure-channels-sms.md)
[WhatsApp 채널 구성](./admin/configure-channels-whatsapp.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=ko)

여정 만들기

개인화된 계정 및 개인 여정을 디자인하고, 조정하고, 관리하고, 최적화합니다.

[여정 탐색](./journeys/journeys-overview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/users.svg?lang=ko)

구매 그룹 이해

효과적인 타기팅을 위해 구매 그룹을 생성, 관리 및 최적화하는 방법에 대한 자세한 지침입니다.

[구매 그룹에 대해 알아보기](./buying-groups/buying-groups-overview.md)
:::

::::

<!--
:::
![icon](https://cdn.experienceleague.adobe.com/icons/image.svg?lang=ko)

Design Content

Learn how to author and manage content for personalized customer experiences orchestrated through journeys.

[Explore Content Components](./content/content-components.md)
::: 
-->

## 개요 데모

구매 그룹의 구성 요소를 살펴보고 계정 여정을 빌드하는 기본 사항을 이해합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3432054?quality=12)

## 설명서 살펴보기

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px" alt="시작하기"><br/>
      <strong>시작</strong><br/><a href="home-page.md">로그인 및 홈페이지</a><br/><a href="./start/get-started.md">온보딩 지침</a> <br/><a href="./ai-coworker/ai-overview.md">AI 기능</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon_audience.svg" width="35px" alt="구매 그룹"><br/>
      <strong>구매 그룹</strong><br/><a href="./buying-groups/buying-groups-overview.md">구매 그룹 개요</a><br/><a href="./buying-groups/buying-groups-role-templates.md">역할 템플릿</a><br/><a href="./buying-groups/solution-interests.md">솔루션 관심 분야</a><br/><a href="./buying-groups/buying-groups-create.md">구매 그룹 만들기</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-paths.svg" width="35px" alt="계정 여정"><br/>
      <strong>계정 여정</strong><br/><a href="./journeys/journeys-overview.md">여정 개요</a><br/><a href="./journeys/create-publish-journey.md#create-a-journey">계정 여정 만들기</a><br/><a href="./journeys/journey-nodes.md">여정 노드</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="../assets/do-not-localize/icon-campaign.svg" width="35px" alt="여정 콘텐츠"><br/>
      <strong>여정 콘텐츠</strong><br/><a href="./content/add-email.md">이메일 채널</a><br/><a href="./content/generate-content-emails.md">이메일 콘텐츠 생성</a><br/><a href="./content/genstudio-email-workflow.md">GenStudio 이메일 경험</a><br/><a href="./content/sms-authoring.md">SMS 채널</a>
    </td>
        <td>
      <img src="../assets/do-not-localize/icon_assets.svg" width="35px" alt="콘텐츠 관리"><br/>
      <strong>콘텐츠 관리</strong><br/><a href="./content/assets-overview.md">Assets 개요</a><br/><a href="./content/email-templates.md">전자 메일 템플릿</a><br/><a href="./content/fragments.md">시각적 조각</a><br/><a href="./content/conditional-content.md">조건부 콘텐츠</a><br/><a href="./content/brand-themes.md">브랜드 테마</a>
    </td>
    <td>
      <img src="../assets/do-not-localize/icon-offer.svg" width="35px" alt="인사이트 및 대시보드"><br/>
      <strong>인사이트</strong><br/><a href="./dashboards/intelligent-dashboard.md">지능형 대시보드</a><br/><a href="./dashboards/engagement-dashboard.md">참여 대시보드</a><br/><a href="./dashboards/buying-groups-dashboard.md">구매 그룹 대시보드</a><br/><a href="./dashboards/journeys-dashboard.md">여정 대시보드</a><br/><a href="./buying-groups/incrm-insights.md">CRM 내 인사이트</a>
    </td>

</tr>
</table>

>[!BEGINSHADEBOX]

## [!DNL Marketo Qualifier]

[!DNL Adobe Marketo Qualifier]은(는) [!DNL Journey Optimizer B2B Edition]에서 사용할 수 있는 AI 기반 애플리케이션입니다. 계정 자격 기술을 구현하고 비즈니스 개발 담당자(BDR)를 위한 워크플로를 간소화하도록 설계되었습니다. [!DNL Marketo Qualifier]은(는) 채널 전반에서 잠재 고객 자격, 전달 및 구매자 참여 워크플로를 자동화합니다. 엔터프라이즈 B2B 기업의 수동 BDR 로드를 줄이고 파이프라인 속도를 가속화합니다.

자세한 내용은 [Marketo Qualifier 설명서](https://experienceleague.adobe.com/ko/docs/marketo-qualifier/using/home){target="_blank"}를 참조하세요.

>[!ENDSHADEBOX]

## 추가 리소스

<table style="table-layout:fixed">
<tr><td><strong>Adobe Journey Optimizer B2B Edition</strong><br/>
<a href="https://experienceleague.adobe.com/ko/docs/journey-optimizer-b2b-learn/tutorials/overview" target="_blank">비디오 및 튜토리얼</a> - <a href="https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer-b2b.html" target="_blank">제품 설명</a> <!-- - <a href="https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf" target="_blank">Security overview (PDF)</a> - <a href="https://developer.adobe.com/journey-optimizer-apis/" target="_blank">APIs reference</a> - <a href="https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=ko" target="_blank">Journey Optimizer Schema Dictionary</a> -->
</td>
<td><strong>Adobe Experience Platform</strong><br/>
<a href="https://experienceleague.adobe.com/ko/docs/experience-platform/landing/home" target="_blank">설명서</a> - <a href="https://business.adobe.com/kr/products/experience-platform/documentation-and-developer-resources.html" target="_blank">개발자 리소스</a>
</td></tr>
<tr><td><strong>Adobe Real-Time Customer Data Platform</strong><br/>
<a href="https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/home" target="_blank">설명서</a> - <a href="https://experienceleague.adobe.com/ko/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/overview" target="_blank">개발자 자습서</a>
</td><td><strong>Adobe Marketo Engage</strong><br/>
<a href="https://experienceleague.adobe.com/ko/docs/marketo/using/home" target="_blank">사용자 설명서</a> - <a href="https://experienceleague.adobe.com/ko/docs/marketo-developer/marketo/home" target="_blank">개발자 설명서</a>
</td>
</tr></table>
