---
title: Adobe Journey Optimizer B2B Edition의 동료
description: CX Enterprise Coworker을 사용하여 계정 및 개인 여정을 찾고, 만들고, 구성하고, 초안 미리 보기를 검토하고, 여정 만들기를 승인하는 방법을 알아봅니다.
feature: Account Journeys, Person Journeys, Agentic AI
role: User
level: Beginner
autotag-review: '2026-11-24T23:47:29.469Z'
TQID: 'https://experienceleague.adobe.com/gkizS-MB6qEMoG1pMqD3tSCBtcEuv-m-GMD5H6Z4JsY'
product_v2:
  - id: aacce07f-424e-489e-8d02-a4fb2f4211bd
    internal-label: Journey Optimizer B2B Edition
feature_v2:
  - id: 9b63d357-750f-5558-9208-62fc8a356785
    internal-label: Approval
  - id: a4b836d9-ffdd-4df3-a62a-f78b830cf059
    internal-label: Journeys
  - id: beb5f4be-cec3-471a-9db6-831a77dd3ac9
    internal-label: Audiences
  - id: c2f21a5c-bae4-56c6-97e3-2fc9a0e6c120
    internal-label: Use Cases
subfeature_v2:
  - id: ba367494-9862-4596-bd6f-299c7e10a46b
    internal-label: Person Journeys
  - id: c31bc6c7-76bc-467b-80c0-7315a4e3f6be
    internal-label: Account Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 81b4844bc7b333baaa2218639a542fefd512102f
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 1%
---

# [!DNL Adobe Journey Optimizer B2B Edition]의 [!DNL CX Enterprise Coworker] {#coworker-overview}

[!DNL Adobe Journey Optimizer B2B Edition]에서 작업을 완료하려면 [!DNL Adobe CX Enterprise Coworker] 채팅을 사용하세요. 목표를 쉬운 언어로 설명하십시오. [!DNL Coworker]이(가) 작업을 계획하고, 수행하고, 결과를 확인하고, 승인을 위해 작업을 제공합니다.

기존 계정 및 개인 여정을 찾거나, 새 초안 여정을 만들거나, 저장된 초안을 업데이트합니다. [!DNL Coworker]은(는) 개요가 유효성이 확인된 여정 그래프로 바뀌고 초안을 만들기 전에 미리 봅니다. [!DNL Coworker]에서 여정을 만들기 전에 미리 보기를 명시적으로 승인해야 합니다.

