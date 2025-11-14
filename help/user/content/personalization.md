---
title: 콘텐츠 개인화
description: Journey Optimizer B2B edition에서 계정, 사용자 및 시스템 토큰을 사용하여 B2B 이메일을 개인화합니다. 개인화 편집기 및 구문을 사용하는 방법을 알아봅니다.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: 표현식, 편집기, 시작, 개인화
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# 콘텐츠 개인화 {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="콘텐츠 경험 개인화"
>abstract="**Adobe Journey Optimizer B2B edition**&#x200B;을(를) 사용하여 받는 사람에 대한 데이터와 정보를 활용하여 각 받는 사람에게 메시지를 적용하세요. 이름, 업종, 직함 등이 될 수 있습니다."

[!DNL Adobe Journey Optimizer B2B Edition] 개인화 기능을 사용하면 보유한 데이터 및 정보를 활용하여 전자 메일 메시지를 각 특정 받는 사람에게 적용할 수 있습니다. 이름, 업종, 직함 등이 될 수 있습니다.

_개인화 편집기_&#x200B;를 사용하면 모든 데이터를 선택하고, 정렬하고, 사용자 지정하고, 유효성을 검사하여 콘텐츠에 대한 사용자 지정된 개인화를 만들 수 있습니다. 도우미 함수와 같은 다양한 도구를 사용하여 메시지를 사용자 지정할 수 있습니다. 편집기에서 _Handlebars_&#x200B;을(를) 기반으로 하는 인라인 개인화 구문을 사용합니다. 여기서 식은 중괄호 `{{}}`로 묶은 내용으로 구성됩니다.

메시지를 처리할 때 Journey Optimizer B2B edition은 표현식을 Adobe Experience Platform 데이터 세트 및 로컬 시스템 값에 포함된 데이터로 대체합니다. 예를 들어 `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`은(는) 동적으로 `Hello John Doe`이(가) 됩니다.

이 구문을 사용하면 이메일 제목 줄, 메시지 본문 및 발신자 정보를 포함하여 여러 필드에 메시지를 개인화할 수 있습니다.

## Personalization 토큰

[!DNL Journey Optimizer B2B Edition]에서 개인화 토큰을 사용하여 동적 전자 메일 콘텐츠를 만들 수 있습니다.

* **계정 토큰** - 이러한 토큰은 _계정 이름_, _업계_ 및 _직원 수_&#x200B;와 같은 계정 특성을 기반으로 합니다. 이러한 토큰을 사용하여 Adobe Experience Platform에 정의된 **_XDM 비즈니스 계정 세부 사항_** 스키마에서 관리하는 특성 데이터를 채우십시오.

* **개인 토큰** - 이러한 토큰은 _이름_, _직책_ 및 _회사 이름_&#x200B;과 같은 비즈니스 사용자 특성을 기반으로 합니다. 이러한 토큰을 사용하여 Adobe Experience Platform에 정의된 **_XDM 비즈니스 사용자 세부 사항_** 스키마에서 관리하는 특성 데이터를 채우십시오.

* **시스템 토큰** - 이러한 토큰은 시스템 필드 값(예: _date_, _time_, _구독 취소 링크_)을 기반으로 합니다.

* **내 토큰**(여정에 대해 정의된 경우) - 이메일이 있는 여정에 대해 정의된 [사용자 지정 토큰](./personalization-my-tokens.md).

>[!NOTE]
>
>[XDM(Adobe Experience Platform 데이터 모델) 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home){target="_blank"}에서 XDM 스키마에 대해 자세히 알아보세요.

## Personalization 편집기

개인화 편집기는 이메일 콘텐츠에서 개인화를 정의해야 하는 모든 컨텍스트에서 사용할 수 있습니다. 편집기에서 모든 데이터를 선택하고, 정렬하고, 맞춤화하고, 유효성을 검사하여 콘텐츠에 대한 사용자 지정 개인 맞춤화를 만들 수 있습니다.

>[!NOTE]
>
>개인화 편집기에 대한 다음 정보는 [간소화된 아키텍처](../simplified-architecture.md)에서 프로비저닝된 Journey Optimizer B2B edition 환경에서 사용할 수 있는 변경 사항을 반영합니다.

_개인화 추가_( ![개인화 추가 아이콘](../../assets/do-not-localize/icon-personalization-field.svg) ) 아이콘을 클릭하여 필드 또는 콘텐츠 구성 요소에 개인화를 추가합니다.

![Personalization 편집기](./assets/personalization-editor.png){width="800" zoomable="yes"}

개인화 토큰 또는 도우미 함수를 사용하려면 왼쪽 탐색 창에서 찾은 다음 **+**&#x200B;을(를) 클릭하여 식에 추가하십시오.

각 특성에 대한 자세한 내용을 보고 _즐겨찾기_&#x200B;에 자주 사용하는 특성을 추가하려면 **추가 메뉴**( _..._) 아이콘( **추가**( _+_) 옆)을 클릭하십시오. 즐겨찾기에 추가된 특성은 편집기의 왼쪽 탐색 영역에 있는 **[!UICONTROL 즐겨찾기]** 메뉴에서 액세스할 수 있습니다.

![Personalization 편집기 - 토큰 추가 메뉴](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
문자열 유형 프로필 속성이 비어 있는 경우 표시되는 기본 대체 텍스트 문자열을 정의할 수도 있습니다. 특성에 대한 _추가 메뉴_( **...**) 아이콘을 클릭하고 **[!UICONTROL 대체 텍스트로 삽입]**&#x200B;을 선택합니다. 프로필에 대해 특성 값이 비어 있을 때 표시할 텍스트를 입력한 다음 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

표현식을 콘텐츠에 삽입하기 전에 유효성을 검사하는 것이 좋습니다. 편집기 하단의 **[!UICONTROL 유효성 검사]**&#x200B;를 클릭하여 구문을 확인하고 오류가 없는지 확인합니다.

![Personalization 편집기에서 코드를 확인했습니다](./assets/personalization-editor-validated.png){width="500"}

식이 완료되어 오류가 없으면 **[!UICONTROL 저장]**&#x200B;을 클릭하세요.

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/en/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12) -->