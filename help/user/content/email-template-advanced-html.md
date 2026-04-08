---
title: 이메일 템플릿 디자인을 위한 고급 HTML 모드
description: 고급 HTML 모드를 사용하여 Journey Optimizer B2B edition의 이메일 디자인 공간에서 이메일 템플릿 컨텐츠의 원시 HTML 소스를 직접 보고 편집할 수 있습니다.
feature: Email Authoring, Templates, Content Design Tools
level: Experienced
role: User
source-git-commit: 95dba963e08125370f998cf3960d51ede94c2fb9
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# 이메일 템플릿 디자인을 위한 고급 HTML 모드

_고급 HTML 모드_&#x200B;에서는 숙련된 사용자가 전자 메일 템플릿 콘텐츠의 원시 소스 코드를 직접 보고 편집할 수 있는 보기를 제공합니다. 이 모드는 조건부 논리와 같은 복잡한 표현식을 소스에 직접 삽입하려는 경우에 이상적입니다. 또한 시각적 디자인 도구가 노출하는 것을 초과하는 구조적 조정을 수행하는 데에도 유용합니다.

<!-- We don't have the code editor at this point 
>[!NOTE]
>
>_Advanced HTML mode_ is different from the code editor option that is available when you start a new design. The code editor does not allow you to change to the visual design space. With _advanced HTML mode_, you can toggle back and forth between the HTML source view and the visual design view at any time. -->

>[!AVAILABILITY]
>
>이 기능은 현재 _제한된 가용성_&#x200B;에 있으며 모든 사용자가 사용할 수 없습니다.

## 중요한 제한 사항

[전자 메일 템플릿 작성](./email-template-authoring.md)에 고급 HTML 모드를 사용하기 전에 다음 제한 사항을 이해해야 합니다.

* **유효성 검사 안 함** — HTML 편집기에서 구문 검사나 레이아웃 확인을 수행하지 않습니다. 저장하기 전에 코드를 주의 깊게 검토하십시오.

* **콘텐츠 업데이트** — 향후 시스템 변경 사항은 고급 HTML 모드에서 기본 마크업에 대한 수정 사항에 영향을 주거나 덮어쓸 수 있습니다. 제품 업데이트 후 콘텐츠를 확인하여 예상대로 렌더링되는지 확인하십시오.

* **제한된 지원** — Adobe은 고급 HTML 모드에서 사용자 지정 코드를 수정하여 발생한 렌더링 문제 또는 콘텐츠 오류를 해결할 수 없습니다.

* **미리 보기 제한 사항** - 콘텐츠 시뮬레이션(프로필이 있는 미리 보기)은 HTML 소스 보기에서 직접 사용할 수 없으며 데스크톱 보기에서만 사용할 수 있습니다.

### 고급 HTML 모드 액세스

고급 HTML 모드는 캔버스에 이메일 템플릿이 로드된 경우 시각적 디자인 스페이스 상단의 도구 모음에서 액세스할 수 있습니다.

1. 콘텐츠를 편집하려면 [전자 메일 템플릿을 만들거나](./email-templates.md#create-an-email-template)하고 디자인 공간을 여십시오.

1. 디자인 공간에서 도구 모음의 _[!UICONTROL HTML]_( ![HTML 아이콘](../assets/do-not-localize/icon-code.svg)) 아이콘을 클릭합니다.

   ![전자 메일 서식 파일 디자인 공간 도구 모음에서 HTML 아이콘을 클릭합니다](./assets/email-template-advanced-html-mode-toolbar.png){width="750" zoomable="yes"}

   고급 HTML 모드를 처음 여는 경우(또는 한 달 이상이 경과한 경우) 경고 메시지가 표시됩니다. 정보를 검토하고 **[!UICONTROL 확인]**&#x200B;을 클릭하여 계속하십시오.

   ![계속하려면 고급 HTML 모드 경고를 검토하고 [확인]을 클릭하십시오](./assets/email-template-html-mode-warning.png){width="500"}

   디자인 캔버스는 원시 HTML 소스 보기로 전환됩니다.

1. 코드를 검토하고 이메일 콘텐츠에 원하는 변경 사항을 추가합니다.

   _고급 HTML 모드_&#x200B;에서는 전자 메일 템플릿 컨텐츠의 전체 HTML 소스에 직접 액세스할 수 있습니다.

   * 원시 HTML 마크업의 모든 부분을 보고 수정합니다.
   * 고급 [개인화 표현식](./personalization.md)을(를) 소스에 바로 삽입합니다.
   * 표현식 구문을 사용하여 [조건부 콘텐츠](./conditional-content.md) 논리를 추가합니다.
   * 사용자 지정 HTML 속성, 추적 태그 또는 시각적 편집기 컨트롤을 통해 사용할 수 없는 기타 태그를 추가합니다.

   ![전자 메일 콘텐츠의 원시 HTML 원본을 사용하는 고급 HTML 모드](./assets/email-template-advanced-html-mode.png){width="800" zoomable="yes"}

   >[!IMPORTANT]
   >
   >올바른 HTML 및 CSS 코드를 입력해야 합니다. Adobe에서는 구문 유효성 검사나 사용자 지정 코드 지원을 제공하지 않습니다.

   호환성의 이유로 고급 HTML 모드에서는 콘텐츠 시뮬레이션 및 저장을 사용할 수 없습니다. 데스크탑 보기로 다시 전환하여 콘텐츠를 미리 보고 템플릿을 저장할 수 있습니다. HTML 소스 보기와 시각적 디자인 보기 간에 전환하면 편집한 내용이 모두 유지됩니다.

   고급 HTML 모드에 있는 동안 오른쪽 상단에서 **[!UICONTROL 저장]** 또는 **[!UICONTROL 저장 및 닫기]**&#x200B;를 클릭하면 템플릿을 저장하고 디자인 공간을 종료하기 전에 고급 HTML 모드에서 전환해야 한다는 경고 대화 상자가 나타납니다.

   ![고급 HTML 모드에서 저장할 수 없는 경고 대화 상자](./assets/email-template-advanced-html-save-disabled-alert.png){width="500"}

1. 도구 모음에서 _[!UICONTROL 데스크톱]_( ![데스크톱 아이콘](../assets/do-not-localize/icon-desktop-spectrum-1.svg)) 아이콘을 클릭하여 고급 HTML 모드(HTML 소스 보기)에서 시각적 디자인 캔버스로 전환합니다.

   보기를 전환하면 편집 내용이 유지됩니다.
