---
title: 브랜딩 도메인 구성
description: 각 브랜드에 고유한 브랜딩 추적 링크가 있도록 브랜딩 도메인을 구성합니다.
feature: Setup, Channels
role: Admin
source-git-commit: 023e44e1ad2baed2a5586d95a26ef8693020667a
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 1%

---

# 브랜딩 도메인 구성

Marketo Engage의 브랜딩 도메인은 링크를 다시 작성하고 이메일 클릭을 추적하고 일반 도메인이 아닌 브랜드를 반영하는 데 사용되는 사용자 지정 하위 도메인(예: `links.yourcompany.com`)입니다. 각 브랜딩 도메인은 클릭 추적 도메인으로 작동하여 이메일 및 랜딩 페이지 링크를 도메인과 일치시켜 전달성과 신뢰도를 향상시킵니다.

* 이메일 하이퍼링크에서 일반 링크를 고유한 브랜딩으로 대체합니다.
* 계정 리드가 링크를 클릭하면 이 사용자 정의 도메인을 통해 리디렉션되어 이메일 필터에 합법적인 것처럼 보이는 동안 성능 추적을 허용합니다.
* 여러 브랜드가 있는 경우 다른 비즈니스 단위 또는 브랜드를 지원하도록 추가 브랜딩 도메인을 구성할 수 있습니다.

>[!BEGINSHADEBOX]

**링크 추적을 위한 고유 CNAME**

이메일 추적 링크는 첨부된 Marketo Engage 인스턴스에 대해 새 링크이고 고유해야 합니다. 링크 추적을 위한 기존 CNAME이 기존(프로덕션) Marketo Engage 인스턴스를 가리키면 _있는 그대로_&#x200B;를 재사용할 수 없습니다.

프로덕션 Marketo Engage 인스턴스와 연결된 인스턴스 간에 반환 경로 도메인 브랜딩을 공유할 수 있지만 이는 백엔드 변경 사항입니다. 지원 티켓을 열고 Marketo Engage 접두사(Munchkin ID)와 새 Journey Optimizer B2B edition 접두사(Munchkin ID)를 입력하여 공유 리턴 경로 도메인 브랜딩을 요청합니다.

>[!ENDSHADEBOX]

>[!PREREQUISITES]
>
>UI에서 도메인을 편집하거나 추가하려면 먼저 Adobe에서 제공한 Marketo Engage 도메인[&#128279;](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#customize-your-landing-page-urls-with-a-cname){target="_blank"}에 매핑된 CNAME이 있어야 합니다.
>
>도메인을 추가할 때 시스템은 이전에 수동으로 생성되었을 수 있는 기존 SSL을 확인합니다. 이 유효성 검사가 발생하면 SSL 생성을 선택하지 않고 도메인을 만든 다음 별도의 절차로 연결합니다.

## Marketo Engage의 브랜딩 도메인에 액세스

1. Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL 브랜딩 도메인]** 패널로 스크롤합니다.

   전자 메일 아래의 관리자의 ![브랜딩 도메인 패널에 기본 도메인이 표시됨](./assets/me-admin-email-branding-domains.png){width="700" zoomable="yes"}

   이 목록에는 Marketo Engage 인스턴스에 대한 기본 도메인이 표시됩니다.

## 기본 브랜딩 도메인 편집

브랜딩 도메인 작업의 첫 번째 단계는 Marketo Engage 인스턴스에 정의된 기본 브랜딩 도메인을 편집하는 것입니다.

>[!NOTE]
>
>일반 기본 도메인을 편집하기 전에는 추가 브랜딩 도메인을 정의할 수 없습니다.

1. _[!UICONTROL 브랜딩 도메인]_ 패널에서 일반 도메인을 선택하고 맨 위에 있는 **[!UICONTROL 편집]**&#x200B;을 클릭합니다.

   일반 도메인이 선택된 ![브랜딩 도메인 패널](./assets/me-admin-email-branding-domains-edit-default.png){width="500"}

1. _[!UICONTROL 브랜딩 도메인 편집]_ 대화 상자에서 **[!UICONTROL 도메인]** 필드에 기본 도메인 이름을 입력합니다.

   ![브랜딩 도메인 편집 대화 상자](./assets/me-admin-email-branding-domains-edit-default-name.png){width="400"}

