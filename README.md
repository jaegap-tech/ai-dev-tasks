# 🚀 AI Dev Tasks 🤖

수정 알림: 본 저장소는 snarktank/ai-dev-tasks를 포크후 한국어로 번역하였습니다.

**AI Dev Tasks**에 오신 것을 환영합니다! 이 저장소는 AI 기반 IDE 및 CLI와 함께 기능 개발 워크플로우를 강화할 수 있는 마크다운 파일 모음을 제공합니다. 원래 [Cursor](https://cursor.sh/)용으로 제작되었지만, Claude Code, Windsurf 등 모든 AI 코딩 어시스턴트와 함께 사용할 수 있습니다. 구조화된 프롬프트를 활용하여 아이디어부터 구현까지 체계적으로 기능을 개발하고, 내장된 체크포인트로 검증할 수 있습니다.

복잡한 AI 요청에 고생하지 말고, AI 협업자를 단계별로 안내하세요!

## ✨ 핵심 아이디어

AI로 복잡한 기능을 개발하는 것은 때때로 블랙박스처럼 느껴질 수 있습니다. 이 워크플로우는 다음을 통해 구조, 명확성, 통제력을 제공합니다:

1. **범위 정의:** 제품 요구사항 문서(PRD)로 무엇을 만들지 명확히 정리
2. **상세 계획:** PRD를 세분화된, 실행 가능한 작업 목록으로 분해
3. **반복적 구현:** AI가 한 번에 하나의 작업만 처리하도록 안내하고, 각 변경 사항을 검토 및 승인

이 구조화된 접근법은 AI가 올바른 방향으로 나아가도록 하며, 디버깅을 쉽게 하고, 생성된 코드에 대한 신뢰를 높여줍니다.

## 워크플로우: 아이디어에서 구현된 기능까지 💡➡️💻

이 저장소의 `.md` 파일을 활용한 단계별 프로세스입니다:

### 1️⃣ 제품 요구사항 문서(PRD) 작성

먼저, 기능의 청사진을 만듭니다. PRD는 무엇을, 누구를 위해, 왜 만드는지 명확히 해줍니다.

AI 도구에서 간단하게 PRD를 만들 수 있습니다:

1. 저장소의 `create-prd.md` 파일을 준비하세요.
2. AI 도구에서 PRD 생성을 시작하세요:

    ```text
    Use @create-prd.md
    Here's the feature I want to build: [구체적으로 기능 설명]
    Reference these files to help you: [선택: @file1.py @file2.ts]
    ```
    *(팁: Cursor 사용자는 예산이 허락된다면 복잡한 PRD에 MAX 모드를 추천합니다.)*

    ![PRD 생성 예시](https://pbs.twimg.com/media/Go6DDlyX0AAS7JE?format=jpg&name=large)

### 2️⃣ PRD로부터 작업 목록 생성

PRD가 완성되면(예: `MyFeature-PRD.md`), 다음 단계는 AI 개발자를 위한 상세하고 단계별 구현 계획을 만드는 것입니다.

1. `generate-tasks.md` 파일을 준비하세요.
2. AI 도구에서 PRD를 활용해 작업을 생성하세요:

    ```text
    Now take @MyFeature-PRD.md and create tasks using @generate-tasks.md
    ```
    *(참고: 1단계에서 생성한 PRD 파일명을 실제로 입력하세요.)*

    ![PRD로부터 작업 생성 예시](https://pbs.twimg.com/media/Go6FITbWkAA-RCT?format=jpg&name=medium)

### 3️⃣ 작업 목록 확인

이제 잘 구조화된 작업 목록(상위 작업과 하위 작업 포함)이 생성되어, AI가 실제로 작업을 시작할 준비가 됩니다. 명확한 구현 로드맵을 제공합니다.

![생성된 작업 목록 예시](https://pbs.twimg.com/media/Go6GNuOWsAEcSDm?format=jpg&name=medium)

### 4️⃣ AI에게 작업 진행 및 완료 표시 지시

체계적인 진행과 검증을 위해 `process-task-list.md`를 사용합니다. 이 명령은 AI가 한 번에 하나의 작업에 집중하고, 다음 작업으로 넘어가기 전에 사용자의 승인을 기다리도록 안내합니다.

1. `process-task-list.md` 파일을 준비하세요.
2. AI 도구에서 첫 번째 작업(예: `1.1`)부터 시작하도록 지시하세요:

    ```text
    Please start on task 1.1 and use @process-task-list.md
    ```
    *(중요: 첫 작업에만 `@process-task-list.md`를 참조하면 됩니다. 이후 작업은 파일 내 지침을 따릅니다.)*

    AI가 작업을 시도한 후, 검토를 요청합니다.

    ![process-task-list.md로 작업 시작 예시](https://pbs.twimg.com/media/Go6I41KWcAAAlHc?format=jpg&name=medium)

### 5️⃣ 검토, 승인, 다음 단계 진행 ✅

AI가 각 작업을 완료하면, 변경 사항을 검토하세요.

* 변경 사항이 만족스러우면 "yes" 등 긍정적으로 답해 AI가 작업을 완료로 표시하고 다음 작업으로 넘어가도록 하세요.
* 수정이 필요하면, AI에게 피드백을 주어 현재 작업을 먼저 수정하게 하세요.

완료된 항목이 늘어나는 것을 확인할 수 있어, 기능이 점차 완성되는 시각적 만족감을 얻을 수 있습니다!

![진행 중인 작업 목록 예시](https://pbs.twimg.com/media/Go6KrXZWkAA_UuX?format=jpg&name=medium)

완벽하진 않더라도, 이 방법은 AI와 함께 대형 기능을 안정적으로 개발하는 데 매우 효과적임이 입증되었습니다.

### 영상 시연 🎥

실제 동작을 보고 싶다면 [Claire Vo의 "How I AI" 팟캐스트](https://www.youtube.com/watch?v=fD4ktSkNCw4)에서 시연한 영상을 참고하세요.

![How I AI Podcast에서 AI Dev Tasks 시연](https://img.youtube.com/vi/fD4ktSkNCw4/maxresdefault.jpg)

## 🗂️ 저장소의 파일

* **`create-prd.md`**: 기능에 대한 제품 요구사항 문서(PRD) 생성을 AI에게 안내
* **`generate-tasks.md`**: PRD 마크다운 파일을 입력받아, AI가 상세하고 단계별 구현 작업 목록으로 분해하도록 안내
* **`process-task-list.md`**: 생성된 작업 목록을 AI가 하나씩 처리하고, 매번 사용자의 승인을 기다리도록 안내 (작업 완료 표시 로직 포함)

## 🌟 장점

* **구조화된 개발:** 아이디어에서 코드까지 명확한 프로세스 강제
* **단계별 검증:** AI가 생성한 코드를 매 단계마다 검토 및 승인 가능, 품질과 통제력 확보
* **복잡성 관리:** 대형 기능을 더 작고 소화 가능한 작업으로 분해, AI가 길을 잃거나 과도하게 복잡한 코드를 생성할 위험 감소
* **신뢰성 향상:** 단일 대형 프롬프트보다 더 신뢰할 수 있는 AI 활용 방식 제공
* **진행 상황 추적:** 완료된 작업을 시각적으로 보여주어, 얼마나 진행됐는지 한눈에 파악 가능

## 🛠️ 사용 방법

1. **클론 또는 다운로드:** `.md` 파일을 프로젝트 또는 AI 도구가 접근 가능한 위치에 저장하세요.
   ```bash
   git clone https://github.com/snarktank/ai-dev-tasks.git
   ```
2. **워크플로우 따라 진행:** 위에서 설명한 대로 AI 어시스턴트에서 `.md` 파일을 체계적으로 활용하세요.
3. **적응 및 반복:**
    * 필요에 따라 `.md` 파일 내 프롬프트를 수정해 자신의 요구나 코딩 스타일에 맞게 사용하세요.
    * AI가 작업을 어려워하면, 초기 기능 설명을 다시 표현하거나 작업을 더 세분화해보세요.

## 도구별 안내

### Cursor

Cursor 사용자는 위 워크플로우를 따라, `.md` 파일을 Agent 채팅에서 직접 활용할 수 있습니다:

1. 저장소의 파일을 준비하세요
2. Cursor Agent 채팅에서 `@`로 파일 참조 (예: `@create-prd.md`)
3. 위 5단계 워크플로우를 따라 진행
4. **PRD 생성 시 MAX 모드:** 예산이 허락된다면 Cursor의 MAX 모드로 PRD를 생성하면 더 완성도 높은 결과를 얻을 수 있습니다

### Claude Code

Claude Code에서 이 도구를 사용하려면:

1. **파일 복사:** 세 개의 `.md` 파일을 프로젝트의 하위 디렉터리(예: `/ai-dev-tasks`)에 복사하세요

2. **CLAUDE.md에 참조 추가:** 프로젝트의 `./CLAUDE.md` 파일에 다음을 추가하세요:
   ```
   # AI Dev Tasks
   구조화된 PRD 기반 개발 요청 시 다음 파일을 사용하세요:
   /ai-dev-tasks/create-prd.md
   /ai-dev-tasks/generate-tasks.md
   /ai-dev-tasks/process-task-list.md
   ```

3. **커스텀 명령 생성(선택):** 더 쉽게 접근하려면 `.claude/commands/`에 다음 파일을 생성하세요:
   - `.claude/commands/create-prd.md` 내용:
     ```
     /ai-dev-tasks/create-prd.md의 구조화된 워크플로우를 사용해 새 기능의 PRD를 생성해주세요.
     ```
   - `.claude/commands/generate-tasks.md` 내용:
     ```
     /ai-dev-tasks/generate-tasks.md를 사용해 PRD로부터 작업을 생성해주세요.
     명시적으로 사용할 PRD를 지정하지 않으면 `/tasks` 내 PRD 목록을 생성해 사용자에게 선택을 요청하거나, `create-prd.md`로 새로 생성하세요:
     - `/tasks`에 저장되어 있고 파일명이 `prd-`로 시작한다고 가정 (예: `prd-[name].md`)
     - 이미 `/tasks`에 해당 작업 목록이 없을 것 (예: `tasks-prd-[name].md`)
     - **항상** 진행 전에 PRD 파일명을 사용자에게 확인 요청
     여러 옵션이 있을 경우 숫자 목록으로 제공해 쉽게 선택할 수 있도록 하세요.
     ```
   - `.claude/commands/process-task-list.md` 내용:
     ```
     /ai-dev-tasks/process-task-list.md를 사용해 작업 목록을 처리해주세요.
     ```

   파일 추가 후 Claude Code를 재시작하세요(`/exit`).
   `/create-prd` 등 명령어로 빠르게 워크플로우를 시작할 수 있습니다.
   이 설정은 모든 프로젝트에 글로벌하게 적용할 수도 있습니다. 자세한 내용은 Claude Code 문서 [여기](https://docs.anthropic.com/en/docs/claude-code/memory) 및 [여기](https://docs.anthropic.com/en/docs/claude-code/common-workflows#create-personal-slash-commands)를 참고하세요.

### 기타 도구

다른 AI 기반 IDE 또는 CLI에서는:

1. `.md` 파일을 프로젝트에 복사하세요
2. 도구 문서에 따라 참조하세요
3. 동일한 워크플로우 원칙을 따르세요

## 💡 성공을 위한 팁

* **구체적으로 작성:** 초기 기능 설명과 추가 명확화 모두에서 더 많은 맥락과 명확한 지침을 제공할수록 AI의 결과물이 좋아집니다.
* **성능 좋은 모델 사용:** Cursor 무료 버전은 구조화된 워크플로우를 잘 따르지 못하는 경우가 많으니, 일관되고 정확한 작업 실행을 원한다면 Pro 요금제로 업그레이드하는 것이 좋습니다.
* **PRD 생성 시 MAX 모드:** 앞서 언급한 대로, 예산이 허락된다면 Cursor의 MAX 모드로 PRD를 생성하면 더 완성도 높고 품질 좋은 결과를 얻을 수 있습니다.
* **파일 태그 정확히:** 작업 생성 시 항상 PRD 파일명을 정확히 태그하세요(예: `@MyFeature-PRD.md`).
* **인내와 반복:** AI는 강력하지만 만능은 아닙니다. 안내, 수정, 반복할 준비를 하세요. 이 워크플로우는 그 과정을 더 부드럽게 만들어줍니다.

## 🤝 기여하기

이 `.md` 파일을 개선하거나 워크플로우에 맞는 새로운 파일 아이디어가 있다면 언제든 기여를 환영합니다!

다음과 같이 참여할 수 있습니다:

* 변경 논의나 새로운 기능 제안을 위해 이슈를 열기
* 개선 사항을 담아 풀 리퀘스트 제출

---

AI와 함께 즐거운 개발 되세요!
