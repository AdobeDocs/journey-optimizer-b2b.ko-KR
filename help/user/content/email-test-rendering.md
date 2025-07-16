---
title: 이메일 렌더링 테스트
description: Litmus 계정을 활용하여 Journey Optimizer B2B edition에서 이메일에 대한 렌더링을 테스트하는 방법을 알아봅니다.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
source-git-commit: dbb1c0d57f3d0b9818dc284047bda9562cfb40f6
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Litmus를 사용하여 이메일 렌더링 테스트

이메일을 테스트하려면 Journey Optimizer B2B edition의 [Litmus](https://www.litmus.com/email-testing){target="_blank"} Enterprise 계정을 활용할 수 있습니다. 이 통합을 통해 인기 있는 이메일 클라이언트에서 이메일 렌더링을 미리 볼 수 있습니다. 이 도구를 사용하면 이메일 콘텐츠가 멋진 것처럼 보이고 모든 받은 편지함에서 디자인된 대로 작동하는지 확인할 수 있습니다.

>[!NOTE]
>
>이 통합은 Litmus Enterprise 계정에만 사용할 수 있습니다. 자세한 내용은 Litmus 웹 사이트의 [솔루션 페이지](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}를 참조하세요.

1. 이메일 디자인이 완료되어 테스트할 준비가 되면 이메일 디자인 공간에서 **[!UICONTROL 콘텐츠 시뮬레이션]**&#x200B;을 클릭합니다.

1. 오른쪽 상단의 **[!UICONTROL 전자 메일 렌더링]**&#x200B;을 클릭합니다.

   ![전자 메일 렌더링 단추](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Journey Optimizer B2B edition에서 아직 Litmus 계정에 연결하지 않은 경우 표시된 페이지에서 체험판 계정을 시작하거나 기존 계정에 연결할 수 있는 옵션을 제공합니다.

1. 오른쪽 상단의 **[!UICONTROL Litmus 계정 연결]**&#x200B;을 클릭하거나 페이지 내부의 링크를 사용하십시오.

   ![Litmus 계정 연결](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Litmus 계정 자격 증명을 입력하고 **[!UICONTROL 로그인]**&#x200B;을 클릭합니다.

1. **[!UICONTROL 연결]**&#x200B;을 클릭하여 Litmus와 Journey Optimizer B2B edition 간의 연결을 확인하고 렌더링할 전자 메일 콘텐츠를 보냅니다.

   >[!IMPORTANT]
   >
   >Litmus 계정을 Journey Optimizer B2B edition과 연결하면 테스트 메시지가 Litmus로 전송되는 데 동의하는 것입니다. 그런 다음 이 콘텐츠는 Adobe이 아닌 Litmus 내에서 관리됩니다. 따라서 테스트 메시지에 포함할 수 있는 개인화 데이터를 포함하여 이러한 이메일에 Litmus 데이터 보존 이메일 정책이 적용됩니다.

1. 전자 메일 미리 보기를 생성하려면 오른쪽 상단의 **[!UICONTROL 테스트 실행]**&#x200B;을 클릭하세요.

   ![리트머스 렌더링 테스트 실행](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. 인기 있는 데스크탑, 모바일 및 웹 기반 클라이언트에서 이메일 콘텐츠를 확인합니다.

   렌더링된 클라이언트 테스트에 대한 세부 정보를 보려면 표시된 썸네일을 클릭합니다.

   ![리트머스 이메일 미리 보기](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. 검토를 마치면 왼쪽 상단의 뒤로 화살표(![필터 표시 또는 숨기기 아이콘](../../assets/do-not-localize/icon_back-arrow.svg))를 클릭하여 콘텐츠 시뮬레이트 페이지로 돌아갑니다.

   다른 프로필을 선택하고 다른 렌더링 테스트를 수행하거나 이메일 디자인 공간으로 돌아가 검토를 기반으로 필요한 조정을 수행할 수 있습니다.
