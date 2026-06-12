---
title: 체크리스트 설정
description: Journey Optimizer B2B edition을 설정합니다. XDM 스키마, 이메일/SMS 채널, Marketo Engage 여정 작업 및 사용자를 구성합니다.
feature: Setup, Administration
role: Admin, Developer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: c8f3fb27-3167-48ac-a66a-fa4bc3f58dda
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-03-27T22:15:07.682Z'
source-git-commit: 55446fa98f494b367f9f84abccebc70f59381f26
workflow-type: tm+mt
source-wordcount: 848
ht-degree: 74%

---

# 체크리스트 설정

Adobe Journey Optimizer B2B edition은 Adobe Experience Platform을 기반으로 합니다. 이 구현에서 Journey Optimizer B2B edition과 Marketo Engage은 동일한 시스템이나 동일한 데이터 저장소에 있지 않습니다. Journey Optimizer B2B edition은 Experience Platform에서 데이터를 수신합니다. 하지만 시스템을 프로비저닝하고 구성하기 위해 Marketo Engage 권한과 이메일 게재와 같은 일부 백엔드 기능에 계속 의존합니다.

<!-- 
>>[!NOTE]
>
>Earlier documentation referred to this deployment as the *simplified architecture*. That model is now the Journey Optimizer B2B Edition Ultimate implementation. 
-->

이 구현은 Journey Optimizer B2B edition에서 기능을 활성화하는 기반입니다.

* **데이터 통합 및 크기 조정:** 시스템에서 사용자 지정 개체, 구매 그룹 및 계정 이벤트를 포함한 복잡한 데이터 모델을 지원합니다.

* **여러 Adobe Marketo Engage 인스턴스 연결:** 여러 Marketo Engage 환경에서 데이터를 관리하고 통합합니다.

* **데이터 보호:** 고객 정보를 보호하는 고급 개인 정보 보호 및 보안 기능. (_준비 중_)

* **확장성을 위한 디자인:** 이 설정은 지속적인 개선 및 혁신을 지원합니다.

구성을 위해 다음 지침을 따르십시오.

이 체크리스트를 사용하여 Journey Optimizer B2B edition 설정을 완료합니다.

## &#x200B;1. B2B 네임스페이스 및 스키마 생성

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>환경 설정:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>GitHub에서 네임스페이스 및 스키마 자동 생성 유틸리티를 다운로드합니다.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Experience Platform API 자격 증명 및 필수 헤더를 수집합니다.</td>
<td><a href="https://experienceleague.adobe.com/ko/docs/experience-platform/landing/platform-apis/api-guide">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Postman 환경에 환경 값을 적용합니다.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2"><strong>스크립트를 실행합니다.</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Postman에서 <em>네임스페이스 및 스키마</em> 생성 유틸리티를 실행하고 네임스페이스와 스키마가 만들어졌는지 확인하십시오.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. XDM 필드 및 이벤트 구성

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>표준 XDM 구성</strong>: XDM 개인 프로필 및 XDM 비즈니스 계정 스키마를 설정합니다.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>여정, 구매 그룹 및 이메일 개인화에 대해 노출할 관리 필드를 선택합니다.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>스키마의 업데이트 가능한 필드를 편집합니다.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2"><strong>관계형 스키마</strong>: 관계형 XDM 필드(계정 다대일 사용자 지정 개체)를 선택하십시오.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>스키마에 필요한 구성 값이 있는지 확인합니다.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2"><strong>이벤트</strong>: Experience Platform 이벤트 유형 및 필드를 구성합니다.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>여정 결정/분할 경로에서 지원할 필드로 각 Experience Platform 이벤트 유형을 구성합니다.</td>
<td><a href="./admin/configure-aep-events.md">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. 추적 및 이메일 전달성 구성

