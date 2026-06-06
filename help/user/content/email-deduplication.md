---
title: 이메일 중복 제거
description: 계정 여정에서 이메일 중복 제거를 사용하여 동일한 이메일이 동일한 이메일 주소로 여러 번 전송되지 않도록 하는 방법에 대해 알아봅니다.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 이메일, 중복 제거, 여정, 복제
exl-id: 93107acd-1cb2-4316-acfc-e32ab1e065ae
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
  - id: f01b5556-e951-40ba-8625-2e3001864f2b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
autotag-review: 2026-03-30T22:08:16.582Z
TQID: https://experienceleague.adobe.com/aWKXaC6x4Izeh81A6Fpy-Nrf18fHgnq6jUc-82ohErs
source-git-commit: 2c6aafd07cf033df8801621f7e5275dbeeb2768e
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# 이메일 중복 제거

여정 내의 동일한 이메일 주소에 동일한 이메일이 여러 번 전송되지 않도록 하려면 계정 여정에서 이메일 중복 제거를 사용합니다. 이 기능을 활성화하면 해당 이메일 주소가 있는 첫 번째 레코드가 여정을 완료할 때까지 중복 이메일 주소가 차단됩니다. 여정이 여정을 완료하면 사용자는 계정을 입력하는 새 계정의 일부로 이메일을 다시 받을 자격이 있습니다.

## 이메일 중복 제거 사용 시기

이메일 중복 제거를 활성화하기 위해 고려해야 할 몇 가지 주요 시나리오가 있습니다.

* **전자 메일이 Real-Time CDP에서 ID로 사용되지 않습니다** - 동일한 전자 메일 주소가 여러 사용자 프로필에 표시될 수 있습니다. 이러한 중복 프로필이 동일한 여정에 대한 자격이 있고 이메일을 두 번 이상 보내지 않으려는 경우 이 기능을 활성화합니다.

* **여러 계정과 연결된 한 사람** - [!DNL Real-Time CDP] 데이터 모델이 한 사람을 여러 계정과 연결하는 경우, 이 기능을 사용하면 동일한 이메일 주소를 가진 여러 프로필이 동일한 여정에 대한 자격이 될 때 동일한 이메일을 두 번 보내지 않습니다.

>[!NOTE]
>
>이메일 중복 제거는 여정 수준에서 적용됩니다. 동일한 이메일 주소를 가진 사람이 다른 여정에 적격인 경우에도 각 여정에서 이메일을 받을 수 있습니다.

## 여정에 대해 이메일 중복 제거 활성화

계정 여정에 대해 이메일 중복 제거를 활성화하려면 다음 작업을 수행하십시오.

1. 계정 여정을 엽니다.

1. **[!UICONTROL 자세히]**(**...**) 클릭 여정 작업 영역의 오른쪽 상단 모서리에서 을 참조하십시오.

   ![전자 메일 중복 제거 옵션을 표시하는 기타 메뉴가 확장된 여정 작업 영역](./assets/email-deduplication-more-menu.png){width="450"}

1. **[!UICONTROL 전자 메일 중복 제거]**&#x200B;를 선택하세요.

1. 대화 상자에서 **[!UICONTROL 전자 메일 중복 제거]** 확인란을 선택합니다.

   ![토글이 활성화된 이메일 중복 제거 대화 상자](./assets/email-deduplication-dialog.png){width="400"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이메일 중복 제거가 활성화되면 여정은 이메일을 보내기 전에 각 이메일 주소를 확인합니다. 이메일 주소가 동일한 레코드가 해당 여정 노드에 이미 입력된 경우, 첫 번째 레코드가 여정을 완료할 때까지 새 항목이 차단됩니다.
