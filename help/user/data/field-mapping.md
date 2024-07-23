---
title: XDM 필드 매핑
description: AEP XDM 스키마, Marketo Engage 및 Journey Optimizer B2B 에디션 간의 필드 매핑을 검토합니다.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 17%

---

# XDM 필드 매핑

의 DTS(데이터 전송 서비스)는 Adobe Experience Platform의 데이터를 Journey Optimizer B2B 에디션으로 동기화합니다. DTS는 Marketo Engage의 Experience Platform XDM 스키마 필드와 이와 동등한 항목 간의 매핑에 의존합니다.

## XDM 비즈니스 사용자 기본 필드 매핑

| XDM 비즈니스 사용자 | Marketo Engage 사용자 표시 이름 | AJO B2B 개인 표시 이름 | XDM 유형 | Marketo 유형 | XDM 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | 주소 | ? | 문자열 | 텍스트 | 기본 도로 정보, 아파트 번호, 도로 번호 및 도로명. |
| `workAddress.city ` | 도시 | 도시 | 문자열 | 문자열 | 도시 이름. |
| `b2b.companyName` | 회사 이름 | ? | 문자열 | 문자열 | 사업가와 연계된 회사의 이름. |
| `workAddress.country` | 국가 | 국가 | 문자열 | 문자열 | 정부가 관리하는 지역의 이름입니다. `xdm:countryCode`이(가) 아닌 모든 언어의 국가 이름을 사용할 수 있는 자유 형식의 필드입니다. |
| `person.birthDate` | 생일 | 생년월일 | 문자열 | 날짜 | 개인의 출생월일.  YYYY-MM-DD |
| `workEmail.address` | 이메일 주소 | 이메일 주소 | 문자열 | 이메일 | 기술 주소(예: RFC2822 및 후속 표준에 일반적으로 정의된 &#39;<name@domain.com>&#39;). |
| `workEmail.status` | 이메일 일시 중단됨 | 이메일 일시 중단됨 | 문자열 | 부울 | 이메일 주소 사용 기능에 대한 표시. |
| `faxPhone.number` | 팩스 번호 | ? | 문자열 | 전화 | 팩스 번호. |
| `person.name.firstName` | 이름 | 이름 | 문자열 | 문자열 | 가장 일반적으로 수락된 언어로 작성된 이름의 첫 번째 세그먼트. 많은 문화권에서 이것은 선호하는 개인 또는 이름이다. firstName 및 lastName 속성은 의미 체계와 국제적 규격에서 벗어나 간편한 방식으로 이름을 모델링하는 기존 시스템과의 호환성을 유지하기 위해 도입되었습니다. 항상 xdm:fullName을 사용하는 것이 좋습니다. |
| `extendedWorkDetails.jobTitle` | 직위 | 직위 | 문자열 | 문자열 | 개인의 직책. |
| `person.name.lastName` | 성 | 성 | 문자열 | 문자열 | 가장 일반적으로 수락된 언어로 작성된 이름의 마지막 세그먼트. 많은 문화에서 이것은 유전된 성씨, 성씨, 성씨, 또는 성씨. firstName 및 lastName 속성은 의미 체계와 국제적 규격에서 벗어나 간편한 방식으로 이름을 모델링하는 기존 시스템과의 호환성을 유지하기 위해 도입되었습니다. 항상 xdm:fullName을 사용하는 것이 좋습니다. |
| `b2b.personStatus` | 잠재 고객 상태 | ? | 문자열 | 문자열 | 개인의 현재 마케팅/판매 상태를 기록하는 필드. |
| `b2b.isMarketingSuspended` | 마케팅 중단 | ? | 부울 | 부울 | 사용자에 대한 마케팅이 일시 중단되었는지 여부를 나타냅니다. |
| `b2b.marketingSuspendedCause` | 마케팅 중단 사유 | ? | 문자열 | 문자열 | 사용자에 대해 마케팅이 일시 중단된 경우 이 속성은 그 이유를 제공합니다. |
| `person.name.middleName` | 중간 이름 | ? | 문자열 | 전화 | 이름과 성 사이에 제공되는 중간, 대체 또는 추가 이름. |
| `mobilePhone.number` | 휴대폰 번호 | 휴대폰 번호 | 문자열 | 전화 | 휴대폰 번호. |
| `workPhone.number` | 전화번호 | 전화번호 | 문자열 | 전화 | 회사 전화번호. |
| `workAddress.postalCode` | 우편 번호 | 우편 번호 | 문자열 | 문자열 | 위치의 우편 번호입니다. 우편 번호는 모든 국가에서 사용할 수 없습니다. 일부 국가에서는 우편 번호의 일부만 포함됩니다. |
| `person.name.courtesyTitle` | 인사말 | ? | 문자열 | 문자열 | 일반적으로 사용자 제목, 경칭 또는 경어의 약어입니다. courtesyTitle은 텍스트를 여는 데 전체 이름 또는 성 앞에 사용됩니다. 예를 들어, Mr., Miss 또는 Dr. |
| `workAddress.state` | 주 | 주 | 문자열 | 문자열 | 주 이름입니다. 자유 형식의 필드입니다. |
| `consents.marketing.email.val` | 주소 삭제 | 주소 삭제 | 문자열 | 부울 | 구독 취소가 true(예: 값 = 1)이면 `consents.marketing.email.val`을(를) (n)으로 설정합니다. 구독 취소가 false인 경우(예: 값 = 0) consents.marketing.email.val을 null로 설정합니다. |
| `consents.marketing.email.reason` | 구독 취소 이유 | 구독 취소 이유 | 문자열 | 문자열 |  |
| `b2b.companyWebsite` | 웹 사이트 | ? | 문자열 | url | 사업가와 연계된 회사의 웹 사이트. |

