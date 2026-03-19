---
title: 이메일 설정
description: 플레이스홀더
feature: Setup, Channels
role: Admin
source-git-commit: 55ffa7995a8d74d352a52f14bed5dd89d7d1c239
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 0%

---

# 이메일 설정

첨부된 Marketo Egage 인스턴스에서 제공하는 이메일 게재 인프라를 지원하려면 다음 이메일 옵션을 설정합니다. Marketo Engage 제품 관리자는 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을 선택하여 이러한 설정을 구성할 수 있습니다.

## 이메일 설정

첨부된 Marketo Engage 인스턴스에 대한 이메일 기본값을 설정하려면 마케팅 조직의 사용을 반영하도록 구성된 값을 변경하십시오.

### 이메일 및 레이블에서

새 이메일이 이러한 기본값으로 자동으로 채워지도록 보낸 사람 이메일 및 레이블의 값을 변경합니다.

>[!NOTE]
>
>변경 사항은 사용자가 만든 이메일에만 적용할 수 있으며 다른 Marketo Engage 또는 Journey Optimizer B2B edition 사용자에게는 적용되지 않습니다.

1. 첨부된 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL 설정]_ 패널에서 **[!UICONTROL 전자 메일에서]** 및 **[!UICONTROL 레이블에서]**&#x200B;에 대해 원하는 기본값을 입력하십시오.

   ![전자 메일 설정 - 보낸 사람 전자 메일 및 보낸 사람 레이블 기본값](./assets/me-admin-email-settings-from.png){width="500"}

1. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.

### 메시지 구독 취소

비운영 마케팅 이메일의 경우, 구독 취소 텍스트와 링크가 맨 아래에 추가됩니다. 제품 관리자는 마케터가 이메일을 작동 상태로 표시하지 않을 때 채워지는 기본 HTML 및 텍스트를 구성해야 합니다.

1. 첨부된 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL 설정]_ 패널에서 **[!UICONTROL HTML 구독 취소]** 및 **[!UICONTROL 텍스트 구독 취소]**&#x200B;에 대해 원하는 기본값을 입력하십시오.

   >[!TIP]
   >
   >마케터는 시스템 토큰을 사용하여 이메일에서 구독 취소 HTML의 위치를 변경할 수 있습니다.

   ![전자 메일 설정 - HTML 구독 취소 및 텍스트 구독 취소 기본값](./assets/me-admin-email-settings-unsubscribe.png){width="500"}

   >[!CAUTION]
   >
   >다음 변수는 중요합니다. **&#x200B;**&#x200B;개를 삭제하지 마십시오.
   >
   >* `%mkt_opt_out_prefix%`
   >* `mkt_unsubscribe=1&mkt_tok=##MKT_TOK##`

1. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.

기본 시스템 콘텐츠로 되돌리려면 다음을 복사하여 붙여넣습니다.

+++ 시스템 기본 구독 취소 텍스트

```
<p><font face="Verdana" size="1">If you no longer wish to receive these emails, click on the following link: <a href="%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##">Unsubscribe</a><br/></font></p>` [!UICONTROL Unsubscribe Text]:
%mkt_opt_out_prefix%UnsubscribePage.html?mkt_unsubscribe=1&mkt_tok=##MKT_TOK##
```

+++

### 웹 페이지로 보기

이메일 컨텐츠에 표시 기능이 제한되어 있습니다(CSS가 제한되고 JavaScript 또는 양식이 없음). 마케터는 _웹 페이지로 보기_ 옵션을 사용하여 Marketo Munchkin을 사용하여 전자 메일 받는 사람에 대한 쿠키를 적용할 수 있습니다. 제품 관리자는 마케터가 이 옵션을 선택할 때 채워지는 기본 HTML 및 텍스트를 구성해야 합니다.

1. 첨부된 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. HTML _[!UICONTROL 설정]_ 패널에서 사용자의 말투와 메시지를 반영하도록 **[!UICONTROL 웹 페이지로 보기]** 및 **[!UICONTROL 웹 페이지로 보기]** 필드의 내용을 변경합니다.

   ![전자 메일 설정 - 웹 페이지로 보기 HTML 및 웹 페이지로 보기 텍스트 기본값](./assets/me-admin-email-settings-view-as-web-page.png){width="500"}

   >[!CAUTION]
   >
   >다음 변수는 중요합니다. **&#x200B;**&#x200B;개를 삭제하지 마십시오.
   >
   >`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
   >
   >두 번째 부분 `##MKT_TOK##`은(는) 해당 사용자의 Munchkin 쿠키입니다. 이메일 수신자가 링크를 클릭할 때 쿠키가 적절히 적용되도록 합니다.
   >
   >다음을 피하십시오.
   >
   >* HTML 상자 중 하나에 추가 URL 추가
   >* 텍스트 버전에 HTML 넣기

1. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.

기본 시스템 콘텐츠로 되돌리려면 다음을 복사하여 붙여넣습니다.

+++ 시스템 기본 웹 페이지 HTML

