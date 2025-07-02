---
title: 관리자 및 마케터를 위한 온보딩 지침
description: Journey Optimizer B2B Edition의 신규 관리자 또는 사용자인 경우 온보딩 프로세스의 주요 영역에 대해 알아보십시오.
role: Admin, User
level: Beginner
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: d0bd2d5153b972df92ff42c6f1eebb25448b222f
workflow-type: ht
source-wordcount: '685'
ht-degree: 100%

---

# 온보딩 지침

Adobe Journey Optimizer B2B Edition에서 다루고자 하는 기능과 도구는 팀 내 역할에 따라 달라집니다. 조직에 따라 관리자는 여러 유형의 사용자를 정의하고 권한에 따라 특정 기능에 대한 액세스 권한을 부여할 수 있습니다.

>[!TIP]
>
>또한 성능 가드레일과 정적 제한 사항에 대한 라이선스 권한과 해당 [제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}을 확인하십시오.

>[!BEGINTABS]

>[!TAB 관리자]

팀이 Adobe Journey Optimizer B2B Edition 기능을 사용하기 전에 환경을 준비하기 위해 몇 가지 단계가 필요합니다. 데이터 엔지니어와 마케터가 Adobe Journey Optimizer B2B Edition으로 작업을 시작할 수 있도록 다음 단계를 수행합니다.

시스템 관리자는 샌드박스 관리 및 채널 구성을 위해 제품 프로필을 이해하고 권한을 할당해야 합니다. 또한 사용 가능한 제품 프로필에 대해 샌드박스를 설정하고 관리해야 합니다. 그런 다음 제품 프로필에 팀원을 할당할 수 있습니다. 이러한 기능은 Adobe Admin Console에 액세스할 수 있는 제품 관리자가 관리할 수 있습니다. [Adobe Admin Console에 대한 자세한 내용을 살펴보십시오](https://helpx.adobe.com/kr/enterprise/using/admin-console.html).

다음 페이지에서 액세스 관리에 대해 알아보십시오.

1. **샌드박스를 생성**&#x200B;하여 인스턴스를 별도의 격리된 가상 환경으로 분할합니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **데이터 엔지니어와 협력하여** B2B 대상자와 프로필 활성화를 계획하고 구현하십시오. 게시된 블루프린트를 검토하고 요구 사항에 맞게 지침을 따르십시오. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/blueprints-learn/architecture/b2b-activation/overview){target="_blank"}

1. **제품 프로필 설정**. 제품 프로필은 사용자가 인터페이스의 특정 기능이나 오브젝트에 액세스할 수 있도록 허용하는 Adobe Experience Platform의 단 권한 세트입니다. [자세히 알아보기](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. 샌드박스를 포함하여 제품 프로필에 **사용자 권한을 설정**&#x200B;하고 팀원을 다른 제품 프로필에 할당하여 액세스 권한을 부여합니다. 이 작업은 Admin Console에서 수행할 수 있습니다. [자세히 알아보기](../admin/user-management.md#create-a-user-group)

1. Marketo Engage에서 **이메일 게재를 구성**&#x200B;하여 팀이 계정 여정에서 이메일 콘텐츠를 전송할 수 있도록 합니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **SMS 서비스 구성**. 텍스트 메시지 서비스를 독립적으로 제공하는 지원되는 서드파티 SMS 제공업체 중 하나를 설정하고 Adobe Journey Optimizer B2B Edition에서 계정 자격 증명을 구성합니다. [자세히 알아보기](../admin/configure-channels-sms.md)

1. 중앙 집중식 디지털 자산 관리를 위해 Assets as a Cloud Service를 사용하는 팀이 **Adobe Experience Manager Assets를 구성하고 사용**&#x200B;할 수 있도록 합니다. [자세히 알아보기](../admin/configure-aem-repositories.md)

1. AEP 경험 이벤트를 수신하는 계정 여정을 만드는 팀을 위해 **Adobe Experience Platform(AEP) 경험 이벤트 정의를 설정**&#x200B;합니다. [자세히 알아보기](../admin/configure-aep-events.md)

>[!TAB 마케터]

마케터 또는 _계정 여정 실무자_&#x200B;는 여정을 디자인하고 콘텐츠를 제작할 책임이 있습니다. 시스템 관리자와 데이터 엔지니어가 환경을 준비하고 액세스 권한을 부여한 후 Adobe Journey Optimizer B2B Edition으로 작업을 시작할 수 있습니다.

첫 번째 여정을 설정하고 자산을 추가하고 콘텐츠를 보내려면 다음 섹션을 참조하십시오.

1. **계정 대상자 추가**. Journey Optimizer B2B Edition을 사용하면 애플리케이션에서 직접 세그먼트 정의를 통해 계정 대상자를 만들어 계정 여정에 활용할 수 있습니다. [자세히 알아보기](../audiences/account-audience-overview.md)

1. **구매 그룹 만들기**. 비즈니스 목표와 목적을 달성하기 위한 핵심 구성 요소를 정의하고 목표 계정 목록의 멤버를 식별하는 구매 그룹을 만듭니다. [자세히 알아보기](../buying-groups/buying-groups-overview.md)

1. **자산 생성 및 관리**. Adobe Experience Manager Assets은 메시지를 채우는 데 사용할 수 있는 자산의 중앙 집중식 단일 저장소를 제공합니다. [자세히 알아보기](../content/assets-overview.md)

1. **개인화되고 동적인 이메일 템플릿 추가**. Journey Optimizer B2B Edition 개인화 및 다이내믹 콘텐츠 기능을 활용하여 메시지를 대상자에 맞게 조정하십시오. [자세히 알아보기](../content/email-templates.md)

1. **계정 여정 설계를 통해 개인화된 상황별 경험 제공**. Journey Optimizer B2B Edition을 사용하면 이벤트 또는 데이터 소스에 저장된 상황별 데이터를 활용하여 실시간 오케스트레이션 사용 사례를 빌드할 수 있습니다. 다음 기능을 통해 여러 단계로 구성된 고급 시나리오를 설계할 수 있습니다.

   * 이벤트 수신 시 트리거되는 실시간 단일 게재를 보내거나 Adobe Experience Platform 대상자를 사용하여 일괄적으로 게재를 보냅니다.

   * 이벤트의 컨텍스트 기반 데이터, Adobe Experience Platform의 정보 또는 서드파티 API 서비스의 데이터를 사용합니다.

   * 기본 제공 채널 액션(이메일 및 SMS)을 사용하여 Journey Optimizer B2B Edition에서 설계된 메시지를 전송합니다.

   * 여정 맵에서 여러 단계의 사용 사례를 빌드하고 조건을 추가하며 개인화된 메시지를 보냅니다.

[자세히 알아보기](../journeys/journey-overview.md)

>[!ENDTABS]
