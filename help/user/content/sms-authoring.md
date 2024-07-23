---
title: SMS 작성
description: 모바일 장치에서 고객에게 텍스트 메시지(SMS)를 보내는 방법과 SMS 편집기에서 텍스트 형식의 메시지를 개인화하고 미리 보는 방법에 대해 알아봅니다.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e0d9359560f31b3e66f593426c66e64d31044d54
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---

# SMS 작성

Adobe Journey Optimizer B2B 에디션을 사용하여 모바일 디바이스에서 고객에게 문자 메시지(SMS)를 보냅니다. SMS 편집기에서 텍스트 형식의 메시지를 만들고, 개인화하고, 미리 볼 수 있습니다.

## SMS 구성

Adobe Journey Optimizer B2B 에디션은 SMS 서비스 공급자(또는 SMS 게이트웨이 공급자)를 통해 텍스트 메시지를 전송합니다. SMS 메시지를 만들기 전에 관리자 설정에서 서비스 공급자를 구성합니다.

### SMS 게이트웨이 서비스 공급자

Adobe Journey Optimizer B2B 에디션은 현재 텍스트 메시지 서비스를 독립적으로 제공하는 서드파티 공급자와 통합됩니다. 텍스트 메시지에 대해 지원되는 공급자는 Sinch, Twilio 및 Infobip입니다.

Adobe Journey Optimizer B2B 에디션에서 SMS 채널을 구성하기 전에 이러한 공급자 중 하나로 계정을 만들어 API 토큰 및 서비스 ID를 가져와야 합니다. Adobe Journey Optimizer B2B 에디션과 해당 공급자 간의 연결을 구성하는 데 이러한 자격 증명이 필요합니다.

>[!IMPORTANT]
>
>문자 메시지 서비스 사용은 해당 공급자의 추가 약관이 적용됩니다. 타사 솔루션인 Sinch, Twilio 및 Infobip은 통합을 통해 Adobe Journey Optimizer B2B Edition 사용자가 사용할 수 있습니다. Adobe은 서드파티 제품을 제어하지 않으며 책임지지 않습니다. 문자 메시지 서비스(SMS)와 관련된 문제 또는 지원 요청은 공급자에게 문의하십시오.

### 기존 SMS API 구성 확인

>[!NOTE]
>
>설명된 설정은 SMS 관리자 권한이 있는 사용자만 액세스할 수 있습니다.

왼쪽 탐색에서 **[!UICONTROL 관리자]** 섹션을 확장하고 **[!UICONTROL 구성]**&#x200B;을 클릭합니다.

![AMA API 자격 증명 구성에 액세스](./assets/config-sms-api.png){width="800" zoomable="yes"}

이 페이지에는 인스턴스에 사용 가능한 API 구성이 나열됩니다. SMS 서비스 공급자 또는 생성자가 표시된 API 자격 증명을 필터링할 수 있습니다.

![필터 아이콘을 클릭하여 API 자격 증명 목록을 필터링합니다](./assets/config-sms-api-filter.png){width="500"}

### SMS 서비스 공급자에 대한 새 API 자격 증명 만들기

>[!BEGINTABS]

>[!TAB Sinch]

_Adobe Journey Optimizer B2B 에디션을 사용하여 Sinch를 SMS 공급자로 구성하려면:_

1. 왼쪽 탐색에서 **[!UICONTROL 관리자]** 섹션을 확장하고 **[!UICONTROL 구성]**&#x200B;을 클릭합니다.

1. _[!UICONTROL API 자격 증명]_ 목록의 오른쪽 상단에서 **[!UICONTROL 새 API 자격 증명 만들기]**&#x200B;를 클릭합니다.

1. SMS API 자격 증명을 구성합니다.

   ![Sinch SMS API 자격 증명 구성](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS 공급업체]** - SMS 공급자로 `Sinch`을(를) 선택합니다.

   * **[!UICONTROL 이름]** - API 자격 증명의 이름을 입력하십시오.

   * **[!UICONTROL 서비스 ID]** 및 **[!UICONTROL API 토큰]** - Sinch 계정의 API 페이지에 액세스합니다(SMS 탭에서 자격 증명을 찾을 수 있음).

   Sinch 계정의 이 정보를 찾는 방법에 대한 자세한 내용은 [Sinch 개발자 설명서](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)를 참조하십시오.

1. API 자격 증명의 구성 세부 정보가 완료되면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

>[!TAB Twilio]

_Adobe Journey Optimizer B2B 에디션을 사용하여 Twilio를 SMS 공급자로 구성하려면:_

1. 왼쪽 탐색에서 **[!UICONTROL 관리자]** 섹션을 확장하고 **[!UICONTROL 구성]**&#x200B;을 클릭합니다.

1. _[!UICONTROL API 자격 증명]_ 목록의 오른쪽 상단에서 **[!UICONTROL 새 API 자격 증명 만들기]**&#x200B;를 클릭합니다.