```
<div style="text-align: center"><font face="Verdana" size="1">To view this email as a web page, <a href="%mkt_webview_url%?mkt_tok=##MKT_TOK##">click here</a></font></div>
```

+++

+++ 시스템 기본 웹 페이지 텍스트

```
To view this email as a web page, go to the following address:
`%mkt_webview_url%?mkt_tok=##MKT_TOK##`
```

+++

## 사용자 정의 객체 검색 제한

[!DNL Velocity Script]을(를) 사용하여 전자 메일에 사용자 지정 개체 데이터를 표시하는 경우 상위 사용자 지정 개체 검색 제한을 조정하십시오. 기본적으로 제한은 Velocity 스크립트에서 10개의 상위 사용자 지정 개체에 대한 액세스를 허용합니다. 필요한 경우 이 제한을 늘릴 수 있습니다.

[[!DNL Apache Velocity]](https://velocity.apache.org/)은(는) HTML 콘텐츠를 템플릿화하고 스크립팅하도록 설계된 [!DNL Java]에 빌드된 언어입니다. Marketo Engage 이메일 인프라는 사용자 지정 개체에 저장된 데이터에 대한 액세스를 제공하는 스크립팅 토큰을 통해 이메일 컨텍스트에서 사용을 지원합니다.

리드에 직접 연결된 상위 및 하위 사용자 지정 개체 또는 연락처를 참조할 수 있지만 세 번째 수준 사용자 지정 개체는 참조할 수 없습니다. 각 사용자 지정 개체에 대해 개인/연락처당 가장 최근에 업데이트된 레코드 10개는 런타임에 사용할 수 있으며 가장 최근에 업데이트된 레코드(시간: `0`)부터 가장 오래 업데이트된 레코드(시간: `9`)까지 순서가 지정됩니다.

제한 변경(_T):_

1. 첨부된 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL 사용자 지정 개체 검색 제한]_ 패널로 스크롤한 다음 **[!UICONTROL 상위 검색 제한]**&#x200B;에 새 값을 입력하십시오.
필드.

   ![Marketo Engage 전자 메일 관리자 - 사용자 지정 개체 검색 제한 기본값](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   10 - 100 사이의 값이 지원됩니다. _[!UICONTROL 하위 검색 제한]_&#x200B;은(는) 1000을 상위 제한으로 나누어 자동으로 설정됩니다. 예를 들어 상위 제한을 50으로 설정하면 하위 제한이 20(1000 ÷ 50 = 20)으로 계산됩니다.

1. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.

## 사용자 정의 헤더 옵션

전자 메일 추적 링크 헤더를 구성하려면 전자 메일의 _[!UICONTROL 사용자 지정 헤더 옵션]_&#x200B;을 변경하십시오. 이러한 옵션을 활성화하면 엄격한 전송을 사용하여 HTTPS를 사용하는 보안 추적 링크를 구현할 수 있습니다.

1. 첨부된 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL 사용자 지정 헤더 옵션]_ 패널로 스크롤하고 추적 링크 정책에 따라 설정을 변경합니다.

   ![Marketo Engage 전자 메일 관리자 - 사용자 지정 헤더 옵션 기본 설정](./assets/me-admin-email-custom-object-retrieval-limits.png){width="500"}

   * **[!UICONTROL 엄격한 전송 보안]** - 추적 링크가 항상 HTTPS를 통해 제공되도록 하려면 이 옵션을 [사용]으로 설정하십시오(SSL로 보호되는 추적 링크가 있는 구독에만 설정되어야 함).
   * **[!UICONTROL Max-age]** - 이 필드는 브라우저가 HTTPS를 통해서만 도메인에 액세스해야 하는 시간을 초 단위로 지정하는 필수 지시문을 지원합니다.
   * **[!UICONTROL IncludeSubDomains]** - 이 옵션을 사용하여 호스트의 모든 하위 도메인에 HSTS 정책을 적용하는 지시문을 포함합니다.

   >[!IMPORTANT]
   >
   >IT 팀과 함께 이러한 설정을 검토하여 조직의 정책과 일치하는지 확인하십시오. 잘못된 설정으로 인해 일부 방문자가 이메일 링크에 액세스하지 못할 수 있습니다.

1. **[!UICONTROL 변경 내용 저장]**&#x200B;을 클릭합니다.

## 이메일 보트 활동 필터링 {#filter-email-bots}

NHI(비사람 상호 작용)라고도 하는 이메일 봇 활동은 이메일 _열기_ 및 _클릭 수_ 데이터를 부풀려 참여 지표를 왜곡하고 이벤트 기반 여정 진행을 트리거할 수 있습니다. 이메일 보트 필터링을 사용하여 클릭 참여 지표 및 통찰력의 무결성을 유지합니다. 의심되는 보트 활동을 식별하는 방법에는 두 가지가 있습니다.

* _&#x200B;**[!UICONTROL IAB 보트 목록과 일치]**&#x200B;_ - [대화형 Advertising Bureau 보트 목록](https://www.iab.com/guidelines/iab-abc-international-spiders-bots-list/){target="_blank"}(사용자 에이전트/IP 주소)에 있는 모든 항목과 일치하는 활동이 보트로 표시됩니다.
* _&#x200B;**[!UICONTROL 근접 패턴과 일치]**&#x200B;_ - 동시에 발생하는 두 개 이상의 활동(초 미만)이 봇으로 식별됩니다. 비교 시 고려되는 속성은 다음과 같습니다.
   * 잠재 고객 ID(같아야 함)
   * 이메일 자산(동일해야 함)
   * 링크 클릭 또는 이메일 열기

이메일 링크 클릭 및 이메일 열기 활동의 경우 속성은 다음 값으로 채워집니다.

* 봇으로 식별되는 활동 - _봇 활동_ = `true` 및 _봇 활동 패턴_ = 식별된 패턴/메서드
* 봇이 아닌 것으로 식별된 활동 - _봇 활동_ = `false` 및 _봇 활동 패턴_ = `n/a`

### 필터 설정

1. 첨부된 Marketo Engage 인스턴스의 **[!UICONTROL 관리자]** 영역으로 이동하여 **[!UICONTROL 전자 메일]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL 봇 활동]** 탭을 선택합니다.

   ![Marketo Engage 전자 메일 관리자 - 봇 활동 탭](./assets/me-admin-email-bot-activity.png){width="700" zoomable="yes"}

   보트 활동 식별 패널에는 보트 활동을 식별하는 데 사용할 수 있는 두 개의 슬라이더가 표시됩니다.

1. 슬라이더를 전환하여 한 개 또는 두 개 모두를 활성화합니다.

   사용하는 각 메서드에 대해 _[!UICONTROL 보트 활동 기록]_ 또는 _[!UICONTROL 보트 활동 필터링]_&#x200B;을 선택하십시오.

   >[!IMPORTANT]
   >
   >[!UICONTROL 보트 활동 필터링]을 선택하면 잘못된 활동이 제거되므로 이메일 열림 및 클릭 수가 감소할 수 있습니다.

   ![Marketo Engage 전자 메일 관리자 - 봇 활동 식별 옵션](./assets/me-admin-email-bot-activity-set-filters.png){width="500"}

   _[!UICONTROL 근접 패턴과 일치]_&#x200B;의 경우 **[!UICONTROL 활동 간 기간]**&#x200B;의 시간(초)을 설정할 수도 있습니다(기본값은 `0`, 최대값은 `3`).

   >[!NOTE]
   >
   >_Duration Between Activities_&#x200B;이(가) `0`초로 설정된 상태에서 Marketo Engage은(는) 정확히 같은 시간에 발생하는 전자 메일 활동을 식별합니다. 지정된 시간(초) 내에 여러 개의 이메일 활동이 발생하는 경우 봇 활동으로 식별됩니다.

   두 필터링 방법 중 하나를 비활성화하려면 슬라이더를 왼쪽으로 전환합니다. 그렇게 하면 데이터가 재설정되지 않습니다.

### IP 차단 목록

Adobe은 다음 IP에서 받은 참여가 자동으로 필터링되고 Marketo Engage 인스턴스에 추가되지 않으므로 수백만 개의 가짜 참여를 생성하는 IP 주소 목록을 확인했습니다. 이 필터링을 사용하면 이메일 열기, 클릭 수 및 기타 관련 활동이 감소할 수 있습니다. 이 목록은 주기적으로 업데이트될 수 있습니다.

+++ 차단된 IP 주소

* 40.94.34.52
* 40.94.34.86
* 52.34.76.65
* 54.70.53.60
* 54.71.187.124
* 60.28.2.248
* 64.235.150.252
* 64.235.153.10
* 64.235.153.2
* 64.235.154.105
* 64.235.154.109
* 64.235.154.140
* 64.74.215.1
* 64.74.215.100
* 64.74.215.138
* 64.74.215.139
* 64.74.215.142
* 64.74.215.146
* 64.74.215.150
* 64.74.215.154
* 64.74.215.158
* 64.74.215.162
* 64.74.215.164
* 64.74.215.166
* 64.74.215.170
* 64.74.215.174
* 64.74.215.176
* 64.74.215.178
* 64.74.215.51
* 64.74.215.56
* 64.74.215.58
* 64.74.215.59
* 64.74.215.86
* 64.74.215.98
* 65.154.226.101
* 66.249.91.149
* 70.42.131.106
* 74.125.217.116
* 74.217.90.250
* 104.129.41.4
* 104.47.55.126
* 104.47.58.126
* 104.47.70.126
* 104.47.73.126
* 104.47.73.254
* 104.47.74.126
* 128.220.160.1
* 155.70.39.101
* 162.129.251.14
* 162.129.251.42
* 208.52.157.204

>[!NOTE]
>
>모든 IP 주소는 이 목록에 포함되기 전에 신중하게 분석 및 검사되어 가장 중요하고 해로운 IP만 차단됩니다.

+++

