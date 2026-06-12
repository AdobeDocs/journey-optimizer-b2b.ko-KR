---
title: 이메일 전달성 및 채널 구성
description: Journey Optimizer B2B Prime에 대한 하위 도메인 위임, DMARC, SPF, DKIM, IP 풀 및 이메일 채널 구성을 구성합니다.
source-git-commit: 2f19137465c71f2292d37bea5786533b1df6e286
workflow-type: tm+mt
source-wordcount: '3414'
ht-degree: 0%

---

# 이메일 전달성 및 채널 구성

[!DNL Adobe Journey Optimizer B2B Edition] Prime은 B2B 마케터에게 현대적인 엔터프라이즈급 이메일 작성 및 게재 환경을 제공합니다. 이 릴리스에는 새롭게 디자인된 이메일 디자인 도구 및 전체 이메일 전달성 제어 세트가 도입되었습니다.

다음 정보는 마케터 및 이메일 작성자를 지원하도록 전송 인프라를 구성하는 관리자를 위한 것입니다. 게재 기능, 역할 및 권한, 하위 도메인, 인증, IP 풀 및 채널 구성을 구성하는 방법에 대해 설명합니다.

전자 메일 디자인 공간에서 전자 메일을 만들고 전자 메일 콘텐츠를 작성하는 방법에 대한 자세한 내용은 [전자 메일 작성](../content/email-authoring.md)을 참조하십시오.

## 이메일 채널 개요 {#overview}

* **시각적 드래그 앤 드롭 이메일 디자인 도구** - 구조, 콘텐츠 구성 요소, 테마, 다크 모드 지원 및 재사용 가능한 시각적 조각을 사용하여 이메일 콘텐츠를 디자인할 수 있습니다.
* **전자 메일 채널 구성** - 보낸 사람 ID, 회신 동작, 마케팅과 트랜잭션 메시지 유형 및 추적을 관리합니다.
* **전자 메일 배달 가능성 컨트롤** - 하위 도메인 위임(완전히 위임됨 및 CNAME 메서드), DMARC, SPF/DKIM 자동 구성 및 공유 IP 풀 지원을 포함하여 전자 메일 배달 가능성 채널을 설정합니다.
* **전자 메일 보내기 작업** - 프로필에서 여정 특성(Handlebars 구문)을 사용한 개인화를 포함한 전자 메일 보내기 작업을 추가합니다.
* **Marketo Design Studio 자산** — 전자 메일 캔버스 내부에 직접 있는 Marketo Engage 자산 라이브러리의 일회성 복사본에서 이미지와 자산을 선택합니다.
* **재사용 가능한 템플릿 및 조각** — 일반적인 머리글, 바닥글, CTA 및 전체 이메일 레이아웃을 저장하고 여정 간에 재사용합니다.
* **RBAC(역할 기반 액세스 제어)** — 전자 메일을 만들고, 편집하고, 승인하고, 전송하기 위해 세분화된 권한을 적용합니다.

## 주요 개념 {#key-concepts}

이메일을 구성하기 전에 제품 전체의 이메일 채널 기능에 적용되는 이러한 개념을 검토하십시오.

| 개념 | [!DNL Journey Optimizer B2B Edition] Prime의 의미 |
| ------- | ---------------------- |
| **_채널 구성_** | 여정의 이메일 작업에 첨부하는 재사용 가능한 이메일 전송 설정(발신자 ID, 회신 주소, 하위 도메인, IP 풀, 이메일 유형(마케팅 또는 트랜잭션) 및 추적 포함). 서로 다른 브랜드, 비즈니스 단위 또는 전송 유형에 대해 이름이 지정된 여러 채널 구성을 가질 수 있습니다. |
| **_하위 도메인_** | Prime을 통해 전자 메일을 보내는 데 사용되는 전송 도메인(예: `mail.contoso.com`)의 위임된 부분입니다. 하위 도메인은 B2B 마케팅 평판을 회사 또는 트랜잭션 메일로부터 격리합니다. |
| **_IP 풀_** | 하나 이상의 하위 도메인과 연관된 IP 주소 그룹입니다. Prime은 이번 릴리스에서 Adobe에서 관리하는 공유 IP 풀을 지원합니다. 전용 IP 풀은 GA 로드맵에 있습니다. |
| **_전자 메일 디자인 공간_** | 이메일 콘텐츠를 구성하는 데 사용되는 시각적 캔버스 및 디자인 도구입니다. 여기에는 드래그 앤 드롭 레이아웃 구성 요소, 템플릿, 조각, 테마 및 개인화 편집기가 포함되어 있습니다. |
| **_템플릿_** | 새 이메일을 만드는 데 사용할 수 있는 재사용 가능한 이메일 레이아웃. Adobe에서 제공하는 내장 샘플 템플릿 또는 팀에서 만드는 사용자 지정 빌드 템플릿일 수 있습니다. |
| **_시각적 조각_** | 여러 이메일에 삽입할 수 있는 재사용 가능한 콘텐츠 블록(예: 머리글, 바닥글, CTA, 법적 고지 사항). 조각을 업데이트하면 해당 조각을 사용하는 모든 이메일에 변경 사항이 전파됩니다. |
| **_테마_** | 이메일 전체에 적용되는 재사용 가능한 스타일 사전 설정(색상, 타이포그래피, 간격, 버튼 스타일). |
| **_Personalization 토큰_** | Handlebars 식(예: `{{profile.firstName}}`)은 각 받는 사람의 프로필 데이터를 사용하여 전송 시 확인됩니다. |
| **_전자 메일 동작 보내기_** | 채널 구성 및 이메일 콘텐츠를 사용하여 이메일을 전달하는 여정 작업 노드입니다. |

