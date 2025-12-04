---
title: 이메일 채널 구성
description: Journey Optimizer B2B edition에서 게재 기능을 최적화하도록 이메일 게재 설정, 통신 제한 및 인증 프로토콜을 구성합니다.
feature: Setup, Channels
role: Admin
exl-id: fb16b5e5-f1a5-4e59-b8c6-56985f03225a
source-git-commit: cbd9117daffc3820196c1d8436af2a568e1140b7
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 0%

---

# 이메일 채널 구성

Adobe Journey Optimizer B2B edition은 Marketo Engage의 채널 기능 및 이벤트 추적을 활용합니다. 관리자는 마케터에게 채널 제공을 활성화하기 위해 게재 및 추적 구성이 제대로 되어 있는지 확인해야 합니다. Marketo Engage을 통한 전자 메일 배달 및 추적에 필요한 프로토콜에 대한 자세한 내용은 [추적 및 전자 메일 배달에 필요한 프로토콜](../start/email-protocols.md)을 참조하세요.

## 게재 설정

기본 이메일 설정은 마케터가 계정 여정에서 이메일을 만들 때 사용됩니다. 전자 메일 게재 설정을 검토하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동하세요. 탐색 패널의 _[!UICONTROL 전자 메일]_&#x200B;에서 **[!UICONTROL 배달 설정]**&#x200B;을 선택합니다.

![전자 메일 게재 설정에 액세스](./assets/config-email-delivery-email-header.png){width="800" zoomable="yes"}

설정은 Journey Optimizer B2B edition에서 읽기 전용입니다. 연결된 Marketo Engage 인스턴스의 구성 옵션에 액세스하려면 오른쪽 상단의 **[!UICONTROL 설정 편집]**&#x200B;을 클릭하십시오.

>[!NOTE]
>
>Adobe Marketo Engage에서 이러한 설정에 액세스하고 편집하려면 제품 관리자 권한이 있어야 합니다.

현재 설정을 검토하려면 다음 탭을 각각 선택하십시오.

### [!UICONTROL 전자 메일 헤더 매개 변수] {#email-header}

이메일 헤더 매개 변수는 다음에 대한 기본값을 정의합니다.

* **[!UICONTROL 보낸 사람]** - 전자 메일 헤더의 _보낸 사람_ 필드에 나열된 전자 메일 주소입니다.

* **[!UICONTROL 보낸 사람 레이블]** - 표시된 전자 메일 보낸 사람 주소의 이름입니다.

* **[!UICONTROL HTML 구독 취소]** - 수신자에게 구독 취소 작업을 설명하기 위해 비작동 전자 메일에 표시되는 HTML(지원되는 전자 메일 클라이언트의 경우)입니다. 이 텍스트와 링크는 맨 아래에 추가됩니다.

* **[!UICONTROL 구독 취소 텍스트]** - 수신자에게 구독 취소 작업을 설명하기 위해 비작동 전자 메일에 표시되는 일반 텍스트입니다. 이 텍스트와 링크는 맨 아래에 추가됩니다.

* **[!UICONTROL 웹 페이지로 보기 HTML]** - 브라우저에서 전자 메일을 표시하는 링크를 제공하는 _웹 페이지로 보기_&#x200B;에 사용되는 HTML(지원되는 전자 메일 클라이언트의 경우)입니다.

* **[!UICONTROL 웹 페이지로 보기]** - _웹 페이지로 보기_&#x200B;에 사용되는 일반 텍스트로서, 브라우저에서 전자 메일을 표시하는 링크를 제공합니다.

### [!UICONTROL 브랜딩 도메인] {#branding-domains}

브랜딩 도메인을 검토하려면 **[!UICONTROL 브랜딩 도메인]** 탭을 클릭하십시오.

![브랜딩 도메인 설정에 액세스](./assets/config-email-delivery-branding-domains.png){width="700" zoomable="yes"}

