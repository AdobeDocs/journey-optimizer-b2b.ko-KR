---
title: 거버넌스 기능
description: 현재 Journey Optimizer B2B edition에서 사용할 수 있는 거버넌스 기능에 대해 알아봅니다.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: d6e625c1-468f-4d73-9f32-fd1edb87f96bid: f2da1b69-6919-4386-a5d2-9c7b5c9033db
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: 2026-03-27T23:18:44.352Z
TQID: https://experienceleague.adobe.com/PwH34suDPc84nB9eiAWtrkVzsOw82RRGw4hrRogf9zE
source-git-commit: 94a8ed9584459cf85a72448cd698740ef450ddb2
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 0%

---

# 거버넌스 기능

Journey Optimizer B2B edition은 통합 Adobe Experience Platform 앱입니다. 비즈니스 관행, 법적 의무 및 개발 프로세스를 준수하여 수집된 경험 데이터를 제어하는 여러 가지 도구와 서비스를 사용합니다. 아래 섹션에서는 이러한 각 거버넌스 기능에 대한 요약을 제공합니다.

## 개인 정보 - GDPR

Journey Optimizer B2B edition은 Privacy Service 및 Marketo Privacy Broker Service에서 제공하는 기존 Marketo Engage GDPR 거버넌스 기능을 사용합니다.

## RBAC(역할 기반 액세스 제어)

Journey Optimizer B2B edition 및 Adobe Admin Console에 대한 액세스를 통해 관리자는 엔티티 유형(보기-세그먼트, 관리-세그먼트, 관리-여정 등)에 대한 사용자 권한을 부여할 수 있습니다. 이 기능은 모든 Adobe Experience Platform 고객이 조직에 대한 역할 및 권한을 정의하고 관리할 수 있도록 하는 통합 권한 프레임워크(UPF)의 일부입니다.

## 데이터 암호화

**_사용하지 않는 데이터에 대한 암호화_** - Adobe Experience Platform에서 Journey Optimizer B2B edition으로 전송되는 모든 계정 및 개인 프로필 데이터는 Experience Platform의 기존 준수 상태를 유지하기 위해 암호화됩니다. 여정 및 구매 그룹과 같은 Journey Optimizer B2B edition에서 시작된 모든 엔티티도 암호화됩니다.

**_전송 중인 데이터에 대한 암호화_**(공용 네트워크를 통해) - 모든 Journey Optimizer B2B edition API 및 엔터티는 TLS 1.2를 사용하여 전송 중에 암호화됩니다.

## 동의 옵트인/옵트아웃

Journey Optimizer B2B edition은 Adobe Experience Platform XDM 프로필에 저장된 개인별 동의 환경 설정을 읽고 이메일, SMS 및 WhatsApp 채널에 대한 메시지 게재 시간에 강제 적용합니다. 채널을 옵트아웃한 사람은 채널 또는 다운스트림 메시징 공급자에서 콘텐츠를 전송하기 전에 게재에서 제외됩니다.

동의는 프로필 동의 필드 그룹의 XDM 필드를 사용하여 게재 시 평가됩니다. 기본 동의 비헤이비어는 채널마다 다릅니다. 기본 설정이 없으면 이메일이 기본적으로 옵트인으로 설정되고, SMS와 WhatsApp은 기본적으로 옵트아웃으로 설정됩니다.

각 채널에 대해 평가된 XDM 특성 및 기본 동작에 대한 자세한 내용은 [동의 환경 설정](../content/channels-consent-preferences.md)을 참조하십시오.

## 샌드박스 재설정

샌드박스 재설정은 Adobe Journey Optimizer B2B edition에 대해 현재 지원되지 않습니다&#x200B;**.** Journey Optimizer B2B edition에 매핑된 샌드박스를 재설정하거나 삭제하면 영구적인 데이터 손실이 발생할 수 있으며 새 인스턴스를 프로비저닝해야 합니다.

## 아직 사용할 수 없음

다음 거버넌스 기능은 아직 사용할 수 없습니다.

* 데이터 사용 레이블 적용 (DULE) / 사용 정책
* 데이터 위생
* 동의 정책
* 필드 수준 액세스 제어(FLAC)
* 객체 수준 액세스 제어(OLAC)
* 사용하지 않는 데이터에 대한 CMK 암호화
* 플랫폼 감사 서비스
