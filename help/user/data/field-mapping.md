---
title: XDM 필드 매핑
description: AEP XDM 스키마, Marketo Engage 및 Journey Optimizer B2B 에디션 간의 필드 매핑을 검토합니다.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 838308621a27bcfc6425b8683f642a66f1fa6a7b
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 16%

---

# XDM 필드 매핑

DTS(데이터 전송 서비스)는 Adobe Experience Platform의 데이터를 Journey Optimizer B2B 에디션으로 동기화합니다. DTS는 Marketo Engage의 Experience Platform XDM 스키마 필드와 이와 동등한 항목 간의 매핑에 의존합니다.

## XDM 비즈니스 사용자 기본 필드 매핑

| [XDM 비즈니스 사용자](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | XDM 표시 이름 | Marketo Engage 표시 이름 | XDM 유형 | Marketo 유형 | XDM 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | 회사 이름 | 회사 이름 | 문자열 | 문자열 | 사업가와 연계된 회사의 이름. |
| `b2b.companyWebsite` | 회사 웹 사이트 | 웹 사이트 | 문자열 | url | 사업가와 연계된 회사의 웹 사이트. |
| `b2b.isMarketingSuspended` | 마케팅 중단 표시기 | 마케팅 중단 | 부울 | 부울 | 값은 사용자에 대한 마케팅이 일시 중단되었는지 여부를 나타냅니다. |
| `b2b.marketingSuspendedCause` | 마케팅 중단 사유 | 마케팅 중단 사유 | 문자열 | 문자열 | 사용자에 대해 마케팅이 일시 중단된 경우 이 속성은 그 이유를 제공합니다. |
| `b2b.personStatus` | 개인 상태 | 잠재 고객 상태 | 문자열 | 문자열 | 개인의 현재 마케팅/판매 상태를 기록하는 필드. |
| `consents.marketing.email.reason` | 옵트아웃 이유 | 구독 취소 이유 | 문자열 | 문자열 | 이메일 옵트아웃과 연계된 사유. |
| `consents.marketing.email.val` | 주소 삭제 | 주소 삭제 | 문자열 | 부울 | 구독 취소가 true(예: 값 = 1)이면 `consents.marketing.email.val`을(를) (n)으로 설정합니다. 구독 취소가 false인 경우(예: 값 = 0) consents.marketing.email.val을 null로 설정합니다. |
| `extendedWorkDetails.jobTitle` | 직위 | 직위 | 문자열 | 문자열 | 개인의 직책. |
| `faxPhone.number` | 숫자 | 팩스 번호 | 문자열 | 전화 | 팩스 번호. |
| `mobilePhone.number` | 숫자 | 휴대폰 번호 | 문자열 | 전화 | 사용자와 연계된 휴대폰 번호. |
| `person.birthDate` | 생년월일(YYY-MM-DD) | 생년월일 | 문자열 | 날짜 | 개인이 태어난 전체 날짜. YYYY-MM-DD |
| `person.name.courtesyTitle` | 경칭 | 인사말 | 문자열 | 문자열 | 일반적으로 한 사람의 직함, 경칭 또는 경어의 약어입니다. courtesyTitle은 텍스트를 여는 데 전체 이름 또는 성 앞에 사용됩니다. 예를 들어 Mr., Ms. 또는 Dr. |
| `person.name.firstName` | 이름 | 이름 | 문자열 | 문자열 | 가장 일반적으로 수락되는 작성된 순서로 된 이름의 첫 번째 세그먼트입니다. 많은 문화권에서 선호하는 개인 또는 이름. firstName 및 lastName 속성은 의미 체계와 국제적 규격에서 벗어나 간편한 방식으로 이름을 모델링하는 기존 시스템과의 호환성을 유지하기 위해 도입되었습니다. 항상 `xdm:fullName`을(를) 사용하는 것이 좋습니다. |
| `person.name.lastName` | 성 | 성 | 문자열 | 문자열 | 가장 일반적으로 수락되는 작성된 순서로 된 이름의 마지막 세그먼트입니다. 많은 문화권에서 그것은 상속된 성씨, 성씨, 성씨, 또는 남성어이다. firstName 및 lastName 속성은 의미 체계와 국제적 규격에서 벗어나 간편한 방식으로 이름을 모델링하는 기존 시스템과의 호환성을 유지하기 위해 도입되었습니다. 항상 `xdm:fullName`을(를) 사용하는 것이 좋습니다. |
| `person.name.middleName` | 중간 이름 | 중간 이름 | 문자열 | 전화 | 이름과 성 사이에 제공되는 중간, 대체 또는 추가 이름. |
| `workAddress.city ` | 구/군/시 | 구/군/시 | 문자열 | 문자열 | 도시 이름. |
| `workAddress.country` | 국가 | 국가 | 문자열 | 문자열 | 정부가 관리하는 지역의 이름입니다. `xdm:countryCode`이(가) 아닌 모든 언어의 국가 이름을 사용할 수 있는 자유 형식의 필드입니다. |
| `workAddress.postalCode` | 우편번호 | 우편번호 | 문자열 | 문자열 | 위치의 우편 번호입니다. 우편 번호는 모든 국가에서 사용할 수 없습니다. 일부 국가에서는 우편번호의 일부만 포함되어 있습니다. |
| `workAddress.state` | 주/도 | 주/도 | 문자열 | 문자열 | 주소의 상태 이름입니다. 자유 형식의 필드입니다. |
| `workAddress.street1` | 도로 1 | 주소 | 문자열 | 텍스트 | 기본 도로 정보, 아파트 번호, 도로 번호 및 도로명. |
| `workEmail.address` | 주소 | 이메일 주소 | 문자열 | 이메일 | 기술 주소(예: RFC2822 및 후속 표준에 일반적으로 정의된 `<name@domain.com>`). |
| `workEmail.status` | 상태 | 이메일 일시 중단됨 | 문자열 | 부울 | 이메일 주소 사용 기능에 대한 표시. |
| `workPhone.number` | 숫자 | 전화번호 | 문자열 | 전화 | 회사 전화번호. |

## XDM 비즈니스 계정 기본 필드 매핑

| [XDM 비즈니스 계정](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | XDM 표시 이름 | Marketo Engage 표시 이름 | XDM 유형 | Marketo Engage 유형 | XDM 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | 구/군/시 | 구/군/시 | 문자열 | 문자열 | 청구 주소에 사용되는 도시 이름. |
| `accountBillingAddress.country` | 국가 | 국가 | 문자열 | 문자열 | 청구 주소에 사용되는 정부 관리 영역의 이름. `xdm:countryCode`이(가) 아닌 모든 언어의 국가 이름을 사용할 수 있는 자유 형식의 필드입니다. |
| `accountBillingAddress.postalCode` | 우편번호 | 주소 우편 번호 | 문자열 | 문자열 | 청구 주소 위치의 우편 번호입니다. 우편 번호는 모든 국가에서 사용할 수 없습니다. 일부 국가에서는 우편번호의 일부만 포함되어 있습니다. |
| `accountBillingAddress.region` | 지역 | 주소 영역 | 문자열 | 문자열 | 청구지 주소의 지역, 국가 또는 지역 부분입니다. |
| `accountBillingAddress.state` | 주/도 | 주/도 | 문자열 | 문자열 | 청구 주소의 주 이름입니다. 자유 형식의 필드입니다. |
| `accountBillingAddress.street1` | 도로 1 | 도로 1 | 문자열 | 문자열 | 일반적으로 아파트 번호, 거리 번호 및 거리 이름을 포함하는 청구 주소의 기본 거리 수준 정보입니다. |
| `accountName` | 이름 | 이름 | 문자열 | 문자열 | 회사 이름. 이 필드에는 최대 255자가 허용됩니다. |
| `accountOrganization.annualRevenue.amount` | 연간 수익 | 연간 수익 | 번호 | 통화 | 조직의 예상 연간 매출액. |
| `accountOrganization.industry` | 산업 | 산업 | 문자열 | 문자열 | 그 산업은 조직에 기인했다. 자유 형식의 필드이므로 쿼리에 대해 구조화된 값을 사용하거나 `xdm:classifier` 속성을 사용하는 것이 좋습니다. |
| `accountOrganization.logoUrl` | 로고 Url | 로고 Url | 문자열 | 문자열 | 계정과 연결된 소셜 네트워크 프로필 이미지를 요청하는 URL을 생성하기 위해 Salesforce 인스턴스의 URL과 결합할 경로(예: `https://yourInstance.salesforce.com/`). 생성된 URL은 계정에 대한 소셜 네트워크 프로필 이미지에 대한 HTTP 리디렉션(코드 302)을 반환합니다. |
| `accountOrganization.numberOfEmployees` | 직원 수 | 직원 수 | 정수 | 정수 | 조직의 직원 수. |
| `accountOrganization.SICCode` | SIC 코드 | SIC 코드 | 문자열 | 문자열 | 표준산업분류(SIC) 코드는 기업이 속한 업종을 기업 활동에 따라 분류하는 4자리 코드입니다. |
| `accountOrganization.website` | 웹 사이트 URL | 도메인 이름 | 문자열 | 문자열 | 조직 웹 사이트의 URL. |
| `accountPhone.number` | N/A | 계정 전화번호 | 문자열 | 문자열 | 계정과 연계된 전화번호. |
| `accountSourceType` | N/A | 소스 유형 | 문자열 | 문자열 | Source 계정 유형입니다. |
