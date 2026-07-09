---
title: 체크리스트 설정
description: 사용자 액세스 구성 및 이메일 전달성 인프라를 포함하여 Journey Optimizer B2B Prime 인스턴스에 대한 초기 설정 작업을 완료합니다.
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 제한된 베타 릴리스의 일부입니다."
autotag-review: '2026-06-12T23:06:52.179Z'
TQID: 'https://experienceleague.adobe.com/D8qXM-F4anA8IVYmdlaclUoxgTwqQptN36xYFpsuvHY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: d6e625c1-468f-4d73-9f32-fd1edb87f96b
  - id: f467931a-9b22-4ca8-869f-adfbd64061ce
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: f6df9def-cdf7-4728-9ec8-3f65716828c7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 0f264f00c8018324abf1d409ddc381c6dcc9c08a
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 10%

---

# 체크리스트 설정

프로비전된 [!DNL Journey Optimizer B2B Prime] 인스턴스에서 기능을 활성화하려면 다음 작업을 완료하십시오.

## 사용자 액세스 활성화 {#enable-user-access}

프로비저닝이 완료되고 샌드박스가 바인딩되면 팀 및 사용자에 대한 [!DNL Journey Optimizer B2B Edition] 액세스를 구성하십시오.

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
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>Admin Console에서 Journey Optimizer B2B edition 제품 프로필 만들기(1회/초기 설정만 해당)</td>
<td><a href="./user-management.md#create-profile">프로필 만들기</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>Admin Console에서 사용자 그룹 추가</td>
<td><a href="./user-management.md#add-user-group">사용자 그룹 추가</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>Admin Console에서 사용자 그룹에 제품 프로필을 할당합니다</td>
<td><a href="./user-management.md#assign-profile">제품 프로필 할당</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>Admin Console에서 사용자 그룹에 사용자 추가</td>
<td><a href="./user-management.md#add-users">사용자 추가</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>기본 역할 편집 또는 제품 권한으로 사용자 정의 역할 만들기</td>
<td><a href="./user-management.md#edit-role-permissions">역할 편집</a> <br/> <a href="./user-management.md#create-a-custom-role">사용자 지정 역할 만들기</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>Adobe Experience Platform에서 역할에 사용자 또는 그룹 추가</td>
<td><a href="./user-management.md#add-users-to-a-role">사용자 추가</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">그룹 추가</a></td>
</tr>
</tbody>
</table>

## 이메일 전달성 {#email-deliverability}

마케터가 여정에서 이메일을 보내려면 먼저 하위 도메인 위임, 이메일 인증 및 채널 설정을 포함하여 조직에 대한 전송 인프라를 구성합니다.

<table>
<thead>
<tr>
<th colspan="2">작업</th>
<th>세부 정보 및 지침</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>이메일 게재 기능 및 채널 설정 구성</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>하위 도메인을 Adobe(완전히 위임됨 또는 CNAME)에 위임</td>
<td><a href="./email-deliverability.md#delegate-fully-delegated">완전히 위임됨</a> <br/> <a href="./email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>하위 도메인용 DMARC 구성</td>
<td><a href="./email-deliverability.md#configure-dmarc">DMARC 구성</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>IP 풀 검토 및 할당</td>
<td><a href="./email-deliverability.md#review-ip-pool">IP 풀 검토</a></td>
</tr>
<tr>
<td><img src="../../assets/do-not-localize/icon-checkbox.svg" width="25" alt="작업에 대한 확인란"/></td>
<td>이메일 채널 구성 만들기</td>
<td><a href="../admin/email-channel-configuration.md#create-email-channel-configuration">이메일 채널 구성</a></td>
</tr>
</tbody>
