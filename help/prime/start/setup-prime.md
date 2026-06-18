---
title: 설정
description: 사용자 액세스 구성 및 이메일 전달성 인프라를 포함하여 Journey Optimizer B2B Prime 인스턴스에 대한 초기 설정 작업을 완료합니다.
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
source-git-commit: e849c9406dc83c6dc7c22ff56de32d6a73fed07d
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 55%

---

# 설정

프로비저닝된 여정 B2B Prime 인스턴스에서 기능을 활성화하려면 다음 작업을 완료하십시오.

## 사용자 액세스 활성화

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
<td><a href="./user-management.md#create-profile">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>프로필에 대한 사용자 그룹 추가</td>
<td><a href="./user-management.md#add-user-group">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>B2B 사용자 역할 구성</td>
<td><a href="./user-management.md#edit-roles-for-product-permissions">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>역할에 사용자 또는 그룹 추가</td>
<td><a href="./user-management.md#add-users-to-a-role">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

## 이메일 전달성

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
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>Adobe에 하위 도메인 위임</td>
<td><a href="./admin/configuration-email-deliverability.md#delegate-fully-delegated">완전히 위임됨</a> 또는 <a href="./admin/configuration-email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>하위 도메인용 DMARC 구성</td>
<td><a href="./admin/configuration-email-deliverability.md#configure-dmarc">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>IP 풀 검토 및 할당</td>
<td><a href="./admin/configuration-email-deliverability.md#review-ip-pool">자세히 알아보기</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="확인란"/></td>
<td>이메일 채널 구성 만들기</td>
<td><a href="./admin/configuration-email-deliverability.md#create-email-channel-configuration">자세히 알아보기</a></td>
</tr>
</tbody>
</table>

