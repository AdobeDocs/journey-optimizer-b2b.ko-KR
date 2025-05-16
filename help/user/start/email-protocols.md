---
title: 추적 및 이메일 게재를 위한 프로토콜
description: Marketo Engage에서 추적 및 이메일 채널 기능을 위해 Journey Optimizer B2B 에디션에서 사용할 프로토콜을 구성하는 방법에 대해 알아봅니다.
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '1798'
ht-degree: 93%

---

# 추적 및 이메일 게재를 위한 프로토콜

Adobe Journey Optimizer B2B 에디션은 Marketo Engage의 이메일 채널 기능과 이벤트 추적 기능을 활용합니다. 제한적 방화벽 또는 프록시 서버 설정을 사용하는 조직에서 이메일 게재가 예상대로 작동하도록 하려면 시스템 관리자가 특정 도메인과 IP 주소 범위를 허용 목록에 추가해야 합니다.

>[!NOTE]
>
>조직이 이미 연결된 Marketo Engage 인스턴스를 사용하여 마케팅 작업을 실행하고 있다면 이러한 프로토콜과 구성이 이미 마련되어 있어야 합니다.

모든 Marketo Engage 리소스와 웹 소켓을 활성화하려면 다음 도메인(별표 포함)을 허용 목록에 추가해야 합니다.

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

추적 및 이메일 게재를 보장하기 위해 다음 단계를 따릅니다.

