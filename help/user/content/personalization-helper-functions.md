---
title: 도우미 함수
description: Journey Optimizer B2B edition의 개인화 도우미 기능에 대한 참조 안내서입니다. 여기에는 문자열, 날짜, 수학 등에 대한 구문과 예제가 포함되어 있습니다.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: 표현식, 편집기, 구문, 개인화
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '4857'
ht-degree: 6%

---

# 도우미 함수

개인화 편집기 내의 도우미 함수를 사용하여 데이터를 조작하고, 계산을 수행하고, 콘텐츠 형식을 지정하여 정밀도와 효율성으로 개인화된 콘텐츠 경험을 정의할 수 있습니다. 이러한 기능, 연산자 및 도우미를 탐색하고 실험하여 이러한 기능이 함께 작동하여 맞춤형의 데이터 기반 여정을 구축하는 데 도움이 되는 방법을 알아보십시오.

>[!AVAILABILITY]
>
>도우미 함수는 [간소화된 아키텍처](../simplified-architecture.md)에서 프로비저닝된 Journey Optimizer B2B edition 환경에서 사용할 수 있습니다.

## 집계 함수

집계 함수를 사용하여 여러 값을 그룹화하여 단일 요약 값을 만듭니다. 배열 및 목록 함수를 사용하여 배열, 목록 및 문자열과의 상호 작용을 보다 쉽게 정의할 수도 있습니다.

### 평균 {#average}

`average` 함수를 사용하여 배열에서 선택한 모든 값의 산술 평균을 반환합니다.

+++구문

```sql
{%= average(array) %}
```

**예**

다음 작업은 모든 주문의 평균 가격을 반환합니다.

```sql
{%=average(orders.order.price)%}
```

+++

### count {#count}

`count` 함수를 사용하여 지정된 배열에 있는 요소의 수를 반환합니다.

+++구문

```sql
{%= count(array) %}
```

**예**

다음 작업은 배열에 있는 주문 수를 반환합니다.

```sql
{%= count(orders) %}
```

+++

### max {#max}

`max` 함수를 사용하여 배열에서 선택한 모든 값 중 가장 큰 값을 반환합니다.

+++구문

```sql
{%= max(array) %}
```

**예**

다음 작업은 모든 주문의 가장 높은 가격을 반환합니다.

```sql
{%=max(orders.order.price)%}
```

+++

### min {#min}

`min` 함수를 사용하여 배열에서 선택한 모든 값 중 가장 작은 값을 반환합니다.

+++구문

```sql
{%= min(array) %}
```

**예**

다음 작업은 모든 주문의 최저 가격을 반환합니다.

```sql
{%=min(orders.order.price) %}
```

+++

### sum {#sum}

`sum` 함수를 사용하여 배열에서 선택한 모든 값의 합계를 반환합니다.

+++구문

```sql
{%= sum(array) %}
```

**예**

다음 작업은 모든 주문 가격의 합계를 반환합니다.

```sql
 {%=sum(orders.order.price)%}
```

+++

## 산술 함수 {#maths}

산술 함수를 사용하여 값에 대한 기본 계산을 수행합니다.

### 추가 {#add}

`+`(추가) 함수를 사용하여 두 인수 표현식의 합계를 찾으십시오.

+++구문

```sql
{%= double + double %}
```

**예**

다음 연산은 서로 다른 두 제품의 가격을 합산합니다.

```sql
{%= product1.price + product2.price %}
```

+++

### 곱하기 {#multiply}

`*`(곱하기) 함수를 사용하여 두 인수 표현식의 곱을 찾으십시오.

+++구문

```sql
{%= double * double %}
```

**예**

다음 작업은 재고의 제품과 제품의 가격을 찾아 제품의 총액을 구합니다.

```sql
{%= product.inventory * product.price %}
```

+++

### 빼기 {#substract}

`-`(빼기) 함수를 사용하여 두 인수 표현식의 차이점을 찾습니다.

+++구문

```sql
{%= double - double %}
```

**예**

다음 작업은 두 가지 다른 제품 간의 가격 차이를 확인합니다.

```sql
{%= product1.price - product2.price %}
```

+++

### 나누기 {#divide}

`/`(나눗셈) 함수를 사용하여 두 인수 표현식의 몫을 찾으십시오.

+++구문

```sql
{%= double / double %}
```

**예**

다음 작업은 품목당 평균 비용을 보기 위해 판매된 총 제품과 벌어들인 총 금액 사이의 몫을 구합니다.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

+++

### 나머지 {#remainder}

`%`(remainder) 함수를 사용하여 두 인수 표현식을 나눈 후 나머지를 찾습니다.

+++구문

```sql
{%= double % double %}
```

**예**

다음 수술은 개인의 나이를 5로 나눌 수 있는지 확인합니다.

```sql
{%= person.age % 5 = 0 %}
```

+++

## 배열 및 목록 함수 {#arrays}

이러한 함수를 사용하여 배열, 목록 및 문자열과 보다 쉽게 상호 작용할 수 있습니다.

### countOnlyNull {#count-only-null}

`countOnlyNull` 함수를 사용하여 목록의 null 값 수를 계산하십시오.

+++구문

```sql
{%= countOnlyNull(array) %}
```

**예**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

3을 반환합니다.

+++

### countWithNull {#count-with-null}

`countWithNull` 함수를 사용하여 null 값을 포함한 목록의 모든 요소를 계산합니다.

+++구문

```sql
{%= countWithNull(array) %}
```

**예**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

6을 반환합니다.

+++

### distinct {#distinct}

중복 값이 제거된 배열 또는 목록에서 값을 가져오려면 `distinct` 함수를 사용하십시오.

+++구문

```sql
{%= distinct(array) %}
```

**예**

다음 작업은 두 개 이상의 스토어에서 주문한 사람을 지정합니다.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

+++

### distinctCountWithNull {#distinct-count-with-null}

`distinctCountWithNull` 함수를 사용하여 null 값을 포함한 목록의 다른 값 수를 계산합니다.

+++구문

```sql
{%= distinctCountWithNull(array) %}
```

**예**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

3을 반환합니다.

+++

### head {#head}

`head` 함수를 사용하여 배열 또는 목록의 첫 번째 항목을 반환합니다.

+++구문

```sql
{%= head(array) %}
```

**예**

