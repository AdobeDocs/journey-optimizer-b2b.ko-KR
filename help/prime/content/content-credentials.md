---
title: Content Credentials
description: Adobe Journey Optimizer B2B Prime이 생성 AI로 생성된 이미지에 Content Credentials을 자동으로 적용하는 방법과 이것이 귀하의 콘텐츠에 어떤 의미가 있는지 알아봅니다.
feature: Assets, Content
role: User
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 제한된 베타 릴리스의 일부입니다."
autotag-review: '2026-07-31T22:31:06.899Z'
TQID: 'https://experienceleague.adobe.com/fBPnAmupve3xMSw5fZPQBDTUfr-rwiH2-R3wbKvox-E'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2:
  - id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0b
  - id: e666e996-b2cf-4c45-8fc2-1c625212abab
  - id: aed878b8-11d0-487c-828b-d23b2051ec37
subfeature_v2:
  - id: d270a788-eb1d-40ed-b74e-9158ed975b1f
  - id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: ad794b50f6c6f3b59e853e99f7983136ee098e18
workflow-type: tm+mt
source-wordcount: 560
ht-degree: 0%

---

# Content Credentials

마케팅 조직들은 콘텐츠 투명성, AI 공시, 자산 변조 방지에 어느 때보다 신경을 곤두세우고 있다. Adobe의 Content Authenticity Initiative(CAI)는 [콘텐츠 증명 및 인증을 위한 연합](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model)&#x200B;(C2PA) 기술 표준을 준수하는 도구를 빌드합니다. _Content Credentials_(암호화된, 변조 가능한 메타데이터)은 시청자가 콘텐츠 계보를 이해하고 브랜드 자산의 무결성을 확인하는 데 도움이 됩니다. 이 정보에는 다음이 포함됩니다.

* 발행자 또는 서명자 — 자산을 인증하거나 서명하기 위해 디지털 서명을 발행한 법인 또는 회사에 대한 정보입니다.
* 문제 날짜 — Content Credential이 자산에 적용된 날짜입니다.
* 신용 및 사용 - 이름, 소셜 미디어 핸들 또는 기타 ID 관련 정보를 포함하여 에셋 제작자에 대한 정보입니다.
* 프로세스 — 에셋에 대한 편집 또는 수정 사항의 기록입니다.
* 장치 세부 정보 — 에셋을 만들거나 편집하는 데 사용되는 앱 또는 장치에 대한 정보입니다.
* 사용된 AI 도구 — 생성 AI를 사용하여 에셋을 만든 경우 사용된 모델의 이름이 포함될 수 있습니다.
* 기타 관련 정보 — 에셋 기록에 대한 추가 컨텍스트를 제공하는 데 도움이 되는 추가 데이터도 포함될 수 있습니다.

자산 내역에 대한 포괄적인 정보를 보려면 Adobe Content Authenticity [검사 도구](https://contentauthenticity.adobe.com/inspect)를 사용할 수 있습니다.

Content Credentials은 이미지 파일로 유지됩니다. 생성 AI로 생성되거나 편집된 이미지를 [!DNL Adobe Journey Optimizer B2B Prime]에 업로드하거나 내보내면 해당 Content Credentials이 유지됩니다.

>[!NOTE]
>
>PDF 또는 임베드된(base64) 소스에서 이미지를 추출하는 것과 같이 이미지를 콘텐츠로 가져오는 일부 방법에서는 원본 Content Credentials이 유지되지 않을 수 있습니다. 이러한 경우 Content Credentials은 소스에서 읽을 수 없으며 결과에 대해 아무것도 만들어지지 않습니다.

>[!BEGINSHADEBOX]

## 채널을 통한 Content Credentials 지속성 {#channels}

이메일 또는 WhatsApp 메시지에 이미지를 포함하면 게재된 이미지에 대한 Content Credentials도 유지됩니다.

* **전자 메일** - _전자 메일 보내기_ 여정 작업을 사용하는 경우 _Assets_ 라이브러리의 전자 메일 콘텐츠에 이미지를 추가하십시오. 이메일이 전달되면 수신자는 메시지에서 이미지를 다운로드할 수 있으며 Content Credentials은 그대로 유지됩니다.
* **WhatsApp** - Meta 비즈니스 계정의 WhatsApp 메시지 템플릿에 이미지를 추가합니다. 자체 시스템에서 직접 추가하거나 _Assets_ 라이브러리에서 이미지 파일을 다운로드할 수 있습니다. _WhatsApp 보내기_ 여정 작업에 템플릿을 사용합니다. WhatsApp 메시지가 전달되면 수신자는 메시지에서 이미지를 다운로드할 수 있으며 Content Credentials은 그대로 유지됩니다.

>[!ENDSHADEBOX]

## 이미지 생성 {#generate}

>[!INFO]
>
>생성 AI 투명성을 중심으로 새로운 법이 등장하고 있으며, Adobe은 관할권 전반에서 적용 가능한 요구 사항을 충족하기 위해 노력하고 있습니다. Content Credentials은 Adobe이 이러한 법률의 요구 사항을 충족하기 위해 사용하는 조달 도구입니다.

생성 AI를 사용하여 [!DNL Journey Optimizer B2B Prime]에서 이메일 콘텐츠에 대한 이미지를 만들면 Content Credentials이 생성된 이미지에 자동으로 첨부되며 별도의 작업이 필요하지 않습니다. 생성 AI 도구는 원본 소스를 포함하여 기존 자격 증명과 변형 이미지에 대한 결합된 Content Credentials 요소를 생성합니다.

>[!NOTE]
>
>[!DNL Journey Optimizer B2B Prime]은(는) 현재 수동 이미지 편집 작업을 지원하지 않습니다. 현재 이러한 작업에 대한 Content Credentials 워크플로는 적용할 수 없습니다.
