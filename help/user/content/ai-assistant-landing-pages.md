---
title: 랜딩 페이지 콘텐츠에 대한 AI 지원
description: AI Assistant를 사용하여 랜딩 페이지 콘텐츠 생성 - Journey Optimizer B2B edition에서 참조 에셋 및 구매 그룹 역할 타겟팅을 사용하여 페이지 텍스트 및 이미지를 생성합니다.
feature: Generative AI, Landing Pages, Content
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
topic: Artificial Intelligence
role: User
level: Beginner
exl-id: d1e818fb-7450-4c13-bc6c-24da5fb71285
source-git-commit: 859656dc4e355be0d9efe9414ad93404970d6e73
workflow-type: tm+mt
source-wordcount: '2700'
ht-degree: 1%

---

# 랜딩 페이지 콘텐츠에 대한 AI 지원 {#generative-full-content}

[!DNL Adobe Journey Optimizer B2B Edition]의 랜딩 페이지 콘텐츠용 AI 길잡이는 Adobe의 AI 기반 콘텐츠 생성 기능을 사용하여 마케터가 전문적이고 브랜드 일관적인 랜딩 페이지 콘텐츠를 만드는 방식을 혁신합니다. 고급 생성 AI 모델과 브랜드 지침에 대한 깊은 이해를 통해 AI Assistant는 개인화되고 매력적이며 효과적인 콘텐츠를 자동 생성합니다. 마케팅 목표를 사용하고 브랜드 윤곽선 스타일, 레이아웃, 색조 등에 대한 콘텐츠를 최적화합니다. AI Assistant를 사용하면 캠페인과 프로그램 생성 및 실행이 보다 직관적이고 단순하며 번거롭지 않습니다. 워크플로우에 이 기능을 추가하면 시간을 절약하고 효율성을 개선하며 더 나은 결과를 얻을 수 있습니다.

텍스트와 이미지를 모두 포함하여 랜딩 페이지에 대한 완전한 콘텐츠 경험을 생성할 수 있습니다. 이 강력한 기능은 대상자와 연결하는 매력적인 브랜드 내 콘텐츠를 만드는 데 도움이 됩니다.

>[!NOTE]
>
>이 기능은 Beta 버전에서 사용할 수 있으며 사전 공지 없이 변경될 수 있습니다.

