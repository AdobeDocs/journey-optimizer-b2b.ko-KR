---
title: 웹 채널 구성
description: Journey Optimizer B2B edition에서 컨텐츠 전달에 대한 웹 속성 및 페이지 일치 규칙을 정의하기 위해 웹 채널 설정을 구성하는 방법에 대해 알아봅니다.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="이 기능은 현재 제한된 베타 릴리스에 있습니다"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# 웹 채널 구성

웹 구성은 콘텐츠가 전달되는 URL로 식별되는 웹 속성입니다. 웹 경험이 하나 또는 여러 웹 페이지에서 수정 사항을 전달할 수 있도록 단일 페이지 URL 또는 여러 페이지를 일치시킬 수 있습니다. 이러한 구성은 마케터가 [여정에 웹 개인화 작업 노드를 추가](../content/web-experiences.md#create-a-web-experience)하고 [캠페인에 대한 경험 수정 사항을 디자인](../content/web-experience-design.md)하는 데 필요합니다.

>[!BEGINSHADEBOX]

**전제 조건**

웹 채널을 사용하려면 웹 사이트에 방문자 식별 및 컨텐츠 전달을 위해 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/js/js-overview)&#x200B;(`alloy.js`)이 구현되어 있어야 합니다. Adobe Experience Platform Web SDK 버전이 2.16 이상인지 확인하십시오.