## 역할 및 권한 {#roles-permissions}

[!DNL Journey Optimizer B2B Edition] Prime은 전자 메일 기능에 RBAC(역할 기반 액세스 제어)를 사용합니다. 권한은 Adobe Admin Console(IMS)에서 관리되고 로그인 시 동기화됩니다. 제품 관리자는 제품 프로필에 세분화된 권한을 할당한 다음 해당 제품 프로필을 사용자에게 연결합니다.

[!DNL Journey Optimizer B2B Edition] Prime의 이메일 기능에 대한 액세스는 다음 두 계층으로 구성됩니다.

1. **기능 플래그(LD).** LaunchDarkly 플래그는 조직에 대해 전체 기능이 켜져 있는지 여부를 제어합니다. 전자 메일 작성 및 게재 기능은 `dx_ajo_btob_channel_foundation`에 의해 제어됩니다. 이 플래그가 없으면 권한에 관계없이 기능이 숨겨집니다.
2. **기능 권한** 특정 사용자가 기능 내에서 읽거나 쓸 수 있는지 여부를 제어하는 사용자 수준 권한입니다.

대부분의 전자 메일 기능은 `view-*`(읽기) 및 `manage-*`(쓰기) 패턴을 따릅니다. 사용자에게 탐색에서 기능을 보려면 읽기 권한이 필요하고, 그 안에서 기능을 만들거나, 편집하거나, 삭제하려면 쓰기 권한이 있어야 합니다.

### 이메일 작성 권한 {#email-authoring-permissions}

| 기능 | 사용 권한 | 허용 사항 |
| ---------- | ---------- | -------------- |
| **전자 메일 보기** | `view-b2b-emails` | 이메일 목록 보기, 이메일 열기, 콘텐츠 보기(읽기 전용). |
| **전자 메일 만들기/편집/삭제** | `manage-b2b-emails` | 모든 읽기 권한과 이메일 만들기, 편집, 복제 및 삭제 여정 내에 이메일 콘텐츠를 작성하는 데 필요합니다. |
| **템플릿 보기** | `view-b2b-templates` | 템플릿 갤러리에서 템플릿을 찾아보고 미리 봅니다(읽기 전용). |
| **템플릿 만들기/편집/삭제** | `manage-b2b-templates` | 모든 읽기 액세스와 저장된 템플릿 만들기, 편집 및 삭제 |
| **조각 보기** | `view-b2b-fragments` | 시각적 조각 찾아보기 및 미리보기(읽기 전용) |
| **조각 만들기/편집** | `manage-b2b-fragments` | 모든 읽기 액세스와 더불어 시각적 조각을 만들고 편집합니다. |
| **조각 게시** | `publish-b2b-fragments` | 조직의 이메일 작성자에게 보낼 수 있도록 조각을 게시합니다. |
| **공유 자산 및 라이브러리 항목 관리** | `manage-b2b-library-items` | 템플릿, 조각 및 이메일에 사용되는 기본 공유 라이브러리를 관리합니다. 종종 템플릿/조각 관리 권한과 함께 부여됩니다. |
| **사용 레이블 관리** | `manage-b2b-delete-usage-labels` | 거버넌스를 위해 라이브러리 항목에 첨부된 DULE(데이터 사용 레이블)을 관리합니다. |
| **패키지 관리** | `manage-b2b-packages` | 샌드박스 간에 템플릿, 조각 및 이메일을 번들에 넣고 이동합니다. |
| **에셋 보기(Prime의 Marketo Design Studio 에셋)** | `view-b2b-assets` | 에셋 선택기를 탐색하고 이미지를 미리 봅니다. 읽기 전용. |
| **자산 관리** | `manage-b2b-assets` | 모든 읽기 액세스 권한과 향후 자산 관리 작업(Beta 범위). |
| **메시지 데이터 내보내기** | `manage-b2b-message-export` | 이메일 수준 메시지 데이터 및 보고서를 내보냅니다. |

여정 내에서 **전자 메일 보내기** 작업을 수행하려면 `manage-b2b-person-journeys`이(가) 필요합니다(작업을 추가하고 여정 활성화). 이메일 권한만 있는 여정은 콘텐츠를 작성할 수 있지만 사용자에게 이메일을 추가할 수는 없습니다.