1. [다음에 대한 DNS 레코드 만들기 ](#create-dns-records-for-landing-pages-and-email)
1. [SPF 및 DKIM 설정](#set-up-spf-and-dkim)
1. [DMARC 설정](#set-up-dmarc)
1. [도메인에 대한 MX 레코드 설정](#set-up-mx-records-for-your-domain)
1. [허용 목록에 아웃바운드 IP 주소 추가](#outbound-ip-addresses)

## &#x200B;<!-- landing pages and -->이메일에 대한 DNS 레코드 만들기

CNAME 레코드를 연결하면 마케터는 일관된 브랜딩을 적용하여 이메일, 랜딩 페이지, 블로그의 웹 버전을 호스팅할 수 있어 트래픽과 전환율이 향상됩니다. 마케팅에 중점을 둔 웹 자산을 호스팅하려면 Marketo Engage의 루트 도메인 호스트에 CNAME을 추가하는 것이 좋습니다. 관리자는 마케팅 팀과 협력하여 Marketo Engage를 통해 전송되는 이메일에 포함된 추적 링크에 대한 CNAME 레코드를 계획하고 구현해야 합니다.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### 이메일 추적 링크에 CNAME 추가

`[YourEmailCNAME]`이 Marketo Engage에서 할당한 기본 추적 링크인 `[MktoTrackingLink]`를 가리키도록 이메일 CNAME을 추가합니다.

CNAME `[YourEmailCNAME].[YourDomain].com`의 `[MktoTrackingLink]`

예:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>`[MktoTrackingLink]` 값은 기본 브랜딩 도메인이어야 합니다.

### SSL 인증서 프로비전

SSL 인증서 프로비저닝 프로세스를 시작하려면 [Adobe 지원](https://experienceleague.adobe.com/home?lang=ko&amp;support-tab=home#support){target="_blank"}에 문의하십시오.

이 프로세스를 완료하는 데 영업일 기준 최대 3일이 소요될 수 있습니다.

## SPF 및 DKIM 설정

마케팅 팀은 DNS 리소스 레코드에 추가할 DKIM(Domain Keys Identified Mail) 정보를 제공해야 합니다. 다음 단계에 따라 DDIM 및 SPF(발신자 정책 프레임워크)를 구성한 다음 업데이트되면 마케팅 팀에 알립니다.

1. SPF를 설정하려면 DNS 항목에 다음 줄을 추가합니다.

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   DNS 항목에 이미 기존 SPF 레코드가 있는 경우 다음을 추가하기만 하면 됩니다.

   ```
   include: mktomail.com
   ```

   `CompanyDomain`을 웹 사이트의 메인 도메인(예: `company.com/`)으로, `CorpIP`를 회사 이메일 서버의 IP 주소(예: `255.255.255.255`)로 교체합니다. Marketo Engage를 통해 여러 도메인에서 이메일을 보내려면 각 도메인에 대해 이 줄을 추가합니다(한 줄에).

1. DKIM의 경우 각 도메인에 대한 DNS 리소스 레코드를 만듭니다.

   각 도메인에 대한 호스트 레코드와 TXT 값을 추가합니다.

   `[DKIMDomain1]`: 호스트 레코드는 `[HostRecord1]`이고 TXT 값은 `[TXTValue1]`입니다.

   `[DKIMDomain2]`: 호스트 레코드는 `[HostRecord2]`이고 TXT 값은 `[TXTValue2]`입니다.

   Marketo Engage 설명서의 [지침](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}을(를) 수행한 후 각 DKIM 도메인에 대한 `HostRecord` 및 `TXTValue`을(를) 복사합니다. Journey Optimizer B2B 에디션에서 도메인을 확인할 수 있습니다([SPF/DKIM](../admin/configure-channels-emails.md#spfdkim) 참조).

## DMARC 설정

DMARC(도메인 기반 메시지 인증, 보고 및 적합성)는 무단 사용으로부터 도메인을 보호하기 위해 조직에서 사용하는 인증 프로토콜입니다. SPF 및 DKIM과 같은 기존 인증 프로토콜을 확장하여 도메인에서 인증 실패가 발생할 경우 취해야 할 액션을 수신 서버에 알립니다. DMARC는 선택 사항이지만 브랜드와 평판을 보호하는 데 도움이 되므로 강력히 추천합니다. Google 및 Yahoo와 같은 주요 제공업체는 2024년 2월부터 대량 발신자에게 DMARC 사용을 의무화하기 시작했습니다.

DMARC가 작동하려면 다음 DNS TXT 레코드 중 하나 이상이 있어야 합니다.

* 유효한 SPF
* FROM에 대한 유효한 DKIM 레코드: 도메인(Marketo Engage 및 Journey Optimizer B2B 에디션에 권장)

`FROM:` 도메인에 대한 DMARC 전용 DNS TXT 레코드도 있어야 합니다. 원할 경우, 보고서 모니터링을 위해 조직 내에서 DMARC 보고서가 어디로 전송되어야 하는지 지정하는 이메일 주소를 정의할 수 있습니다.

### DMARC 워크플로 예시

>[!TIP]
>
>DMARC를 _느린 롤아웃_&#x200B;으로 구현하는 것이 최선의 방법입니다. 잠재적 영향을 이해하게 되면 DMARC 정책을 `p=none`에서 `p=quarantine`으로, 그 다음 `p=reject`로 확대하고, DMARC 정책을 SPF와 DMKIM에 대한 완화된 정렬로 설정합니다.

DMARC 보고서를 받으면 다음 작업을 수행해야 합니다.

1. `p=none`을 사용하여 받은 피드백과 보고서를 분석합니다. 보고서는 수신자에게 인증에 실패한 메시지에 대해 아무런 액션을 취하지 말 것을 지시하고, 발신자에게 이메일 보고서를 보냅니다.

   * 정상적인 메시지가 인증에 실패하는 경우 SPF/DKIM 문제를 검토하여 수정합니다.

   * 모든 정상적인 이메일에 대해 SPF 또는 DKIM이 정렬되어 인증을 통과하는지 확인합니다.

   * 보고서를 검토하여 SPF/DKIM 정책에 따라 예상되는 결과가 나오는지 확인합니다.

1. 정책을 `p=quarantine`으로 조정하면 수신 이메일 서버에 인증 실패한 이메일(일반적으로 스팸 폴더에 해당 메시지를 저장)을 격리하도록 지시합니다.

   보고서를 검토하여 결과가 기대에 부합하는지 확인합니다.

1. `p=quarantine` 수준에서 메시지의 비헤이비어에 만족하는 경우 정책을 (`p=reject`)로 조정할 수 있습니다.

   거부 정책은 수신자에게 인증 실패한 도메인의 이메일을 거부(바운스)하라고 지시합니다. 이 정책을 활성화하면 도메인에서 100% 인증된 것으로 확인된 이메일만 받은 편지함을 배치할 수 있습니다.

   >[!CAUTION]
   >
   >이 정책을 신중하게 사용하고 조직에 적합한지 확인합니다.

### DMARC 보고

DMARC는 SPF/DKIM에 실패한 이메일에 대한 보고서를 수신할 수 있는 기능을 제공합니다. 인증 프로세스의 일환으로 ISP 서비스 제공자가 두 가지 서로 다른 보고서를 생성합니다. 발신자는 DMARC 정책의 RUA/RUF 태그를 통해 이러한 보고서를 받을 수 있습니다.

* **집계 보고서(RUA)**: GDPR(일반정보보호 규정)에 따라 민감할 수 있는 PII(개인 식별 정보)를 포함하지 않습니다.

* **포렌식 보고서(RUF)** - GDPR에 따라 민감한 이메일 주소를 포함합니다. 이 보고서를 실행하기 전에 GDPR 준수가 필요한 정보를 처리하기 위한 조직 정책을 확인합니다.

이러한 보고서의 주요 용도는 스푸핑 시도가 있는 이메일에 대한 개요를 받는 것입니다. 이러한 보고서는 매우 기술적인 내용이므로 서드파티 도구를 통해 이해하는 것이 가장 좋습니다.

### DMARC 레코드 예시

* 최소 레코드: `v=DMARC1; p=none`

* 보고서를 받기 위해 이메일 주소로 연결되는 레코드: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC 태그

DMARC 레코드에는 _DMARC 태그_&#x200B;라는 여러 구성 요소가 있습니다. 각 태그에는 DMARC의 특정 측면을 지정하는 값이 있습니다.

| 태그 이름 | 사용 | 함수 | 예 | 기본 값 |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | 필수 | 버전을 지정합니다. 버전이 하나뿐이므로 고정된 값은 `v=DMARC1`입니다. | V=DMARC1 DMARC1 | DMARC1 |
| `p` | 필수 | 수신자가 인증 확인에 실패한 이메일을 보고, 격리 또는 거부하도록 지시하는 DMARC 정책을 지정합니다. | `p=none`, `p=quarantine` 또는 `p=reject` | - |
| `fo` | 선택 사항입니다 | 도메인 소유자가 보고 옵션을 지정할 수 있습니다. | `0`: SPF와 DKIM 모두 실패하면 보고서 생성 <br> `1` - SPF 또는 DKIM이 실패하면 보고서 생성 <br> `d` - DKIM이 실패하면 보고서 생성 <br> `s` - SPF가 실패하면 보고서 생성 | `1` (DMARC 보고서에 권장됨) |
| `pct` | 선택 사항입니다 | 필터링 대상 메시지의 비율을 지정합니다. | `pct=20` | `100` |
| `rua` | 선택 사항 (권장) | 집계 보고서가 게재되는 위치를 지정합니다. | `rua=mailto:aggrep@example.com` | - |
| `ruf` | 선택 사항 (권장) | 포렌식 보고서가 게재되는 장소를 지정합니다. | `ruf=mailto:authfail@example.com` | - |
| `sp` | 선택 사항입니다 | 상위 도메인의 하위 도메인에 대한 DMARC 정책을 지정합니다. | `sp=reject` | - |
| `adkim` | 선택 사항입니다 | 엄격한(`s`) 또는 완화된(`r`) 정렬을 지정합니다. 완화된 정렬은 도메인이 DKIM 서명에 사용되고 `From:` 주소의 하위 도메인이 될 수 있음을 의미합니다. 엄격한 정렬은 도메인이 DKIM 서명에 사용되고 `From:` 주소에 사용된 도메인과 정확히 일치해야 함을 의미합니다. | `adkim=r` | `r` |
| `aspf` | 선택 사항입니다 | 엄격하거나(`s`) 완화될(`r`) 수 있습니다. 완화 모드는 반환 경로 도메인이 `From:` 주소의 하위 도메인이 될 수 있음을 의미합니다. 엄격 모드는 반환 경로 도메인이 `From:` 주소와 정확히 일치해야 함을 의미합니다. | `aspf=r` | `r` |

DMARC 및 모든 옵션에 대한 자세한 내용은 [https://dmarc.org/](https://dmarc.org/){target="_blank"}을(를) 참조하십시오.

### Marketo Engage를 위한 DMARC 구현

DMARC에는 두 가지 유형의 정렬이 있습니다.

* **DKIM**(Domain Keys Identified Mail) 정렬: 이메일의 `From:` 헤더에 지정된 도메인이 DKIM 서명과 일치합니다. DKIM 서명에는 도메인이 `d=` 헤더 도메인과 일치하도록 지정된 `From:` 값이 포함되어 있습니다.

  DKIM 정렬은 발신자가 도메인에서 메일을 보낼 권한이 있는지 확인하고 이메일 전송 중에 콘텐츠가 변경되지 않았는지 확인합니다. DKIM에 정렬된 DMARC를 구현하려면:

   * 메시지의 MAIL FROM 도메인에 대한 DKIM을 설정합니다. Marketo Engage 설명서의 [지침](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"}을 사용하십시오.

   * DKIM MAIL FROM 도메인에 대해 DMARC를 구성합니다.

  >[!NOTE]
  >
  >Marketo Engage에는 DKIM 정렬이 권장됩니다.

* **SPF**(발신자 정책 프레임워크) 정렬: `From:` 헤더의 도메인은 Return-Path: 헤더의 도메인과 일치해야 합니다. 두 DNS 도메인이 동일하면 SPF가 일치(정렬)되어 통과 결과가 나옵니다. SPF에 정렬된 DMARC를 구현하려면:

   * 브랜드 Return-Path 도메인을 설정합니다.

      * 적절한 SPF 레코드를 구성합니다.
      * 메일을 보낸 데이터 센터의 기본 MX를 가리키도록 MX 레코드를 변경합니다

   * 브랜드 Return-Path 도메인에 대해 DMARC를 구성합니다.

  >[!NOTE]
  >
  >Marketo Engage에서는 엄격한 SPF 정렬이 지원되거나 권장되지 않습니다.

### 전용 IP 및 공유 풀

전용 IP를 통해 Marketo Engage을 통해 메일을 보내고 브랜드 반환 경로를 구현하지 않은 경우(또는 반환 경로가 있는지 확실하지 않은 경우) [Adobe 지원](https://experienceleague.adobe.com/home?lang=ko&amp;support-tab=home#support){target="_blank"}에서 티켓을 엽니다.

신뢰할 수 있는 IP는 월 75,000건 미만을 보내는 저용량 사용자를 위해 예약된 공유 IP 풀로, 전용 IP에 적합하지 않습니다. 이러한 사용자는 모범 사례 요구 사항도 충족해야 합니다.

* 공유 IP 풀을 사용하여 Marketo Engage을 통해 메일을 보내는 경우 [신뢰할 수 있는 IP 전송 범위 프로그램에 적용](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}하여 신뢰할 수 있는 IP에 대한 자격이 있는지 확인할 수 있습니다. Marketo Engage의 신뢰할 수 있는 IP에서 보내는 경우 브랜드 return-path가 포함됩니다. 이 프로그램에 승인되면 Adobe 지원 센터에 연락하여 브랜드 return-path를 설정합니다.

* 한 달에 10만 개 이상의 메시지를 보내고 공유 IP를 사용하여 Marketo Engage를 통해 이메일을 보내려는 경우 Adobe 계정 팀(계정 관리자)에 문의하여 전용 IP를 구매하십시오.

## 도메인에 대한 MX 레코드 설정

MX 레코드를 사용하면 이메일을 보내는 도메인으로 메일을 수신하여 답장과 자동 응답을 처리할 수 있습니다. 회사 도메인에서 보내는 경우 이미 구성되어 있을 수 있습니다. 그렇지 않은 경우 일반적으로 회사 도메인 MX 레코드에 매핑하도록 설정할 수 있습니다.

## 아웃바운드 IP 주소

아웃바운드 연결은 Marketo Engage가 사용자를 대신하여 인터넷 서버에 연결하는 것입니다. 귀하의 IT 조직과 일부 파트너/공급업체는 서버 접근을 제한하기 위해 허용 목록을 사용할 수 있습니다. 그렇다면 허용 목록에 추가할 수 있도록 Marketo Engagement 아웃바운드 IP 주소 블록을 제공해야 합니다.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/ko/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## 아웃바운드 IP 주소 블록

다음 목록은 아웃바운드 호출을 수행하는 모든 Marketo Engage 서버를 다룹니다. Marketo Engage에서 발신 연결을 수신하도록 IP 허용 목록, 서버, 방화벽, 액세스 제어 목록, 보안 그룹 또는 서드파티 서비스를 구성하려면 다음 목록을 참조하십시오.

| IP 블록 (CIDR 표기법) | 개별 IP 주소 |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