1. SMS API 자격 증명을 구성합니다.

   ![Twilio SMS API 자격 증명 구성](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL SMS 공급업체]** - SMS 공급자로 `Twilio`을(를) 선택합니다.

   * **[!UICONTROL 이름]** - API 자격 증명 정의의 이름을 입력하십시오.

   * **[!UICONTROL 계정 SID]** 및 **[!UICONTROL 인증 토큰]** - Twilio 콘솔 대시보드 페이지의 _계정 정보_ 창에 액세스하여 자격 증명을 찾습니다.

   Twilio 계정에 대한 이 정보를 찾는 방법에 대한 자세한 내용은 [Twilio 도움말 센터](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-)를 참조하십시오.

1. API 자격 증명의 구성 세부 정보가 완료되면 페이지 오른쪽 상단의 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

>[!TAB Infobip]

_Adobe Journey Optimizer B2B 에디션을 사용하여 Infobip를 SMS 공급자로 구성하려면:_

1. 왼쪽 탐색에서 **[!UICONTROL 관리자]** 섹션을 확장하고 **[!UICONTROL 구성]**&#x200B;을 클릭합니다.

1. _[!UICONTROL API 자격 증명]_ 목록의 오른쪽 상단에서 **[!UICONTROL 새 API 자격 증명 만들기]**&#x200B;를 클릭합니다.