### 이메일 게재 권한 {#email-deliverability-permissions}

게재 기능(하위 도메인, DMARC, IP 풀, 제외 목록, 허용 목록, IP 준비 계획 및 시드 목록)은 관리자 수준 구성입니다. 전체 **[!UICONTROL 채널]** > **[!UICONTROL 전자 메일 설정]** 영역에 대한 두 가지 권한이 적용됩니다.

| 기능 | 사용 권한 | 허용 사항 |
| ---------- | ---------- | -------------- |
| **전자 메일 설정 보기** | `view-b2b-email-settings` | 하위 도메인, PTR 레코드, IP 풀, 제외 목록, 허용 목록, IP 웜업 계획 및 시드 목록(읽기 전용)을 봅니다. |
| **전자 메일 설정 관리** | `manage-b2b-email-settings` | 모든 읽기 액세스 및 위임 하위 도메인, DMARC 구성, 제외 및 허용 목록 관리, IP 준비 계획 및 시드 목록 관리. |

이메일 설정 내의 일부 하위 기능은 추가 LaunchDarkly 플래그, 즉 비표시 목록(`enable-suppression`), 허용 목록(`enable-allow-list`), 시드 목록(`enable-seedlist-ui`)에 의해 게이팅됩니다. 하위 기능이 조직에 표시되지 않으면 플래그 활성화에 대해 Adobe 담당자에게 문의하십시오.

### 채널 구성 권한 {#channel-configuration-permissions}

채널 구성은 **[!UICONTROL 채널]** → **[!UICONTROL 일반 설정]**&#x200B;에 있습니다. 게재 가능성 프리미티브(하위 도메인, IP 풀, 발신자 ID)를 여정 작성자가 참조하는 재사용 가능한 오브젝트에 연결합니다. 이러한 권한은 단일 권한에 의해 관리됩니다.

| 기능 | 사용 권한 | 허용 사항 |
| ---------- | ---------- | -------------- |
| **채널 구성 관리** | `manage-b2b-channels-configurations` | 이메일 채널 구성 보기, 만들기, 편집 및 삭제 |

## 이메일 게재 기능 개요 {#deliverability-overview}

[!DNL Journey Optimizer B2B Edition] Prime의 전자 메일 게재 기능은 전자 메일 메시지가 스팸 폴더가 아니라 받는 사람의 받은 편지함에 도달하고 ISP(인터넷 서비스 공급자)에 의해 차단되지 않도록 하는 인프라 및 인증 구성 집합입니다.

일반적으로 다음 순서로 관리자가 구성한 다음 구성 요소를 사용합니다.

1. 하나 이상의 하위 도메인을 Adobe에 위임합니다.
1. 각 하위 도메인에서 DMARC, SPF 및 DKIM 레코드를 구성합니다.
1. 하위 도메인용 이메일을 보낼 IP 풀을 확인합니다.
1. 하위 도메인, IP 풀 및 발신자 ID를 바인딩하는 이메일 채널 구성을 하나 이상 만듭니다.
1. 여정 이메일 작업에서 이러한 채널 구성을 사용합니다.

>[!TIP]
>
>게재 기능 설정을 비즈니스 단위 또는 브랜드당 1회 관리자 활동으로 처리합니다. 구성된 경우 마케터와 이메일 작성자는 다시 방문할 필요가 없습니다.

## 하위 도메인 위임 {#subdomain-delegation}

하위 도메인 위임은 Adobe에 도메인의 특정 하위 도메인(예: `mail.contoso.com`) 대신 전자 메일을 보낼 수 있는 권한이 있음을 인터넷에 알려줍니다. 루트 도메인이 아닌 전용 하위 도메인을 위임하면 기업 메일이 보호되고 다음과 같은 결과가 발생합니다.

* **신뢰도 격리.** 마케팅 전송은 회사 메일과 별도로 유지됩니다. 마케팅 평판이 떨어지는 경우 트랜잭션 및 기업 메일은 영향을 받지 않습니다.
* **더 빠른 IP 준비** 전용 하위 도메인을 사용하면 ISP를 통해 긍정적인 발신자 평판을 보다 신속하게 구축할 수 있습니다.
* **최신 인증.** SPF, DKIM 및 DMARC은 다른 메일 흐름에 영향을 주지 않고 하위 도메인별로 깔끔하게 설정할 수 있습니다.
* **준수.** Gmail, Yahoo 및 기타 주요 ISP의 대량 발신자 요구 사항을 충족하도록 도와줍니다.

>[!NOTE]
>
>Prime의 각 하위 도메인은 하나의 Adobe 제품에서만 사용할 수 있습니다. Prime과 다른 제품(예: Adobe Marketo Engage 또는 Adobe Campaign) 간에 동일한 전송 하위 도메인을 공유할 수 없습니다. 고유한 하위 도메인을 사용해야 합니다.

### 지원되는 메서드

