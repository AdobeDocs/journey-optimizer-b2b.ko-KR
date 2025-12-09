---
title: 간소화된 아키텍처 설정
description: 간소화된 아키텍처에 대해 Journey Optimizer B2B edition을 설정합니다. XDM 스키마, 이메일/SMS 채널, Marketo Engage 여정 작업 및 사용자를 구성합니다.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: 8f2cd2a657892b0f776b51776d3056946930df21
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 6%

---

# 간소화된 아키텍처 설정

이제 간소화된 아키텍처를 사용하여 Adobe Journey Optimizer B2B edition을 사용할 수 있습니다. 이 업데이트된 아키텍처를 통해 Journey Optimizer B2B Edition과 Marketo Engage는 더 이상 동일한 시스템과 동일한 데이터 저장소에 있지 않습니다. Journey Optimizer B2B Edition은 Adobe Experience Platform에서만 데이터를 수신합니다. 하지만 계속해서 Marketo Engage 자격 및 일부 구성 기능을 사용하여 시스템을 프로비저닝하고 구성합니다.

간소화된 아키텍처는 Adobe Journey Optimizer B2B edition의 새로운 기능을 잠금 해제하는 기반입니다.

* **데이터를 쉽게 통합하고 확장할 수 있습니다.** 새 플랫폼은 사용자 지정 개체, 구매 그룹 및 계정 이벤트를 포함한 복잡한 데이터 모델을 지원합니다. 

* **여러 Adobe Marketo Engage 인스턴스 연결:** 한 곳에서 여러 Adobe Marketo Engage 환경의 데이터를 관리하고 통합합니다.

* **데이터를 안전하게 보호:** 고객 정보를 보호하는 고급 개인 정보 보호 및 보안 기능. (_준비 중_)

* **미래를 위한 빌드:** 이 업그레이드를 통해 지속적인 개선 및 혁신을 수행할 수 있습니다. 

이 아키텍처에 대해 프로비저닝된 환경의 경우 구성에 다음 지침을 사용하십시오.

## 네임스페이스 및 스키마

개요는 Experience Platform 설명서의 [B2B 네임스페이스 및 스키마](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces)를 참조하십시오.

### 환경 설정

B2B 네임스페이스 및 스키마 자동 생성 유틸리티를 지원하도록 Postman 환경을 설정합니다.

* [GitHub 저장소](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility)에서 네임스페이스와 스키마 자동 생성 유틸리티 컬렉션 및 환경을 다운로드할 수 있습니다.

* 필요한 헤더에 대한 값을 수집하고 샘플 API 호출을 읽는 방법에 대한 세부 정보를 포함하여 Experience Platform API 사용에 대한 자세한 내용은 [Experience Platform API 시작하기](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/platform-apis/api-guide) 안내서를 참조하십시오.

* Experience Platform API에 대한 자격 증명을 생성하는 방법에 대한 자세한 내용은 [Experience Platform API 인증 및 액세스](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication)에 대한 자습서를 참조하십시오.

* Experience Platform API용 Postman 설정에 대한 자세한 내용은 [Adobe Experience Platform의 Postman](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman)를 참조하십시오.

이제 Experience Platform 개발자 콘솔 및 Postman을 설정하여 Postman 환경에 적절한 환경 값 적용을 시작할 수 있습니다.

### 스크립트 실행

Postman 컬렉션 및 환경 설정을 사용하면 Postman 인터페이스를 통해 스크립트를 실행할 수 있습니다.

Postman 인터페이스에서 자동 생성기 유틸리티의 루트 폴더를 선택한 다음 상단 헤더에서 **실행**&#x200B;을 선택합니다.

Runner 인터페이스가 표시되면 모든 확인란이 선택되었는지 확인한 다음 **네임스페이스 및 스키마 자동 생성 유틸리티 실행**&#x200B;을 선택합니다.

요청이 성공하면 B2B에 필요한 네임스페이스와 스키마가 만들어집니다.

## XDM 필드 선택

Journey Optimizer B2B edition UI에서 애플리케이션 전체에서 사용할 수 있는 XDM 필드를 관리할 수 있습니다. 이러한 필드는 **_여정_**, **_구매 그룹_** 또는 **_전자 메일 개인화_**&#x200B;와 관련된 필드만 노출하여 인스턴스를 간소화하는 데 도움이 됩니다.

### XDM 클래스

#### 표준 클래스

아래 단계를 사용하여 표준 XDM 클래스의 필드를 정의합니다.

1. **[!UICONTROL 관리] > [!UICONTROL 구성]**(으)로 이동합니다.

1. 탐색 패널에서 **[!UICONTROL XDM 클래스]**&#x200B;를 선택합니다.

1. 사용 가능한 XDM 클래스를 보려면 **[!UICONTROL 표준]** 탭을 선택하십시오.

   * XDM 개별 프로필

   * XDM 비즈니스 계정

#### 관리되는 필드