[!DNL Coworker]은(는) 조직의 기존 [제품 권한](../admin/user-management.md#b2b-product-permissions)을 준수합니다. 이미 허용된 작업만 수행할 수 있습니다. 관리자는 사용자가 쓰기 액세스 권한을 가지는 시점을 제어합니다. 액세스 요구 사항은 [AI 액세스 활성화](../ai-coworker/enable-ai-access.md)를 참조하십시오.

[!DNL Coworker]은(는) [!DNL Journey Optimizer B2B Edition]뿐만 아니라 Adobe 에코시스템에서 작동합니다. 더 광범위한 기능을 보려면 [Adobe CX Enterprise Coworker 채팅 개요](https://experienceleague.adobe.com/ko/docs/coworker/content/chat/overview){target="_blank"}를 참조하세요. 앱을 열고 대화를 시작하는 방법에 대한 지침은 [Coworker 인터페이스 안내서](https://experienceleague.adobe.com/ko/docs/coworker/content/chat/ui-guide){target="_blank"}를 사용하십시오.

## 여정 스킬 {#skills}

이 세 가지 기술을 사용하여 여정을 검사하고, 여정 그래프를 작성하고, 노드를 구성합니다. 스킬 식별자는 정확한 기술적 이름입니다.

| 스킬 | 도움이 되는 작업 | 스킬 범위 외부 |
| --- | --- | --- |
| `journey-lookup-ajob2b` | 계정 및 개인 여정 나열, 계산, 찾기 및 설명 여정이 사용하는 노드, 다시 입력 설정 및 활동, 속성 또는 이벤트 대상을 검사합니다. 이 스킬은 여정을 변경하지 않습니다. | 여정 만들기 또는 변경, 규칙 구성, 메시지 사본 작성, 구매 그룹 템플릿 관리, 게시 또는 삭제 |
| `journey-creation-ajob2b` | 간단한 내용을 여정으로 전환합니다. 여정 유형을 선택하고 대상을 해당 [!DNL Adobe Experience Platform] 대상 ID로 확인한 다음 그래프의 유효성을 검사하고 미리 봅니다. 명시적 승인 후 초안을 만듭니다. 저장된 초안의 그래프를 편집하고 설정을 다시 입력합니다. | 기존 여정 조회, 규칙 구성, 메시지 사본 작성, 구매 그룹 템플릿 관리, 대상자 검색, 게시 또는 삭제 |
| `journey-rules-ajob2b` | 저장된 여정의 구성되지 않은 노드에서 분할 조건, 작업, 이벤트 및 동적 목록 대상자를 구성합니다. | 그래프 변경, 여정 조회, 작성자 이메일 또는 SMS 사본 작성, 대상자 검색 또는 게시 |

추가 프롬프트 지침은 [B2B 여정 기술](./journey-skills.md)을 참조하세요. 계정 및 사용자 대상으로 작업하려면 [B2B 계정 및 사용자에 대한 대상 기술](./audience-skills-b2b.md)을 참조하세요.

## 사용 사례 예시 {#use-cases}

별도의 요청을 사용하여 초안을 작성하고, 해당 노드를 구성하고, 기존 여정을 검사합니다.

### 계정 여정 작성 {#build-account-journey}

간단한 항목으로 계정 육성 여정을 만든 다음 해당 노드를 구성합니다.

예제 프롬프트: _환영 이메일을 보내고 3일을 기다린 다음 사례 연구 이메일을 보내는 Enterprise Target 여정 대상자에 대한 계정 계정을 만듭니다._

1. [!DNL Coworker] 채팅에서 대상자 및 여정 흐름을 설명합니다.
1. 검증된 여정 그래프를 검토하고 미리 봅니다. [!DNL Coworker]이(가) 명명된 대상을 [!DNL Experience Platform] 대상 ID로 확인합니다.
1. 미리 보기를 명시적으로 승인합니다. [!DNL Coworker]이(가) 초안을 만들고 링크를 반환합니다.
1. [!DNL Coworker]에게 초안의 구성되지 않은 노드를 구성하도록 요청하십시오.
1. [!DNL Journey Optimizer B2B Edition]에서 초안을 열어 메시지 복사본을 추가하고 여정을 검토하십시오.

그 결과는 게시된 여정이 아닌 초안 여정이 됩니다. 응용 프로그램에서 [여정 검토 및 게시 단계](../journeys/create-publish-journey.md)를 완료합니다.

### 여정 검사 및 업데이트 {#inspect-update-journeys}

여정 인벤토리를 검토한 다음 저장된 초안의 분할 조건을 구체화하고 설정을 다시 입력합니다.

조회 프롬프트 예: _라이브 계정 여정 수 계정 대기 중인 여정 14251의 위치를 보여 줍니다._

1. [!DNL Coworker]에게 상태별 여정 수를 요청하거나 이름 또는 ID별로 여정을 찾으십시오.
1. 각 노드에서 여정 세부 정보 및 계정 수를 검토합니다.
1. 갱신할 저장된 초안을 식별합니다.
1. [!DNL Coworker]에게 분할 조건을 구성하도록 요청하십시오. 예를 들어, _초안 여정 14252의 경우, 고의도의 분기에 가격 페이지를 방문해야 합니다._
1. 재입력 변경을 요청합니다. 예를 들어 _초안 여정 14252의 경우 30일 동안 계정이 다시 입력되지 않도록 설정하십시오._

저장된 초안에 변경 사항이 적용됩니다. 게시는 별도의 단계입니다. 구성 세부 정보는 [경로 분할 및 병합](../journeys/split-merge-paths-nodes.md) 및 [여정 재입력](../journeys/journey-re-entry.md)을 참조하십시오.

## MCP 도구 {#mcp-tools}

[!DNL Coworker]은(는) 여정 작업에 다음 MCP(모델 컨텍스트 프로토콜) 도구를 사용합니다. 읽기 도구는 기존 정보를 검사하고, 확인 도구는 그래프의 유효성을 검사하고, 쓰기 도구는 여정 설정 또는 초안을 변경합니다.

| 도구 | 지원되는 작업 | 유형 |
| --- | --- | --- |
| `list_account_journeys` | 계정 여정의 페이지가 매겨진 목록을 반환합니다. | 읽기 |
| `list_person_journeys` | 개인 여정의 페이지가 매겨진 목록을 반환합니다. | 읽기 |
| `count_account_journeys` | 상태별 계정 여정 수 | 읽기 |
| `count_person_journeys` | 주별 개인 여정 수 | 읽기 |
| `get_journey` | 여정 노드를 읽고 설정을 다시 입력합니다. | 읽기 |
| `get_journey_rules` | 여정의 구성되지 않은 노드에 대한 구성 타겟을 읽습니다. | 읽기 |
| `get_journey_node_catalog` | 규칙 데이터에 대한 올바른 입력인 `ruleset_types`을(를) 반환합니다. | 읽기 |
| `validate_journey_graph` | 작성된 초안 그래프의 유효성을 검사합니다. | 확인 |
| `create_journey` | `confirm=false`(으)로 여정을 미리 봅니다. 명시적 승인 후 초안을 만들고 링크를 반환합니다. | 쓰기 |
| `update_journey` | 저장된 초안 여정의 그래프를 변경합니다. | 쓰기 |
| `set_journey_reentry` | 재입력 설정을 변경합니다. | 쓰기 |
| `set_journey_split_conditions` | 분할 분기 조건을 설정합니다. | 쓰기 |
| `apply_journey_rules` | 조건, 작업, 이벤트 및 동적 목록 대상에 대해 `rule_data`을(를) 여정에 적용합니다. | 쓰기 |