1. Marketo Engage 인스턴스에 대해 여러 작업 공간이 정의된 경우 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   업데이트된 주 도메인을 적용할 각 작업 공간을 선택합니다.

   ![주 도메인에 대한 작업 영역 선택이 포함된 브랜딩 도메인 편집 대화 상자](./assets/me-admin-email-branding-domains-edit-default-workspaces.png){width="400"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 추가 도메인 정의

기본 도메인을 편집한 후, Journey Optimizer B2B edition 환경에서 여러 브랜드를 실행하고자 할 때 다른 브랜딩 도메인을 추가할 수 있습니다. 이 경우 각 브랜드에는 고유한 추적 링크가 있습니다. 도메인을 추가할 때 다음 옵션이 제공됩니다.

>* _주 도메인으로 설정_: 이 도메인을 작업 영역의 주 도메인으로 설정합니다. 이 옵션을 선택하면 기존의 전송되지 않은 모든 이메일이 기본 주 도메인으로 설정되고 새로 생성된 모든 이메일은 자동으로 이 주 도메인으로 설정됩니다. 마케터는 필요한 경우 대체 브랜딩 도메인을 선택할 수 있습니다.
>
>* _SSL 인증서 생성_: 도메인 생성으로 SSL(Secure Sockets Layer)을 만듭니다. 첫 번째 추적 도메인은 몇 시간이 소요될 수 있는 인프라의 일회성 설정을 개시한다. 완료 시 시스템에서 알림이 전송됩니다.

도메인을 추가하려면(_T):_

1. _[!UICONTROL 브랜딩 도메인]_ 패널에서 상단의 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

   상단의 추가 단추가 있는 ![브랜딩 도메인 패널](assets/me-admin-email-branding-domains-add.png){width="500"}

1. _[!UICONTROL 새 브랜딩 도메인]_ 대화 상자에서 **[!UICONTROL 도메인]** 필드에 브랜딩 도메인의 이름을 입력합니다.

1. (선택 사항) **[!UICONTROL SSL 인증서 생성]** 확인란을 선택하여 도메인에 대한 SSL을 자동으로 생성합니다.

   ![새 브랜딩 도메인 대화 상자](assets/me-admin-email-branding-domains-add-name.png){width="400"}

   필요한 경우 _주 도메인 만들기_ 확인란을 선택할 수도 있습니다.

   >[!NOTE]
   >
   >**_사용자 지정 SSL_**: 사용자 지정 SSL이 필요한 경우 [지원 티켓](https://nation.marketo.com/t5/support/ct-p/Support){target="_blank"}을 제출할 수 있습니다. SSL 작성에 확인란을 사용하지 마십시오.

1. Marketo Engage 인스턴스에 대해 여러 작업 공간이 정의된 경우 **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   필요한 경우 새 도메인을 주 도메인으로 적용할 각 작업 공간을 선택합니다.

   ![주 도메인을 적용하기 위한 작업 영역 선택이 있는 새 브랜딩 도메인 대화 상자](assets/me-admin-email-branding-domains-add-workspaces.png){width="400"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 기존 브랜딩 도메인의 SSL 편집

기존 도메인에 대해 SSL을 활성화하려면 다음 단계를 따르십시오.

1. _[!UICONTROL 관리자]_ 영역에서 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL 브랜딩 도메인]_ 패널에서 도메인 행을 선택하고 **[!UICONTROL SSL 추가]**&#x200B;를 클릭합니다.

   ![맨 위에 SSL을 추가하는 브랜딩 도메인 패널](./assets/me-admin-email-branding-domain-add-ssl.png){width="500"}

1. 대화 상자에서 **[!UICONTROL 확인]**&#x200B;을 클릭합니다.

   ![SSL 인증서 생성 확인 대화 상자](./assets/me-admin-email-branding-domain-generate-ssl-cert-confirm.png){width="400"}

## 오류 메시지

| 오류 | 세부 사항 |
| ----- | ------- |
| `Domain already exists.` | 같은 이름의 도메인이 이미 있습니다. |
| `Domain is not mapped to the default domain.` | 사용자 정의 도메인이 기본 도메인에 올바르게 매핑되지 않습니다. 도메인 매핑 설정을 확인하고 DNS 구성이 올바른 기본 도메인을 가리켜야 합니다. |
| `SSL certificates could not be issued due to unsupported CAA records. Request your IT to update your CAA records.` | CAA 레코드가 최신 상태가 아닙니다. Adobe 관리 SSL 인증서를 사용하는 사용자의 경우 CAA 레코드를 공급업체에서 권장하는 인증서로 업데이트해야 합니다. |
| `SSL certificate has already been issued.` | 이 사용자 정의 도메인에 대한 SSL 인증서가 이미 있습니다. 인증서가 만료되었거나 다시 발급해야 하는 경우가 아니면 추가 작업이 필요하지 않습니다. |
| `The default domain was not found. Please contact Support for assistance.` | 기본 도메인을 찾으려고 할 때 문제가 발생했습니다. 조사를 트리거하려면 Adobe 지원에 문의하십시오. |
| `Unexpected error encountered while creating a domain. Please contact Support for assistance.` | 예기치 않은 오류가 발생했습니다. 로그 및 오류 세부 정보를 수집한 다음 Adobe 지원으로 문제를 에스컬레이션합니다. |

## 브랜딩 도메인 삭제

>[!NOTE]
>
>하나 이상의 작업 공간에서 기본 브랜딩 도메인을 삭제하려면 먼저 다른 브랜딩 도메인을 각 작업 공간의 기본 도메인으로 선택해야 합니다.
>
>**_도메인을 삭제하면 SSL 인증서가 삭제되지 않습니다_**. 이 가드레일은 SSL 인증서 없이 웹 사이트를 생성하는 사용자 오류를 방지합니다. SSL 인증서를 제거하려면 Adobe 지원에 문의하십시오.

_[!UICONTROL 브랜딩 도메인]_ 패널에서 도메인을 선택하고 맨 위에 있는 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.