1. SMS API 자격 증명을 구성합니다.

   ![Infobip SMS API 자격 증명 구성](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL SMS 공급업체]** - SMS 공급자로 `Infobip`을(를) 선택합니다.

   * **[!UICONTROL 이름]** - API 자격 증명 정의의 이름을 입력하십시오.

   * **[!UICONTROL API 기본 URL]** 및 **[!UICONTROL API 키]** - 웹 인터페이스 홈 페이지 또는 Infobip 계정의 API 키 관리 페이지에 액세스하여 자격 증명을 찾을 수 있습니다.

   Infobip 계정에 대한 이 정보를 찾는 방법에 대한 자세한 내용은 [Infobip 설명서](https://www.infobip.com/docs/api/_blank)를 참조하세요.

1. API 자격 증명의 구성 세부 정보가 완료되면 페이지 오른쪽 상단의 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.

>[!ENDTABS]

_[!UICONTROL 제출]_&#x200B;을 클릭하면 자격 증명이 즉시 확인 및 저장되며, _[!UICONTROL API 자격 증명]_ 목록 페이지로 리디렉션됩니다. 제출된 자격 증명이 유효하지 않은 경우 목록 페이지에 오류 메시지가 표시됩니다. 이 경우 구성을 취소하거나 업데이트한 후 다시 제출하도록 선택할 수 있습니다.

## 계정 여정에 SMS 작업 추가

_[!UICONTROL 작업 수행]_ 노드를 추가하고 다음을 수행하면 계정 여정에서 문자 메시지 게재를 설정할 수 있습니다.

1. _[!UICONTROL Action on]_ 대상에 대해 **[!UICONTROL 사람]**&#x200B;을 선택하세요.

1. _[!UICONTROL 사용자에 대한 작업]_&#x200B;에 대해 **[!UICONTROL SMS 보내기]**&#x200B;를 선택하세요.

   ![작업 수행 - sms 보내기](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. _[!UICONTROL 작업 수행]_ 패널 아래쪽에서 **[!UICONTROL SMS 만들기]**&#x200B;를 클릭합니다.

1. 대화 상자에서 전자 메일의 고유한 **[!UICONTROL 이름]**&#x200B;과(와) **[!UICONTROL 제목 줄]**&#x200B;을(를) 입력합니다.

   ![새 SMS 대화 상자 만들기](assets/create-new-sms.png){width="500"}

## SMS 메시지 만들기

>[!IMPORTANT]
>
>**SMS 동의 관리**<br/>
><br/>
>업계 표준 및 규정에 따라 모든 SMS 마케팅 메시지에는 수신자가 간편하게 구독을 취소할 수 있는 방법이 포함되어야 합니다. 이를 위해 SMS 수신자는 옵트인 및 옵트아웃 키워드로 회신할 수 있습니다. 모든 표준 옵트인 및 옵트아웃 키워드가 지원되며 적용됩니다. 또한 SMS 서비스 공급자 계정에 대해 구성된 모든 사용자 지정 키워드가 지원되고 적용됩니다.

1. **[!UICONTROL 메시지]** 필드에 보낼 텍스트를 입력하십시오.

   160자마다 하나의 SMS 메시지로 간주하여 최대 1600자의 메시지를 만들 수 있습니다.

1. **문자 메시지를 개인화합니다**.

   언제든지 텍스트 메시지를 작성하는 동안 텍스트 메시지 상자 오른쪽에 있는 _개인화_ 아이콘을 클릭합니다.

   ![메시지에 토큰을 추가하려면 개인화 아이콘을 클릭합니다](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   표시된 페이지에서는 Adobe Marketo Engage Lead 및 시스템 토큰에 액세스할 수 있습니다. 표준 및 사용자 지정 토큰이 모두 포함됩니다. 검색 창을 사용하여 필요한 토큰을 찾거나 폴더 트리를 탐색하여 리드/시스템 토큰을 찾아 선택할 수 있습니다.

   메시지를 통해 토큰을 추가할 위치에 커서를 놓습니다. 토큰 옆에 있는 더하기(**+**) 기호를 클릭하여 토큰을 추가합니다. 대체 항목이 있는 토큰을 추가하려면(잠재 고객에 대해 해당 필드를 사용할 수 없는 경우 나타나는 기본값) 줄임표(**...** )를 클릭하고 **[!UICONTROL 대체 텍스트를 사용하여 삽입]**&#x200B;을 선택합니다.

   ![토큰에 대한 대체 요소를 사용하려면 생략 부호를 클릭하세요](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   _[!UICONTROL 대체 값 입력]_ 대화 상자에서 대체 값으로 나타나는 텍스트를 입력한 다음 **[!UICONTROL 추가]**&#x200B;를 클릭합니다.

   ![토큰에 대한 대체 텍스트를 입력하십시오](./assets/sms-message-personalize-fallback-text.png){width="400"}

   개인화 토큰이 배치되면 **[!UICONTROL 저장]**&#x200B;을 클릭하여 변경 내용을 저장하고 기본 SMS 작성 작업 영역으로 돌아갑니다. 필요에 따라 토큰으로 메시지를 계속 편집할 수 있습니다.

<!-- 1. **Add URLs to text message**.

   After defining your content, you can add URLs to your message by clicking the _Link_ icon.
   
   You can add two types of URLs: 

   External URLs - This is ANY external URL that can be directly typed into/ pasted into the input text box
   Adobe Marketo Engage Design Studio Landing Pages - Selecting this option, you will see a 'Landing Page picker' from which you can select any of the listed approved Landing Pages from Marketo Engage

   You can choose to 'shorten' either of these URLs by selecting the checkbox
   Note that the URL shortening function, uses the Marketo subdomain for shortening
   The shortened URL appears as a read-only field within the modal
   You can optionally track clicks on the URL
   You can also choose to include 'mkt_tok' for tracking activity against a user
   Click on Add to save changes & add the chosen URL to the SMS message
-->

## SMS 속성 설정

1. _[!UICONTROL SMS 속성]_ 섹션에서 메시지에 대해 **[!UICONTROL 이름]**(필수, 100cha\racter 최대값) 및 **[!UICONTROL 설명]**(선택 사항, 최대 300자)을 입력합니다.

   이러한 필드에는 Alpha, 숫자, 특수 문자가 허용됩니다. 다음 예약 문자는 **허용되지 않음**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` 및 `|`입니다.

1. **[!UICONTROL SMS 유형]** 선택:

   * 사용자 동의가 필요한 홍보용 문자 메시지에 `Marketing`을(를) 사용합니다.
   * 주문 확인, 암호 재설정 알림 또는 게재 정보와 같은 비상업적인 메시지에 `Transactional`을(를) 사용합니다.

1. **[!UICONTROL SMS 구성]**&#x200B;의 경우 미리 정의된 API 구성 중 하나를 선택하십시오.

   이 설정은 메시지를 전달하는 데 사용할 SMS 게이트웨이 서비스 공급자 및 계정을 결정합니다.

1. 통신에 사용할 **[!UICONTROL 발신자 번호]**&#x200B;을(를) 입력하십시오.

   ![작업 수행 - sms 보내기](./assets/sms-properties.png){width="700" zoomable="yes"}

   받는 사람 번호는 항상 Marketo Engage의 `Lead.MainPhone` 필드에 매핑됩니다.

<!-- ## Preview the text message content

When your message content is defined, you can use test profiles to preview its content. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate Content]** at the top of the SMS authoring workspace.

1. From the _[!UICONTROL Simulate Content]_ page, click **[!UICONTROL Add People]**.

1. Use the # page to manage the leads used for your test profile.

   In the displayed list, you can search for and add any of the leads (up to 10 leads at a time) from the Marketo Engage lead database.

   To search, enter the whole email address and click enter. The corresponding lead profile shows up for selection.

   The preview updated to the personalization fields for the selected profile.

   All the added leads appear on the left rail of the 'Simulate Content' page

   You can manage this list by adding more people and deleting individual leads from the profile listing (it does not remove them from the database).

1. Simulate content for a lead.

   Select any of the leads listed on the left rail of the Simulate Content page and the SMS preview on the page updates for the corresponding lead.

   You can also select a lead from the 'drop-down' box above the preview space and the SMS preview on the page updates for the corresponding lead

1. To exit the _[!UICONTROL Simulate Content]_ page and return back to the SMS authoring workspace, click Close. -->