다음 작업은 가격이 가장 높은 상위 5개 주문 중 첫 번째 주문을 반환합니다. `topN` 함수에 대한 자세한 내용은 배열의 [첫 번째 `n`](#first-n) 섹션에서 찾을 수 있습니다.

```sql
{%= head(topN(orders,price, 5)) %}
```

+++

### topN {#first-n}

`topN` 함수는 지정된 수식을 기반으로 내림차순으로 배열을 정렬하고 첫 번째 `N`개 항목을 반환합니다. 배열 크기가 `N`보다 작으면 정렬된 전체 배열을 반환합니다.

+++구문

```sql
{%= topN(array, value, amount) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열 또는 목록을 정렬하는 데 사용되는 속성입니다. |
| `{AMOUNT}` | 반환할 항목의 수입니다. |

**예**

다음 작업은 가격이 가장 낮은 처음 5개의 주문을 반환합니다.

```sql
{%= topN(orders,price, 5) %}
```

+++

### in {#in}

항목이 배열의 멤버인지 또는 목록의 멤버인지 확인하려면 `in` 함수를 사용하십시오.

+++구문

```sql
{%= in(value, array) %}
```

**예**

다음 작업은 3월, 6월 또는 9월에 생일이 있는 사람을 정의합니다.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

+++

### 포함 {#includes}

`includes` 함수를 사용하여 배열 또는 목록에 지정된 항목이 포함되어 있는지 확인하십시오.

+++구문

```sql
{%= includes(array,item) %}
```

**예**

다음 작업은 즐겨 찾는 색상에 빨간색이 포함된 사람을 정의합니다.

```sql
{%= includes(person.favoriteColors,"red") %}
```

+++

### 교차 {#intersects}

`intersects` 함수는 두 배열 또는 목록에 하나 이상의 공통 멤버가 있는지 확인하는 데 사용됩니다.

+++구문

```sql
{%= intersects(array1, array2) %}
```

**예**

다음 작업은 좋아하는 색상에 빨간색, 파란색 또는 녹색 중 하나 이상을 포함하는 사용자를 정의합니다.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```

+++

<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

### bottomN {#last-n}

`bottomN` 함수는 지정된 수식을 기반으로 배열을 오름차순으로 정렬하고 첫 번째 `N`개 항목을 반환합니다. 배열 크기가 `N`보다 작으면 정렬된 전체 배열을 반환합니다.

+++구문

```sql
{%= bottomN(array, value, amount) %}
```

| 인수 | 설명 |
| --------- | ----------- | 
| `{ARRAY}` | 정렬할 배열 또는 목록입니다. |
| `{VALUE}` | 배열 또는 목록을 정렬하는 데 사용되는 속성입니다. |
| `{AMOUNT}` | 반환할 항목의 수입니다. |

**예**

다음 작업은 가격이 가장 높은 마지막 5개의 주문을 반환합니다.

```sql
{%= bottomN(orders,price, 5) %}
```

+++

### notIn {#notin}

`notIn` 함수를 사용하여 항목이 배열 또는 목록의 멤버가 아닌지 확인합니다.

>[!NOTE]
>
>`notIn` 함수 *also*&#x200B;에서는 두 값 모두 null이 아닙니다. 따라서 결과는 `in` 함수에 대한 정확한 부정 결과가 아닙니다.

+++구문

```sql
{%= notIn(value, array) %}
```

**예**

다음 작업은 생일이 3월, 6월 또는 9월이 아닌 사람을 정의합니다.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```

+++

### 부분 집합 {#subset}

`subsetOf` 함수를 사용하여 특정 배열(배열 A)이 다른 배열(배열 B)의 하위 집합인지 확인합니다. 즉, 배열 A의 모든 요소는 배열 B의 요소이다.

+++구문

```sql
{%= subsetOf(array1, array2) %}
```

**예**

다음 작업은 자신이 좋아하는 모든 도시를 방문한 사람들을 정의합니다.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

+++

### 위 집합 {#superset}

`supersetOf` 함수를 사용하여 특정 배열(배열 A)이 다른 배열(배열 B)의 상위 집합인지 확인합니다. 즉, 배열 A는 배열 B의 모든 요소를 포함합니다.

+++구문

```sql
{%= supersetOf(array1, array2) %}
```

**예**

다음 작업은 스시와 피자를 한 번이라도 먹은 사람들을 정의합니다.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

+++

## 날짜 및 시간 함수 {#date-time}

날짜 및 시간 함수를 사용하여 값에 대한 날짜 및 시간 작업을 수행합니다.

### addDays {#add-days}

`addDays` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 일수만큼 지정된 날짜를 조정합니다.

+++구문

```sql
{%= addDays(date, number) %}
```

**예**

* 입력: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 출력: `2024-11-11T17:19:51Z`

+++

### addHours {#add-hours}

`addHours` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 시간만큼 지정된 날짜를 조정합니다.

+++구문

```sql
{%= addHours(date, number) %}
```

**예**

* 입력: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* 출력: `2024-11-01T18:19:51Z`

+++

### addMinutes {#add-minutes}

`addMinutes` 함수는 양수 값을 사용하여 증가 및 음수 값을 사용하여 지정된 시간(분)만큼 지정된 날짜를 조정합니다.

+++구문

```sql
{%= addMinutes(date, number) %}
```

**예**

* 입력: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* 출력: `2024-11-01T18:09:51Z`

+++

### addMonth {#add-months}

`addMonths` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 개월 수만큼 지정된 날짜를 조정합니다.

+++구문

```sql
{%= addMonths(date, number) %}
```

**예**

* 입력: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 출력: `2025-01-01T17:19:51Z`

+++

### addSeconds {#add-seconds}

`addSeconds` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 시간(초)만큼 날짜를 조정합니다.

+++구문

```sql
{%= addSeconds(date, number) %}
```

**예**

* 입력: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 출력: `2024-11-01T17:20:01Z`

+++

### addYears {#add-years}

`addYears` 함수는 양수 값을 사용하여 증가되고 음수 값을 사용하여 지정된 연도 수만큼 지정된 날짜를 조정합니다.

+++구문

```sql
{%= addYears(date, number) %}
```

**예**

* 입력: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 출력: `2026-11-01T17:19:51Z`

+++

### 나이 {#age}

`age` 함수를 사용하여 지정된 날짜의 기간을 검색합니다.

+++구문

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

+++

### ageInDays {#age-days}

`ageInDays` 함수는 지정된 날짜와 현재 날짜 사이에 경과된 일 수를 계산합니다. 이후 날짜에는 음수를 사용하고 이전 날짜에는 양수를 사용합니다.

+++구문

```sql
{%= ageInDays(date) %}
```

**예**

currentDate = 2025-01-07T12:17:10.720122+05:30(아시아/콜카타)

* 입력: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* 출력: `5`

+++

### ageInMonths {#age-months}

`ageInMonths` 함수는 지정된 날짜와 현재 날짜 사이에 경과된 개월 수를 계산합니다. 이후 날짜에는 음수를 사용하고 이전 날짜에는 양수를 사용합니다.

+++구문

```sql
{%= ageInMonths(date) %}
```

**예**

currentDate = 2025-01-07T12:22:46.993748+05:30(아시아/콜카타)

* 입력: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* 출력: `12`

+++

### compareDate {#compare-dates}

`compareDates` 함수는 첫 번째 입력 날짜와 다른 입력 날짜를 비교합니다. date1이 date2와 같으면 0, date1이 date2 앞에 오면 -1, date1이 date2 뒤에 오면 1을 반환합니다.

+++구문

```sql
{%= compareDates(date1, date2) %}
```

**예**

* 입력: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* 출력: `-1`

+++

### convertZonedDateTime {#convert-zoned-date-time}

`convertZonedDateTime` 함수는 날짜-시간을 지정된 시간대로 변환합니다.

+++구문

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

**예**

* 입력: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* 출력: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

### currentTimeInMillis {#current-time}

`currentTimeInMillis` 함수를 사용하여 에포크 밀리초로 현재 시간을 검색합니다.

+++구문

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

+++

### dateDiff {#date-diff}

`dateDiff` 함수를 사용하여 두 날짜 사이의 차이점을 일 수로 검색합니다.

+++구문

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfMonth {#day-month}

`dayOfMonth`은(는) 그 달의 요일을 나타내는 숫자를 반환합니다.

+++구문

```sql
{%= dayOfMonth(datetime) %}
```

**예**

* 입력: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* 출력: `5`

+++

### DayOfWeek {#day-week}

`dayOfWeek` 함수를 사용하여 요일을 검색합니다.

+++구문

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### dayOfYear {#day-year}

`dayOfYear` 함수를 사용하여 연간 일자를 검색합니다.

+++구문

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInSeconds {#diff-seconds}

`diffInSeconds` 함수는 두 날짜 간의 차이점을 초 단위로 반환합니다.

+++구문

```sql
{%= diffInSeconds(endDate, startDate) %}
```

**예**

* 입력: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* 출력: `50`

+++

### extractHours {#extract-hours}

`extractHours` 함수는 특정 타임스탬프에서 시간 구성 요소를 추출합니다.

+++구문

```sql
{%= extractHours(date) %}
```

**예**

* 입력: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `17`

+++

### extractMinutes {#extract-minutes}

`extractMinutes` 함수는 특정 타임스탬프에서 분 구성 요소를 추출합니다.

+++구문

```sql
{%= extractMinutes(date) %}
```

**예**

* 입력: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `19`

+++

### extractMonths {#extract-months}

`extractMonth` 함수는 지정된 타임스탬프에서 월 구성 요소를 추출합니다.

+++구문

```sql
{%= extractMonths(date) %}
```

**예**

* 입력: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `11`

+++

### extractSeconds {#extract-seconds}

`extractSeconds` 함수는 특정 타임스탬프에서 두 번째 구성 요소를 추출합니다.

+++구문

```sql
{%= extractSeconds(date) %}
```

**예**

* 입력: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `51`

+++

### formatDate {#format-date}

`formatDate` 함수를 사용하여 날짜/시간 값의 형식을 지정하십시오. 형식은 올바른 Java `DateTimeFormat` 패턴이어야 합니다.

+++구문

```sql
{%= formatDate(datetime, format) %}
```

여기서 첫 번째 문자열은 날짜 속성이고 두 번째 값은 날짜를 변환하여 표시하는 방식입니다.

>[!NOTE]
>
> 날짜 패턴이 유효하지 않은 경우 날짜는 ISO 표준 형식으로 대체됩니다.
>
> [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}에 요약된 대로 Java 날짜 서식 함수를 사용할 수 있습니다.

**예**

다음 작업은 날짜를 MM/DD/YY 형식으로 반환합니다.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

#### 패턴 문자 {#pattern-characters}

일부 패턴 문자는 비슷해 보이지만 다른 개념을 나타냅니다.

| 패턴 | 의미 | 예(예: `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | 달력 연도(표준 연도) | `2023` |
| `Y` | 주 기준 연도(ISO 8601). 연도 경계가 다를 수 있습니다. | `2024`(2023년 12월 31일은 2024년 첫째 주에 해당됨) |
| `M` | 월(1-12 또는 `Jan`, `January` 같은 텍스트) | `12` 또는 `Dec` |
| `m` | 분/시간(0-59) | `15` |
| `d` | 날짜(1-31) | `31` |
| `D` | 일(1-366) | `365` |

#### 로케일 지원을 사용하여 날짜 형식 지정 {#format-date-locale}

`formatDate` 함수를 사용하여 원하는 로케일과 같이 날짜 시간 값을 해당 언어에 맞는 표현으로 서식을 지정할 수 있습니다. 형식은 올바른 Java `DateTimeFormat` 패턴이어야 합니다.

+++구문

```sql
{%= formatDate(datetime, format, locale) %}
```

여기서 첫 번째 문자열은 date 속성이고 두 번째 값은 날짜를 변환하여 표시하는 방식이며 세 번째 값은 로케일을 문자열 형식으로 나타냅니다.

>[!NOTE]
>
> 날짜 패턴이 유효하지 않은 경우 날짜는 ISO 표준 형식으로 대체됩니다.
>
> [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)에 요약된 대로 Java 날짜 서식 함수를 사용할 수 있습니다.
>
> [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 및 [지원되는 로케일](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)에 요약된 대로 서식 및 올바른 로케일을 사용할 수 있습니다.

**예**

다음 작업은 날짜를 MM/dd/YY 및 로케일 FRANCE 형식으로 반환합니다.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
```

+++

### getCurrentZonedDateTime {#get-current-zoned-date-time}

`getCurrentZonedDateTime` 함수는 표준 시간대 정보와 함께 현재 날짜 및 시간을 반환합니다.

+++구문

```sql
{%= getCurrentZonedDateTime() %}
```

**예**

* 입력: `{%= getCurrentZonedDateTime() %}`
* 출력: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

### diffInHours {#hours-difference}

`diffInHours` 함수는 시간 측면에서 두 날짜 간의 차이를 반환합니다.

+++구문

```sql
{%= diffInHours(endDate, startDate) %}
```

**예**

* 입력: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* 출력: `10`

+++

### diffInMinutes {#diff-minutes}

`diffInMinutes` 함수는 분 단위로 두 날짜 간의 차이점을 반환합니다.

+++구문

```sql
{%= diffInMinutes(endDate, startDate) %}
```

**예**

* 입력: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* 출력: `60`

+++

### diffInMonths {#months-difference}

`diffInMonths` 함수는 월 단위로 두 날짜 간의 차이점을 반환합니다.

+++구문

```sql
{%= diffInMonths(endDate, startDate) %}
```

**예**

* 입력: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* 출력: `3`

+++

### setDays {#set-days}

`setDays` 함수를 사용하여 지정된 날짜-시간에 대한 날짜의 날짜를 설정합니다.

+++구문

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### setHours {#set-hours}

`setHours` 함수를 사용하여 날짜-시간의 시간을 설정합니다.

+++구문

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### toDateTime {#string-to-date-time}

`toDateTime` 함수는 문자열을 날짜로 변환합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.

+++구문

```sql
{%= toDateTime(string, string) %}
```

**예**

* 입력: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* 출력: `2024-11-01T17:19:51Z`

+++

### toUTC {#to-utc}

`toUTC` 함수를 사용하여 날짜/시간을 UTC로 변환합니다.

+++구문

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### truncateToStartOfDay {#truncate-day}

`truncateToStartOfDay` 함수를 사용하여 지정된 날짜-시간을 00:00에 시간이 있는 날의 시작으로 설정합니다.

+++구문

```sql
{%= truncateToStartOfDay(date) %}
```

**예**

* 입력: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* 출력: `2024-11-01T00:00Z`

+++

### truncateToStartOfQuarter {#truncate-quarter}

`truncateToStartOfQuarter` 함수 사용은 00:00에서 날짜-시간을 해당 분기의 첫 번째 날(예: 1월 1일, 4월 1일, 7월 1일, 10월 1일)로 자르는 데 사용됩니다.

+++구문

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

**예**

* 입력: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `2024-10-01T00:00Z`

+++

### truncateToStartOfWeek {#truncate-week}

`truncateToStartOfWeek` 함수는 특정 날짜-시간을 주의 시작(월요일 00:00)으로 설정하여 수정합니다.

+++구문

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

**예**

* 입력: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* 출력: `2024-11-18T00:00Z // monday`

+++

### truncateToStartOfYear {#truncate-year}

`truncateToStartOfYear` 함수를 사용하여 지정된 날짜-시간을 00:00에서 연도의 첫째 날(1월 1일)로 자릅니다.

+++구문

```sql
{%= truncateToStartOfYear(dateTime) %}
```

**예**

* 입력: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* 출력: `2024-01-01T00:00Z`

+++

### 주/연도 {#week-of-year}

`weekOfYear` 함수를 사용하여 연간 주를 검색합니다.

+++구문

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

+++

### diffInYears {#diff-years}

`diffInYears` 함수를 사용하여 연도 단위로 두 날짜 간의 차이를 반환합니다.

+++구문

```sql
{%= diffInYears(endDate, startDate) %}: int
```

**예**

* 입력: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* 출력: `5`

+++

## 연산자 함수 {#operators}

부울 및 비교 함수를 사용하여 논리 평가를 수행합니다.

### 및 {#and}

`and` 함수는 논리 결합을 만드는 데 사용됩니다.

+++구문

```sql
{%= query1 and query2 %}
```

**예**

다음 작업은 본국(프랑스) 및 출생연도(1985)를 가진 모든 사람을 반환합니다.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

+++

### 또는 {#or}

`or` 함수는 논리 분리를 만드는 데 사용됩니다.

+++구문

```sql
{%= query1 or query2 %}
```

**예**

다음 작업은 본국(프랑스) 또는 출생연도(1985)가 있는 모든 사람을 반환합니다.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

+++

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

### 같음 {#operator-equals}

`=`(equals) 함수는 하나의 값 또는 식이 다른 값 또는 식과 같은지 확인합니다.

+++구문

```sql
{%= expression = value %}
```

**예**

다음 작업에서는 홈 주소 국가가 프랑스인지 확인합니다.

```sql
{%= profile.homeAddress.country = "France" %}
```

+++

### 같지 않음 {#notequal}

`!=`(같지 않음) 함수는 하나의 값 또는 식이 다른 값 또는 식과 **같지 않음**&#x200B;인지 확인합니다.

+++구문

```sql
{%= expression != value %}
```

**예**

다음 작업에서는 홈 주소 국가가 프랑스가 아닌지 확인합니다.

```sql
{%= profile.homeAddress.country != "France" %}
```

+++

### 다음보다 큼 {#greaterthan}

`>`(보다 큼) 함수를 사용하여 첫 번째 값이 두 번째 값보다 큰지 확인합니다.

+++구문

```sql
{%= expression1 > expression2 %}
```

**예**

다음 수술은 1970년 이후 출생한 사람들을 엄격하게 정의합니다.

```sql
{%= profile.person.birthYear > 1970 %}
```

+++

### 크거나 같음 {#greaterthanorequal}

`>=`(크거나 같음) 함수를 사용하여 첫 번째 값이 두 번째 값보다 크거나 같은지 확인하십시오.

+++구문

```sql
{%= expression1 >= expression2 %}
```

**예**

다음 수술은 1970년 이후 출생자를 정의합니다.

```sql
{%= profile.person.birthYear >= 1970 %}
```

+++

### 다음보다 작음 {#lessthan}

`<`(보다 작음) 비교 함수를 사용하여 첫 번째 값이 두 번째 값보다 작은지 확인하십시오.

+++구문

```sql
{%= expression1 < expression2 %}
```

**예**

다음 작업은 2000년 이전에 태어난 사람들을 정의합니다.

```sql
{%= profile.person.birthYear < 2000 %}
```

+++

### 보다 작거나 같음{#lessthanorequal}

`<=`(작거나 같음) 비교 함수를 사용하여 첫 번째 값이 두 번째 값보다 작거나 같은지 확인하십시오.

+++구문

```sql
{%= expression1 <= expression2 %}
```

**예**

다음 작업은 2000년 이전에 태어난 사람들을 정의합니다.

```sql
{%= profile.person.birthYear <= 2000 %}
```

+++

## 동적 함수 {#dynamic-helpers}

동적 개인화를 위해 조건부 평가, 반복 및 변수 할당을 사용하려면 동적 도우미 함수를 사용하십시오.

### 기본 대체 값 {#default-value}

`Default Fallback Value` 도우미는 특성이 비어 있거나 null인 경우 기본 대체 값을 반환하는 데 사용됩니다. 이 메커니즘은 프로필 속성 및 여정 이벤트에 대해 작동합니다.

+++구문

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

이 예제에서는 이 프로필의 `there` 특성이 비어 있거나 null인 경우 값 `firstName`이(가) 표시됩니다.

+++

### if (conditions) {#if-function}

`if` 도우미는 조건부 블록을 정의하는 데 사용됩니다.
표현식 계산이 true를 반환하면 블록이 렌더링되고 그렇지 않으면 건너뜁니다.

+++구문

```sql
{%#if contains(account.accountOrganization.primaryEmailDomain, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

`if` 도우미 다음에 `else` 문을 입력하여 동일한 조건이 false인 경우 실행할 코드 블록을 지정할 수 있습니다.
`elseif` 문은 첫 번째 문이 false를 반환하는 경우 테스트할 새 조건을 지정합니다.


**형식**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

<!-- 
**Examples**

* **Render different store links based on conditional expressions**

    ```sql
    {%#if profile.homeAddress.countryCode = "FR"%}
    <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
    {%else%}
    <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
    {%/if%}
    ```

* **Determine email address extension**

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Add a conditional link**

    The following operation adds a link to the `www.adobe.com/academia` website for profiles with '.edu' email addresses only, the `www.adobe.com/org` website for profiles with '.org' email addresses, and the default URL `www.adobe.com/users` for all other profiles:

    ```sql
    {%#if contains(profile.personalEmail.address, ".edu")%}
    <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
    {%else if contains(profile.personalEmail.address, ".org")%}
    <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
    {%else%}
    <a href="https://www.adobe.com/users">Checkout our page</a>
    {%/if%}
    ```

* **Conditional content based on audience membership**

    ```sql
    {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
    Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
    {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
    Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
    {%/if%}
    ```
-->

+++

### unless {#unless}

`unless` 도우미를 사용하여 조건부 블록을 정의합니다. `if` 헬퍼와 반대로 식 계산이 false를 반환하는 경우 블록이 렌더링됩니다.

+++구문

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**예**

이메일 주소 확장을 기반으로 일부 콘텐츠를 렌더링합니다.

```sql
{%#unless endsWith(account.accountOrganization.primaryEmailDomain}, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

+++

### 각각 {#each}

`each` 도우미를 사용하여 배열을 반복합니다.

도우미 구조가 ```{{#each ArrayName}}``` YourContent `{{/each}}`입니다.

블록 내에서 `this` 키워드를 사용하여 개별 배열 항목을 참조할 수 있습니다. 배열 요소의 인덱스를 렌더링하려면 `{{@index}}`을(를) 사용합니다.

+++구문

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**예**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**예**

이 사용자가 장바구니에 보유한 제품 목록을 렌더링합니다.

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

+++

### 포함 {#with}

`with` 도우미를 사용하여 템플릿 부분의 평가 토큰을 변경하십시오.

+++구문

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with` 도우미는 바로 가기 변수를 정의하는 데에도 유용합니다.

**예**

긴 변수 이름을 짧은 변수 이름으로 앨리어싱하려면 `with`을(를) 사용하십시오.

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

+++

### let {#let}

`let` 함수를 사용하면 나중에 쿼리에서 사용할 변수로 식을 저장할 수 있습니다.

+++구문

```sql
{% let variable = expression %} {{variable}}
```

**예**

다음 예에서는 장바구니에 있는 제품의 가격 합계를 100에서 1000 사이로 계산할 수 있습니다.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

+++

## 실행 메타데이터 {#execution-metadata}

>[!AVAILABILITY]
>
>이 기능은 제한된 가용성입니다. 액세스 권한을 얻으려면 Adobe 담당자에게 문의하십시오.

`executionMetadata`을(를) 사용하여 사용자 지정 키-값 쌍을 캡처하고 메시지 실행 컨텍스트에 동적으로 저장합니다.

이 함수를 사용하면 캠페인 또는 여정의 모든 기본 작업에 컨텍스트 정보를 추가할 수 있습니다. 이를 사용하여 추적, 분석, 개인화 및 다운스트림 처리와 같은 다양한 목적을 위해 실시간 게재 컨텍스트 데이터를 외부 시스템으로 내보냅니다.

>[!NOTE]
>
>사용자 지정 작업은 `executionMetadata` 함수를 지원하지 않습니다.

예를 들어 `executionMetadata` 도우미를 사용하여 각 프로필로 전송되는 각 게재에 특정 ID를 추가할 수 있습니다. 이 정보는 런타임 중에 생성되며, 그런 다음 외부 보고 플랫폼과의 다운스트림 조정을 위해 보강된 실행 메타데이터를 내보낼 수 있습니다.

+++구문

```
{{executionMetadata key="your_key" value="your_value"}}
```

이 구문에서 `key`은(는) 메타데이터 이름을 참조하며 `value`은(는) 유지할 메타데이터입니다.

**작동 방식**

캠페인 또는 여정 내의 채널 콘텐츠에서 요소를 선택하고 개인화 편집기를 사용하여 이 요소에 `executionMetadata` 도우미를 추가하십시오.

>[!NOTE]
>
>콘텐츠 자체가 표시되면 `executionMetadata` 함수가 표시되지 않습니다.

런타임 시 메타데이터 값이 다음 스키마를 추가하여 기존 **[!UICONTROL 메시지 피드백 이벤트 데이터 세트]**&#x200B;에 추가됩니다.

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!IMPORTANT]
>
>작업당 키 값 쌍에는 2kb의 상한이 있습니다. 2Kb 제한을 초과하는 경우 메시지가 계속 전달되지만 키 값 쌍은 잘릴 수 있습니다.

**예**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

이 예에서 `profile.person.name.firstName` = &quot;Alex&quot;라고 가정하면 결과 엔터티는 다음과 같습니다.

```
{
  "key": "firstName",
  "value": "Alex"
}
```

+++

## 맵 함수 {#maps}

개인화에 맵 함수를 사용하여 맵과의 상호 작용을 보다 쉽게 만듭니다.

### get {#get}

지정된 키에 대한 맵 값을 검색하려면 `get` 함수를 사용하십시오.

+++구문

```sql
{%= get(map, string) %}
```

**예**

다음 작업은 키 `example@example.com`에 대한 ID 맵 값을 가져옵니다.

```sql
{%= get(identityMap,"example@example.com") %}
```

+++

### 키 {#keys}

지정된 맵에 대한 모든 키를 검색하려면 `keys` 함수를 사용하십시오.

+++구문

```sql
{%= keys(map) %}
```

**예**

다음 작업은 맵 `identityMap`의 모든 키를 검색합니다.

```sql
{%= keys(identityMap) %}
```

+++

### 값 {#values}

`values` 함수는 지정된 맵의 모든 값을 검색하는 데 사용됩니다.

+++구문

```sql
{%= values(map) %}
```

**예**

다음 작업은 맵 `identityMap`의 모든 값을 검색합니다.

```sql
{%= values(identityMap) %}
```

+++

## 수학 함수 {#math}

개인화 편집기에서 수학 함수를 사용하는 방법에 대해 알아봅니다.

### 절대 {#absolute}

`absolute` 함수를 사용하여 숫자를 절대값으로 변환합니다.

+++구문

```sql
{%= absolute(int) %}: int
```

+++

### formatNumber {#format-number}

`formatNumber` 함수를 사용하여 모든 숫자를 해당 언어 구분 표현으로 서식을 지정합니다.

숫자와 로케일을 나타내는 문자열을 수락하고 원하는 로케일에서 숫자의 서식 있는 문자열을 반환합니다.

+++구문

```sql
{%= formatNumber(number/double,string) %}: string
```

[Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 및 [지원되는 로케일](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}에 요약된 대로 서식 및 올바른 로케일을 사용할 수 있습니다.

**예**

이 쿼리는 입력 숫자로 123456.789에 해당하는 아랍어로 형식이 지정된 문자열을 반환합니다.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

+++

### random {#random}

`random` 함수를 사용하여 0과 1 사이의 임의 값을 반환합니다.

+++구문

```sql
{%= random() %}: double
```

+++

### 내림 {#round-down}

`roundDown` 함수를 사용하여 숫자를 내림하십시오.

+++구문

```sql
{%= roundDown(double) %}: double
```

+++

### roundUp {#round-up}

`roundUp` 함수를 사용하여 숫자를 올림하십시오.

+++구문

```sql
{%= roundUp(double) %}: double
```

+++

### toHexString {#to-hex-string}

`toHexString` 함수는 임의의 숫자를 16진수 문자열로 변환합니다.

+++구문

```sql
{%= toHexString(number) %}: string
```

**예**

이 쿼리는 158의 16진수 값을 9e로 반환합니다.

```sql
{%= toHexString(158) %}
```

+++

### toInt {#to-int}

`toInt` 함수를 사용하여 형식(숫자, 더블, 정수, long, float, short, 바이트, 부울, 문자열)을 정수로 변환합니다.

+++구문

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**예**

이 쿼리는 42.6의 정수 값을 42로 반환합니다.

```sql
{%= toInt(42.6) %}: integer
```

+++

### toPercent {#to-percentage}

`toPercentage` 함수를 사용하여 숫자를 백분율로 변환합니다.

+++구문

```sql
{%= toPercentage(double) %}: string
```

+++

### toPrecision {#to-precision}

`toPrecision` 함수를 사용하여 숫자를 필요한 전체 자릿수로 변환합니다.

+++구문

```sql
{%= toPrecision(double,int) %}: string
```

+++

### toString {#to-string}

`toString` 함수는 숫자를 문자열 표시로 변환합니다.

+++구문

```sql
{%= toString(string) %}: string
```

**예**

이 쿼리는 `"12"`을(를) 반환합니다.

```sql
{%= toString(12) %} 
```

+++

## 개체 함수 {#objects}

객체 등록 정보 또는 속성을 쿼리하는 객체 함수입니다.

### isNull {#isNull}

`isNull` 함수는 개체 참조가 없는지 확인합니다.

+++구문

```sql
{%= isNull(object) %}
```

**예**

다음 작업은 해당 사용자의 홈 주소가 존재하지 않는지 확인합니다.

```sql
{%= isNull(person.homeAddress) %}
```

+++

### isNotNull {#isNotNull}

`isNotNull` 함수는 개체 참조가 있는지 확인합니다.

+++구문

```sql
{%= isNotNull(object) %}
```

**예**

다음 작업은 해당 사용자의 집 주소가 있는지 확인합니다.

```sql
{%= isNotNull(person.homeAddress) %}
```

+++

## 문자열 함수 {#string-functions}

개인화 편집기에서 String 함수를 사용하는 방법을 알아봅니다.

### 카멜 대/소문자 {#camelCase}

`camelCase` 함수는 문자열의 각 단어의 첫 번째 문자를 대문자로 바꿉니다.

+++구문

```sql
{%= camelCase(string)%}
```

**예**

다음 함수는 프로필의 주소에서 단어의 첫 번째 문자를 대문자로 바꿉니다.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

+++

### charCodeAt {#char-code-at}

`charCodeAt` 함수는 JavaScript의 `charCodeAt` 함수와 같은 문자의 ASCII 값을 반환합니다. 이 메서드는 문자열과 정수(문자 위치를 정의함)를 입력 인수로 사용하고 해당 ASCII 값을 반환합니다.

+++구문

```sql
{%= charCodeAt(string,int) %}: int
```

**예**

다음 함수는 `o`(111)의 ASCII 값을 반환합니다.

```sql
{%= charCodeAt("some", 1)%}
```

+++

### concat {#concate}

`concat` 함수는 2개의 문자열을 하나로 결합합니다.

+++구문

```sql
{%= concat(string,string) %}
```

**예**

다음 함수는 프로필 도시와 국가를 단일 문자열로 결합합니다.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

+++

### 포함 {#contains}

문자열에 지정된 하위 문자열이 포함되어 있는지 확인하려면 `contains` 함수를 사용하십시오.

+++구문

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `STRING_1` | 확인을 수행하는 문자열입니다. |
| `STRING_2` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `CASE_SENSITIVE` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

* 다음 함수는 프로파일 이름에 문자 A(대소문자)가 포함되어 있는지 확인합니다. 프로필이 성공하면 `true`을(를) 반환합니다. 그렇지 않으면 `false`을(를) 반환합니다.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* 다음 쿼리는 대/소문자 구분을 통해 개인의 전자 메일 주소에 문자열 `2010@gm`이(가) 포함되어 있는지 확인합니다.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

+++

### doesNotContain {#doesNotContain}

문자열에 지정된 하위 문자열이 포함되어 있지 않은지 확인하려면 `doesNotContain` 함수를 사용하십시오.

+++구문

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `STRING_1` | 확인을 수행하는 문자열입니다. |
| `STRING_2` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `CASE_SENSITIVE` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 전자 메일 주소에 문자열 `2010@gm`이(가) 포함되어 있지 않은지 확인합니다.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```

+++

### doesNotEndWith {#doesNotEndWith}

문자열이 지정된 하위 문자열로 끝나지 않은지 확인하려면 `doesNotEndWith` 함수를 사용하십시오.

+++구문

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이메일 주소가 `.com`(으)로 끝나지 않는 경우를 결정합니다.

```sql
doesNotEndWith(person.emailAddress,".com")
```

+++

### doesNotStartWith {#doesNotStartWith}

문자열이 지정된 하위 문자열로 시작되지 않는지 확인하려면 `doesNotStartWith` 함수를 사용하십시오.

+++구문

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이름이 `Joe`(으)로 시작되지 않는 경우 결정합니다.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

+++

### encode64 {#encode64}

URL에 포함되는 개인 정보(PI)를 보존하기 위해 문자열을 인코딩하려면 `encode64` 함수를 사용하십시오.

+++구문

```sql
{%= encode64(string) %}
```

+++

### endsWith {#endsWith}

문자열이 지정된 하위 문자열로 끝나는지 확인하려면 `endsWith` 함수를 사용하십시오.

+++구문

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 가능한 값은 true (기본값) / false 입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 전자 메일 주소가 `.com`(으)로 끝나는지 여부를 결정합니다.

```sql
{%= endsWith(person.emailAddress,".com") %}
```

+++

### 같음 {#equals}

`equals` 함수를 사용하여 문자열이 지정된 문자열과 같은지 확인합니다. 대/소문자를 구분합니다.

+++구문

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이름이 `John`인지 확인합니다.

```sql
{%=equals(profile.person.name,"John") %}
```

+++

### equalsIgnoreCase {#equalsIgnoreCase}

문자열을 대/소문자를 구분하지 않고 지정한 문자열과 같은지 확인하려면 `equalsIgnoreCase` 함수를 사용하십시오.

+++구문

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자 구분 없이 개인의 이름이 `John`인지 확인합니다.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

+++

### extractEmailDomain {#extractEmailDomain}

`extractEmailDomain` 함수를 사용하여 전자 메일 주소의 도메인을 추출하십시오.

+++구문

```sql
{%= extractEmailDomain(string) %}
```

**예**

다음 쿼리는 개인 이메일 주소의 이메일 도메인을 추출합니다.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

+++

### formatCurrency {#format-currency}

`formatCurrency` 함수를 사용하여 두 번째 인수에서 문자열로 전달된 로케일에 따라 모든 숫자를 해당 언어 구분 통화 표시로 변환합니다.

+++구문

```sql
{%= formatCurrency(number/double,string) %}: string
```

**예**

이 쿼리는 £56.00 반환

```sql
{%= formatCurrency(56L,"en_GB") %}
```

+++

### getUrlHost {#get-url-host}

`getUrlHost` 함수를 사용하여 URL의 호스트 이름을 검색합니다.

+++구문

```sql
{%= getUrlHost(string) %}: string
```

**예**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

&quot;www.myurl.com&quot; 반환

+++

### getUrlPath {#get-url-path}

`getUrlPath` 함수를 사용하여 URL의 도메인 이름 뒤에 있는 경로를 검색합니다.

+++구문

```sql
{%= getUrlPath(string) %}: string
```

**예**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

&quot;/contact.html&quot; 반환

+++

### getUrlProtocol {#get-url-protocol}

`getUrlProtocol` 함수를 사용하여 URL의 프로토콜을 검색합니다.

+++구문

```sql
{%= getUrlProtocol(string) %}: string
```

**예**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

&quot;http&quot; 반환

+++

### indexOf {#index-of}

`indexOf` 함수를 사용하여 두 번째 매개 변수의 첫 번째 발생 횟수 위치(첫 번째 인수에서)를 반환합니다. 일치하는 항목이 없으면 -1을 반환합니다.

+++구문

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 매개 변수에서 검색할 문자열 |

**예**

```sql
{%= indexOf("hello world","world" ) %}
```

6을 반환합니다.

+++

### isEmpty {#isEmpty}

문자열이 비어 있는지 확인하려면 `isEmpty` 함수를 사용하십시오.

+++구문

```sql
{%= isEmpty(string) %}
```

**예**

다음 함수는 프로필의 휴대폰 번호가 비어 있는 경우 &#39;true&#39;를 반환합니다. 그렇지 않으면 `false`을(를) 반환합니다.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

+++

### isNotEmpty {#is-not-empty}

문자열이 비어 있지 않은지 확인하려면 `isNotEmpty` 함수를 사용하십시오.

+++구문

```sql
{= isNotEmpty(string) %}: boolean
```

**예**

다음 함수는 프로필의 휴대폰 번호가 비어 있지 않으면 &#39;true&#39;를 반환합니다. 그렇지 않으면 `false`을(를) 반환합니다.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

+++

### lastIndexOf {#last-index-of}

`lastIndexOf` 함수를 사용하여 두 번째 매개 변수의 마지막 발생 횟수 위치(첫 번째 인수에서)를 반환합니다. 일치하는 항목이 없으면 -1을 반환합니다.

+++구문

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 매개 변수에서 검색할 문자열 |

**예**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

7을 반환합니다.

+++

### leftTrim {#leftTrim}

`leftTrim` 함수를 사용하여 문자열의 시작 부분에서 공백을 제거합니다.

+++구문

```sql
{%= leftTrim(string) %}
```

+++

### length {#length}

`length` 함수를 사용하여 문자열 또는 식의 문자 수를 가져옵니다.

+++구문

```sql
{%= length(string) %}
```

**예**

다음 함수는 프로필의 도시 이름 길이를 반환합니다.

```sql
{%= length(profile.homeAddress.city) %}
```

+++

### 좋아요 {#like}

문자열이 지정된 패턴과 일치하는지 확인하려면 `like` 함수를 사용하십시오.

+++구문

```sql
{%= like(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 일치하는 표현식. 식을 만드는 데 지원되는 특수 문자 `%`과(와) `_`이(가) 있습니다. <ul><li>`%`은(는) 0개 이상의 문자를 나타내는 데 사용됩니다.</li><li>`_`은(는) 정확히 하나의 문자를 나타내는 데 사용됩니다.</li></ul> |

**예**

다음 쿼리는 `es` 패턴을 포함하는 프로필이 있는 모든 도시를 검색합니다.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

+++

### 소문자 {#lower}

문자열을 소문자로 변환하려면 `lowerCase` 함수를 사용하십시오.

+++구문

```sql
{%= lowerCase(string) %}
```

**예**

이 함수는 프로필 이름을 소문자로 변환합니다.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

+++

### matches {#matches}

문자열이 특정 정규 표현식과 일치하는지 확인하려면 `matches` 함수를 사용하십시오. 정규 표현식에서 일치하는 패턴에 대한 자세한 내용은 [Oracle 설명서](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)를 참조하세요.

+++구문

```sql
{%= matches(STRING_1, STRING_2) %}
```

**예**

다음 쿼리는 대/소문자 구분 없이 개인의 이름이 `John`(으)로 시작하는지 여부를 결정합니다.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

+++

### 마스크 {#mask}

문자열의 일부를 &quot;X&quot; 문자로 바꾸려면 `mask` 함수를 사용하십시오.

+++구문

```sql
{%= mask(string,integer,integer) %}
```

**예**

다음 쿼리는 &quot;123456789&quot; 문자열을 처음 2자와 마지막 2자를 제외한 &quot;X&quot; 문자로 바꿉니다.

```sql
{%= mask("123456789",1,2) %}
```

쿼리가 `1XXXXXX89`을(를) 반환합니다.

+++

### md5 {#md5}

`md5` 함수를 사용하여 문자열의 md5 해시를 계산하고 반환합니다.

+++구문

```sql
{%= md5(string) %}: string
```

**예**

```sql
{%= md5("hello world") %}
```

&quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot; 반환

+++

### notEqualTo {#notEqualTo}

문자열이 지정된 문자열과 같지 않은지 확인하려면 `notEqualTo` 함수를 사용하십시오.

+++구문

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이름이 `John`이(가) 아닌 경우 결정합니다.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

+++

### notEqualWithIgnoreCase {#not-equal-with-ignore-case}

`notEqualWithIgnoreCase` 함수를 사용하여 대/소문자를 무시하는 두 문자열을 비교합니다.

+++구문

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열과 비교할 문자열입니다. |

**예**

다음 쿼리는 대/소문자를 구분하지 않고 사용자의 이름이 `john`이(가) 아닌지 확인합니다.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

+++

### regexGroup {#regexGroup}

제공된 정규 표현식을 기반으로 특정 정보를 추출하려면 `regexGroup` 함수를 사용하십시오.

+++구문

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING}` | 확인을 수행하는 문자열입니다. |
| `{EXPRESSION}` | 첫 번째 문자열과 일치하는 정규 표현식. |
| `{GROUP}` | 일치시킬 표현식 그룹. |

**예**

다음 쿼리는 이메일 주소에서 도메인 이름을 추출합니다.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

+++

### replace {#replace}

`replace` 함수를 사용하여 문자열의 지정된 하위 문자열을 다른 하위 문자열로 바꿉니다.

+++구문

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 하위 문자열을 대체해야 하는 문자열입니다. |
| `{STRING_2}` | 대체할 하위 문자열. |
| `{STRING_3}` | 대체 하위 문자열. |

**예**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

`Hello Mark, here is your monthly newsletter!` 반환

+++

### replaceAll {#replaceAll}

`replaceAll` 함수를 사용하여 regex 식과 일치하는 텍스트의 모든 하위 문자열을 지정된 리터럴 대체 문자열로 바꿉니다. Regex에는 `\` 및 `+`에 대한 특수 처리가 있으며 모든 regex 표현식은 PQL 이스케이프 전략을 따릅니다. 바꾸기는 문자열의 시작부터 끝까지 계속됩니다. 예를 들어, `aa`을(를) `b` 문자열에서 `aaa`(으)로 바꾸면 `ba`이(가) 아닌 `ab`이(가) 됩니다.

+++구문

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> 두 번째 인수로 사용된 식이 특수 정규 표현식 문자인 경우 이중 백슬래시(`//`)를 사용합니다.  특수 정규 표현식 문자는 [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> 자세한 내용은 [Oracle 설명서](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}를 참조하세요.
>

+++

### rightTrim {#rightTrim}

`rightTrim` 함수는 문자열 끝에서 공백을 제거합니다.

+++구문

```sql
{%= rightTrim(string) %}
```

+++

### sha256 {#sha256}

`sha256` 함수는 문자열의 sha256 해시를 계산하고 반환합니다.

+++구문

```sql
{%= sha256(string) %} : string
```

**예**

```sql
{%= sha256("Eliechxh")%}
```

`0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d` 반환

+++

### split {#split}

문자열을 지정된 문자로 분할하려면 `split` 함수를 사용하십시오.

+++구문

```sql
{%= split(string,string) %}
```

+++

### startsWith {#startsWith}

문자열이 지정된 하위 문자열로 시작하는지 확인하려면 `startsWith` 함수를 사용하십시오.

+++구문

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 인수 | 설명 |
| --------- | ----------- |
| `{STRING_1}` | 확인을 수행하는 문자열입니다. |
| `{STRING_2}` | 첫 번째 문자열에서 검색할 문자열입니다. |
| `{CASE_SENSITIVE}` | 검사가 대/소문자를 구분하는지 여부를 결정하는 선택적 매개 변수입니다. 기본적으로 true로 설정되어 있습니다. |

**예**

다음 쿼리는 대/소문자 구분을 통해 개인의 이름이 `Joe`(으)로 시작하는지 확인합니다.

```sql
{%= startsWith(person.name,"Joe") %}
```

+++

### stringToDate {#string-to-date}

`stringToDate` 함수는 문자열 값을 날짜-시간 값으로 변환합니다. 이 메서드에는 날짜-시간의 문자열 표현과 포맷터의 문자열 표현이라는 두 가지 인수가 사용됩니다.

+++구문

```sql
{= stringToDate("date-time value","formatter" %}
```

**예**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

+++

### string_to_integer {#string-to-integer}

`string_to_integer` 함수를 사용하여 문자열 값을 정수 값으로 변환합니다.

+++구문

```sql
{= string_to_integer(string) %}: int
```

+++

### stringTonumber {#string-to-number}

문자열을 숫자로 변환하려면 `stringToNumber` 함수를 사용하십시오. 잘못된 입력에 대한 출력과 동일한 문자열을 반환합니다.

+++구문

```sql
{%= stringToNumber(string) %}: double
```

+++

### substr {#sub-string}

`substr` 함수를 사용하여 시작 인덱스와 끝 인덱스 사이에 문자열 식의 하위 문자열을 반환합니다.

+++구문

```sql
{= substr(string, integer, integer) %}: string
```

+++

### titleCase {#titleCase}

문자열의 각 단어의 첫 문자를 대문자로 표시하려면 `titleCase` 함수를 사용하십시오.

+++구문

```sql
{%= titleCase(string) %}
```

**예**

사용자가 Washington high street에 거주하는 경우 이 함수는 `Washington High Street`을(를) 반환합니다.

```sql
{%= titleCase(profile.person.location.Street) %}
```

+++

### toBool {#to-bool}

인수 유형에 따라 인수 값을 부울 값으로 변환하려면 `toBool` 함수를 사용하십시오.

+++구문

```sql
{= toBool(string) %}: boolean
```

+++

### toDateTime {#to-date-time}

문자열을 날짜로 변환하려면 `toDateTime` 함수를 사용하십시오. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다.

+++구문

```sql
{%= toDateTime(string, string) %}: date-time
```

+++

### toDateTimeOnly {#to-date-time-only}

`toDateTimeOnly` 함수를 사용하여 인수 값을 날짜/시간 전용 값으로 변환합니다. 잘못된 입력에 대한 출력으로 에포크 날짜를 반환합니다. 이 함수는 문자열, 날짜, 긴 필드 및 정수 필드 유형을 수락합니다.

+++구문

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

+++

### trim {#trim}

`trim` 함수는 문자열의 시작과 끝에서 모든 공백을 제거합니다.

+++구문

```sql
{%= trim(string) %}
```

+++

### upperCase {#upper}

`upperCase` 함수는 문자열을 대문자로 변환합니다.

+++구문

```sql
{%= upperCase(string) %}
```

**예**

이 함수는 프로필 성을 대문자로 변환합니다.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

+++

### urlDecode {#url-decode}

`urlDecode` 함수를 사용하여 URL로 인코딩된 문자열을 디코딩하십시오.

+++구문

```sql
{%= urlDecode(string) %}: string
```

+++

### urlEncode {#url-encode}

문자열을 URL로 인코딩하려면 `urlEncode` 함수를 사용하십시오.

+++구문

```sql
{%= urlEncode(string) %}: string
```

+++