Journey Optimizer B2B edition의 웹 채널을 구성하려면 다음 [권한](../admin/user-management.md#b2b-product-permissions)이 필요합니다.

* _[!UICONTROL 채널 구성]_ > _[!UICONTROL 메시지 사전 설정 관리]_ - 웹 채널 구성을 만들고 업데이트하고 삭제하는 데 필요합니다.
* _[!UICONTROL 채널 구성]_ > _[!UICONTROL 메시지 사전 설정 보기]_ - 웹 채널 구성을 보는 데 필요합니다.

>[!ENDSHADEBOX]

## 웹 채널 구성 만들기

1. 왼쪽 탐색에서 **[!UICONTROL 관리]** > **[!UICONTROL 채널]**(으)로 이동합니다.

1. 탐색 패널의 _[!UICONTROL 웹]_&#x200B;에서 **[!UICONTROL 채널 구성]**&#x200B;을 선택합니다.

   ![웹 채널 구성에 액세스](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. 오른쪽 상단의 **[!UICONTROL 채널 구성 만들기]**&#x200B;를 클릭합니다.

1. 구성에 대해 **[!UICONTROL 이름]**(필수)과 **[!UICONTROL 설명]**(선택 사항)을 입력하십시오.

   >[!NOTE]
   >
   >이름은 문자(A-Z)로 시작해야 하며 영숫자만 포함할 수 있습니다. 밑줄 `_`, 점 `.` 및 하이픈 `-`자를 사용할 수도 있습니다.

1. **[!UICONTROL 웹 설정]** 섹션에서 다음 옵션 중 하나를 선택합니다.

   * **[!UICONTROL 단일 페이지]** - 변경 내용을 단일 페이지에만 적용하려면 **[!UICONTROL 페이지 URL]**&#x200B;을 입력하거나 선택하십시오.

     ![단일 페이지 웹 채널 구성에 대한 페이지 URL 선택](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL 페이지 일치 규칙]** - 동일한 규칙과 일치하는 여러 URL을 타겟팅하려면 [페이지 일치 규칙을 빌드](#build-a-pages-matching-rule)하고 **[!UICONTROL 기본 작성 및 미리 보기 URL]**&#x200B;을(를) 입력하십시오.

1. 변경 내용을 저장하려면 **[!UICONTROL 제출]**&#x200B;을 클릭하세요.

구성을 저장하면 _초안_ 상태가 되며 마케터는 여정에서 웹 채널을 사용할 때 사용할 수 있습니다. 초안 상태가 지속되는 한 구성을 계속 편집할 수 있습니다. 이름 옆에 있는 _자세히_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 삭제]**&#x200B;를 선택하여 초안 웹 채널 구성을 삭제할 수도 있습니다.

웹 채널은 여정에서 사용되는 즉시 _Active_ 상태로 이동합니다. 이 상태에서는 구성의 이름 및 설명을 편집할 수 있습니다. 웹 설정을 변경하거나 구성을 삭제할 수 없습니다.

## 페이지 일치 규칙 {#pages-matching-rule}

웹 구성을 만들 때 동일한 규칙과 일치하는 여러 URL을 대상으로 _[!UICONTROL 페이지 일치 규칙]_&#x200B;을(를) 만들 수 있습니다. 이러한 규칙을 사용하면 여러 페이지에 동일한 콘텐츠 변경 사항을 적용할 수 있습니다.

예를 들어 전체 웹 사이트에서 영웅 배너에 변경 사항을 적용하거나 모든 제품 페이지에 표시되는 상위 이미지를 추가할 수 있습니다.

### 규칙 작성

1. [웹 채널 구성을 만들](#create-a-web-channel-configuration)때 **[!UICONTROL 페이지 일치 규칙]**&#x200B;을 선택하세요.

1. 규칙을 만들려면 각 섹션에서 다른 연산자를 사용하여 **[!UICONTROL 도메인]** 및 **[!UICONTROL 페이지]** 필드에 대한 조건을 정의하십시오.

   +++도메인 연산자

   입력한 문자열 값에 따라 도메인을 일치시키려면 다음 연산자를 사용하십시오.

   | 연산자 | 설명 | 예 |
   | --- | --- | --- |
   | [!UICONTROL 같음] | 도메인의 정확한 일치 | |
   | [!UICONTROL 다음으로 시작] | 입력한 문자열로 시작하는 모든 도메인(하위 도메인 포함)과 일치합니다. | `Starts with: dev`은(는) `dev`, `dev.example.com`, `dev.products.example.com` 등 `developer.example.com`(으)로 시작하는 모든 도메인 및 하위 도메인과 일치합니다. |
   | [!UICONTROL 다음으로 끝남] | 입력한 문자열로 끝나는 모든 도메인(하위 도메인 포함)과 일치합니다. | `Ends with: example.com`은(는) `example.com`, `stage.example.com`, `prod.example.com` 등 `myexample.com`(으)로 끝나는 모든 도메인 및 하위 도메인과 일치합니다. |
   | [!UICONTROL 와일드카드 일치] | 문자열 가운데 와일드카드 일치(예: `dev.*.example.com`)를 정의할 수 있습니다. 연산자가 _와일드카드 일치_&#x200B;인 경우 유효성 검사 규칙에서는 값에 와일드카드(별표)를 하나만 포함해야 합니다. | `Wildcard matching: dev.*.example.com`이(가) `dev.products.example.com`, `dev.mytest.products.example.com`, `dev.blog.example.com` 등의 도메인과 일치합니다. |
   | [!UICONTROL 모두] | 모든 도메인과 일치합니다. 도메인 간 특정 경로를 테스트할 때 유용합니다. | |

   +++

   +++경로 연산자

   입력한 문자열 값에 따라 경로를 일치시키려면 다음 연산자를 사용하십시오.

   | 연산자 | 설명 | 예 |
   | --- | --- | --- |
   | [!UICONTROL 같음] | 경로의 정확한 일치. | |
   | [!UICONTROL 다음으로 시작] | 문자열로 시작하는 모든 경로(하위 경로 포함)와 일치합니다. | |
   | [!UICONTROL 다음으로 끝남] | 문자열로 끝나는 모든 경로(하위 경로 포함)와 일치합니다. | |
   | [!UICONTROL 모두] | 모든 경로와 일치 이 기능은 하나 또는 여러 도메인 아래의 모든 경로를 타겟팅할 때 유용합니다. | |
   | [!UICONTROL 와일드카드 일치] | 경로 내부에 `/products/*/detail`과(와) 같은 내부 와일드카드를 정의할 수 있습니다. 경로 구성 요소의 와일드카드 문자 `*`이(가) 첫 번째 `/` 문자까지 문자 시퀀스와 일치합니다.  `/*/`은(는) 모든 문자 시퀀스(하위 경로 포함)와 일치합니다. | `Wildcard matching: /products/*/detail`이(가) `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail`, `example.com/products/yoga/pants/detail` 등의 경로와 일치합니다. |
   | [!UICONTROL 포함] | 값은 `*mystring*`과(와) 같은 와일드카드로 변환되며 문자 시퀀스를 포함하는 모든 경로와 일치합니다. | `Contains: product`은(는) `product`, `example.com/products`, `example.com/yoga/perfproduct` 및 `example.com/surf/productdescription`과(와) 같이 문자열 `example.com/home/product/page`을(를) 포함하는 모든 경로와 일치합니다. |

   +++

   예를 들어, _Bodea_ 웹 사이트의 모든 _LumaSecure_ 솔루션 페이지에서 콘텐츠 변경을 지원하려면 **[!UICONTROL 도메인]** > **[!UICONTROL 다음으로 시작]** > `bodea` 및 **[!UICONTROL 페이지]** > **[!UICONTROL 포함]** > `lumasecure`을(를) 선택합니다.

   ![웹 채널 구성에 대한 페이지 일치 규칙 정의](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. 사용 사례에 여러 규칙이 필요한 경우 **[!UICONTROL 다른 페이지 규칙 추가]**&#x200B;를 클릭하고 이전 단계를 반복합니다.

   * 최대 10개의 규칙을 정의할 수 있습니다.

   * 다른 규칙 사이에 **[!UICONTROL Or]** 또는 **[!UICONTROL Exclude]** 연산자를 사용하십시오.

     _[!UICONTROL Or]_&#x200B;은(는) 여러 규칙을 정의하는 기본 연산자이며 일치시킬 수 있는 여러 기준 정의를 추가하는 데 유용합니다.

     _[!UICONTROL Exclude]_&#x200B;은(는) 정의된 규칙과 일치하는 페이지 중 하나를 타깃팅해서는 안 되는 경우에 유용합니다. 예를 들어 `bodea.com`이(가) 들어 있지만 블로그 페이지(예: `lumasecure`)를 제외한 모든 `bodea.com/blogs/lumasecure/latest-release` 페이지를 대상으로 지정할 수 있습니다.

   ![제외가 있는 규칙과 일치하는 페이지](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. **[!UICONTROL 기본 작성 및 미리 보기 URL]**&#x200B;을(를) 입력하십시오.

   이 단계에서는 규칙을 통해 생성되거나 일치된 페이지에 웹 경험 콘텐츠 디자인 및 미리보기 목적을 위해 지정된 URL이 있는지 확인합니다.

## 웹 채널 복제

기존 웹 채널 구성을 복제한 다음 변경하여 기존 웹 채널을 기반으로 새 웹 채널을 만들 수 있습니다. 라이브러리에 저장된 활성 웹 채널 구성은 수정할 수 없습니다.

1. 변형에 대한 _추가 메뉴_ 아이콘(**...**)을 클릭하고 **[!UICONTROL 복제]**&#x200B;를 선택합니다.

   ![기존 웹 채널 구성을 복제하려면 [더 보기] 아이콘을 클릭하세요](./assets/config-web-channels-more-menu.png){width="450"}

   이 작업을 수행하면 이름에 `_Copy_nnn`이(가) 추가된 중복 웹 채널이 만들어집니다.

1. 매개변수를 편집하려면 복제된 웹 채널의 이름을 누릅니다.

   * 규칙의 목적 또는 항목과 일치하도록 이름 및 설명을 변경합니다.
   * 필요한 경우 단일 페이지 URL을 변경합니다.
   * 필요한 경우 요구 사항에 따라 페이지 일치 규칙을 변경합니다.

1. 구성이 완료되면 **[!UICONTROL 제출]**&#x200B;을 클릭합니다.
