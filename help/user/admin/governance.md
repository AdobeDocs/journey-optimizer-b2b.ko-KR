---
title: 거버넌스 기능
description: 현재 Journey Optimizer B2B edition에서 사용할 수 있는 거버넌스 기능에 대해 알아봅니다.
feature: Setup
role: Admin
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 거버넌스 기능

Journey Optimizer B2B edition은 통합 Adobe Experience Platform 앱입니다. 비즈니스 관행, 법적 의무 및 개발 프로세스를 준수하여 수집된 경험 데이터를 제어하는 여러 가지 도구와 서비스를 사용합니다. 아래 섹션에서는 이러한 각 거버넌스 기능에 대한 요약을 제공합니다.

## 개인 정보 - GDPR

Journey Optimizer B2B edition은 Privacy Service 및 Marketo Privacy Broker Service에서 제공하는 기존 Marketo Engage GDPR 거버넌스 기능을 사용합니다.

## RBAC(역할 기반 액세스 제어)

Journey Optimizer B2B edition 및 Adobe Admin Console에 대한 액세스를 통해 관리자는 엔티티 유형(보기-세그먼트, 관리-세그먼트, 관리-여정 등)에 대한 사용자 권한을 부여할 수 있습니다. 이 기능은 모든 Adobe Experience Platform 고객이 조직에 대한 역할 및 권한을 정의하고 관리할 수 있도록 하는 통합 권한 프레임워크(UPF)의 일부입니다.

## 데이터 암호화

**_사용하지 않는 데이터에 대한 암호화_** - Adobe Experience Platform에서 Journey Optimizer B2B edition으로 전송되는 모든 계정 및 개인 프로필 데이터는 Experience Platform의 기존 규정 준수를 유지하기 위해 암호화됩니다. 여정 및 구매 그룹과 같은 Journey Optimizer B2B edition에서 시작된 모든 엔티티도 암호화됩니다.

**_전송 중인 데이터에 대한 암호화_**(공용 네트워크를 통해) - 모든 Journey Optimizer B2B edition API 및 엔터티는 TLS 1.2를 사용하여 전송 중에 암호화됩니다.

## 동의 옵트인/옵트아웃

동의 옵트인/옵트아웃은 프로필이 이메일 또는 SMS와 같은 통신 채널에서 옵트아웃할 수 있는 거버넌스 형식이며, 프로필은 통신 채널에서 제외됩니다.

Journey Optimizer B2B edition을 사용하여 이메일 및 SMS 게재 사용 사례에 대한 구독/구독 취소 사용 사례를 작성하고 관리할 수 있습니다. 이러한 동의 환경 설정은 XDM 프로필 동의 필드 그룹 내에 저장되며 데이터 동기화 프레임워크의 일부로 Journey Optimizer B2B edition에 동기화되고 동기화되지 않습니다. 이러한 환경 설정은 게재에서 옵트아웃된 프로필을 제외하기 위해 게재 시간에 사용됩니다.

## 샌드박스 재설정

샌드박스 재설정은 Adobe Journey Optimizer B2B edition에 대해 현재 지원되지 않습니다&#x200B;**.** Journey Optimizer B2B edition에 매핑된 샌드박스를 재설정하거나 삭제하면 Journey Optimizer B2B edition의 데이터가 영구적으로 손실될 수 있으며 새 Journey Optimizer B2B edition 인스턴스를 프로비저닝해야 할 수 있습니다.

## 아직 사용할 수 없음

다음 거버넌스 기능은 아직 사용할 수 없습니다.

* 데이터 사용 레이블 적용 (DULE) / 사용 정책
* 데이터 위생
* 동의 정책
* 필드 수준 액세스 제어(FLAC)
* 객체 수준 액세스 제어(OLAC)
* 사용하지 않는 데이터에 대한 CMK 암호화
* 플랫폼 감사 서비스
