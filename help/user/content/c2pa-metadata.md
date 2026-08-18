---
title: C2PA 메타데이터
description: Adobe Journey Optimizer B2B edition에서 생성 AI 도구로 생성 또는 편집한 이미지에 C2PA 메타데이터를 자동으로 적용하는 방법과 콘텐츠에 대한 의미에 대해 알아봅니다.
feature: Assets, Content
role: User
autotag-review: '2026-07-31T22:15:54.535Z'
TQID: 'https://experienceleague.adobe.com/9XCqPWz62uDDLFAyxARfD2jErYx2aOiOB5fAOGLLTbo'
product_v2: id: aacce07f-424e-489e-8d02-a4fb2f4211bd
feature_v2: id: a65c8aea-b21a-41ce-9ed7-6b517a69fd0bid: bef5003b-cad2-4f40-bdb2-a80426d52ef5id: e666e996-b2cf-4c45-8fc2-1c625212abab
subfeature_v2: id: c8402946-ff35-44c5-ab98-74c1bba0975f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: dd969d66eab5649ccb19fe6582dafe0b7304772c
workflow-type: tm+mt
source-wordcount: 913
ht-degree: 0%

---

# C2PA 메타데이터

마케팅 조직들은 콘텐츠 투명성, AI 공시, 자산 변조 방지에 어느 때보다 신경을 곤두세우고 있다. Adobe의 Content Authenticity Initiative(CAI)는 [콘텐츠 증명 및 인증을 위한 연합](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model)&#x200B;(C2PA) 기술 표준을 준수하는 도구를 빌드합니다. _C2PA 메타데이터_&#x200B;은(는) 시청자가 콘텐츠 계보를 이해하고 브랜드 자산의 무결성을 확인하는 데 도움이 되는 변조 가능한 암호화된 정보입니다. 이 정보에는 다음이 포함됩니다.

* 발행자 또는 서명자 - 에셋을 인증하거나 서명하기 위해 디지털 서명을 발행한 법인 또는 회사에 대한 정보.
* 문제 날짜 - C2PA 메타데이터가 에셋에 적용된 날짜입니다.
* 신용 및 사용 - 이름, 소셜 미디어 핸들 또는 기타 ID 관련 정보를 포함하여 에셋 제작자에 대한 정보입니다.
* 프로세스 - 에셋에 대한 편집 또는 수정 사항을 기록합니다.
* 장치 세부 정보 - 에셋을 만들거나 편집하는 데 사용되는 앱 또는 장치에 대한 정보입니다.
* 사용된 AI 도구 - 에셋을 편집하거나 만드는 데 생성 AI가 사용된 경우 사용된 모델의 이름이 포함될 수 있습니다.
* 기타 관련 정보 - 에셋 기록에 대한 추가 컨텍스트를 제공하는 데 도움이 되는 추가 데이터도 포함될 수 있습니다.