애플리케이션 전체에서 사용할 수 있는 필드를 정의합니다.

1. _추가 메뉴_(**...**) 아이콘을 클릭하고 **[!UICONTROL 관리 필드 편집]**&#x200B;을 선택합니다.

1. 사용 가능한 필드 목록을 검토합니다. 필드 메타데이터의 _정보_ 아이콘을 클릭합니다.

1. 포함할 필드를 선택하고 필요하지 않은 필드에 대한 선택 내용을 지웁니다.

1. **[!UICONTROL 선택한 필드만 표시]** 슬라이더를 사용하여 선택 내용을 검토하십시오.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

#### 업데이트할 수 있는 필드

**[!UICONTROL 계정 프로필 업데이트]** 또는 **[!UICONTROL 개인 프로필 업데이트]** 여정 작업을 통해 수정할 수 있는 필드를 선택하십시오.

1. _추가 메뉴_(**...**) 아이콘을 클릭하고 **[!UICONTROL 업데이트할 수 있는 필드 편집]**&#x200B;을 선택합니다.

1. **[!UICONTROL 스키마]**&#x200B;를 선택한 다음 **[!UICONTROL 데이터 집합]**&#x200B;을 선택하십시오.

   이러한 스키마와 데이터 세트는 조직에서 제공합니다.

   업데이트 가능한 필드 보호:

   * 스키마 - 스키마에는 XDM 개별 프로필 클래스의 시스템 정의 필드 이외의 필수 필드(예: `identityMap` 또는 `personID`)가 포함되지 않아야 합니다.
   * 데이터 세트 - 다른 용도로 이미 사용 중인 데이터 세트를 선택하지 마십시오. 업데이트할 수 있는 필드를 저장하기 위한 전용 데이터 세트를 만드는 것이 좋습니다. 각 XDM 클래스에 대해 별도의 데이터 세트를 사용합니다.

1. 업데이트할 수 있는 필드 목록을 검토합니다. 메타데이터의 _정보_ 아이콘을 클릭합니다.

   관리되는 필드만 편집할 수 있습니다.

1. 여정에서 업데이트할 수 있도록 하려는 필드를 선택합니다.

1. **[!UICONTROL Save]**&#x200B;를 클릭합니다

### 관계형 스키마

[여정 결정](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational) 및 **_개인화_**&#x200B;에 사용할 **_관계형 스키마_**&#x200B;를 선택하십시오. 현재 이러한 스키마는 사용자 지정 개체 사용 사례용입니다. 향후에는 다른 객체 사용 사례에도 관계형 스키마를 사용할 수 있습니다.

1. **[!UICONTROL 관계형]** 탭을 선택합니다.

1. **[!UICONTROL 관계형 XDM 클래스 선택]**&#x200B;을 클릭합니다.

   현재 계정 다대일 사용자 지정 개체만 지원됩니다.

1. 스키마 필드 목록을 검토합니다. _정보_ 아이콘을 클릭하여 메타데이터를 봅니다.

1. 포함할 필드를 선택합니다.

1. **[!UICONTROL 선택한 필드만 표시]** 슬라이더를 사용하여 선택 내용을 검토하십시오.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

>[!NOTE]
>
>관계형 스키마에는 다음 구성이 있어야 합니다.
>
><li>동작: 레코드
>&gt; <li>세그먼테이션: 활성화됨
>&gt; <li>관계 유형: 다대일
>&gt; <li>참조 스키마: <a href="https://experienceleague.adobe.com/ko/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data">B2B 계정 - XDM 비즈니스 계정 스키마</a>
>&gt; <li>필수 필드: 기본 키, 외래 키 및 버전 설명자
>&gt; <li>관련 데이터 세트: 스키마에 정의 및 매핑됨

### 이벤트

**_여정 결정_**&#x200B;에서 사용할 경험 이벤트를 선택하십시오.

1. **[!UICONTROL 이벤트]** 탭을 선택합니다.

1. **[!UICONTROL 경험 이벤트 선택]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 이벤트 유형 선택]**&#x200B;을 클릭하고 이벤트 유형을 선택한 다음 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 필드 선택]**&#x200B;을 클릭하고 필요한 필드를 선택한 다음 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

## 이메일 구성

Journey Optimizer B2B edition에서 이메일을 보내도록 다음을 구성해야 합니다.  

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### 추적 및 이메일 게재를 위한 프로토콜

