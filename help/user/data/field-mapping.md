---
title: XDM 필드
description: Adobe Experience Platform 및 Journey Optimizer B2B edition 간에 동기화된 기본 속성 필드를 검토합니다.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 12%

---

# XDM 필드

계정 대상자 데이터는 XDM 비즈니스 계정 및 XDM 비즈니스 사용자 클래스 모두에 속성으로 저장됩니다. 데이터는 Adobe Experience Platform 및 Journey Optimizer B2B edition 간에 정기적으로 동기화됩니다. 다음 섹션에는 기본 속성 세트가 나열됩니다.

>[!TIP]
>
>[Experience Platform XDM 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}에 설명된 대로 XDM 비즈니스 계정 사용자 관계 클래스를 사용하여 다대다 관계에서 XDM 비즈니스 사용자 및 XDM 비즈니스 계정 클래스를 모델링할 수 있습니다.

## XDM 비즈니스 계정 사용자 관계 속성

| [속성](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | 표시 이름 | Journey Optimizer B2B 표시 이름 | 데이터 유형 | 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | 개인 역할 | 역할 | 문자열 배열 | 계정의 사용자와 연결된 역할의 배열(예: `owner, accountant, designer`). |

## XDM 비즈니스 사용자 속성

>[!IMPORTANT]
>
>`workEmail.Address` 특성이 필요합니다. 계정 대상자 구성원의 경우 비어 있는 경우 해당 사람은 수집되지 않으며 대상자를 참조하는 계정 여정 및 구매 그룹에서 생략됩니다.

| [속성](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | 표시 이름 | Journey Optimizer B2B 표시 이름 | 데이터 유형 | 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | 마케팅 중단 표시기 | 마케팅 중단 | 부울 | 값은 사용자에 대한 마케팅이 일시 중단되었는지 여부를 나타냅니다. |
| `b2b.marketingSuspendedCause` | 마케팅 중단 사유 | 마케팅 중단 사유 | 문자열 | 사용자에 대해 마케팅이 일시 중단된 경우 이 속성은 그 이유를 제공합니다. |
| `b2b.personStatus` | 개인 상태 | 잠재 고객 상태 | 문자열 | 개인의 현재 마케팅/판매 상태를 기록하는 필드. |
| `consents.marketing.email.reason` | 옵트아웃 이유 | 구독 취소 이유 | 문자열 | 이메일 옵트아웃과 연계된 사유. |
| `consents.marketing.email.val` | 주소 삭제 | 주소 삭제 | 문자열 | 구독 취소가 true(예: 값 = 1)이면 `consents.marketing.email.val`을(를) (n)으로 설정합니다. 구독 취소가 false인 경우(예: 값 = 0) `consents.marketing.email.val`을(를) null로 설정하십시오. |
| `extendedWorkDetails.jobTitle` | 직위 | 직위 | 문자열 | 개인의 직책. |
| `faxPhone.number` | 숫자 | 팩스 번호 | 문자열 | 팩스 번호. |
| `mobilePhone.number` | 숫자 | 휴대폰 번호 | 문자열 | 사용자와 연계된 휴대폰 번호. |
| `person.birthDate` | 생년월일(YYY-MM-DD) | 생년월일 | 문자열 | 개인이 태어난 전체 날짜. YYYY-MM-DD |
| `person.name.courtesyTitle` | 경칭 | 인사말 | 문자열 | 일반적으로 한 사람의 직함, 경칭 또는 경어의 약어입니다. courtesyTitle은 텍스트를 여는 데 전체 이름 또는 성 앞에 사용됩니다. 예를 들어 Mr., Ms. 또는 Dr. |
| `person.name.firstName` | 이름 | 이름 | 문자열 | 가장 일반적으로 수락되는 작성된 순서로 된 이름의 첫 번째 세그먼트입니다. 많은 문화권에서 선호하는 개인 또는 이름. firstName 및 lastName 속성은 의미 체계와 국제적 규격에서 벗어나 간편한 방식으로 이름을 모델링하는 기존 시스템과의 호환성을 유지하기 위해 도입되었습니다. 항상 `xdm:fullName`을(를) 사용하는 것이 좋습니다. |
| `person.name.lastName` | 성 | 성 | 문자열 | 가장 일반적으로 수락되는 작성된 순서로 된 이름의 마지막 세그먼트입니다. 많은 문화권에서 그것은 상속된 성씨, 성씨, 성씨, 또는 남성어이다. firstName 및 lastName 속성은 의미 체계와 국제적 규격에서 벗어나 간편한 방식으로 이름을 모델링하는 기존 시스템과의 호환성을 유지하기 위해 도입되었습니다. 항상 `xdm:fullName`을(를) 사용하는 것이 좋습니다. |
| `person.name.middleName` | 중간 이름 | 중간 이름 | 문자열 | 이름과 성 사이에 제공되는 중간, 대체 또는 추가 이름. |
| `workAddress.city ` | 구/군/시 | 구/군/시 | 문자열 | 도시 이름. |
| `workAddress.country` | 국가 | 국가 | 문자열 | 정부가 관리하는 지역의 이름입니다. `xdm:countryCode`이(가) 아닌 모든 언어의 국가 이름을 사용할 수 있는 자유 형식의 필드입니다. |
| `workAddress.postalCode` | 우편번호 | 우편번호 | 문자열 | 위치의 우편 번호입니다. 우편 번호는 모든 국가에서 사용할 수 없습니다. 일부 국가에서는 우편번호의 일부만 포함되어 있습니다. |
| `workAddress.state` | 주/도 | 주/도 | 문자열 | 주소의 상태 이름입니다. 자유 형식의 필드입니다. |
| `workAddress.street1` | 도로 1 | 주소 | 문자열 | 기본 도로 정보, 아파트 번호, 도로 번호 및 도로명. |
| `workEmail.address` | 주소 | 이메일 주소 | 문자열 | **필수 필드** <br/>기술 주소(예: RFC2822 및 후속 표준에서 일반적으로 정의된 `<name@domain.com>`). |
| `workEmail.status` | 상태 | 이메일 일시 중단됨 | 문자열 | 이메일 주소 사용 기능에 대한 표시. |
| `workPhone.number` | 숫자 | 전화번호 | 문자열 | 회사 전화번호. |

## XDM 비즈니스 계정 속성

>[!IMPORTANT]
>
>`accountName` 특성이 필요합니다. 계정 대상의 계정이 비어 있는 경우 해당 계정은 수집되지 않으며 대상을 참조하는 계정 여정 및 구매 그룹에서 생략됩니다.

| [속성](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | 표시 이름 | Journey Optimizer B2B 표시 이름 | 데이터 유형 | 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | 구/군/시 | 구/군/시 | 문자열 | 청구 주소에 사용되는 도시 이름. |
| `accountBillingAddress.country` | 국가 | 국가 | 문자열 | 청구 주소에 사용되는 정부 관리 영역의 이름. `xdm:countryCode`이(가) 아닌 모든 언어의 국가 이름을 사용할 수 있는 자유 형식의 필드입니다. |
| `accountBillingAddress.postalCode` | 우편번호 | 주소 우편 번호 | 문자열 | 청구 주소 위치의 우편 번호입니다. 우편 번호는 모든 국가에서 사용할 수 없습니다. 일부 국가에서는 우편번호의 일부만 포함되어 있습니다. |
| `accountBillingAddress.region` | 지역 | 주소 영역 | 문자열 | 청구지 주소의 지역, 국가 또는 지역 부분입니다. |
| `accountBillingAddress.state` | 주/도 | 주/도 | 문자열 | 청구 주소의 주 이름입니다. 자유 형식의 필드입니다. |
| `accountBillingAddress.street1` | 도로 1 | 도로 1 | 문자열 | 일반적으로 아파트 번호, 거리 번호 및 거리 이름을 포함하는 청구 주소의 기본 거리 수준 정보입니다. |
| `accountName` | 이름 | 이름 | 문자열 | **필수 필드** <br/>회사 이름. 이 필드에는 최대 255자가 허용됩니다. |
| `accountOrganization.annualRevenue.amount` | 연간 수익 | 연간 수익 | 숫자 | 조직의 예상 연간 매출액. |
| `accountOrganization.industry` | 업종 | 업종 | 문자열 | 그 산업은 조직에 기인했다. 자유 형식의 필드이므로 쿼리에 대해 구조화된 값을 사용하거나 `xdm:classifier` 속성을 사용하는 것이 좋습니다. |
| `accountOrganization.logoUrl` | 로고 Url | 로고 Url | 문자열 | 계정과 연결된 소셜 네트워크 프로필 이미지를 요청할 URL을 생성하기 위해 Salesforce 인스턴스의 URL과 결합할 경로(예: `https://yourInstance.salesforce.com/`). 생성된 URL은 계정에 대한 소셜 네트워크 프로필 이미지에 대한 HTTP 리디렉션(코드 302)을 반환합니다. |
| `accountOrganization.numberOfEmployees` | 직원 수 | 직원 수 | 정수 | 조직의 직원 수. |
| `accountOrganization.SICCode` | SIC 코드 | SIC 코드 | 문자열 | 표준산업분류(SIC) 코드는 기업 비즈니스 활동에 따라 기업이 속한 업종을 분류하는 4자리 코드다. |
| `accountOrganization.website` | 웹 사이트 URL | 도메인 이름 | 문자열 | 조직 웹 사이트의 URL. |
| `accountPhone.number` | N/A | 계정 전화번호 | 문자열 | 계정과 연계된 전화번호. |
| `accountSourceType` | N/A | 소스 유형 | 문자열 | Source 계정 유형입니다. |

## XDM 비즈니스 영업 기회 속성

또한 영업 기회 데이터는 [Experience Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}에 설명된 대로 다대일 관계를 통해 XDM 비즈니스 계정 클래스와 연결할 수 있는 XDM 비즈니스 영업 기회 클래스에 특성으로 저장됩니다.

| [속성](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} | 표시 이름 | Journey Optimizer B2B 표시 이름 | 데이터 유형 | 설명 |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | 예상 종료일 | 예상 영업 기회 종료일 | 문자열 | 영업 기회의 예상 종료일. |
| `expectedRevenue.amount` | 예상 수익 | 총 영업 기회 예상 수익 | 문자열 | 금액 및 확률에 따라 계산된 매출액. |
| `fiscalQuarter` | 회계 분기 | 영업 기회 회계 분기 | 문자열 | 영업 기회의 대상 회계 분기입니다. |
| `fiscalYear` | 회계 연도 | 영업 기회 회계 연도 | 문자열 | 영업 기회에 대한 대상 회계 연도입니다. |
| `forecastCategory` | 예측 범주 | 영업 기회 예측 범주 | 문자열 | 영업 기회 단계 값에 의해 결정된 예측 범주. |
| `forecastCategoryName` | 예측 범주 이름 | 영업 기회 예측 범주 이름 | 문자열 | 특정 예측 범주에 대한 보고서에 표시되는 예측 범주 이름. |
| `isClosed` | 마감 플래그 | 영업 기회 종료됨 | 문자열 | 영업 기회가 종료되었는지 보여 주는 플래그. |
| `isWon` | 성공한 플래그 | 기회 획득함 | 문자열 | 영업 기회의 성공 여부를 보여 주는 플래그. |
| `lastActivityDate` | 마지막 활동 날짜 | 마지막 활동 날짜 | 문자열 | 영업 기회에 대한 마지막 활동 날짜입니다. |
| `leadSource` | 잠재 고객 소스 | 잠재 고객 소스 | 문자열 | Advertising, Partner 또는 Web 과 같은 영업 기회의 Source |
| `nextStep` | 다음 단계 | 영업 기회 다음 단계 | 문자열 | 영업 기회 종료에 대한 다음 작업에 대한 설명. |
| `opportunityAmount.amount` | 영업 기회 금액 | 총 영업 기회 금액 | 문자열 | 영업 기회에 대한 예상 총 판매 금액. |
| `opportunityDescription` | 영업 기회 설명 | 영업 기회 설명 | 문자열 | 영업 기회를 설명하는 추가 정보(예: 판매 가능한 제품 또는 고객의 과거 구매). |
| `opportunityName` | 기회 이름 | 영업 기회 이름 | 문자열 | 영업 기회에 대한 예상 주문 또는 회사명과 같은 제목이나 설명적인 이름. |
| `opportunityQuantity` | 영업 기회 수량 | 영업 기회 수량 | 문자열 | 영업 기회에 대한 관련 제품 목록의 모든 제품에 대한 모든 수량 필드 값의 합계. |
| `opportunityStage` | 영업 기회 단계 | 영업 기회 단계 | 문자열 | 영업 단계에서 영업 팀이 수주하는 데 도움을 줄 수 있습니다. |
| `opportunityType` | 영업 기회 유형 | 영업 기회 유형 | 문자열 | 영업 기회에 할당된 형식(예: _기존 비즈니스_ 또는 _새 비즈니스_) |
| `probabilityPercentage` | 확률 백분율 | 영업 기회 확률 백분율 | 문자열 | 백분율로 표시된 영업 기회 종료 가능성. |
