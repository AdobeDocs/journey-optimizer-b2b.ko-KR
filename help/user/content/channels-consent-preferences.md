---
title: 채널 메시징 동의
description: Journey Optimizer B2B edition에서 AEP XDM 프로필 동의 환경 설정을 읽고 이메일, SMS 및 WhatsApp 채널에 대한 메시지 게재 시간에 옵트인 및 옵트아웃을 적용하는 방법에 대해 알아봅니다.
feature: Setup, Channels
role: Admin, User
autotag-review: '2026-05-19T16:18:37.228Z'
TQID: 'https://experienceleague.adobe.com/-c0dJnpfiIcj0B5gViyEQ7E1Ws0BwP864OLF003rOjw'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a4b836d9-ffdd-4df3-a62a-f78b830cf059id: f01b5556-e951-40ba-8625-2e3001864f2b
subfeature_v2: id: ff0c35fa-aa7e-4050-a37c-198fcacd09e6id: a22f05f6-0fcf-40c0-a70e-e13a3db185f7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 94a8ed9584459cf85a72448cd698740ef450ddb2
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 1%

---

# 채널 메시징 동의

Adobe Journey Optimizer B2B edition은 Adobe Experience Platform XDM 프로필에 저장된 개인별 동의 환경 설정을 읽고 앱의 [거버넌스 컨트롤](../admin/governance.md)의 일부로 메시지 배달 시간에 적용합니다. 채널을 옵트아웃한 사람은 채널 또는 다운스트림 메시징 공급자에서 콘텐츠를 전송하기 전에 게재에서 제외됩니다.

다음 섹션에서는 Journey Optimizer B2B edition이 지원되는 각 채널에 대한 메시지 전송 시 동의를 평가하는 방법을 설명합니다.

## 이메일 {#email}

Journey Optimizer B2B edition은 [전자 메일 채널](../admin/configure-channels-emails.md)에서 메시지를 보낼 때 전자 메일 동의에 대해 다음 XDM 특성을 평가합니다.

| XDM 속성 | `y` | `n` | 값 없음 |
| --- | --- | --- | --- |
| `consents.marketing.email.val` | 옵트인 | 옵트아웃됨 | 옵트인 |

이메일 동의를 위해 다음 고려 사항을 염두에 두십시오.

* 이메일에서 전역적으로 옵트아웃한 사람은 여전히 작동 중으로 표시된 이메일을 받을 수 있습니다.
* 구독 수준 환경 설정은 지원되지 않습니다.

## SMS {#sms}

Journey Optimizer B2B edition은 [SMS 채널](../admin/configure-channels-sms.md)을 통해 메시지를 보낼 때 SMS 동의에 대해 다음 XDM 특성을 평가합니다.

| XDM 속성 | `y` | `n` | 값 없음 |
| --- | --- | --- | --- |
| `consents.marketing.sms.val` | 옵트인 | 옵트아웃됨 | 옵트아웃됨 |
| `consents.marketing.subscriptions.<senderID>` | 옵트인 | 옵트아웃됨 | 옵트아웃됨 |
| `consents.marketing.sms.subscriptions.<senderId>.subscribers.<phoneNumber>` | 옵트인 | 옵트아웃됨 | 옵트아웃됨 |

SMS 동의를 위해 다음 고려 사항을 염두에 두십시오.

* 잠재 고객(개인) 레코드가 SMS에서 옵트아웃되면 레코드가 완전히 제외되고 다운스트림 SMS 공급자로 전달되지 않습니다.
* 사용 가능한 경우 구독 수준 동의가 평가됩니다. 전역 옵트아웃은 구독 수준 동의를 사용할 수 없는 경우 폴백으로 사용됩니다.
* SMS에서 옵트아웃한 사람은 여전히 작동 중으로 표시된 메시지를 받을 수 있습니다.
* 여러 잠재 고객 레코드가 동일한 전화 번호를 공유하는 경우 동일한 옵트인 또는 옵트아웃 상태를 공유합니다.

## WhatsApp {#whatsapp}

Journey Optimizer B2B edition은 구성된 [WhatsApp 채널](../admin/configure-channels-whatsapp.md)을 통해 메시지를 보낼 때 WhatsApp 동의에 대해 다음 XDM 특성을 평가합니다.

| XDM 속성 | `y` | `n` | 값 없음 |
| --- | --- | --- | --- |
| `consents.marketing.whatsApp.val` | 옵트인 | 옵트아웃됨 | 옵트아웃됨 |
| `consents.idSpecific.Phone.<number>.marketing.whatsApp.val` | 옵트인 | 옵트아웃됨 | 옵트아웃됨 |

WhatsApp 동의에 대해 다음 고려 사항을 염두에 두십시오.

* 전역 WhatsApp 특성 값(`consents.marketing.whatsApp.val`)이 있으면 동의 평가에 사용됩니다.
* 전역 속성 값이 없지만 발신자별 항목이 있는 경우 동의 평가에 발신자별 항목이 사용됩니다.
* 두 속성 중 하나에 대한 값이 없으면 개인이 옵트아웃된 것으로 처리됩니다.

## 지원되지 않음 {#not-supported}

다음 동의 관련 기능은 현재 Journey Optimizer B2B edition에서 지원되지 않습니다.

* AEP 동의 정책
* 마케팅 기본 설정 특성(`consents.marketing.preferred`)