>[!IMPORTANT]
>
>[!DNL Journey Optimizer B2B Edition]에서 이러한 기능에 액세스하려면 _[!UICONTROL AI Assistant]_ > _[!UICONTROL 콘텐츠 생성]_ 권한이 있어야 합니다. 제품 관리자가 기능 권한을 부여하는 방법에 대한 자세한 내용은 [제품 권한에 대한 역할 편집](../admin/user-management.md#edit-roles-for-product-permissions)을 참조하십시오.

## 지침 및 제한 사항

이 기능을 사용하기 전에 [지침 및 제한 사항](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations)을 검토하십시오. [!DNL Journey Optimizer B2B Edition]에서 AI 기능을 사용하려면 [사용자 동의](https://www.adobe.com/kr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} 동의가 필요합니다. 자세한 내용은 Adobe 담당자에게 문의하십시오.

미디어 생성 시 생성 AI 도구 사용의 투명성을 강화하기 위한 Adobe의 약속으로, Adobe은 Firefly 생성 에셋을 포함하는 모든 콘텐츠 또는 프로젝트에 다운로드하거나 내보낼 때 [콘텐츠 자격 증명](https://helpx.adobe.com/kr/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"}을 적용합니다.

[!DNL Journey Optimizer B2B Edition]에서 랜딩 페이지 콘텐츠 생성에 사용되는 AI Assistant 기능에는 다음 제한 사항과 지침이 적용됩니다.

* 영어는 유일하게 지원되는 언어입니다.
* 생성된 콘텐츠가 정확하지 않을 수 있습니다. Adobe 엔지니어가 모델을 개선할 수 있도록 피드백을 공유하십시오.
* 여러 콘텐츠 참조 에셋을 업로드할 수 있지만 특정 세대에 대해 하나의 에셋만 활용할 수 있습니다.
* 전체 랜딩 페이지에 대한 콘텐츠를 생성하는 데 브랜드별 또는 맞춤형 템플릿을 사용합니다. 최대 8~10개의 이미지가 있는 랜딩 페이지 템플릿이 권장됩니다.
* 생성된 변형을 선택할 때 썸네일 위로, 썸네일 아래로 또는 플래그 아이콘을 사용하여 문제가 있는 출력을 보고해야 합니다.

## 콘텐츠 생성을 위한 입력 및 설정

랜딩 페이지 또는 페이지에서 선택한 구성 요소에 대한 전체 콘텐츠를 생성할 수 있습니다. AI 비서 도구를 사용하여 필요한 콘텐츠를 생성하는 경우 프롬프트 및 참조 콘텐츠, 텍스트 및 이미지에 대한 설정 등 입력을 제공합니다.

### 프롬프트

생성 AI 모델이 정확하게 해석되도록 잘 정의된 프롬프트를 사용합니다. 제공하는 마케팅 목표/프롬프트는 생성된 콘텐츠의 품질에 큰 영향을 줍니다.

![프롬프트 필드](./assets/gen-ai-prompt.png){width="320"}

효과적인 프롬프트를 만드는 방법에 대한 자세한 내용은 _[프롬프트 모범 사례](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_&#x200B;를 참조하십시오.

>[!BEGINSHADEBOX]

**프롬프트 라이브러리**

최상의 콘텐츠를 생성하기 위해서는 효과적인 프롬프트가 필수적입니다. 프롬프트를 만드는 데 도움이 필요하면 _프롬프트 라이브러리_ ![프롬프트 라이브러리 아이콘](../assets/do-not-localize/icon-library.svg) 아이콘을 클릭하여 목표에 따라 구성된 프롬프트 아이디어 라이브러리에 액세스합니다. 검색 필드에 텍스트를 입력하여 키워드 문자열을 기반으로 프롬프트를 찾습니다.

![AI 길잡이 - 프롬프트 라이브러리에 액세스](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

의도한 목표를 가장 잘 반영하는 프롬프트를 선택하고 **[!UICONTROL 이 프롬프트 사용]**&#x200B;을 클릭합니다. _[!UICONTROL 프롬프트]_ 필드에서 자리 표시자(예: `[Key Feature/Information]`)를 브랜드, 오퍼, 캠페인 및 사용 사례를 지정하는 필요한 값으로 바꿉니다.

>[!ENDSHADEBOX]

### 텍스트 설정

오른쪽 패널에서 **[!UICONTROL 텍스트 설정]**&#x200B;을 확장하고 생성된 텍스트에 대한 옵션을 설정합니다.

* **[!UICONTROL 구매 그룹]** - 메시지를 타겟팅하는 데 사용할 [구매 그룹 역할](../buying-groups/buying-groups-role-templates.md)을(를) 선택하십시오.
* **[!UICONTROL 마케팅 여정 단계]** - 메시지를 타깃팅하는 데 사용할 [구매 그룹 단계](../buying-groups/buying-group-stages.md)를 선택합니다.
* **[!UICONTROL 커뮤니케이션 전략]** - 생성된 텍스트에 가장 적합한 커뮤니케이션 스타일을 선택합니다.
* **[!UICONTROL 언어]** - 생성된 콘텐츠의 언어를 선택합니다.
* **[!UICONTROL 음색]** - 음색이 대상자에게 울려 퍼집니다. 예를 들어 메시지를 유익하거나, 장난스럽거나, 설득력 있는 소리로 조정할 수 있습니다.

![구매 그룹, 마케팅 여정 단계, 커뮤니케이션 전략, 언어 및 색조 옵션을 보여 주는 텍스트 설정 패널](./assets/gen-ai-text-settings.png){width="350" zoomable="yes"}

왼쪽 화살표를 클릭하여 기본 _[!UICONTROL 설정]_(으)로 돌아갑니다.

### 이미지 설정

생성된 콘텐츠에 이미지를 포함하려면 오른쪽 패널에서 **[!UICONTROL 이미지 설정]**&#x200B;을 확장하고 옵션을 설정합니다.

**[!UICONTROL AI를 사용하여 이미지 생성]** 옵션은 기본적으로 비활성화되어 있습니다. 이 기능을 활성화하고 다음 옵션을 설정하여 제안된 콘텐츠 변형에 생성된 이미지를 포함합니다.

* **[!UICONTROL 생성 모델]**: 즉시 사용할 수 있는 Adobe 제공 모델, 전문 기능을 위한 파트너 모델 또는 브랜드 자산에 대해 교육된 구성된 사용자 지정 모델 중에서 선택합니다. 생성 모델에 대한 자세한 내용은 _[브랜드 정렬을 위한 생성 AI 모델](generative-ai-models.md)_&#x200B;을 참조하십시오.
* **[!UICONTROL 종횡비]**: 이미지 구성 요소를 선택하면 이 설정이 에셋의 너비와 높이를 결정합니다. 16:9, 4:3, 3:2 또는 1:1과 같은 일반적인 비율 중에서 선택할 수 있는 옵션이 있거나 사용자 지정 크기를 입력할 수 있습니다.
* **[!UICONTROL 콘텐츠 형식]**: 이 형식은 시각적 요소의 특성을 분류하여 사진, 그래픽 또는 미술과 같은 다양한 형식의 시각적 표현을 구별합니다.
* **[!UICONTROL 시각적 강도]**: 이미지의 강도를 조정하여 이미지의 영향을 제어합니다. 낮은 설정(예: 2)은 더 부드럽고 절제된 모양을 만드는 반면 높은 설정(예: 10)은 이미지를 더 생동감 있고 시각적으로 강력하게 만듭니다.
* **[!UICONTROL 색상 및 색조]**: 이미지 내의 전체 색상 모양과 이미지 내의 분위기 또는 분위기를 전달합니다.
* **[!UICONTROL 조명]**: 이미지에 사용되는 조명 스타일로, 이미지의 분위기를 형성하고 특정 요소를 강조 표시합니다.
* **[!UICONTROL 컴포지션]**: 이미지 프레임 내의 요소 배열입니다.

![생성 모델, 콘텐츠 유형, 시각적 강도, 색상 및 톤, 조명 및 컴포지션 옵션을 표시하는 이미지 설정 패널](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

왼쪽 화살표를 클릭하여 기본 _[!UICONTROL 설정]_(으)로 돌아갑니다.

### 참조 콘텐츠

참조 컨텐츠 자산을 업로드하여 정확한 브랜드 내 컨텐츠를 생성합니다. 그렇지 않으면 생성된 콘텐츠는 공개적으로 사용 가능한 정보를 기반으로 합니다. 참조 콘텐츠는 콘텐츠 생성 및 이미지 권장 사항의 소스 역할을 합니다. 지침 및 모범 사례에 대해서는 _[최적화된 참조 콘텐츠](../ai-assistant/generative-ai-content.md#reference-content)_&#x200B;를 참조하십시오.

**[!UICONTROL 참조 콘텐츠]** 설정에서 **[!UICONTROL 파일 업로드]**&#x200B;를 클릭하여 추가 컨텍스트에 사용할 콘텐츠가 포함된 에셋을 추가합니다.

![참조 콘텐츠에 사용할 파일 업로드](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

업로드할 파일은 PDF, JPEG, PNG 또는 ZIP 파일(지원되는 파일 형식 포함) 형식일 수 있습니다. 업로드된 브랜드 에셋의 최대 크기는 50MB입니다. 파일이 크거나 이미지가 많으면 작동할 수 있지만, 이렇게 하면 처리 시간이 늘어납니다.

이전에 업로드한 파일을 선택하려면 **[!UICONTROL 업로드한 참조 콘텐츠]** 목록을 확장하고 콘텐츠 생성에 사용할 자산을 활성화합니다.

![사용할 기존 참조 콘텐츠 사용](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## 생성 AI 도구 사용 {#gen-ai-tools}

콘텐츠 생성을 시작하려면 랜딩 페이지의 콘텐츠 편집기를 열고 오른쪽 패널의 외부 레일에 있는 생성 AI 도구에 액세스합니다. 현재 콘텐츠 선택에 사용할 수 있는 콘텐츠 생성 도구를 표시하려면 _AI Assistant_( ![콘텐츠 전환 AI Assistant](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} )을(를) 선택하십시오.

사용하려는 랜딩 페이지 콘텐츠 생성 유형에 따라 다음 단계를 사용하십시오.

>[!BEGINTABS]

>[!TAB 전체 페이지]

기존 랜딩 페이지 템플릿을 개선하여 전체 랜딩 페이지 생성에 AI Assistant를 사용하려면 다음 단계를 따르십시오.

1. [랜딩 페이지를 만든](./landing-pages.md#create-a-landing-page) 후 **[!UICONTROL 랜딩 페이지 편집]**&#x200B;을 클릭합니다.

1. 템플릿을 선택합니다.

   전체 콘텐츠를 생성하려면 템플릿이 필요합니다. Adobe에서 제공하는 표준 템플릿 또는 저장된 템플릿일 수 있습니다. _[!UICONTROL HTML 가져오기]_ 옵션을 사용하여 템플릿을 가져올 수도 있습니다.

   랜딩 페이지 템플릿 사용에 대한 자세한 내용은 _[저장된 템플릿 또는 샘플 템플릿 선택](./landing-pages.md#select-a-saved-or-sample-template)_&#x200B;을 참조하십시오.

1. 오른쪽 패널의 바깥쪽 레일에서 _AI Assistant_(![AI Assistant for content toggle](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) 아이콘을 선택합니다.

   ![랜딩 페이지 디자인 공간에서 AI 길잡이 전환](./assets/gen-ai-full-landing-page-ai-panel.png){width="600" zoomable="yes"}

   오른쪽의 AI Assistant 설정은 전체 랜딩 페이지에 대한 생성 설정을 반영합니다.

1. (Beta) **[!UICONTROL 브랜드]**&#x200B;를 선택하여 AI 생성 콘텐츠가 브랜드 사양에 맞게 조정되도록 합니다.

   게시된 브랜드가 없는 경우 **[!UICONTROL 브랜드 만들기]**&#x200B;를 클릭하여 [재사용 가능한 브랜드 지침](./brands-overview.md)을(를) 정의합니다.

1. **[!UICONTROL 프롬프트]** 필드에 생성할 내용에 대한 설명을 입력합니다.

   효과적인 프롬프트를 만드는 데 도움이 필요하면 [프롬프트 라이브러리](#prompt-library)를 사용하십시오.

   ![AI 길잡이 - 랜딩 페이지 콘텐츠를 생성하기 위한 프롬프트 라이브러리](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >생성된 콘텐츠를 묻는 메시지를 처음 표시하는 경우 _[확인 모범 사례](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_&#x200B;를 검토하십시오.

1. 생성된 콘텐츠를 사용자 지정하려면 콘텐츠 지침 설정을 완료합니다.

   * [**[!UICONTROL 텍스트 설정]**](#text-settings) - 생성된 텍스트 콘텐츠에 대한 지침을 제공합니다.
   * [**[!UICONTROL 이미지 설정]**](#image-settings) - 생성된 콘텐츠에 이미지를 포함하려면 이미지 생성을 활성화하고 지침을 제공하십시오.
   * [**[!UICONTROL 참조 콘텐츠]**](#reference-content) - 콘텐츠 생성의 원본 역할을 하는 콘텐츠 자산을 제공합니다.

1. 프롬프트 및 설정이 준비되면 **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

1. AI 도우미 패널에서 아래로 스크롤하여 생성된 변형을 탐색하여 가장 적합한 변형을 결정합니다.

   * _전체 화면_( ![전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg)) 아이콘을 클릭하여 _[!UICONTROL 랜딩 페이지 생성]_ 대화 상자를 엽니다

   * 필요한 경우 [개선 작업](#refine-a-variation)을 사용하여 변형을 미세 조정하여 정확한 요구 사항을 충족하도록 합니다.

   * [생성된 변형에 대한 피드백을 제출](#submit-variation-feedback)하려면 _엄지손가락 위로_, _엄지손가락 아래로_ 또는 _플래그_ 아이콘을 클릭하고 피드백을 가장 잘 요약하는 이유를 선택하세요.

1. 템플릿 콘텐츠를 선택한 변형으로 바꾸고 랜딩 페이지 디자인 공간으로 돌아가려면 **[!UICONTROL 선택]**&#x200B;을 클릭합니다.

   캔버스에서 편집 및 서식 도구를 사용하여 생성된 콘텐츠와 오른쪽의 _[!UICONTROL 설정]_ 및 _[!UICONTROL 스타일]_ 옵션을 변경할 수 있습니다.

>[!TAB 텍스트만]

다음 단계에 따라 AI Assistant를 사용하여 기존 랜딩 페이지에 대한 텍스트 콘텐츠를 세분화하거나 강화합니다.

1. 랜딩 페이지 디자인 공간에서 특정 콘텐츠를 타깃팅할 _텍스트_ 구성 요소를 선택합니다.

1. 오른쪽 패널의 바깥쪽 레일에서 _AI Assistant_(![AI Assistant for content toggle](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) 아이콘을 선택합니다.

   ![랜딩 페이지 디자인 공간에서 AI 길잡이 전환](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   오른쪽의 설정은 텍스트 구성 요소에 대한 콘텐츠 생성 설정을 반영합니다.

1. (Beta) **[!UICONTROL 브랜드]**&#x200B;를 선택하여 AI 생성 콘텐츠가 브랜드 사양에 맞게 조정되도록 합니다.

   게시된 브랜드가 없으면 **[!UICONTROL 브랜드 만들기]**&#x200B;를 클릭하여 [재사용 가능한 브랜드 지침을 정의](./brands-overview.md)하세요.

1. **[!UICONTROL 프롬프트]** 필드에 생성할 내용에 대한 설명을 입력합니다.

   ![AI 길잡이 - 텍스트 설정](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   효과적인 프롬프트를 만드는 데 도움이 필요하면 [프롬프트 라이브러리](#prompt-library)를 사용하십시오.

1. 생성된 콘텐츠를 사용자 지정하려면 콘텐츠 지침 설정을 완료합니다.

   * [**[!UICONTROL 텍스트 설정]**](#text-settings) - 생성된 텍스트 콘텐츠에 대한 지침을 제공합니다.

   * [**[!UICONTROL 참조 콘텐츠]**](#reference-content) - 콘텐츠 생성의 원본 역할을 하는 콘텐츠 자산을 제공합니다.

1. 프롬프트 및 설정이 준비되면 **[!UICONTROL 생성]**&#x200B;을 클릭합니다.

1. AI 도우미 패널에서 아래로 스크롤하여 생성된 변형을 탐색하여 가장 적합한 변형을 결정합니다.

   * _전체 화면_( ![전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg)) 아이콘을 클릭하여 _[!UICONTROL 텍스트 생성]_ 대화 상자를 엽니다

   * 필요한 경우 [개선 작업](#refine-a-variation)을 사용하여 변형을 미세 조정하여 정확한 요구 사항을 충족하도록 합니다.

   * [생성된 변형에 대한 피드백을 제출](#submit-variation-feedback)하려면 _엄지손가락 위로_, _엄지손가락 아래로_ 또는 _플래그_ 아이콘을 클릭하고 피드백을 가장 잘 요약하는 이유를 선택하세요.

1. 원하는 컨텐츠가 있으면 **[!UICONTROL 선택]**&#x200B;을 클릭하여 텍스트를 선택한 변형으로 바꾸고 랜딩 페이지 디자인 공간으로 돌아갑니다.

   캔버스에서 편집 및 서식 도구를 사용하여 텍스트를 변경할 수 있으며 오른쪽의 _[!UICONTROL 설정]_ 및 _[!UICONTROL 스타일]_ 옵션도 변경할 수 있습니다.

>[!TAB 이미지만]

다음 단계에 따라 AI Assistant를 사용하여 기존 랜딩 페이지에 대한 이미지 콘텐츠를 개선하거나 강화합니다.

1. 랜딩 페이지 디자인 공간에서 특정 콘텐츠를 타깃팅할 _이미지_ 구성 요소를 선택합니다.

1. 오른쪽 패널의 바깥쪽 레일에서 _AI Assistant_(![AI Assistant for content toggle](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) 아이콘을 선택합니다.

   ![랜딩 페이지 디자인 공간에서 AI 길잡이 전환](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   오른쪽의 AI Assistant 설정은 이미지 구성 요소에 대한 생성 설정을 반영합니다.

1. (Beta) **[!UICONTROL 브랜드]**&#x200B;를 선택하여 AI 생성 콘텐츠가 브랜드 사양에 맞게 조정되도록 합니다.

   게시된 브랜드가 없으면 **[!UICONTROL 브랜드 만들기]**&#x200B;를 클릭하여 [재사용 가능한 브랜드 지침을 정의](./brands-overview.md)하세요.

1. **[!UICONTROL 프롬프트]** 필드에 원하는 내용에 대한 설명을 입력하십시오.

   ![AI 길잡이 - 텍스트 설정](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   효과적인 프롬프트를 만드는 데 도움이 필요하면 [프롬프트 라이브러리](#prompt-library)를 사용하십시오.

1. 생성된 콘텐츠를 사용자 지정하려면 콘텐츠 지침 설정을 완료합니다.

   * [**[!UICONTROL 이미지 설정]**](#image-settings) - 생성된 콘텐츠에 이미지를 포함하려면 이미지 생성을 활성화하고 지침을 제공하십시오.

   * [**[!UICONTROL 참조 콘텐츠]**](#reference-content) - 콘텐츠 생성의 원본 역할을 하는 콘텐츠 자산을 제공합니다.

1. 프롬프트 및 설정이 만족스러우면 **[!UICONTROL 생성]**&#x200B;을 클릭하세요.

   AI Assistant는 요청을 처리하고 프롬프트 및 기타 입력을 기반으로 가장 적합한 이미지를 생성합니다.

   >[!IMPORTANT]
   >
   >참조 콘텐츠에 이미지가 없거나 입력 프롬프트와 관련된 이미지가 없는 경우 출력이 비어 있습니다.

1. 생성된 변형을 찾아보거나 _전체 화면_( ![전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg)) 아이콘을 클릭하여 _[!UICONTROL 이미지 생성]_ 대화 상자를 엽니다.

   이 대화 상자에서는 변형을 비교하고, 이미지 및 참조 콘텐츠 설정(필요한 경우)을 조정하고, 변형을 재생성할 수 있는 추가 공간을 제공합니다.

   변형을 선택하고 **[!UICONTROL 비슷하게 생성]**&#x200B;을 클릭하여 선택한 변형과 유사한 추가 이미지를 생성할 수 있습니다. 또는 **[!UICONTROL Adobe Express에서 편집]**&#x200B;을 클릭하여 이미지를 직접 변경합니다. Adobe Express을 사용하여 이미지를 구체화하는 방법에 대한 자세한 내용은 [Adobe Express의 빠른 작업](./image-edit-adobe-express.md#quick-actions-in-adobe-express)을 참조하십시오.

   ![텍스트 변형 및 세분화 옵션의 AI Assistant 미리 보기](./assets/email-designer-ai-assistant-image-refine.png){width="700" zoomable="yes"}

   생성된 변형에 대해 [피드백을 제출](#submit-variation-feedback)할 수도 있습니다.

1. 원하는 이미지를 강조 표시하고 **[!UICONTROL 선택]**&#x200B;을 클릭하여 이미지 또는 자리 표시자를 선택한 항목으로 바꾸고 랜딩 페이지 디자인 공간으로 돌아갑니다.

   캔버스에서 편집 및 서식 도구를 사용하여 이미지를 변경할 수 있으며 오른쪽의 _[!UICONTROL 설정]_ 및 _[!UICONTROL 스타일]_ 옵션도 변경할 수 있습니다.

>[!ENDTABS]

## 미리 보기 및 콘텐츠 개선 {#refine-finalize}

콘텐츠 변형을 생성한 후 결과를 미세 조정하여 정확한 요구 사항을 충족할 수 있습니다. 브랜드 정렬을 검토하고, 색조와 언어를 조정하고, 내용을 미리 볼 수 있도록 준비합니다. 또한 AI Assistant를 교육하고 향후 출력을 개선하는 데 도움이 되는 변형에 대한 피드백을 제출할 수 있습니다.

### 전체 화면 보기 열기

1. 초기 콘텐츠 생성 후 **[!UICONTROL 변형]**&#x200B;을 살펴보십시오.

1. 목표에 가장 일치하는 변형을 식별하고 _전체 화면_(![전체 화면 아이콘](../assets/do-not-localize/icon-full-screen.svg)) 아이콘을 클릭하여 대화 상자를 엽니다.

   ![생성 대화 상자에 액세스](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. 선택한 변형이 만족스러우면 **[!UICONTROL 선택]**&#x200B;을 클릭하여 캔버스에 적용합니다.

### 변형 세분화

랜딩 페이지 및 텍스트 변형에 대한 추가 사용자 지정 기능에 액세스하려면 **[!UICONTROL 세분화]** 옵션을 클릭하십시오.

* **[!UICONTROL 자세히]** - AI Assistant를 통해 특정 주제를 확장하고 더 나은 이해와 참여를 위해 추가 세부 정보를 제공할 수 있습니다.

* **[!UICONTROL 요약]** - 정보가 길면 페이지 뷰어가 오버로드될 수 있습니다. AI Assistant를 사용하여 주요 사항을 명확하고 간결한 요약으로 요약하여 주목 받고 더 자세히 읽을 수 있도록 장려합니다.

* **[!UICONTROL 구문 변경]** - 의미를 유지하면서 메시지를 다시 작성합니다. 이 옵션은 핵심 메시지를 변경하지 않고 대체 단어를 생성하거나, 흐름을 개선하거나, 구문 조정을 하는 데 도움이 됩니다.

* **[!UICONTROL 더 간단한 언어 사용]** - 언어를 단순화하여 더 많은 대상자가 명확하고 쉽게 사용할 수 있도록 합니다.

* **[!UICONTROL 번역]** - 텍스트를 다른 언어로 번역합니다. (현재 지원되는 언어는 영어뿐입니다.)

* **[!UICONTROL 색조 변경]** - 메시지 색조를 조정하여 친숙하거나, 전문적이거나, 긴급하거나, 영감을 주는 등 사용자의 커뮤니케이션 스타일에 맞게 조정하십시오.

* **[!UICONTROL 통신 전략 변경]** - 긴급성을 만들거나 흥미로운 어필을 강조하는 등 목표에 따라 메시징 접근 방식을 수정합니다.

<!-- * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![콘텐츠 세분화 옵션을 표시하는 메뉴 세분화](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### 변형 피드백 제출

_엄지손가락 위로_, _엄지손가락 아래로_ 또는 _플래그_ 아이콘을 클릭하여 생성된 변형에 대한 피드백을 제공하고 피드백을 가장 잘 요약하는 이유를 선택하세요.

![AI 길잡이 - 생성된 변형 미리 보기](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### 브랜드 정렬 확인(Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

브랜드 정렬 평가 및 채점을 통해 캠페인 전반에서 톤, 메시징 및 시각적 정체성의 일관성을 보장함은 물론 콘텐츠가 라이브로 전환되기 전에 품질을 확인하는 역할을 할 수 있습니다. 랜딩 페이지 콘텐츠가 완료되면 오른쪽의 _브랜드 정렬_( ![브랜드 정렬 아이콘](../assets/do-not-localize/icon-brand-compliance.svg)) 아이콘을 클릭하여 랜딩 페이지 디자인 공간에서 _브랜드 정렬_ 오른쪽 패널을 엽니다.

![브랜드 정렬 도구 액세스](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

자세한 내용은 [브랜드 정렬 확인](./brand-alignment.md#validate-your-brand-alignment)을 참조하세요.
