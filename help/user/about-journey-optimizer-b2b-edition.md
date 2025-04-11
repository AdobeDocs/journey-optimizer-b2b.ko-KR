---
title: Adobe Journey Optimizer B2B 에디션 개요
description: Adobe Journey Optimizer B2B 에디션의 주요 기능, 사용 사례 및 아키텍처를 살펴봅니다.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 5ca03b12fd459c64b245ad95e60a382c355922f9
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 100%

---

# Adobe Journey Optimizer B2B 에디션 개요

Adobe Journey Optimizer B2B 에디션을 사용하면 기본 제공 생성형 AI와 업계 최고 수준의 자동화를 활용하여 계정 및 구매 그룹 여정을 조율하고, 마케팅 적격 구매 그룹을 사용하여 특정 오퍼에 대한 수요를 극대화할 수 있습니다.

## 구매 그룹과 계정 여정

Adobe Journey Optimizer B2B 에디션을 표준 Marketo Engage와 Adobe Journey Optimizer와 비교할 때 가장 큰 차이점은 계정 여정이 사람이 아닌 여정을 통해 계정을 이동한다는 것입니다. 일반적으로 계정에 연결된 사람은 개인적인 행동이 아닌 계정의 여정 진행 상태에 따라 비선형적으로 진행됩니다. 예를 들어 계정이 구매 여정의 초기 단계에 있을 때는 일반적인 솔루션 기능이나 특징에 대한 정보가 전송될 수 있습니다. 구매 여정이 진행됨에 따라, 콘텐츠는 판매를 성사시키는 데 도움이 되는 특정 혜택이나 기타 항목에 더욱 집중하게 됩니다. 솔루션을 구매한 후에는 방법 안내서, 모범 사례, 예정된 이벤트에 대한 정보 또는 추가 업셀에 대한 콘텐츠로 정보가 다시 변경될 수 있습니다. 개인이 초기 단계 콘텐츠와 상호 작용하지 않았더라도, 그 개인의 행동이 아닌 해당 계정 또는 구매 그룹 내 다른 사람들의 행동에 따라 현재 단계로 진행해야 합니다.

## 고차원의 아키텍처

Adobe Journey Optimizer B2B 에디션은 Adobe Experience Platform의 _계정 대상자_&#x200B;와 _사람 대상자_&#x200B;를 사용하여 Marketo Engage 내에서 실행되는 계정 여정을 구동합니다. Experience Platform은 항상 이러한 데이터의 최종 소스이지만 계정 여정의 모든 실행과 처리는 Marketo Engage B2B 마케팅 인프라 내에서 이루어집니다. 오케스트레이션은 기존 Marketo Engage - Adobe Real-Time CDP B2B 에디션 소스 커넥터를 통해 거의 실시간으로 데이터를 Experience Platform으로 다시 가져오며, 이를 통해 Marketo Engage에서 Experience Platform으로 데이터 변경 사항이 스트리밍됩니다.

![고차원의 데이터 아키텍처](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>성능 가드레일과 정적 제한 사항에 대한 라이선스 권한과 해당 [제품 설명](https://helpx.adobe.com/kr/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"}을 확인하십시오.

### 구독 모델

Journey Optimizer B2B 에디션 구독은 Marketo Engage _Munchkin_ 구독이 포함된 Experience Platform(AEP) 샌드박스 2개로 정의됩니다. 단일 Marketo Engage 구독을 두 개 이상의 AEP 샌드박스와 연결할 수는 없습니다. 기존 Marketo Engage 구독을 Journey Optimizer B2B 에디션과 연결하지 않도록 선택하는 경우, Journey Optimizer B2B 에디션과 함께 사용할 수 있는 비어 있는 새 Marketo Engage 구독이 프로비저닝됩니다.

이러한 설정에서 Experience Platform의 목적은 Marketo Engage 인스턴스(및 연결된 CRM 시스템)의 데이터를 종합적으로 보여 주고, 계정 여정을 사용하여 통합된 데이터에 대한 조치를 취할 수 있도록 하는 것입니다.

### 계정 여정 운영

계정 여정은 Journey Optimizer B2B 에디션에서 작성되며, 구독과 관련된 Marketo Engage 인스턴스에 저장됩니다. Marketo Engage 데이터 저장소에 저장되지만 Marketo Engage UI에서는 볼 수 없으며 Journey Optimizer B2B 에디션에서만 사용할 수 있습니다.

계정 여정은 항상 여정의 계정 대상자로 사용할 계정 세그먼트를 선택하는 것으로 시작됩니다. 대상자 선택에는 표준 Experience Platform 대상자 선택기 구성 요소가 사용됩니다. 마케터는 계정 기준, 사람 기준 또는 구매 그룹 기준 등의 자체 기준에 따라 여정 경로를 분할하여 계정 여정을 구현할 수 있습니다. 각 분기에서는 이메일을 보내거나 이벤트가 발생할 때까지 기다리는 등 여정을 구현하기 위한 조치를 취할 수 있습니다.

계정 여정을 만든 후에는 게시해야 합니다. 게시 시점에 계정 여정이 검증되며 여정 경험을 구현하는 일련의 Marketo Engage 캠페인으로 변환됩니다. 데이터 통합 서비스에 연락하면 데이터 흐름이 시작되고, 이를 통해 계정 여정 작업이 시작됩니다. 첫 번째 단계는 계정 내 사람들에 대한 세그먼트를 만드는 것입니다.

### 데이터 흐름

Journey Optimizer B2B 에디션은 Real-Time CDP 계정 세분화를 사용하여 여정에 필요한 계정 세그먼트와 관련 계정 담당자 세그먼트를 정의하고 실행합니다. 게시된 여정이 진행됨에 따라 사람과 계정에 대한 데이터가 변경될 수 있으며, 여정과 상호 작용하는 사람들에 대한 데이터가 수집됩니다. Journey Optimizer B2B 에디션은 Real-Time CDP B2B 에디션용 Marketo Engage 소스 커넥터를 사용하여 데이터 변경 사항을 최종 소스인 Experience Platform 샌드박스로 다시 전달합니다. 이 데이터는 거의 실시간으로 AEP에 전달됩니다.

Marketo Engage 소스 커넥터가 지원하는 기존 데이터 유형(계정, 사람, 기회)만 Real-Time CDP로 다시 흐릅니다. 즉, 구매 그룹 데이터는 AEP로 흐르지 않고 대신 Journey Optimizer B2B 에디션 구독에서 사용하는 Marketo Engage 인스턴스에 저장됩니다.
