# K-publid-API-Skill — 설치·호환 안내

한국 서비스에 필요한 공개 API를 찾고 비교할 때 사용하는 **호스트 중립적인 Agent Skills 참조 스킬**입니다. 원본 [yybmion/public-apis-4Kr](https://github.com/yybmion/public-apis-4Kr)의 API 목록을 탐색하고, 실제 제공기관 문서에서 조건을 확인하도록 안내합니다.

**API를 일괄 연결하는 프로그램이 아닙니다.** 별도 서버, npm/Python 의존성, MCP, 훅, 자동 API 호출이 없습니다. 전체 목록 탐색과 최신 정보 검증에는 AI 도구의 웹 접근 기능 또는 사용자가 제공한 공식 문서가 필요합니다. 오프라인에서는 동봉된 분야별 탐색 안내와 후보 링크만 참고하며, 최신 조건은 확인되지 않은 것으로 표시합니다.

## 배포 구성

```text
skills/
└── k-publid-api-skill/
    ├── SKILL.md
    ├── LICENSE
    └── references/
        └── catalog-guide.md
```

설치 대상은 **`skills/k-publid-api-skill` 폴더 전체**입니다. 원본 저장소의 `scripts/`, `.github/`, 보고서, 이미지 등은 설치 대상이 아닙니다. 저장소를 포크하거나 클론하는 것만으로 스킬이 자동 설치되지는 않습니다.

## 가장 간단한 설치 요청

스킬 설치를 지원하는 AI 개발 도구에 다음 요청을 전달하세요.

```text
다음 GitHub 스킬을 현재 AI 도구의 공식 설치 기능 또는 공식 스킬 디렉터리로 설치해줘.
저장소: https://github.com/contentriumkorea/K-publid-API-Skill
스킬 경로: skills/k-publid-api-skill
SKILL.md와 참조 파일을 먼저 검토하고, 대상 스킬 폴더만 설치해줘.
저장소의 셸 명령이나 관리용 스크립트는 실행하지 마.
스킬 설치를 지원하지 않으면 설치했다고 하지 말고, 참고자료로 사용하는 방법을 알려줘.
설치 후 실제 인식 여부와 새로고침 필요 여부를 확인해줘.
```

계정 전체 설치인지 현재 프로젝트 설치인지 확인하세요. 이미 같은 이름의 스킬이 있으면 덮어쓰기 전에 비교하고 보존하세요. 여러 검색 경로에 같은 스킬을 중복 배치하지 않는 것이 좋습니다.

## 도구별 공식 지원 확인

**문서 확인일: 2026-09-04.** 아래 표는 공식 문서에 기재된 설치 형식·경로입니다. 각 제품의 실제 설치·실행 시험을 모두 통과했다는 뜻이 아닙니다. 버전, 조직 정책, 요금제, 도구 권한에 따라 사용 가능 범위가 달라질 수 있습니다.

경로는 **스킬 폴더를 넣을 부모 디렉터리**입니다. 예를 들어 Claude Code 프로젝트 경로는 `.claude/skills/k-publid-api-skill/SKILL.md`가 됩니다. `~`는 사용자 홈이며 Windows에서는 보통 `C:\Users\<사용자>`입니다.

| 도구 | 프로젝트 설치 경로 | 사용자 설치 경로 / 방식 | 공식 근거 |
| --- | --- | --- | --- |
| Codex | `.agents/skills/` | `~/.agents/skills/`; 기본 제공 `skill-installer`로 GitHub 경로 설치도 가능 | [OpenAI Docs](https://learn.chatgpt.com/docs/build-skills) |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` | [Claude Code](https://code.claude.com/docs/en/skills) |
| GitHub Copilot / VS Code | `.github/skills/` | `~/.copilot/skills/`; `.agents/skills/` 계열도 지원 | [VS Code](https://code.visualstudio.com/docs/agent-customization/agent-skills) |
| GitHub Copilot CLI | `.github/skills/` | `~/.copilot/skills/`; `.agents/skills/` 계열도 지원 | [GitHub](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/add-skills) |
| Gemini CLI | `.gemini/skills/` 또는 `.agents/skills/` | `~/.gemini/skills/` 또는 `~/.agents/skills/` | [Gemini CLI](https://geminicli.com/docs/cli/skills/) |
| Cursor | `.cursor/skills/` 또는 `.agents/skills/` | `~/.cursor/skills/` 또는 `~/.agents/skills/` | [Cursor](https://cursor.com/docs/skills) |
| OpenCode | `.opencode/skills/` | `~/.config/opencode/skills/`; `.agents/skills/` 계열도 지원 | [OpenCode](https://opencode.ai/docs/skills/) |
| Windsurf Cascade | `.windsurf/skills/` | `~/.codeium/windsurf/skills/` | [Cascade](https://docs.devin.ai/desktop/cascade/skills) |
| Cline | `.cline/skills/` | `~/.cline/skills/` | [Cline](https://docs.cline.bot/customization/skills) |
| Antigravity IDE | `.agents/skills/` 권장 | IDE 문서는 `~/.gemini/antigravity/skills/`; 아래 주의 참고 | [Antigravity IDE](https://www.antigravity.google/docs/ide/skills/) |
| Claude.ai | 파일 경로 방식 아님 | 단일 스킬 폴더가 들어 있는 ZIP 업로드 | [사용 안내](https://support.claude.com/en/articles/12512180-use-skills-in-claude), [ZIP 작성 규칙](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills) |

추가 주의:

- **Codex:** 공식 문서의 수동 경로와 설치기 기본 목적지가 다를 수 있습니다. 현재 도구의 내장 설치기를 사용할 때는 설치기가 선택한 지원 경로를 따르세요. 이 패키지에는 Codex 전용 메타데이터가 없어 다른 도구가 이를 해석할 필요가 없습니다.
- **Antigravity:** 일반 문서와 IDE 문서의 전역 경로가 다르므로 공통으로 확인된 프로젝트 `.agents/skills/`를 권장합니다. Antigravity CLI는 별도 제품으로, 이 표가 CLI의 동일한 설치 형식을 보증하지 않습니다.
- **Cline:** 일부 통합 설치기는 `.agents/skills/`를 대상으로 표시하지만, 위 표는 제품 공식 문서에 있는 `.cline/skills/`를 우선합니다.
- **OpenCode:** V2의 HTTP 스킬 카탈로그 설정은 단순 GitHub 저장소 URL 설치와 다릅니다. 이 패키지는 폴더 배치 방식입니다.
- **Claude.ai:** 스킬 기능과 코드 실행·파일 생성 기능이 활성화되어 있어야 하며 조직 정책이 업로드를 제한할 수 있습니다. Claude Code의 `/plugin install` 명령은 ZIP 업로드와 다른 기능입니다.
- **그 외 AI 앱:** Agent Skills 또는 사용자 스킬 가져오기를 명시적으로 지원하는지 먼저 확인하세요. 일반 채팅창에 파일을 첨부하거나 프로젝트 지침에 내용을 넣는 것은 참고자료 활용이며, 스킬 설치와 같지 않습니다. 일반 ChatGPT 웹 채팅의 독립형 ZIP 설치도 이 패키지의 검증 범위에 포함하지 않습니다.

## 네이티브 설치 예시

아래는 사용자가 선택해서 실행하는 안내입니다. 패키지 작성·검증 과정에서는 실행하지 않았습니다.

### Codex

```text
$skill-installer install the skill from https://github.com/contentriumkorea/K-publid-API-Skill at skills/k-publid-api-skill
```

### Gemini CLI

```sh
gemini skills install https://github.com/contentriumkorea/K-publid-API-Skill.git --path skills/k-publid-api-skill --scope user
```

프로젝트 범위는 `--scope workspace`입니다. 설치 검토·동의 단계는 건너뛰지 마세요.

### GitHub CLI

GitHub CLI **2.90.0 이상, public preview**의 `gh skill` 기능을 사용하는 경우입니다. [공식 명령 규격](https://cli.github.com/manual/gh_skill_install)을 확인하고, 표시되는 설치 대상과 범위를 선택하세요.

```sh
gh skill install contentriumkorea/K-publid-API-Skill skills/k-publid-api-skill
```

검토한 버전을 고정하려면 공식 `--pin` 옵션에 실제 릴리스 태그 또는 커밋 SHA를 지정할 수 있습니다. 오래된 GitHub CLI에 이 명령이 없다고 해서 스킬 자체가 호환되지 않는 것은 아닙니다.

### Cursor

공식 문서의 `Customize → Rules → Add Rule → Remote Rule (Github)` 가져오기 기능 또는 위의 스킬 폴더 경로를 사용합니다. 가져온 뒤 `Customize → Skills`에서 `k-publid-api-skill`이 표시되는지 확인하세요.

### Claude.ai ZIP 업로드

1. [Releases](https://github.com/contentriumkorea/K-publid-API-Skill/releases/latest)에서 **`K-publid-API-Skill.zip`로 끝나는 스킬 전용 ZIP**을 받습니다.
2. `Customize → Skills → + → Create skill → Upload a skill`에서 업로드하고 활성화합니다.
3. ZIP 안에 `k-publid-api-skill/SKILL.md`, `k-publid-api-skill/LICENSE`, `k-publid-api-skill/references/catalog-guide.md`가 있는지 확인합니다.

GitHub의 저장소 전체 **Download ZIP / Source code (zip)**은 스킬 전용 ZIP이 아닙니다. ZIP 이름에 날짜가 붙어 있어도 내부 스킬 폴더 이름은 `k-publid-api-skill`로 고정됩니다.

## 선택 사항: 통합 설치기

[Vercel의 skills CLI](https://github.com/vercel-labs/skills)는 여러 AI 개발 도구를 대상으로 GitHub 스킬을 설치하는 **별도의 오픈소스 설치기**입니다. 각 AI 제품의 공식 설치기와 동일한 것은 아닙니다. Node.js/npm이 필요하며 실행 시 설치기 코드를 다운로드·실행할 수 있으므로 신뢰 여부를 직접 검토한 뒤 사용하세요.

```sh
npx skills add contentriumkorea/K-publid-API-Skill --skill k-publid-api-skill
```

상호작용 화면에서 원하는 AI 도구와 설치 범위만 선택합니다. 이 저장소는 모든 도구에 무조건 설치하는 `--all` 명령이나 원격 셸 설치 스크립트를 제공하지 않습니다.

## 설치 후 확인

| 도구 | 확인 방법 |
| --- | --- |
| Codex | 스킬 목록 또는 `$k-publid-api-skill`; 변경이 안 보이면 새 세션/재시작 |
| Claude Code | `/k-publid-api-skill`; 최상위 skills 디렉터리를 세션 도중 처음 만들었다면 재시작 |
| Gemini CLI | `/skills list`, 필요하면 `/skills reload` |
| Copilot CLI | `/skills reload`, `/skills info k-publid-api-skill` |
| VS Code / Cursor / Cline | Skills UI 또는 `/k-publid-api-skill`; 목록에 없으면 경로와 제품 버전 확인 |
| Windsurf Cascade | Skills UI 또는 `@k-publid-api-skill` |
| OpenCode / Antigravity IDE | 사용 가능한 스킬 목록 확인 후 이름을 명시해 사용 요청 |
| Claude.ai | 업로드한 스킬의 활성화 상태와 사용 시 로딩 여부 확인 |

프로젝트/사용자 경로에 파일이 있다는 사실만으로 실제 활성화가 검증되지는 않습니다. 자동 선택 여부는 도구의 검색·호출 정책과 사용자 요청에 따라 달라집니다.

사용 예시:

```text
전국 전기차 충전소 위치와 상태를 조회할 API 후보를 비교해줘. 아직 키는 없어.
```

```text
한국 관광지와 축제 정보를 제공할 API를 찾아줘. 인증 방식과 이용 조건도 공식 문서로 확인해줘.
```

## 왜 이 형식인가?

[Agent Skills 표준](https://agentskills.io/specification)은 `SKILL.md`와 선택적 참조 파일을 한 폴더에 묶습니다. [Anthropic의 공개 스킬](https://github.com/anthropics/skills), [Vercel의 스킬](https://github.com/vercel-labs/agent-skills), [GitHub의 커뮤니티 스킬](https://github.com/github/awesome-copilot)이 참고할 수 있는 배포 사례입니다. Vercel도 [여러 개발 에이전트를 대상으로 한 설치 생태계](https://vercel.com/changelog/introducing-skills-the-open-agent-skills-ecosystem)를 설명합니다. 이는 시장점유율 순위나 모든 제품의 실행 인증을 뜻하지 않습니다.

이 패키지는 공통 필드만 사용하고 description을 200자 이하로 유지합니다. 제품별 전용 frontmatter, 도구 이름, 셸 주입, hooks, 플러그인 manifest를 요구하지 않습니다. 따라서 공식적으로 이 폴더 형식을 읽는 도구에 같은 스킬을 배포할 수 있습니다.

## 원본·업데이트·검증 범위

- 원본 API 목록 및 원저작자 표시는 유지했습니다. 초기 기준 커밋은 `5f0570083484a5b8ce10d71628f16eb811a3295e`입니다.
- 스킬의 동봉 안내는 소수의 탐색 링크와 분야별 경로이며 전체 API 목록의 복사본이 아닙니다. 최신 카탈로그와 제공기관 문서는 사용 시 확인합니다.
- 포크, 설치된 스킬, ZIP은 자동으로 동기화되지 않습니다. 업데이트할 때 원본 변경과 스킬 변경을 검토하고 새 릴리스를 배포하세요.
- 검증 대상은 표준 메타데이터, 폴더 독립성, 상대 참조, ZIP 내부 구조 및 에이전트의 자료 검색·불확실성 처리입니다. 모든 AI 제품에 대한 실제 설치·실행 검증은 하지 않았습니다.
- 목록의 MIT 라이선스는 개별 API의 요금, 데이터 재배포, 상업 이용을 허가하는 라이선스가 아닙니다. 원본 [LICENSE](LICENSE)와 스킬에 동봉된 [LICENSE](skills/k-publid-api-skill/LICENSE)를 보존하세요.