Prime은 Alpha에서 세 가지 하위 도메인 위임 방법 중 두 가지를 지원합니다. 세 번째 방법(사용자 지정 위임)은 로드맵에 있습니다.

| 메서드 | 사용 시기 | 관련 항목 |
| ------ | ----------- | ---------------- |
| **완전히 위임됨** | 추천 | 하위 도메인에 대한 전체 DNS 권한을 Adobe에 위임합니다. Adobe은 MX, SPF, DKIM, DMARC, A 및 CNAME 레코드를 생성하고 유지 관리합니다. 운영 부담 최소화 Adobe은 DNS 변경 사항을 처리합니다. |
| **CNAME** | 제한된 정책의 경우 | DNS 권한을 사용자 측에 유지하고 Adobe 관리 레코드를 가리키는 CNAME 레코드를 만듭니다. 조직의 DNS 정책이 전체 위임을 허용하지 않을 때 사용합니다. DNS 레코드를 유지 관리할 책임이 있습니다. |
| **사용자 지정 위임** | 로드맵(GA) | DNS 및 SSL 인증서의 완전한 소유권을 유지합니다. 자체 인증서를 사용하는 기능을 포함하여 최대 제어 기능을 제공합니다. 이는 GA 릴리스를 대상으로 합니다. |

### 하위 도메인 위임(완전히 위임된 메서드) {#delegate-fully-delegated}

