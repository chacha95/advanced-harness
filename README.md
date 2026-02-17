# Advanced Harness

Claude Code를 위한 고급 스킬/커맨드 모음 모노레포. FastAPI 백엔드 + Next.js 15 프론트엔드 프로젝트에 Claude Code 자동화 스킬,  프레임워크 가이드라인을 통합하여 개발 생산성을 극대화합니다.

## 기술 스택

| 영역 | 기술 |
|------|------|
| **Backend** | Python 3.12, FastAPI, SQLModel, PostgreSQL, asyncpg |
| **Frontend** | Next.js 15 (App Router), React 19, TypeScript, Tailwind CSS 4, MUI |
| **AI Agent** | Pydantic AI, SSE streaming |

## Skills (15개)

| # | 스킬 | 설명 |
|---|------|------|
| 1 | `brand-guidelines` | Anthropic 공식 브랜드 컬러와 타이포그래피(Poppins/Lora) 적용 |
| 2 | `docx` | Word 문서(.docx) 생성/편집/분석 - docx-js 생성, XML 직접 편집 |
| 3 | `error-tracking` | Sentry v8 에러 트래킹 및 성능 모니터링 통합 패턴 가이드 |
| 4 | `fastapi-backend-guidelines` | FastAPI 백엔드 DDD 개발 가이드 - SQLModel ORM, 레포지토리 패턴, async/await |
| 5 | `frontend-design` | 독창적이고 프로덕션급 프론트엔드 UI 생성 디자인 가이드 |
| 6 | `mermaid` | Mermaid 다이어그램 생성 - 플로우차트, ER, 간트 등 23종 지원 |
| 7 | `nextjs-frontend-guidelines` | Next.js 15 프론트엔드 가이드 - App Router, shadcn/ui, Tailwind CSS 4, 한국어 로컬라이제이션 |
| 8 | `pdf` | PDF 읽기/병합/분할/회전/워터마크/생성/OCR 등 전방위 처리 |
| 9 | `ppt-brand-guidelines` | VRL 프레젠테이션 브랜드 가이드라인 (라임그린 + 다크네이비) |
| 10 | `pptx` | PowerPoint 생성/편집/분석 - HTML→PPTX 변환, OOXML 편집 |
| 11 | `pytest-backend-testing` | FastAPI 백엔드 pytest 테스팅 가이드 - 유닛/통합/비동기/목킹 |
| 12 | `skill-developer` | Claude Code 스킬 생성/관리 가이드 - 트리거, 훅, 500줄 룰 |
| 13 | `vercel-react-best-practices` | Vercel 엔지니어링 기준 React/Next.js 성능 최적화 가이드 |
| 14 | `web-design-guidelines` | Vercel Web Interface Guidelines 기반 UI 코드 접근성/UX 리뷰 |
| 15 | `yebi-startup-writer` | 예비창업패키지 사업계획서 PSST 프레임워크 기반 docx 직접 작성 |

## Commands (3개)

| 커맨드 | 설명 |
|--------|------|
| `/dev-docs-update` | 컨텍스트 컴팩션 전 개발 문서(active task, 세션 상태) 업데이트 |
| `/dev-docs` | 전략적 개발 계획 생성 - `dev/active/`에 plan/context/tasks 구조화 |
| `/route-research-for-testing` | 편집된 라우트 자동 감지 후 auth-route-tester로 스모크 테스트 |

## Agents (12개)

자율적으로 복잡한 서브태스크를 수행하는 전문 에이전트입니다.

| # | 에이전트 | 설명 |
|---|---------|------|
| 1 | `auth-route-debugger` | 인증 관련 이슈(401/403 에러, 쿠키, JWT, Keycloak) 디버깅 전문 |
| 2 | `auth-route-tester` | 인증된 API 라우트 테스트 - DB 변경 검증 및 코드 리뷰 |
| 3 | `auto-error-resolver` | TypeScript 컴파일 에러 자동 감지 및 수정 |
| 4 | `code-architecture-reviewer` | 코드 품질, 아키텍처 일관성, 시스템 통합 리뷰 |
| 5 | `code-refactor-master` | 파일 재구성, 의존성 추적, 컴포넌트 추출 등 종합 리팩토링 실행 |
| 6 | `documentation-architect` | 개발 문서, API 문서, 데이터 플로우 다이어그램 생성 |
| 7 | `frontend-error-fixer` | 빌드타임/런타임 프론트엔드 에러 진단 및 수정 (browser-tools MCP 활용) |
| 8 | `plan-reviewer` | 구현 전 개발 계획 리뷰 - 리스크 평가, 갭 분석 |
| 9 | `planner` | `dev/active/`에 구조화된 개발 계획(plan/context/tasks) 생성 |
| 10 | `refactor-planner` | 코드 구조 분석 후 단계별 리팩토링 전략 수립 |
| 11 | `threads-aggro-writer` | 개발자/창업 주제 바이럴 스레드(Threads) 글 작성 (한국어) |
| 12 | `web-research-specialist` | GitHub Issues, Reddit, SO 등에서 기술 이슈 리서치 |

## 빠른 시작

### Backend

```bash
cd backend
uv venv && source .venv/bin/activate
uv pip install -e .[dev]
uvicorn backend.main:app --reload --port 28080
```

### Frontend

```bash
cd frontend
pnpm install
pnpm dev  # http://localhost:3000
```