이 설정은 연결된 Marketo Engage 인스턴스에서 하나 이상의 작업 공간에 대한 주 도메인을 정의합니다. 새 전자 메일은 이 도메인을 기본값으로 사용하지만 마케터는 [전자 메일을 기준으로 이 도메인을 재정의할 수 있습니다](../content/add-email.md#define-the-email-settings). 기본 브랜딩 도메인 정의에 대한 자세한 내용은 [Marketo Engage 설명서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/edit-your-default-branding-domain){target="_blank"}를 참조하세요.

>[!NOTE]
>
>여러 브랜드를 마케팅하는 경우 각 브랜드에 고유한 브랜드 추적 링크를 제공하려는 경우 브랜딩 도메인을 추가할 수 있습니다. 여러 브랜딩 도메인을 추가하는 방법에 대한 자세한 내용은 [Marketo Engage 설명서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/administration/email-setup/add-multiple-branding-domains/add-an-additional-branding-domain){target="_blank"}를 참조하세요.

### [!UICONTROL 사용자 지정 헤더 옵션] {#custom-header-options}

사용자 지정 헤더 옵션을 검토하려면 **[!UICONTROL 사용자 지정 헤더 옵션]** 탭을 클릭하십시오.

![사용자 지정 헤더 옵션에 액세스](./assets/config-email-delivery-custom-header.png){width="700" zoomable="yes"}

_[!UICONTROL 엄격한 전송 보안]_&#x200B;을 사용하도록 설정하면 추적 링크가 HTTPS를 통해 제공됩니다(SSL로 보호되는 추적 링크가 있는 구독에만 해당).

## 커뮤니케이션 제한

통신 제한은 연락처가 조직에서 받는 전자 메일 수를 제어합니다. 설정한 제한은 Journey Optimizer B2B edition과 연결된 Marketo Engage 인스턴스 간에 공유됩니다. 이러한 제한을 설정하면 한 잠재 고객이 지정된 기간 동안 최대 이메일 수를 넘지 않도록 합니다.

>[!AVAILABILITY]
>
>통신 제한은 [간소화된 아키텍처](../simplified-architecture.md)에서 프로비저닝된 Journey Optimizer B2B edition 환경에 사용할 수 있습니다. Adobe 지원 센터에 문의하거나 지원 티켓을 열어 Journey Optimizer B2B edition과 하나 이상의 Marketo Engage 인스턴스 간에 통신 제한을 공유할 수 있습니다.

예를 들어 하루에 5개의 이메일로 정의된 제한을 사용하는 경우 시스템에서는 6번째 이메일을 억제하여 한 연락처가 하루 내에 6번째 이메일을 받지 못하도록 합니다. Journey Optimizer B2B edition과 Marketo Engage 간에 공유된 통신 제한을 통해 통신 제한 규칙이 한 위치에 정의됩니다. 여섯 번째 이메일은 Journey Optimizer B2B edition 또는 Marketo Engage의 보내기 작업과 관계없이 표시되지 않습니다.

모든 Marketo Engage 프로덕션 인스턴스에는 기본적으로 통신 제한이 정의되어 있습니다(자세한 내용은 [Marketo Engage 설명서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/administration/email-setup/enable-communication-limits){target="_blank"} 참조). 공유 통신 제한을 사용하려면 Journey Optimizer B2B edition에서 규칙을 정의하고 이러한 제한의 공유를 Marketo Munchkin 코드로 확장합니다.

>[!IMPORTANT]
>
>Marketo Munchkin 코드로 설정된 통신 규칙을 확장하려면 Adobe 계정 관리 팀에 문의하십시오. 이 구성은 일반적으로 온보딩 프로세스의 일부입니다.

통신 제한 규칙을 검토하거나 설정하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동하십시오. 탐색 패널의 _[!UICONTROL 전자 메일]_&#x200B;에서 **[!UICONTROL 통신 제한]**&#x200B;을 선택합니다.

![통신 제한 구성에 액세스](./assets/config-email-communication-limits.png){width="700" zoomable="yes"}

기본적으로 요구 사항에 따라 여러 규칙을 정의, 활성화 및 비활성화할 수 있는 글로벌 규칙 세트가 있습니다. 규칙 목록을 표시하려면 규칙 세트 이름을 클릭합니다.

### 규칙 만들기

1. 오른쪽 상단의 **[!UICONTROL 규칙 만들기]**&#x200B;를 클릭합니다.

   ![통신 제한 구성에 액세스](./assets/config-email-communication-limits-create-rule-select.png){width="600" zoomable="yes"}

1. **[!UICONTROL 규칙 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL 최대 한도]**&#x200B;를 설정합니다.

   값을 입력하거나 오른쪽의 _위쪽_ 또는 _아래쪽_ 화살표를 클릭하여 값을 늘리거나 줄입니다.

1. 제한 기간을 정의하는 방법에 따라 **[!UICONTROL 최대 가용량 다시 설정]** 값을 선택하십시오.

   _[!UICONTROL 시간별]_, _[!UICONTROL 일별]_, _[!UICONTROL 주별]_ 또는 _[!UICONTROL 월별]_&#x200B;을 선택할 수 있습니다.

   ![통신 제한 구성에 액세스](./assets/config-email-communication-limits-create-rule-settings.png){width="600" zoomable="yes"}

1. 기간에 포함할 빈도 단위의 수에 따라 **[!UICONTROL Every]** 값을 설정하십시오.

   예를 들어 _일별_&#x200B;을 빈도로 사용하고 이 값을 `3`(으)로 설정하면 기간은 3일로 정의됩니다.

1. 오른쪽 상단의 **[!UICONTROL 규칙 만들기]**&#x200B;를 클릭합니다.

새 규칙은 _초안_ 상태이며 활성화하기로 선택할 때까지 통신 제한에 적용되지 않습니다.

### 규칙 관리

규칙이 _초안_ 상태인 동안에는 정의를 편집하거나 규칙을 삭제할 수 있습니다. 규칙을 적용하려는 경우 규칙을 활성화할 수 있습니다. 목록에서 초안 규칙 이름 옆에 있는 _추가 메뉴_(***...***) 아이콘을 클릭하고 **[!UICONTROL 활성화]**&#x200B;를 선택합니다.

![초안 통신 제한 규칙에 대한 기타 메뉴를 클릭합니다](./assets/config-email-communication-limits-draft-more-menu.png){width="400" zoomable="yes"}

확인 대화 상자에서 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

활성 규칙은 편집하거나 삭제할 수 없으며 비활성화만 가능합니다. 적용된 통신 제한에서 제거할 활성 규칙의 경우 활성 규칙 이름 옆에 있는 _비활성화_( ![비활성화 아이콘](../assets/do-not-localize/icon-deactivate.svg)) 아이콘을 클릭합니다.

![활성 통신 제한 규칙에 대한 비활성화 아이콘을 클릭합니다](./assets/config-email-communication-limits-active-deactivate.png){width="400" zoomable="yes"}

그런 다음 확인 대화 상자에서 **[!UICONTROL 비활성화]**&#x200B;를 클릭합니다.

규칙이 _비활성_ 상태로 표시됩니다. 초안 규칙과 유사하며 필요한 경우 편집, 삭제 또는 활성화할 수 있습니다.

## SPF/DKIM

DNS 설정에 SPF(Sender Policy Framework) 및 DKIM(Domain Keys Identified Mail)를 통합하여 이메일 게재 속도를 개선합니다. 이러한 기술은 수신자에게 이메일이 스팸이 아님을 보장합니다. 수신자의 스팸 필터가 이메일을 거부하지 않도록 하려면 도메인에 대해 SPF 및 DKIM이 설정되어 있는지 확인하십시오.

현재 설정을 검토하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동하세요. 탐색 패널의 _[!UICONTROL 전자 메일]_&#x200B;에서 **[!UICONTROL SPF/DKIM]**&#x200B;을(를) 선택합니다.

![SPF/DKIM 구성 액세스](./assets/config-email-spf-dkim.png){width="700" zoomable="yes"}

설정은 Journey Optimizer B2B edition에서 읽기 전용입니다. 연결된 Marketo Engage 인스턴스의 구성 옵션에 액세스하려면 오른쪽 상단의 **[!UICONTROL 설정 편집]**&#x200B;을 클릭하십시오.

>[!NOTE]
>
>Adobe Marketo Engage에서 이러한 설정에 액세스하고 편집하려면 제품 관리자 권한이 있어야 합니다.

### SPF 설정

네트워크 관리자가 DNS 항목에 다음 줄을 추가해야 합니다.

`[domain] IN TXT v=spf1 mx ip4:[corpIP] include:mktomail.com ~all`

이 항목에서 `[domain]`을(를) 웹 사이트의 주 도메인(예: `company.com`)으로 바꾸고 `[corpIP]`을(를) 회사 전자 메일 서버의 IP 주소(예: `255.255.255.255`)로 바꿉니다. Marketo Engage을 통해 여러 도메인에서 이메일을 보내는 경우 한 줄에 각 도메인에 대해 이 항목을 추가하십시오.

DNS 항목에 이미 SPF 레코드가 있는 경우 다음을 추가합니다.

`include:mktomail.com`

### DKIM 설정

DKIM은 이메일 수신자가 이메일 메시지 발신자의 유효성을 검사하는 데 사용하는 인증 프로토콜입니다. 수신자는 메시지가 위조가 아님을 확신할 수 있으므로 종종 받은 편지함으로 이메일을 배달하는 기능이 향상됩니다.

DNS 레코드에 공개 키가 있고 연결된 Marketo Engage 인스턴스에서 전송 도메인이 활성화된 경우 보내는 메시지에 사용자 지정 DKIM 서명이 사용됩니다. 사용자 지정 DKIM 서명에는 전송된 각 이메일이 있는 암호화된 디지털 서명이 포함됩니다. 그러면 수신자는 보내는 도메인의 DNS에서 _공개 키_&#x200B;를 조회하여 디지털 서명을 해독할 수 있습니다. 이메일의 키가 DNS 레코드의 키와 일치하는 경우 수신 메일 서버는 Marketo Engage을 통해 전송된 이메일을 수락할 가능성이 높습니다.

전자 메일 게재를 위한 사용자 지정 DKIM 서명 구성에 대한 자세한 내용은 [Marketo Engage 설명서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}를 참조하세요.

## 보트 활동

이메일 봇 활동은 이메일 열기 및 클릭 데이터를 잘못 부풀릴 수 있습니다.

Marketo Engage에서는 보트 활동을 확인하는 두 가지 방법을 사용합니다.

* **IAB(Interactive Advertising Bureau) 목록과 일치** - IAB UA/IP(사용자 에이전트/IP 주소) 목록에 있는 모든 활동과 일치하는 활동이 봇으로 표시됩니다.

* **근접 패턴과 일치** - 두 개 이상의 활동이 동시에(1초 이내) 발생하면 봇으로 식별됩니다. 이 메서드는 비교를 위해 다음 속성을 고려합니다.

   * 잠재 고객 ID(같아야 함)
   * 이메일 자산(동일해야 함)
   * 링크 클릭 또는 이메일 열기
   * 시간 차이(1초 미만이어야 함)

이메일 링크 클릭 및 이메일 열기 활동의 경우 새 속성이 다음 값으로 채워집니다.

* 봇으로 식별되는 활동에는 식별된 패턴/메서드로 _봇 활동_&#x200B;이(가) `True`(으)로, _봇 활동 패턴_&#x200B;이(가) 있습니다.
* 봇이 아닌 것으로 식별된 활동에는 _봇 활동_&#x200B;이 `False`(으)로 _봇 활동 패턴_&#x200B;이 `N/A`(으)로 있습니다.
* 특성이 도입되기 전에 발생하는 활동에는 _봇 활동_&#x200B;이 비어 있음(null)으로 표시되고 _봇 활동 패턴_&#x200B;이 비어 있음(null)으로 표시됩니다.

현재 설정을 검토하려면 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동하세요. 탐색 패널의 _[!UICONTROL 전자 메일]_&#x200B;에서 **[!UICONTROL 봇 활동]**&#x200B;을 선택합니다.

![전자 메일 게재를 위한 봇 활동 구성에 액세스](./assets/config-email-bot-activity.png){width="700" zoomable="yes"}

설정은 Journey Optimizer B2B edition에서 읽기 전용입니다. 연결된 Marketo Engage 인스턴스의 구성 옵션에 액세스하려면 오른쪽 상단의 **[!UICONTROL 설정 편집]**&#x200B;을 클릭하십시오.

>[!NOTE]
>
>Adobe Marketo Engage에서 이러한 설정에 액세스하고 편집하려면 제품 관리자 권한이 있어야 합니다.

보트 활동 옵션 구성에 대한 자세한 내용은 [Marketo Engage 설명서](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/administration/email-setup/filtering-email-bot-activity#select-filter-type){target="_blank"}를 참조하세요.