>[!PREREQUISITES]
>
>* 하위 도메인 명명 규칙을 결정합니다(예: 마케팅의 경우 `mail.contoso.com`, 트랜잭션의 경우 `alerts.contoso.com`).
>* 하위 도메인(NS 레코드)을 Adobe에 위임할 수 있는지 IT/DNS 팀에 확인합니다.
>* DNS 공급자에서 새 하위 도메인을 만든 다음 Adobe으로 위임하기 전에 DNS 전파가 시작될 때까지 24-48시간 대기합니다.
>* Prime에서 관리자 역할이 있는지 확인합니다.

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime, **[!UICONTROL 관리]** → **[!UICONTROL 채널]** → **[!UICONTROL 전자 메일 설정]** → **[!UICONTROL 하위 도메인]**(으)로 이동.
1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.
1. 전체 하위 도메인 이름을 입력하십시오(예: `mail.contoso.com`).
1. 위임 방법으로 **[!UICONTROL 완전히 위임됨]**&#x200B;을(를) 선택하십시오.
1. 하위 도메인용 DMARC을 구성합니다([DMARC, SPF 및 DKIM](#dmarc-spf-dkim) 참조).

   최소한 `none`의 시작 정책으로 DMARC 레코드를 설정하여 배달에 영향을 주지 않고 보고서를 모니터링할 수 있습니다.

1. Adobe에서 관리할 DNS 레코드 목록을 검토하십시오.

   여기에는 일반적으로 MX, SPF, DKIM, DMARC, A 및 CNAME 레코드(추적 및 미러 페이지 URL용)가 포함됩니다.

1. **[!UICONTROL 레코드 다운로드]** 단추를 사용하여 DNS 레코드를 CSV 파일로 다운로드합니다. 이 파일을 DNS 팀과 공유합니다.

1. DNS 팀은 도메인 호스팅 솔루션에 하위 도메인을 Adobe에 위임하는 NS 레코드를 추가합니다.

1. DNS 팀이 레코드가 있는 것을 확인한 후 [!DNL Journey Optimizer B2B Edition] Prime으로 돌아가서 호스팅 사이트에 필요한 레코드를 만들었음을 확인하는 상자를 선택합니다.

1. 일련의 유효성 검사(사전 유효성 검사, MX, SPF, DKIM, DMARC, FBL 등록)를 시작하려면 **[!UICONTROL 제출]**&#x200B;을 클릭하십시오.

1. 하위 도메인 상태가 **[!UICONTROL 성공]**(으)로 변경될 때까지 기다리십시오.

   일반적으로 DNS 전파가 완료되면 몇 분 정도 소요됩니다.

>[!NOTE]
>
>유효성 검사가 실패하면 상태가 **[!UICONTROL 실패]**(으)로 변경되고 [!DNL Journey Optimizer B2B Edition] Prime에 이유가 표시됩니다(예: NS 레코드를 찾을 수 없음, MX 레코드가 누락됨 또는 DMARC이 잘못 구성됨). 기본 DNS 문제를 해결한 다음 제출을 다시 시도하십시오.

### 하위 도메인 위임(CNAME 메서드) {#delegate-cname}

조직의 DNS 정책이 전체 위임을 금지하는 경우에만 이 방법을 사용하십시오. CNAME을 사용하면 DNS 레코드를 사용자 측에서 유지 관리할 수 있습니다.

1. [!DNL Adobe Journey Optimizer B2B Edition] Prime에서 **[!UICONTROL 관리]** → **[!UICONTROL 채널]** → **[!UICONTROL 전자 메일 설정]** → **[!UICONTROL 하위 도메인]**&#x200B;으로 이동합니다.
1. **[!UICONTROL 하위 도메인 설정]**&#x200B;을 클릭합니다.
1. 전체 하위 도메인 이름을 입력합니다.
1. 위임 방법으로 **[!UICONTROL CNAME]**&#x200B;을(를) 선택하십시오.
1. 하위 도메인([DMARC, SPF 및 DKIM](#dmarc-spf-dkim))에 대해 DMARC을 구성합니다.
1. Prime에서 생성하는 CNAME 레코드 목록을 검토하십시오. 이렇게 하면 하위 도메인의 구성 요소가 Adobe 관리 레코드를 가리키게 됩니다.
1. 레코드를 CSV로 다운로드하고 DNS 팀과 공유합니다.
1. DNS 팀이 각 CNAME 레코드를 DNS 호스팅 솔루션에 추가합니다.
1. 레코드가 배치되고 전파되면 Prime으로 돌아가서 확인합니다. **[!UICONTROL 제출을 클릭합니다]**.
1. 상태가 **[!UICONTROL 성공]**&#x200B;에 도달할 때까지 기다리십시오.

>[!IMPORTANT]
>
>Adobe은 CNAME을 사용하여 하위 도메인의 DNS를 변경, 유지 관리 또는 문제를 해결할 수 없습니다. 기능 업데이트를 위해 새 CNAME을 추가하는 등 향후 변경 사항은 DNS 팀이 수행해야 합니다.

### 하위 도메인 보호 기능 {#subdomain-guardrails}

* **기본 제한:** 조직당 하위 도메인 10개. 더 필요한 경우 Adobe 담당자에게 문의하십시오(계약에 따라 최대 100개).
* **DNS 전파:** 변경 내용이 전역적으로 전파되는 데 24-48시간을 허용합니다. DNS가 아직 전파되지 않았기 때문에 유효성 검사가 실패할 수 있습니다.
* **하위 도메인 재사용:** 다른 Adobe 제품(Marketo Engage, Adobe Campaign)에서 이미 사용 중인 하위 도메인은 Prime에서 재사용할 수 없습니다.

## DMARC, SPF 및 DKIM {#dmarc-spf-dkim}

DMARC, SPF 및 DKIM은 이메일 인증 표준입니다. 이 둘을 합치면 메시지가 도메인을 대신하여 실제로 전송되고 스푸핑되지 않았음을 메일 서버를 받는 것으로 입증됩니다. Gmail, Yahoo, Microsoft과 같은 최신 ISP는 대량 발송자를 위해 이러한 표준을 필요로 합니다.

| 레코드 | 의 스탠드 | 용도 |
| ------ | ---------- | ------- |
| **SPF** | 보낸 사람 정책 프레임워크 | 도메인에서 메일을 보낼 수 있는 메일 서버 IP를 나열합니다. 수신 서버가 이 목록에 없는 IP의 메일을 거부합니다. Adobe은 하위 도메인(완전히 위임됨)을 위임할 때 SPF 레코드를 자동으로 만들고 유지 관리합니다. |
| **DKIM** | 식별된 메일 도메인 키 | 모든 아웃바운드 이메일에 암호화 서명이 추가되었습니다. 수신 서버는 DNS에 게시된 공개 키에 대해 서명을 확인합니다. Adobe은 하위 도메인을 위임하는 동안 DKIM 키 및 DNS 레코드를 자동으로 생성합니다. |
| **DMARC** | 도메인 기반 메시지 인증, 보고 및 적합성 | SPF 또는 DKIM이 실패할 경우 수행할 작업을 수신 서버에 알려주고 인증 결과에 대한 보고서를 제공합니다. DMARC에는 없음, 격리 및 거부의 세 가지 정책 모드가 있습니다. |

### DMARC 정책 모드

| 정책 | 액션 | 사용 시기 |
| ------ | ------ | ----------- |
| `none` | 모니터 | DMARC이 실패하면 수신 서버는 아무 작업도 하지 않지만 보고서를 전송합니다. 메시지 손실의 위험 없이 인증이 작동하는지 확인하기 위해 하위 도메인을 처음 위임할 때 사용합니다. |
| `quarantine` | 격리 | 수신 서버가 실패한 메시지를 스팸/정크 폴더에 배치합니다. |
| `reject` | 거부 | 수신 서버는 인증에 실패한 메시지를 거부(반송)합니다. 가장 엄격한 모드. 인증 설정이 확실하면 권장됩니다. |

### DMARC 구성 {#configure-dmarc}

DMARC은 하위 도메인 위임 시 구성되지만 이미 위임된 하위 도메인에 대해 DMARC을 추가하거나 업데이트할 수도 있습니다.

1. **[!UICONTROL 관리]** → **[!UICONTROL 채널]** → **[!UICONTROL 전자 메일 설정]** → **[!UICONTROL 하위 도메인]**&#x200B;으로 이동합니다.

1. 하위 도메인 목록에서 하위 도메인을 찾아 DMARC 레코드 열을 확인합니다.

   레코드가 누락된 경우 경고가 표시됩니다.

1. 하위 도메인을 열고 DMARC 레코드 섹션으로 스크롤합니다.

   * 부모 도메인에 DMARC 레코드가 이미 있으면 [!DNL Journey Optimizer B2B Edition] Prime에서 값을 자동으로 가져옵니다. 유지하거나 재정의할 수 있습니다.
   * 레코드가 없으면 **[!UICONTROL Adobe으로 관리]**&#x200B;를 선택하면 Adobe에서 DMARC 레코드를 만들고 호스팅합니다.

1. 정책: `none`, `quarantine` 또는 `reject`을(를) 설정합니다. 부모 도메인에서 성숙한 DMARC 자세를 가지고 있지 않은 경우 `none`부터 시작하십시오.

1. (선택 사항) 추가 DMARC 태그를 구성합니다(하위 도메인 정책은 `sp`, 백분율은 `pct`, 보고서 주소는 `rua` 및 `ruf`).

1. 완전히 위임된 경우 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

   Adobe은 레코드를 자동으로 적용합니다. CNAME을 사용하는 경우 DNS 레코드를 복사하고 DNS 팀이 추가하도록 한 다음 [!DNL Journey Optimizer B2B Edition] Prime에서 확인합니다.

1. DNS 전파에 최대 48시간을 허용한 다음 하위 도메인 페이지의 DMARC 상태 표시기가 녹색/정상인지 확인합니다.

>[!TIP]
>
>`policy=none`(으)로 시작하여 인증 보고서를 모니터링한 다음 보고서에 정상적인 SPF 및 DKIM 정렬이 표시되면 `quarantine`(으)로 진행하고 마지막으로 `reject`(으)로 진행합니다. 모니터링 없이 `reject`(으)로 바로 이동하면 합법적인 메일이 거부될 수 있습니다.

## IP 풀 {#ip-pools}

IP 풀은 이메일을 보내는 데 사용되는 명명된 IP 주소 그룹입니다. IP 풀은 보낸 사람의 신뢰도에 매우 중요합니다. 각 풀은 ISP에 대한 자체 신뢰도가 있으므로 한 풀의 문제(예: 스팸 불만을 트리거하는 마케팅 버스트)는 다른 풀을 오염시키지 않습니다(예: 트랜잭션 확인).

### 풀 유형

| 풀 유형 | 가용성 | 설명 |
| --------- | ------------ | ----------- |
| **공유 IP 풀** | Alpha에서 사용 가능 | Adobe에서 관리하고 많은 고객이 공유하는 IP 주소 풀입니다. 평판은 풀 전체에서 Adobe에 의해 유지됩니다. IP 웜업을 관리하지 않으려는 중저가 이메일 볼륨 및 고객에게 적합합니다. |
| **전용 IP 풀** | 로드맵(GA) | 조직에 독점적으로 할당된 하나 이상의 IP 주소. 명성은 당신이 가지고 있습니다. 대량 발송자에게 권장됩니다. IP 준비 계획 및 PTR 기록 관리를 포함합니다. |

### IP 풀 검토 및 할당 {#review-ip-pool}

이 릴리스에서는 조직에 대해 IP 풀이 사전 프로비저닝됩니다. 이메일 채널 구성을 만들 때 IP 풀을 할당합니다.

1. **[!UICONTROL 관리]** → **[!UICONTROL 채널]** → **[!UICONTROL 전자 메일 설정]** → **[!UICONTROL IP 풀]**&#x200B;로 이동합니다.
1. 조직에서 **[!UICONTROL 활성]** 상태의 IP 풀을 사용할 수 있는지 확인하십시오.
1. 풀 위로 마우스를 가져가 IP 주소 및 해당 PTR 레코드를 확인합니다(역방향 DNS).
1. 조직에 여러 사업부나 브랜드가 있는 경우 채널 구성을 만들기 전에 IP 풀(예: 마케팅 풀과 웨비나 풀)을 사용하는 방법을 계획하십시오.

>[!IMPORTANT]
>
>공유 풀을 사용할 수 있는 경우에도 동일한 IP 풀에서 마케팅 및 트랜잭션 트래픽을 혼합하지 마십시오. 채널 구성(마케팅 및 트랜잭션)의 이메일 유형 설정이 억제 동작을 제어하지만 채널 구성은 가능한 경우 여전히 개별 풀을 사용해야 합니다.

## 이메일 채널 구성 {#email-channel-configurations}

채널 구성은 발신자 ID, 하위 도메인, IP 풀 및 추적 설정을 함께 연결하는 중앙 개체입니다. 여정의 이메일 작업은 메시지를 보내는 방법을 알기 위해 채널 구성을 참조합니다.

* **채널:** 전자 메일.
* **이메일 유형:** 마케팅 또는 트랜잭션. 이 설정은 제외 규칙이 적용되는지 여부를 결정합니다(마케팅은 제외 규칙을 적용하며, 트랜잭션은 합법적인 트랜잭션 메시지에 대해 기본적으로 스팸 위반 제외를 무시합니다.).
* **헤더 매개 변수:** 보낸 사람 이름, 보낸 사람 전자 메일, 받는 사람 이름, 받는 사람 전자 메일, 오류 전자 메일.
* **하위 도메인:** 위임된 하위 도메인이 전송에 사용되었습니다. 발신자 이메일은 이 하위 도메인을 사용해야 합니다.
* **IP 풀:** 메시지를 전달하는 데 사용되는 IP 풀입니다.
* **URL 추적:** 클릭 및 열기 추적을 활성화하거나 비활성화하고 추적 도메인을 구성합니다.
* **태그:** 조직 및 검색용 태그입니다.

### 이메일 채널 구성 만들기 {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* 하나 이상의 하위 도메인을 위임하고 활성화해야 합니다.
>* 조직에 IP 풀을 하나 이상 할당해야 합니다.
>* 관리자 역할이 필요합니다.

1. **[!UICONTROL 채널]** → **[!UICONTROL 일반 설정]** → **[!UICONTROL 채널 구성]**(으)로 이동합니다.
1. **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭합니다.
1. 이름(예: &quot;Contoso B2B Marketing — North America&quot;) 및 선택적 설명을 입력합니다.
1. **[!UICONTROL 전자 메일]** 채널을 선택하십시오.
1. 필요한 경우 구성을 분류할 태그를 선택합니다.
1. **[!UICONTROL 이메일 유형]** 섹션에서 마케팅 또는 트랜잭션 을 선택합니다.
1. **[!UICONTROL 하위 도메인]** 섹션에서 이전에 위임된 하위 도메인을 선택합니다.
1. **[!UICONTROL IP 풀]** 섹션에서 활성 IP 풀을 선택하십시오. IP에 마우스를 가져다 대고 PTR 레코드를 볼 수 있습니다.
1. **[!UICONTROL 헤더 매개 변수 구성]**:
   * 보낸 사람 이름(예: &quot;Contoso Marketing&quot;).
   * 이메일에서 — 선택한 하위 도메인을 사용해야 합니다(예: `marketing@mail.contoso.com`).
   * 회신 주소 이름 및 회신 주소 이메일 — 비어 있는 경우 기본값이 [보낸 사람]으로 설정됩니다.
   * 오류 이메일 — 배달 못 함 알림을 받는 주소입니다.
1. **[!UICONTROL URL 추적]**&#x200B;을 사용하도록 설정하고 추적 도메인을 선택하세요.
1. **[!UICONTROL 제출을 클릭합니다]**.
1. Prime은 유효성 검사: 하위 도메인 상태, MX 레코드, SPF/DKIM/DMARC 정렬, IP 풀 준비, FBL 등록 구성은 초안 → 처리 → 활성 상태로 이동합니다.

>[!NOTE]
>
>유효성 검사가 실패하면 구성이 **[!UICONTROL 실패]** 상태로 이동합니다. 구성을 열어 실패 이유를 확인합니다. 일반적인 원인은 MX 레코드 유효성 검사 실패, 구성과 일치하지 않는 풀의 IP 또는 DMARC 오정렬입니다. 해결하고 다시 제출합니다.

### 채널 구성 편집 또는 삭제 {#edit-channel-configuration}

생성 후 채널 구성을 편집할 수 있지만 한 가지 중요한 제한 사항이 있습니다.

* **채널을 변경할 수 없습니다.** 구성은 해당 채널에 바인딩됩니다.

사용 중인 구성을 편집할 때:

* **게시된 여정의 경우:** 다음 반복 또는 다음 실행 시 변경 내용이 적용됩니다. 진행 중 실행은 이전 설정으로 계속됩니다.
* **트랜잭션 또는 실시간 메시지의 경우:**&#x200B;개의 변경 내용이 약 5분 내에 전파됩니다.

구성을 삭제하려면 먼저 해당 구성을 참조하는 모든 이메일 작업을 제거하거나 업데이트합니다. [!DNL Journey Optimizer B2B Edition] Prime은 현재 활성 여정에서 사용하는 구성을 삭제하지 않습니다.

### 여러 채널 구성 {#multiple-channel-configurations}

대부분의 B2B 조직은 여러 채널 구성을 사용하여 브랜드, 지역 또는 전송 유형을 구분합니다. 일반적인 패턴:

* 비즈니스 단위당 별도의 마케팅 구성(예: *BU-A 마케팅*, *BU-B 마케팅*).
* 이메일 유형의 전용 트랜잭션 구성 = 제품 또는 계약 알림에 대한 트랜잭션.
* 지역별 하위 도메인(예: `mail.eu.contoso.com`, `mail.us.contoso.com`)을 사용하여 지역별 ISP 및 규정 준수에 맞게 지역별로 구성합니다.

>[!TIP]
>
>명확하고 구조화된 규칙으로 구성의 이름을 지정합니다(예: *[브랜드] - [지역] - [유형]*). 12개 이상의 구성이 있는 경우 이 문제가 심각해집니다.

### 알려진 제한 사항 {#known-limitations}

* 하위 도메인 위임에 대한 **사용자 지정 위임 방법**&#x200B;을 아직 사용할 수 없습니다. 완전히 위임되었거나 CNAME을 사용하십시오. 사용자 지정 위임은 GA를 타깃팅합니다.
* Alpha에서 **전용 IP 풀**&#x200B;을(를) 사용할 수 없습니다. 공유 IP 풀만 선택할 수 있습니다. 전용 IP는 IP 웜업 계획 및 PTR 기록 관리를 포함하여 GA 시점에 제공됩니다.
* **.html 또는 .zip 업로드를 통한 HTML 가져오기**&#x200B;는 Alpha에서 제한됩니다. 코드 편집기 + 시각적 캔버스 이중 보기, 유효성 검사 및 인라인 CSS 자동 전환을 포함한 전체 HTML 가져오기는 Beta에서 제공됩니다.
* **Prime의 기본 이미지 업로드 및 DAM**(업로드, 구성, 편집)은 Beta 로드맵에 있습니다. 이 릴리스에서는 Marketo Design Studio 자산을 사용합니다. Marketo에서의 재업로드는 Prime에 반영되지 않습니다.
* 이 릴리스에서는 **테스트 프로필, 콘텐츠 시뮬레이션 및 증명 보내기**&#x200B;를 사용할 수 없습니다. Litmus 렌더링 및 SpamAssassin 기반 스팸 보고서는 Beta 로드맵에 있습니다.
* 이 릴리스에서는 **계정 수준 개인화 및 사용자 지정 개체 데이터**&#x200B;를 사용할 수 없습니다. 프로필 속성을 사용합니다.
* 기존 Marketo 템플릿의 **Velocity-to-Handlebars 자동 마이그레이션**&#x200B;이(가) GA에 제공됩니다.
* **이메일에 대한 댓글 및 공동 작업**(인라인 댓글, @mentions, 리뷰 요청 워크플로)은 빠른 후속 릴리스에서 제공됩니다.
* **AEM Assets, AEM 콘텐츠 조각 및 Adobe Express** 통합이 빠른 후속 로드맵에 있습니다.

<!--

### Frequently asked questions {#faq}

| Question | Answer |
| -------- | ------ |
| **Can I reuse the subdomain I already use in Marketo Engage?** | No. A subdomain can only be associated with one Adobe product at a time. Create a new subdomain (for example, mail2.contoso.com) for Prime. |
| **Why does my channel configuration show Failed?** | The most common reasons are: MX record validation failed (your subdomain DNS isn't fully configured); DMARC misalignment; or an IP pool that is in Processing and has never been associated with the selected subdomain. Open the configuration to see the specific reason. |
| **What happens if a personalization token has no value at send time?** | If you defined a fallback with the Handlebars `default` helper, the fallback is used. If not, the token resolves to an empty string. Prime warns you when a token has no fallback and the underlying attribute is not guaranteed by the audience definition. |
| **Can I personalize using account-level attributes?** | Not in this release. Personalization in Prime today supports profile attributes only. |
| **What's the maximum email size?** | 100 KB is the recommended best-practice cap for inbox rendering. Prime warns you in the editor if you exceed it. |
| **Can I migrate existing Marketo email templates into Prime?** | A guided self-serve migration tool — including Velocity-to-Handlebars conversion — is delivered at GA. In this release, you can manually rebuild templates or paste raw HTML. |
| **Will my updates to Marketo assets show up in Prime?** | No. Asset availability in Prime is based on a one-time copy from Marketo Design Studio. Re-uploaded or modified Marketo assets are not reflected in Prime today. Native asset upload and management within Prime is on the Beta roadmap. |

## Glossary {#glossary}

| Term | Definition |
| ---- | ---------- |
| **DKIM** | DomainKeys Identified Mail — cryptographic email signature. |
| **DMARC** | Domain-based Message Authentication, Reporting & Conformance. |
| **FBL** | Feedback Loop — a service ISPs offer to receive spam-complaint reports back to senders. |
| **Handlebars** | JavaScript templating language used in Prime for personalization expressions. |
| **IP pool** | Group of IP addresses used to send email. |
| **MX record** | Mail Exchange DNS record — directs incoming mail to the correct mail servers. |
| **NS record** | Name Server DNS record — used to delegate a subdomain. |
| **PTR record** | Pointer record — reverse DNS that maps an IP address back to a hostname. |
| **RBAC** | Role-Based Access Control. |
| **SPF** | Sender Policy Framework — DNS record listing authorized sending IPs. |
| **Subdomain delegation** | Granting Adobe authority over a portion of your domain (a subdomain) for sending email. |

-->