[!DNL Journey Optimizer B2B Edition]에서 전자 메일을 보내려면 첨부된 [!DNL Marketo Engage] 프로덕션 인스턴스와 [!DNL Journey Optimizer B2B Edition] 앱에서 전자 메일 추적 및 게재 기능을 구성하십시오.

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">첨부된 Marketo Engage 인스턴스의 <strong>초기 설정</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>DNS 레코드의 링크 추적을 위해 새 CNAME 구성</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>첨부된 Marketo Engage 인스턴스에 대한 브랜딩 도메인 구성</td>
<td><a href="./start/branding-domains.md">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>연결된 Marketo Engage 인스턴스에 DKIM 및 SPF 구성</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>DMARC 설정</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>도메인에 대한 MX 레코드 설정</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>허용 목록에 아웃바운드 IP 주소 추가</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2">첨부된 Marketo Engage 인스턴스의 <strong>전자 메일 설정</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td><em>전자 메일에서</em> 및 <em>레이블에서</em> 구성(선택 사항)</td>
<td><a href="./start/email-setup.md#from-email-and-label">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td><em>HTML 구독 취소</em> 및 <em>텍스트 구독 취소</em> 구성</td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td><em>웹 페이지로 보기 HTML</em> 및 <em>웹 페이지로 보기</em> 구성</td>
<td><a href="./start/email-setup.md#view-as-web-page">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td><em>사용자 지정 개체 검색 제한 구성</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td><em>사용자 지정 헤더 옵션 구성</em></td>
<td><a href="./start/email-setup.md#custom-header-options">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td><em>보트 활동 구성</em> 필터링</td>
<td><a href="./start/email-setup.md#filter-email-bots">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2">Journey Optimizer B2B edition용 <strong>전자 메일 채널 구성</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Journey Optimizer B2B edition에서 <em>통신 제한</em> 구성</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

<!--
 TBD for later

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. 추가 콘텐츠 채널 구성

여정에 다른 채널을 포함하는 마케팅 팀을 지원하려면 추가 채널을 구성하십시오.

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">Journey Optimizer B2B edition에 대한 <strong>SMS</strong> 채널 구성</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>지원할 각 SMS 계정을 구성합니다.</td>
<td><a href="./admin/configure-channels-sms.md">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2">Journey Optimizer B2B edition에 대한 <strong>랜딩 페이지</strong>(Beta) 채널 구성.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>랜딩 페이지 설정을 완료하여 이 페이지를 작성하고 게시하는 마케터를 지원합니다</td>
<td><a href="./admin/configure-channels-landing-pages.md">자세히 알아보기</a></td>
</tr>
<tr>
<td colspan="2">Journey Optimizer B2B edition에 대한 <strong>웹</strong>(Beta) 채널 구성</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Adobe Experience Platform Web SDK을 지원하도록 비즈니스 웹 사이트를 구성합니다.</td>
<td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>콘텐츠가 전달되는 URL별로 웹 속성을 추가합니다.</td>
<td><a href="./admin/configure-channels-web.md">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>웹 경험 작성자가 Adobe Experience Cloud Visual Editing Helper 브라우저 확장 기능을 설치하도록 지시합니다.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Marketo Engage 인스턴스를 연결하여 여정 작업 지원(선택 사항)

Marketo Engage의 캠페인 및 프로그램을 통해 Journey Optimizer B2B edition 기능을 보완하려는 경우 Marketo Engage 작업에 대한 지원을 설정하십시오. 이러한 작업을 통해 마케팅 팀은 Journey Optimizer B2B edition의 _계정 기반_ 마케팅 및 Marketo Engage의 _리드 기반_ 마케팅 활동을 조정할 수 있습니다.

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">여정 작업을 지원하기 위한 <strong>각 Marketo Engage 인스턴스의 경우</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Marketo Engage 사용자 정의 서비스 만들기</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Journey Optimizer B2B edition에서 통합 추가</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. 사용자 액세스 활성화

프로비저닝이 완료되고 샌드박스가 바인딩되며 초기 설정 작업이 완료되면 팀과 사용자에 대한 Journey Optimizer B2B edition 및 Marketo Engage 액세스를 구성합니다.

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">사용자를 위한 <strong>제품 액세스 및 권한 제공</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Adobe Admin Console에서 Marketo Engage 제품 프로필 만들기(새 Marketo Engage 인스턴스만 해당)</td>
<td><a href="./admin/user-management.md#marketo-engage-profile">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>프로필에 대한 사용자 그룹 추가</td>
<td><a href="./admin/user-management.md#add-user-group">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>B2B 사용자 역할 구성</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>역할에 사용자 또는 그룹 추가</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">자세히 알아보기</a></td>
</tr>
</tbody>
</table>
