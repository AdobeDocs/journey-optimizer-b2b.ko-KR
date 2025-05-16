---
title: 이메일 Personalization에 대한 사용자 지정 토큰
description: 계정 여정에 대해 정의된 토큰 세트를 사용하여 이메일 콘텐츠의 개인화를 관리하는 방법을 알아봅니다.
feature: Personalization, Content, Email Authoring
role: User
exl-id: 05d4f446-6348-4555-9c46-316c2857f01d
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# 이메일 개인화를 위한 사용자 지정 토큰

콘텐츠 개인화는 토큰을 콘텐츠 아티팩트가 생성될 때 채워지는 자리 표시자 또는 변수로 사용합니다. 표준 개인화 토큰은 이메일, 랜딩 페이지, 조각 및 템플릿에 사용할 수 있습니다. 계정 여정에 고유한 값을 사용하여 사용자 지정 토큰 세트를 정의할 수도 있습니다. 이 사용자 지정 토큰 집합을 _내 토큰_&#x200B;이라고 하며 이러한 사용자 지정 토큰은 [여정 전자 메일을 작성](./email-authoring.md#content-authoring---personalization)할 때 개인화됩니다.

계정 여정에 해당하는 _내 토큰_ 외에도 전자 메일 개인화에 표준(기본 제공) 토큰을 사용할 수 있습니다.

## 내 토큰 관리 {#my-tokens}

_내 토큰_&#x200B;은(는) 초안 상태의 계정 여정에 대해 만들거나 수정하는 사용자 지정 변수입니다. 이 사용자 지정 토큰 세트는 현재 텍스트 및 숫자 토큰 정의를 지원합니다.

사용자 지정 토큰을 전자 메일에 추가하면 `{{my.TokenName}}`(으)로 표시됩니다. 예를 들어 예정된 웨비나와 관련된 이메일 콘텐츠를 관리하기 위해 만든 토큰이 `{{my.EventDate}}` 또는 `{{my.WebinarSpeaker}}`개일 수 있습니다.

_계정 여정의 사용자 지정 토큰에 액세스하려면:_

1. 초안 계정 여정을 엽니다.

1. 오른쪽 상단의 **[!UICONTROL 자세히..]** 메뉴를 클릭하고 **[!UICONTROL 내 토큰]**&#x200B;을 선택하세요.

   ![오른쪽 상단의 자세히 클릭](../journeys/assets/account-journey-draft-more-menu.png){width="450"}

   _내 토큰_ 페이지에는 여정에 대해 정의된 모든 사용자 지정 토큰이 나열됩니다.

   ![내 토큰](./assets/my-tokens-list-page.png){width="700" zoomable="yes"}

### 토큰 만들기

1. _[!UICONTROL 내 토큰]_ 페이지에서 **[!UICONTROL 만들기]**&#x200B;를 클릭하고 정의할 토큰 형식을 선택하십시오.

   * **[!UICONTROL 텍스트]** - 이 형식을 사용하여 기본 텍스트 문자열 값으로 토큰을 정의합니다.

   * **[!UICONTROL 숫자]** - 이 형식을 사용하여 숫자 값으로 토큰을 정의합니다.

1. 대화 상자에서 토큰의 **[!UICONTROL 이름]** 및 **[!UICONTROL 값]**&#x200B;을(를) 입력하십시오.

   ![텍스트 토큰의 이름과 값을 입력하십시오](./assets/my-tokens-create-text-token-dialog.png){width="400"}

   토큰 이름에는 공백이나 특수 문자를 사용할 수 없습니다. `EventType`과(와) 같은 _카멜 대/소문자_&#x200B;을(를) 사용하여 쉽게 식별할 수 있는 여러 단어 이름을 사용할 수 있습니다.

   _숫자_ 토큰을 정의하는 경우 값에는 숫자만 사용할 수 있습니다. 십진수 값을 사용할 수 있습니다.

   ![숫자 토큰의 이름과 값을 입력하십시오](./assets/my-tokens-create-number-token-dialog.png){width="400"}

1. **[!UICONTROL 추가를 클릭합니다]**.

### 토큰 편집

계정 여정이 초안 상태로 있는 동안 정의된 내 토큰을 편집할 수 있습니다.

1. _[!UICONTROL 내 토큰]_ 페이지에서 토큰 이름 옆에 있는 _추가 작업_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.

   ![토큰 추가 작업 메뉴](./assets/my-tokens-more-actions.png){width="430"}

1. 대화 상자에서 여정에 필요한 **[!UICONTROL 이름]** 및 **[!UICONTROL 값]**&#x200B;을 변경합니다.

   ![토큰의 이름과 값을 변경합니다](./assets/my-tokens-edit-text-token-dialog.png){width="400"}

1. **[!UICONTROL 편집]**&#x200B;을 클릭합니다.

### 토큰 삭제

_내 토큰_ 목록에서 사용자 지정 토큰을 삭제할 수 있지만 현재 여정 전자 메일 콘텐츠에 사용되고 있지 않은지 확인해야 합니다.

1. _[!UICONTROL 내 토큰]_ 페이지에서 토큰 이름 옆에 있는 _추가 작업_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 삭제]**&#x200B;를 선택합니다.

1. 확인 대화 상자에서 **[!UICONTROL 삭제]**&#x200B;를 클릭합니다.

## 콘텐츠에서 사용자 지정 토큰 사용

계정 여정의 전자 메일 콘텐츠를 작성하는 경우 시각적 디자인 공간에서 개인화 도구를 사용할 때 _내 토큰_ 목록의 토큰을 사용할 수 있습니다.

1. 텍스트 구성 요소를 선택하고 도구 모음에서 _개인화 추가_(![개인화 추가 아이콘](../../assets/do-not-localize/icon-personalization-field.svg) ) 아이콘을 클릭합니다.

   ![개인화 추가 아이콘 클릭](./assets/email-personalize-text.png){width="600"}

   이 작업은 _Personalization 편집_ 대화 상자를 엽니다. 계정 여정에 대해 정의된 사용자 지정 토큰이 있는 경우 대화 상자에 _[!UICONTROL Personalization 토큰]_ 라이브러리의 _[!UICONTROL 내 토큰]_ 폴더가 포함됩니다.

1. **[!UICONTROL 내 토큰]** 폴더를 확장한 다음 **+** 또는 **...**&#x200B;을 클릭하여 사용자 지정 토큰 중 하나를 빈 공간에 추가합니다.

   필요에 따라 정적 텍스트를 추가할 수 있습니다.

   ![내 토큰을 사용하여 개인화된 텍스트 만들기](./assets/personalization-edit-dialog-my-tokens.png){width="700" zoomable="yes"}

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
