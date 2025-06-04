---
title: XDM 필드
description: Adobe Experience Platform 및 Journey Optimizer B2B edition 간에 동기화된 기본 속성 필드를 검토합니다.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9ad8ba495cdae4c88d9422f758ea912ca84e143c
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 13%

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

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->