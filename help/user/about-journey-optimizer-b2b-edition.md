---
title: Adobe Journey Optimizer B2B edition 개요
description: Adobe Journey Optimizer B2B 에디션의 주요 기능, 사용 사례 및 아키텍처를 살펴봅니다.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d1696eb54c9ff25963b51a0e3934a02e103923e4
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# Adobe Journey Optimizer B2B edition 개요

Adobe Journey Optimizer B2B 에디션을 사용하면 빌트인된 생성형 AI와 업계 최고 수준의 자동화를 활용하여 계정 및 구매 그룹 여정을 조율하고, 마케팅 적격 구매 그룹을 사용하여 특정 오퍼에 대한 수요를 극대화할 수 있습니다.

## 구매 그룹이 있는 계정 여정

Adobe Journey Optimizer B2B edition을 Marketo Engage 및 Adobe Journey Optimizer 표준과 비교할 때, 주요 차이점은 계정 여정이 사람이 아닌 여정을 통해 계정을 이동한다는 것입니다. 일반적으로 계정과 연결된 사람은 개별 작업이 아닌 여정을 통한 계정 진행 상황에 따라 비선형 진행이 발생합니다. 예를 들어 계정이 구매 여정 초기 단계에 있는 경우 전송되는 정보는 일반적인 솔루션 기능에 대한 것일 수 있습니다. 구매 프로세스가 진행됨에 따라 콘텐츠는 특정 오퍼 또는 판매 종료에 맞춰진 다른 항목에 더 많이 타겟팅될 수 있습니다. 솔루션을 구입한 후 정보가 다시 변경되어 사용 방법 안내서, 모범 사례 또는 예정된 이벤트에 대한 정보나 추가 상향 판매에 대한 콘텐츠를 제공할 수 있습니다. 개인이 초기 단계 콘텐츠와 상호 작용하지 않았더라도 자신의 작업이 아닌 계정 또는 구매 그룹 내의 다른 사람의 작업에 따라 현재 단계로 진행하려고 합니다.

## 높은 수준의 아키텍처

Adobe Journey Optimizer B2B edition은 Adobe Experience Platform의 _계정 대상_ 및 _사람 대상_&#x200B;을 사용하여 Marketo Engage 내에서 실행되는 계정 여정을 실행합니다. Experience Platform은 항상 이 데이터에 대한 신뢰할 수 있는 소스이지만, Marketo Engage B2B 마케팅 인프라 내에서 계정 여정의 모든 실행 및 처리가 발생합니다. 오케스트레이션은 기존 Marketo Engage(Adobe Real-Time CDP B2B edition 소스 커넥터)에 의해 거의 실시간으로 데이터를 Experience Platform 상태로 되돌려 보내 Marketo Engage에서 Experience Platform으로 데이터 변경 사항을 스트리밍합니다.

![높은 수준의 데이터 아키텍처](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>성능 보호 및 정적 제한에 대해 라이선스 권한 및 해당 [제품 설명](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}을(를) 확인하십시오.

### 구독 모델

Journey Optimizer B2B edition 구독은 Marketo Engage _Munchkin_ 구독이 있는 Experience Platform(AEP) 샌드박스 쌍으로 정의됩니다. 단일 Marketo Engage 구독은 두 개 이상의 AEP 샌드박스와 쌍을 이룰 수 없습니다. 기존 Marketo Engage 구독과 Journey Optimizer B2B edition의 연결을 선택하지 않으면 Journey Optimizer B2B edition에서 사용할 수 있도록 새로운 빈 Marketo Engage 구독이 제공됩니다.

이 설정의 Experience Platform 목적은 Marketo Engage 인스턴스(및 연결된 CRM 시스템)의 데이터에 통합 보기를 제공한 다음 계정 여정을 사용하여 통합 데이터에 대한 작업을 수행할 수 있도록 하는 것입니다.

### 계정 여정 작업

계정 여정은 Journey Optimizer B2B edition에서 작성되며 구독과 연결된 Marketo Engage 인스턴스에 저장됩니다. Marketo Engage 데이터 저장소에 저장되지만 Marketo Engage UI에서는 표시되지 않으며 Journey Optimizer B2B edition에서만 사용할 수 있습니다.

계정 여정은 항상 여정의 계정 대상자로 사용할 계정 세그먼트를 선택하는 것으로 시작합니다. 대상을 선택하면 표준 Experience Platform 대상 선택기 구성 요소가 사용됩니다. 그런 다음 마케터는 계정 기준, 사람 기준 또는 구매 그룹 기준을 포함할 수 있는 자체 기준에 따라 여정 경로를 분할하여 계정 여정을 구현할 수 있습니다. 각 분기에서 이메일을 보내거나 이벤트가 발생할 때까지 기다리는 등 여정을 구현하기 위한 작업을 수행할 수 있습니다.

계정 여정이 만들어지면 게시해야 합니다. 게시 시 계정 여정은 검증되고 여정 경험을 구현하는 일련의 Marketo Engage 캠페인으로 변환됩니다. Data Integration Services에 연락하여 데이터 흐름을 시작하면 계정 여정 작업이 시작됩니다. 첫 번째 단계는 계정의 사용자에 대한 세그먼트를 만드는 것입니다.

### 데이터 흐름

Journey Optimizer B2B edition은 여정에 필요한 계정 세그먼트 및 관련 계정 사용자 세그먼트를 정의 및 실행하기 위해 Real-Time CDP 계정 세그먼테이션을 사용합니다. 게시된 여정이 실행되면 사용자 및 계정에 대한 데이터가 변경될 수 있으며, 여정과 상호 작용하는 사람들에 대한 데이터가 수집됩니다. Journey Optimizer B2B edition은 Real-Time CDP B2B edition용 Marketo Engage 소스 커넥터를 사용하여 데이터 변경 사항을 소스로 하는 Experience Platform 샌드박스로 다시 전달합니다.  이 데이터는 거의 실시간으로 AEP에 전달됩니다.

Marketo Engage 소스 커넥터에서 지원하는 기존 데이터 유형(계정, 사람 및 기회)만 Real-Time CDP으로 다시 흐릅니다. 즉, 구매 그룹 데이터는 AEP로 흐르지 않고 대신 Journey Optimizer B2B edition 구독에서 사용하는 Marketo Engage 인스턴스에 있습니다.
