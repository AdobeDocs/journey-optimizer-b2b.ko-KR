---
title: Marketo Engage을 활성화하여 여정 작업 지원
description: Marketo Engage 연결을 활성화하여 여정 작업을 지원하면 마케터가 Marketo Engage과 Journey Optimizer B2B edition 간의 캠페인을 조정할 수 있습니다.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# Marketo Engage 인스턴스를 활성화하여 작업 지원

Marketo Engage 작업은 Journey Optimizer B2B edition과 Marketo Engage의 _리드 기반_ 마케팅 활동 간에 _계정 기반_ 마케팅 오케스트레이션을 조정할 수 있는 _사람 기반_ 작업입니다. 이러한 작업을 사용하여 정적 목록 멤버십을 조정하고 사람을 캠페인에 배치합니다.

Marketo Engage 작업을 사용하려면 관리자가 먼저 인증에 필요한 자격 증명을 제공하는 Marketo Engage에서 [사용자 지정 서비스](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/custom-services#)를 만듭니다.
그런 다음 Journey Optimizer B2B edition의 제품 관리자가 자격 증명을 입력하여 Marketo Engage에 대한 연결을 만듭니다.
그런 다음 Journey Optimizer B2B edition 사용자는 연결을 참조하여 <!-- Person and -->계정 여정에서 Marketo Engage 작업을 구성할 수 있습니다(예: Marketo Engage 목록에서 사용자를 추가 또는 제거하거나 요청 캠페인에 추가).

목록 및 캠페인과 같은 에셋에 대한 Marketo Engage 작업 영역 가시성은 사용자 지정 서비스에서 할당된 역할 권한에 의해 제어됩니다.

여정 내에서 동일한 연결을 여러 번 사용할 수 있으며, 단일 여정에서 서로 다른 Marketo Engage 연결이 공존할 수 있습니다.

작업이 실행되면 선택 정책을 사용하여 Marketo Engage에서 어느 개인 레코드를 사용하여 통합 개인 프로필에 여러 식별자가 있는지 여부를 선택합니다. 옵션에는 가장 오래된 레코드, 가장 최신 레코드 또는 일치하는 모든 Marketo Engage 레코드를 선택하는 옵션이 포함됩니다. 사람들은 오류가 발생하는 경우를 제외하고 일치 항목에 관계없이 여정을 진행합니다.

## Marketo Engage 연결 구성

Marketo Engage 여정 작업에 사용할 원격 Marketo Engage 인스턴스를 구성합니다.

### Marketo Engage 사용자 정의 서비스 만들기

1. Marketo Engage에 관리자로 로그인하고 사용자 지정 서비스를 만듭니다.
1. 연결에 사용할 다음 값을 기록하십시오.

   * Munchkin ID
   * 클라이언트 ID
   * 클라이언트 암호

### 통합 추가

![통합 세부 정보 추가](assets/integration-connection-details.png)

1. Journey Optimizer B2B edition에서 **관리** > **구성**&#x200B;으로 이동합니다.
1. **통합** 탭을 선택합니다.
1. **[!UICONTROL 연결 만들기]**&#x200B;를 클릭합니다.
1. 이름(필수) 및 설명(선택 사항)을 입력합니다.
1. 일치하는 개인 레코드에 대해 **선택 정책**&#x200B;을 선택하세요.
1. Munchkin ID, 클라이언트 ID 및 클라이언트 암호를 입력합니다.
1. **[!UICONTROL Marketo에 연결]**&#x200B;을 클릭합니다.
1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

마케터가 여정에서 Marketo Engage 작업을 사용할 때 연결 이름을 사용하여 노드를 구성할 수 있습니다.

통합이 완료되면 노드 속성의 **다음에 대한 작업:**&#x200B;에서 Marketo Engage 작업을 사용할 수 있습니다.

![Marketo 작업 목록](assets/marketo-actions-list.png)