1. [전자 메일에 대한 DNS 레코드 만들기](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [SPF 및 DKIM 설정](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [DMARC 설정](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [도메인의 MX 레코드 설정](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [허용 목록에 아웃바운드 IP 주소 추가](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. 전용 IP 풀을 공유해야 하는 경우 실현 가능성 및 지원 설정에 대해 게재 팀에 문의하십시오.

### 이메일 채널 구성

간소화된 아키텍처에서 이메일 설정은 Marketo Engage 애플리케이션에서 구성됩니다. 전자 메일 관련 설정 단계를 완료합니다.

* [https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps)

* [https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### 커뮤니케이션 제한

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**&#x200B;을 선택합니다.

1. 탐색 패널에서 **[!UICONTROL 통신 제한]**&#x200B;을 선택합니다.

1. 글로벌 통신 제한 규칙 세트를 만듭니다(이 규칙 세트는 기본적으로 모든 Journey Optimizer B2B edition 인스턴스에 만들어집니다.).

   전역 규칙 세트가 만들어지지 않으면 통신 제한이 없습니다.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### 공유된 커뮤니케이션 제한

새 아키텍처 내에서 Journey Optimizer B2B edition 및 Marketo Engage은 기본적으로 독립적인 통신 제한을 갖습니다.

Marketo Engage 인스턴스가 Journey Optimizer B2B edition 인스턴스에 설정된 통신 제한을 공유하도록 하려면 Adobe 지원에 연락하여 구성에 대한 지원을 받거나 지원 티켓을 엽니다. 요청 시 엔지니어링 팀은 Journey Optimizer B2B edition과 하나 이상의 Marketo Engage 인스턴스 간에 통신 제한을 공유할 수 있습니다.

공유 통신 제한이 활성화되면 Journey Optimizer B2B edition에서 규칙을 정의하고 이러한 제한의 공유를 Marketo Munchkin 코드로 확장할 수 있습니다. 자세한 내용은 [통신 제한](./admin/configure-channels-emails.md#communication-limits)을 참조하세요.

<!-- internal info only 

Currently, the shared communication limit in the Marketo Engage instance must be set up through an API call.

For example, when:

* The munchkinId of the Journey Optimizer B2B Edition instance is `JKL-567-MNO`.
* The munchkinId of the Marketo Engage instance is `ABC-123-DEF` and it is in the SJ datacenter

The API request should look similar to the following:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```
-->

## SMS 채널 구성

자세한 내용은 [_SMS 구성_](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms)을 참조하세요.

## 여정의 Marketo Engage 작업

다음 여정 작업에서 사용할 하나 이상의 원격 **_Marketo Engage_** 인스턴스를 구성할 수 있습니다.

* Marketo 목록에 추가
* Marketo 목록에서 제거
* Marketo 요청 캠페인에 추가

이러한 연결을 구성하려면 다음 단계를 완료하십시오.

1. **[!UICONTROL 관리] > [!UICONTROL 구성]**(으)로 이동합니다.

1. 탐색 패널에서 **[!UICONTROL XDM 클래스]**&#x200B;를 선택합니다.

1. **[!UICONTROL 통합]** 탭을 선택합니다.

1. **[!UICONTROL 연결 만들기]**&#x200B;를 클릭합니다.

1. **[!UICONTROL 이름]** 및 **[!UICONTROL 설명]**&#x200B;을 입력하십시오.

1. 일치하는 개인 레코드에 대해 **[!UICONTROL 정책 업데이트]**&#x200B;를 선택하십시오.

1. **[!UICONTROL Munchkin ID]**, **[!UICONTROL 클라이언트 ID]**, **[!UICONTROL 클라이언트 암호]**&#x200B;를 입력하고 **[!UICONTROL Marketo에 연결]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 만들기]**&#x200B;를 클릭합니다.

## 사용자 온보딩

개요는 [사용자 관리](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) 페이지를 참조하십시오.

### 기존 사용자 그룹

기존의 모든 Journey Optimizer B2B edition 사용자가 새 아키텍처에 액세스해야 하는 경우 기존의 Journey Optimizer B2B edition 사용자 그룹을 사용하십시오. 시스템 관리자 또는 제품 관리자는 다음 단계를 수행할 수 있습니다.

1. 전용 Marketo Engage에서 제품 프로필을 만듭니다.

1. 생성된 제품 프로필에 기존 사용자 그룹을 추가합니다.

프로필은 해당 사용자 그룹에 이미 할당된 모든 역할과 권한을 부여합니다. 이 권한은 사용자가 Journey Optimizer B2B edition에 액세스할 수 있도록 이미 구성되어 있어야 합니다. 사용자 중 일부만 새 아키텍처에 액세스해야 하는 경우 아래에 설명된 단계를 완료합니다. 자세한 내용은 [현재 설명서](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)를 참조하세요.

### 새 사용자 그룹 만들기

1. 전용 Marketo Engage 인스턴스에서 제품 프로필을 만듭니다.
1. 새 사용자에 대한 사용자 그룹을 만듭니다.
1. 필요한 제품 프로필을 선택하여 사용자 그룹에 할당합니다.

   * 만든 Marketo Engage 프로필
   * Adobe Experience Platform 프로필
      * AEP-Default-All-Users
      * Adobe Experience Platform 데이터 수집
      * 데이터 수집 모든 액세스

1. 사용자를 사용자 그룹에 추가합니다.
1. Experience Platform에서 Journey Optimizer B2B edition 역할에 새 사용자 그룹을 추가합니다.