자산 내역에 대한 포괄적인 정보를 보려면 Adobe Content Authenticity [검사 도구](https://contentauthenticity.adobe.com/inspect)를 사용할 수 있습니다.

C2PA 메타데이터는 이미지 파일과 함께 유지됩니다. 생성 AI로 생성 또는 편집한 이미지를 [!DNL Adobe Journey Optimizer B2B Edition]에 업로드하거나 내보내면 해당 C2PA 메타데이터가 유지됩니다.

>[!NOTE]
>
>PDF 또는 임베드된(base64) 소스에서 이미지를 추출하는 것과 같이 이미지를 콘텐츠로 가져오는 일부 방법에서는 원본 C2PA 메타데이터를 보존하지 않을 수 있습니다. 이러한 경우 소스에서 C2PA 메타데이터를 읽을 수 없으며 결과에 대해 아무것도 만들어지지 않습니다.

>[!BEGINSHADEBOX]

## 채널을 통한 C2PA 메타데이터 지속성 {#channels}

이메일 또는 WhatsApp 메시지에 이미지를 포함하면 게재된 이미지에 대한 C2PA 메타데이터도 유지됩니다.

* **전자 메일** - _전자 메일 보내기_ 여정 작업을 사용하는 경우 _Assets_ 라이브러리의 전자 메일 콘텐츠에 이미지를 추가하십시오. 이메일이 전달되면 수신자는 메시지에서 이미지를 다운로드할 수 있고 C2PA 메타데이터는 그대로 유지됩니다.
* **WhatsApp** - Meta 비즈니스 계정의 WhatsApp 메시지 템플릿에 이미지를 추가합니다. 자체 시스템에서 직접 추가하거나 _Assets_ 라이브러리에서 이미지 파일을 다운로드할 수 있습니다. _WhatsApp 보내기_ 여정 작업에 템플릿을 사용합니다. WhatsApp 메시지가 전달되면 수신자는 메시지에서 이미지를 다운로드할 수 있으며 C2PA 메타데이터가 그대로 유지됩니다.

>[!ENDSHADEBOX]

## C2PA 메타데이터에 영향을 주는 작업 {#cc-workflows}

>[!INFO]
>
>생성 AI 투명성을 중심으로 새로운 법이 등장하고 있으며, Adobe은 관할권 전반에서 적용 가능한 요구 사항을 충족하기 위해 노력하고 있습니다. C2PA 메타데이터는 Adobe이 이러한 법률의 요구 사항을 충족하기 위해 사용하는 증명 도구입니다.

[!DNL Journey Optimizer B2B Edition]에서 생성 AI 도구를 사용하여 이미지를 생성하거나 편집하면 C2PA 메타데이터가 해당 이미지에 자동으로 첨부되며 별도의 작업이 필요하지 않습니다.

### 이미지 생성 {#generate}

**_예제:_** 원하는 시각적 개체를 설명하는 텍스트 프롬프트에서 전자 메일에 대한 배너 이미지를 생성합니다. 생성된 이미지에 C2PA 메타데이터가 첨부됩니다.

텍스트 프롬프트, 참조 이미지에서 새 이미지를 생성하거나 유사한 이미지를 생성하는 경우 C2PA 메타데이터가 항상 첨부됩니다.

### 이미지 자르기 {#crop}

**_예:_**

* 웹 페이지에 맞게 생성된 배너 이미지를 자릅니다. C2PA 메타데이터는 자르기를 통해 보존됩니다.
* 업로드한 스톡 사진을 이메일 배경으로 사용하고 화면에 맞게 자릅니다. 스톡 사진에 생성 AI 정보가 없으면 C2PA 메타데이터가 만들어지지 않습니다.

이미지 파일을 요청된 크기로 자르는 등 조정할 때 소스 이미지에 이미 해당 C2PA 메타데이터가 있는 경우에만 해당 C2PA 메타데이터가 유지됩니다. 자르기는 이미지 픽셀을 다시 만듭니다. 이렇게 하면 일반적으로 해당 C2PA 메타데이터가 제거되므로, AI 도우미는 자르기 전에 소스 이미지에서 이미지를 읽은 다음 자른 결과에 다시 만들어 다시 연결합니다. 자르기 자체로는 새로운 생성 AI 작업이 추가되지 않으며 기존 AI 작업을 유지합니다.

### 텍스트 오버레이 추가

**_예제:_** 랜딩 페이지의 생성된 배경 이미지에 텍스트 오버레이로 홍보용 헤드라인을 생성합니다. 배경 이미지의 C2PA 메타데이터는 유지됩니다.

생성된 텍스트를 배경 이미지 위에 렌더링하면 배경 이미지에 이미 C2PA 메타데이터가 있는 경우에만 C2PA 메타데이터가 결과 이미지에 첨부됩니다. 오버레이를 렌더링하면 새 이미지가 생성되므로 이미지 편집 도구는 배경에서 C2PA 메타데이터를 읽고 결과에 다시 첨부합니다. 오버레이 단계는 새로운 생성 AI 작업을 추가하지 않습니다.

### 이미지 오버레이

**_예:_**

* 생성된 제품 이미지를 생성된 배경과 결합하여 이메일 헤더를 만듭니다. 이 결과는 두 생성 AI 소스를 모두 반영하는 C2PA 메타데이터를 전달합니다.
* 업로드된 두 개의 브랜드 사진을 하나의 콜라주 이미지로 결합합니다. 두 소스 이미지 모두 생성 AI 작업을 전달하지 않으므로 C2PA 메타데이터는 생성되지 않습니다.

두 개 이상의 이미지를 함께 합성하고 소스 이미지에 C2PA 메타데이터가 있으면 결합된 이미지가 이를 유지하며 단일 C2PA 메타데이터 요소에 병합됩니다. 합성은 소스에서 새 이미지를 만들어 일반적으로 해당 C2PA 메타데이터를 제거합니다. 그러나 이미지 편집 도구는 합성하기 전에 소스 메타데이터를 읽은 다음, 생성 AI 작업에 기여한 모든 소스를 나열하는 단일 결합된 C2PA 메타데이터 요소를 빌드합니다.

<!--

In [!DNL Adobe Journey Optimizer B2B Edition], you can see C2PA metadata directly within the _Assets_ library. When you open the asset details, any image with C2PA metadata (such as those created with GenAI services) shows the manifest details in a dedicated panel. If the asset is downloaded, published, or shared, the C2PA metadata remains intact with the asset.

_To access C2PA metadata:_

1. In the left navigation, expand **[!UICONTROL Content Management]** and select **[!UICONTROL Assets]**.

   This action opens a listing page with all the assets listed.

1. Navigate to a folder, and select the desired asset.

1. In the right panel, ??? where is it.

-->
