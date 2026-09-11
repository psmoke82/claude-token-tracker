> **포크 안내**: 이 저장소는
> [pepperonas/claude-token-tracker](https://github.com/pepperonas/claude-token-tracker)의
> 개인 포크입니다. 독일어·영어에 이어 세 번째 UI 언어로 한국어(KO) 번역을 추가했습니다.
> **한국어 번역(앱 UI, 업적 이름/설명, 이 문서 포함)은 전부 AI(Claude)로 생성했습니다.**
> 원본 프로젝트와 문서는 upstream 저장소를 참고하세요. 이 문서의 원본(영문)은
> [readme_origin.md](readme_origin.md)에 그대로 남겨두었습니다.
>
> **빠른 설치**
> ```bash
> git clone https://github.com/psmoke82/claude-token-tracker
> cd claude-token-tracker
> npm install
> npm start
> ```

<p align="center">
  <img src="public/og-image.png" alt="Claude Token Tracker" width="720">
</p>

<h1 align="center">Claude Token Tracker</h1>

<p align="center">
  Claude Code 토큰 사용량, API 환산 비용 추정, 코딩 활동을 추적하는 실시간 대시보드.
</p>

<!-- BADGES:START -->

<p align="center">
  <img src="https://img.shields.io/badge/version-v0.2.1-ff6b00?style=for-the-badge&logo=semanticrelease&logoColor=white" alt="Version 0.2.1">
  <img src="https://img.shields.io/badge/lines_of_code-40.8k-58a6ff?style=for-the-badge&logo=javascript&logoColor=white" alt="40757 lines of code across 58 files">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/tests-463_passing-3fb950?style=for-the-badge&logo=vitest&logoColor=white" alt="463 tests passing">
  <img src="https://img.shields.io/badge/achievements-1200-8957e5?style=for-the-badge&logo=trophy&logoColor=white" alt="1200 achievements">
  <img src="https://img.shields.io/badge/build_step-none-1a7f37?style=for-the-badge&logo=esbuild&logoColor=white" alt="no build step">
</p>

<p align="center">
  <a href="https://github.com/pepperonas/claude-token-tracker/actions/workflows/ci.yml"><img src="https://github.com/pepperonas/claude-token-tracker/actions/workflows/ci.yml/badge.svg" alt="CI status"></a>
  <img src="https://img.shields.io/github/license/pepperonas/claude-token-tracker?style=flat-square&label=license&color=blue&logo=opensourceinitiative&logoColor=white" alt="license">
  <img src="https://img.shields.io/github/v/release/pepperonas/claude-token-tracker?style=flat-square&label=release&color=orange&logo=github&logoColor=white" alt="release">
  <img src="https://img.shields.io/github/last-commit/pepperonas/claude-token-tracker?style=flat-square&label=last%20commit&color=informational&logo=git&logoColor=white" alt="last commit">
  <img src="https://img.shields.io/github/commit-activity/m/pepperonas/claude-token-tracker?style=flat-square&label=commits%2Fmonth&color=informational&logo=git&logoColor=white" alt="commits/month">
  <img src="https://img.shields.io/github/languages/code-size/pepperonas/claude-token-tracker?style=flat-square&label=code%20size&color=informational&logo=github&logoColor=white" alt="code size">
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/pepperonas/claude-token-tracker?style=flat-square&label=stars&color=gold&logo=github&logoColor=white" alt="stars">
  <img src="https://img.shields.io/github/forks/pepperonas/claude-token-tracker?style=flat-square&label=forks&color=informational&logo=github&logoColor=white" alt="forks">
  <img src="https://img.shields.io/github/issues/pepperonas/claude-token-tracker?style=flat-square&label=open%20issues&color=informational&logo=github&logoColor=white" alt="open issues">
  <img src="https://img.shields.io/github/issues-pr/pepperonas/claude-token-tracker?style=flat-square&label=open%20PRs&color=informational&logo=github&logoColor=white" alt="open PRs">
  <img src="https://img.shields.io/github/contributors/pepperonas/claude-token-tracker?style=flat-square&label=contributors&color=informational&logo=github&logoColor=white" alt="contributors">
  <a href="https://github.com/pepperonas/claude-token-tracker/pulls"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square" alt="PRs welcome"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/API_routes-70-0969da?style=flat-square" alt="70 API routes">
  <img src="https://img.shields.io/badge/DB_tables-12-0969da?style=flat-square" alt="12 database tables">
  <img src="https://img.shields.io/badge/lib_modules-16-0969da?style=flat-square" alt="16 library modules">
  <img src="https://img.shields.io/badge/charts-43-FF6384?style=flat-square&logo=chartdotjs&logoColor=white" alt="43 chart types">
  <img src="https://img.shields.io/badge/doc_pages-5-6f42c1?style=flat-square&logo=readthedocs&logoColor=white" alt="5 documentation pages">
  <img src="https://img.shields.io/badge/test_files-25-3fb950?style=flat-square&logo=vitest&logoColor=white" alt="25 test files">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/achievement_categories-14-8957e5?style=flat-square" alt="14 achievement categories">
  <img src="https://img.shields.io/badge/tiers-5_bronze_to_diamond-8957e5?style=flat-square" alt="5 tiers">
  <img src="https://img.shields.io/badge/models_priced-14-D4A574?style=flat-square&logo=anthropic&logoColor=white" alt="14 models in the fallback price table">
  <img src="https://img.shields.io/badge/i18n_keys-8844_x_3-bf8700?style=flat-square" alt="8844 translation keys in 3 languages">
  <img src="https://img.shields.io/badge/languages-DE_%7C_EN_%7C_KO-bf8700?style=flat-square" alt="DE, EN, KO">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-%3E%3D20.12-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js &gt;=20.12">
  <img src="https://img.shields.io/badge/better--sqlite3-11.0.0-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="better-sqlite3 11.0.0">
  <img src="https://img.shields.io/badge/chokidar-4.0.0-orange?style=flat-square&logo=files&logoColor=white" alt="chokidar 4.0.0">
  <img src="https://img.shields.io/badge/Chart.js-4.4.7-FF6384?style=flat-square&logo=chartdotjs&logoColor=white" alt="Chart.js 4.4.7">
  <img src="https://img.shields.io/badge/Vitest-4.1.8-6E9F18?style=flat-square&logo=vitest&logoColor=white" alt="Vitest 4.1.8">
  <img src="https://img.shields.io/badge/ESLint-9.0.0-4B32C3?style=flat-square&logo=eslint&logoColor=white" alt="ESLint 9.0.0">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/runtime_deps-2-cf222e?style=flat-square" alt="2 runtime dependencies">
  <img src="https://img.shields.io/badge/dev_deps-3-cf222e?style=flat-square" alt="3 dev dependencies">
  <img src="https://img.shields.io/badge/framework-none-1a7f37?style=flat-square" alt="no frontend framework">
  <img src="https://img.shields.io/badge/bundler-none-1a7f37?style=flat-square" alt="no bundler">
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square&logo=opensourceinitiative&logoColor=white" alt="MIT license">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/storage-SQLite_WAL-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite in WAL mode">
  <img src="https://img.shields.io/badge/live_updates-SSE-FF6600?style=flat-square&logo=lightning&logoColor=white" alt="Server-Sent Events">
  <img src="https://img.shields.io/badge/auth-GitHub_OAuth-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub OAuth">
  <img src="https://img.shields.io/badge/secrets-AES----256----GCM-critical?style=flat-square&logo=letsencrypt&logoColor=white" alt="AES-256-GCM encrypted">
  <img src="https://img.shields.io/badge/pricing-live_via_LiteLLM-6f42c1?style=flat-square&logo=anthropic&logoColor=white" alt="live pricing from LiteLLM">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/cache_tiers-5min_%2B_1h-0969da?style=flat-square" alt="both cache-write tiers priced">
  <img src="https://img.shields.io/badge/cost_model-time--aware-0969da?style=flat-square" alt="historical prices pinned per message">
  <img src="https://img.shields.io/badge/data-never_deleted-1a7f37?style=flat-square" alt="no DELETE FROM messages anywhere">
  <img src="https://img.shields.io/badge/offline-works_fully-lightgrey?style=flat-square" alt="works without network access">
  <img src="https://img.shields.io/badge/mobile-responsive_393px%2B-purple?style=flat-square" alt="mobile responsive from 393px">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-macOS_%7C_Linux_%7C_Windows-lightgrey?style=flat-square&logo=linux&logoColor=white" alt="runs on macOS, Linux and Windows">
  <img src="https://img.shields.io/badge/deploy-PM2_%2B_nginx-2B037A?style=flat-square&logo=pm2&logoColor=white" alt="PM2 and nginx">
  <img src="https://img.shields.io/badge/sync_agent-included-success?style=flat-square&logo=rsync&logoColor=white" alt="sync agent included">
  <a href="https://tracker.celox.io"><img src="https://img.shields.io/badge/demo-tracker.celox.io-blue?style=flat-square&logo=googlechrome&logoColor=white" alt="Live demo"></a>
</p>

<p align="center">
  <a href="docs/API.md"><img src="https://img.shields.io/badge/docs-API-informational?style=flat-square&logo=readthedocs&logoColor=white" alt="API reference"></a>
  <a href="docs/ARCHITECTURE.md"><img src="https://img.shields.io/badge/docs-Architecture-informational?style=flat-square&logo=readthedocs&logoColor=white" alt="Architecture"></a>
  <a href="docs/METRICS.md"><img src="https://img.shields.io/badge/docs-Metrics-informational?style=flat-square&logo=readthedocs&logoColor=white" alt="Metrics"></a>
  <a href="docs/CONFIGURATION.md"><img src="https://img.shields.io/badge/docs-Configuration-informational?style=flat-square&logo=readthedocs&logoColor=white" alt="Configuration"></a>
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/docs-Contributing-informational?style=flat-square&logo=readthedocs&logoColor=white" alt="Contributing"></a>
  <a href="CHANGELOG.md"><img src="https://img.shields.io/badge/docs-Changelog-informational?style=flat-square&logo=readthedocs&logoColor=white" alt="Changelog"></a>
</p>

<!-- BADGES:END -->

---

<p align="center">
  <a href="readme_origin.md"><img src="https://img.shields.io/badge/%F0%9F%87%AC%F0%9F%87%A7_English-Original-black?style=for-the-badge" alt="English (original)"></a>
  &nbsp;&nbsp;
  <a href="README_DE.md"><img src="https://img.shields.io/badge/%F0%9F%87%A9%F0%9F%87%AA_Deutsch-Dokumentation-black?style=for-the-badge" alt="Deutsch"></a>
  &nbsp;&nbsp;
  <a href="README_EN.md"><img src="https://img.shields.io/badge/%F0%9F%87%AC%F0%9F%87%A7_English-Documentation-black?style=for-the-badge" alt="English"></a>
</p>

---

## 빠른 시작

```bash
git clone https://github.com/pepperonas/claude-token-tracker.git
cd claude-token-tracker
npm install
npm start
```

[http://localhost:5010](http://localhost:5010) 접속

## 주요 기능

- **40개 이상의 인터랙티브 차트** — 10개 탭, 실시간 SSE 업데이트
- **Claude API 탭** — Anthropic 관리자 API 사용량/비용 대시보드: 진행률 표시줄이 있는 예산 추적, KPI 4종(총 비용, 토큰, 일평균 비용, 캐시 효율), 모델별 일일 비용/토큰 차트, 모델 분포 도넛, 누적 비용 추이. **API 키별 세부 내역**: 키별·모델별 비용을 보여주는 가로 누적 막대 차트, 키별 일일 비용 타임라인, 키 비교 표(토큰, 입력, 출력, 캐시 %, 계산된 비용, 마지막 사용), 토큰 이력 타임라인(누적 영역). 비용 API가 `group_by api_key_id`를 지원하지 않아 키별 비용은 모델 가격으로 직접 계산합니다. 키 이름은 `/v1/organizations/api_keys`로 조회. AES-256-GCM으로 키 암호화 저장, TTL 설정 가능한 SWR 캐싱
- **사용량 추이** — 오늘/이번 주/이번 달/최근 7일, 네 개의 실시간 카드가 **같은 시점까지 자른** 직전 기간과 비교(어제 이 시각까지, 지난주 같은 요일·시각까지, 지난달 같은 날짜까지, 짧은 달은 클램프), 각각 변화율 배지·오버레이 스파크라인·월말 예상치 포함. 그 아래 같은 데이터로 만든 비교 차트 5종: 90일 거래량과 7일/30일 이동평균, 이번 달 vs 지난달 누적, 월~일 주간 비교, 프로젝트 모멘텀(최근 7일 vs 이전 7일), 100% 누적 막대로 보는 모델 비중 변화. 기간 필터와 무관하며 캐시/토큰-비용 토글 반영
- **GitHub 연동** — SWR 캐싱, 요금제 감지 및 비율이 포함된 결제 정보, 코드 통계(저장소별 LOC), PR 코드 영향, 저장소별 Actions 사용량, 기여 히트맵
- **도구 비용 귀속** — 도구별 비용/토큰 비례 분배, MCP 서버 분류(`mcp__` 접두사로 자동 감지), 서브 에이전트 추적(`/subagents/` 경로 기준), 시간에 따른 비용 차트, 유형/비용/토큰 열이 추가된 표
- **프로젝트 상세 다이얼로그** — 차트나 표에서 프로젝트를 클릭하면 KPI 6종(토큰, 비용, 세션, 메시지, **활성 시간**, 순 라인)이 담긴 상세 모달, 일별 토큰 차트, 모델 분포 도넛, 주요 도구, 세션 목록, JSON 클립보드 내보내기가 열립니다. 모든 KPI에 한 줄 설명이 붙어있고 클릭하면 공식·5분 유휴 상한선·가격 출처·**집계에서 제외되는 항목**을 설명하는 **산정 방식 다이얼로그**가 열립니다
- **프로젝트별 리포트 (HTML + PDF)** — 프로젝트별로 독립 실행되는 인쇄 최적화 리포트: KPI, 구성요소별 비용 분할(5분·1시간 캐시 쓰기 등급 포함), 시간에 따른 비용 차트, 모델·세션 표, 문서 자체를 설명하는 산정 방식 섹션. CDN도 차트 라이브러리도 없이 인라인 SVG로 그려서 메일로 주고받거나 인쇄해도 그대로 살아남습니다. "PDF"는 브라우저 자체의 인쇄-PDF 변환 기능
- **프로젝트 검색 & 병합** — 프로젝트 표에 실시간 부분 문자열 필터, 그리고 이름만 바뀌었거나(이동/다른 기기에서 동기화) 실제로는 같은 코드베이스인 프로젝트를 하나의 정식 이름으로 비파괴적으로 병합. 경로 이름에서 중복 가능성을 자동 감지하는 🪄 추천 버튼 포함
- **레이트 리밋 추적** — JSONL 로그에서 Claude Code 레이트 리밋 이벤트 자동 감지, 일별 집계, KPI 카드, 과거 데이터 백필
- **기간 이동** — 날짜 선택기 옆 이전/다음 화살표로 선택한 기간 단위만큼 이동
- **생산성 탭** — 분당 토큰, 시간당 라인, 라인당 비용, 캐시 절감액, 코드 비율을 추세 표시와 함께
- **기간 비교** — 인라인 필 선택기(끄기/직전 기간/최근 7일/30일/90일/사용자 지정)로 두 기간을 지표 8종, 변화율 %, 색상 표시와 함께 나란히 비교
- **HTML 내보내기** — Chart.js 기반 모바일 반응형 인터랙티브 스냅샷, 탭 8개, 차트 12개 이상, 정렬 가능한 표. 412px 이상 폰 화면에 맞춘 적응형 레이아웃
- **전체 비교** — 모든 사용자 평균과 내 통계를 비교(멀티 유저 모드)
- **업적 1200개** — 14개 카테고리, 5개 등급의 게임화 시스템. 등급별 포인트, 타임라인 차트, 일별 달성 통계, SSE를 통한 실시간 달성 알림
- **코드 라인 수 추적** — 작성(초록)·수정(노랑)·삭제(빨강)을 시간/일 단위 적응형 차트로
- **사용량 히트맵** — 개요 화면의 요일 × 시간 그리드로 토큰 사용 강도 표시(여러 날 범위는 월~일 행, 하루는 24시간 단일 줄), 캐시 토글 반영, 셀별 툴팁
- **요일 표시 날짜** — 차트 축 라벨과 기간 범위 헤더에 요일 표시(예: `Sa 06-27`, `Thu 05/28/2026 – Sat 06/27/2026`)
- **다중 기기 추적** — 여러 기기(MacBook, VPS, 데스크톱)의 사용량을 함께 추적, 기기별 API 키, 대시보드 내 기기 전환기, 통합 "전체 기기" 보기, 클릭으로 기기 이름 변경, OS 선택 가능한 설치 명령
- **멀티 유저 모드** — GitHub OAuth, 사용자별 데이터 격리, 원클릭 설치 지원 Sync Agent(macOS/Linux/Windows)
- **토큰 내역** — 입력, 출력, 캐시 읽기, 캐시 생성별 API 환산 비용 추정. 캐시 쓰기는 **TTL 등급**별로 과금(5분 = 입력의 1.25배, 1시간 = 입력의 2배) — Claude Code는 대부분 1시간 캐시에 기록하므로, 단일 요율로 계산하면 비용이 약 8.5% 적게 나옵니다
- **Share API** — 프로젝트별 토큰 사용량을 외부 클라이언트와 안전하게 공유하는 API. 공유 토큰(48자리 16진수, 192비트 엔트로피)이 정제된 프로젝트 데이터(토큰, 비용, 세션, 코드 라인, 일별 내역)를 공개 엔드포인트로 노출. 관리자 키 인증, 레이트 리밋(30회/분/IP), CORS 제한, 선택적 만료 기간. [OPS](https://github.com/pepperonas/celox-ops)가 고객 대상 투명성 대시보드에 사용. 설정 화면에서 복사 버튼과 함께 Share Admin Key 표시
- **"이렇게 계산됩니다"** — 모든 KPI에 한 줄 설명이 붙고, 클릭하면 공식·5분 유휴 상한선·가격 출처·일부러 **집계에서 뺀** 항목(웹 검색, 고속 모드, 미국 전용 추론, Batch 할인, Bash로 이뤄진 수정)까지 설명하는 산정 방식 다이얼로그가 열립니다
- **정확한 캐시 가격 산정** — 캐시 쓰기는 TTL 등급별 과금: 5분은 입력의 1.25배, **1시간은 2배**. Claude Code는 대부분 1시간 캐시에 기록하므로 단일 요율로는 비용이 약 8.5% 적게 나옵니다
- **데이터베이스 다운로드** — 설정에서 전체 SQLite 데이터베이스를 다운로드해 로컬 백업이나 분석에 사용
- **자동화 테스트 463개** — 단위, 통합, 멀티 유저 API 테스트
- **프레임워크 없는 프론트엔드** — 바닐라 JS, 런타임 의존성 2개, 빌드 단계 없음

## 스크린샷

| | |
|---|---|
| ![Overview](public/screenshots/01-overview.png) | ![Usage trends](public/screenshots/02-trends.png) |
| **개요** — 실시간 세션, KPI 카드, 토큰 내역, 활성 작업 시간 | **사용량 추이** — 오늘/이번 주/이번 달/최근 7일을 같은 시점의 직전 기간과 비교, 이동평균이 포함된 90일 추이 |
| ![Trend charts](public/screenshots/03-trend-charts.png) | ![Sessions](public/screenshots/04-sessions.png) |
| **추이 비교** — 이번 달 vs 지난달 누적, 주간 비교, 프로젝트 모멘텀, 모델 비중 변화 | **세션** — 프로젝트, 모델, 기간, 활성 시간, 토큰, 비용을 정렬 가능한 표로 |
| ![Projects](public/screenshots/05-projects.png) | ![Tools](public/screenshots/06-tools.png) |
| **프로젝트** — 프로젝트별 토큰과 비용, 실시간 검색, 비파괴적 병합 | **도구** — 도구 비용 귀속, MCP 서버 분류, 서브 에이전트 추적 |
| ![Models](public/screenshots/07-models.png) | ![Insights](public/screenshots/08-insights.png) |
| **모델** — 시간에 따른 모델 사용량, 모델별 토큰과 비용 | **인사이트** — 비용 내역, 누적 비용, 요일별 활동, 캐시 효율 |
| ![Productivity](public/screenshots/09-productivity.png) | ![Achievements](public/screenshots/10-achievements.png) |
| **생산성** — 기간 비교가 포함된 효율 지표 | **업적** — 14개 카테고리에 걸친 업적 1200개, 달성 날짜와 함께 |

### 모바일 (iPhone 16 — 393px)

| | | | | |
|---|---|---|---|---|
| ![Overview](public/screenshots/mobile-overview.png) | ![Trends](public/screenshots/mobile-trends.png) | ![Insights](public/screenshots/mobile-insights.png) | ![Productivity](public/screenshots/mobile-productivity.png) | ![Achievements](public/screenshots/mobile-achievements.png) |
| **개요** | **추이** | **인사이트** | **생산성** | **업적** |

## 아키텍처

```
~/.claude/projects/**/*.jsonl
    -> Parser (incremental byte-offset, dedup by message ID)
    -> SQLite (WAL mode, 10 tables)
    -> Aggregator (in-memory pre-computed maps)
    -> HTTP Server (50+ JSON endpoints + SSE)
    -> Frontend (Chart.js, vanilla JS, i18n DE/EN/KO)
```

**멀티 유저 모드:**
```
Sync Agent (client) -> POST /api/sync (API key auth)
    -> Per-user SQLite storage
    -> AggregatorCache (lazy loaded, incremental sync, 30min eviction)
    -> GitHub OAuth sessions
```

**Share API (외부 연동):**
```
OPS -> POST /api/shares (admin key auth) -> project_shares table
Customer browser -> GET /api/public/share/:token -> sanitized project data
```

## 기술 스택

| 계층 | 기술 |
|---|---|
| **런타임** | Node.js >= 20.12 (Express 없이 네이티브 HTTP 서버) |
| **데이터베이스** | better-sqlite3 기반 SQLite (WAL 모드, 트랜잭션) |
| **프론트엔드** | 바닐라 JS + HTML5 + CSS3 (빌드 단계 없음) |
| **차트** | Chart.js 4.x |
| **파일 감시** | Chokidar 4.x |
| **인증** | GitHub OAuth + HttpOnly 세션 쿠키 |
| **암호화** | AES-256-GCM (관리자 API 키) |
| **테스트** | Vitest + Supertest |
| **린트** | ESLint 9 (flat config) |
| **CI** | GitHub Actions |

## Share API

### 엔드포인트

| 엔드포인트 | 인증 | 설명 |
|----------|------|-------------|
| GET /api/share-admin-key | 세션 | 관리자 키 + base URL 조회 (설정 화면) |
| POST /api/share-admin-key | 세션 | 관리자 키 재발급 |
| GET /api/shares | 관리자 키 / 세션 | 전체 공유 목록 |
| POST /api/shares | 관리자 키 / 세션 | 공유 생성 { project, label, expires_in_days } |
| DELETE /api/shares/:id | 관리자 키 / 세션 | 공유 취소 |
| GET /api/shares/projects | 관리자 키 / 세션 | 통계 포함 프로젝트 목록 |
| GET /api/public/share/:token | 공개 | 프로젝트 데이터 조회 (레이트 리밋 적용) |

### 보안

- 공유 토큰: 48자리 16진수 (24바이트 / 192비트 암호학적 난수)
- 관리자 키: 64자리 16진수, `.env`에 저장, 관리용 엔드포인트에 필요
- 레이트 리밋: 공개 엔드포인트에 IP당 분당 30회
- CORS: 지정된 origin으로 제한(ops.celox.io, tracker.celox.io)
- 내부 경로 노출 없음, 프로젝트 목록 열거 불가
- 공유 토큰에 선택적 만료일 설정 가능

### 설정

```bash
# .env에 추가
SHARE_ADMIN_KEY=your-64-char-hex-key
# 또는 설정 -> Share API -> "재발급"에서 생성
```

### OPS 연동

1. Token Tracker 열기 -> 설정 -> Share API
2. Tracker URL과 Share Admin Key 복사
3. OPS의 .env에 추가: TOKEN_TRACKER_BASE_URL, TOKEN_TRACKER_ADMIN_KEY
4. OPS에서: 고객 편집 -> "프로젝트 연결" -> 프로젝트 선택
5. 고객 상세 페이지에 차트, 비용, 세션이 담긴 AI 사용량 탭 표시

### 공개 응답 형식

```json
{
  "label": "Project Label",
  "summary": { "total_cost", "total_sessions", "lines_written", "..." },
  "daily": [{ "date", "messages", "cost", "lines_written", "..." }],
  "sessions": [{ "start", "end", "duration_min", "cost", "model", "..." }]
}
```

## 데이터 연속성 & 복구

`~/.claude/projects`의 JSONL은 **롤링 윈도우**일 뿐입니다 — Claude Code가 오래된
세션 파일을 정리하므로, 트래커의 SQLite DB(`data/tracker.db`)가 전체 이력을
보관하는 장기 저장소입니다. 기기 간, 재설치 간 연속성:

- **호스팅(멀티 유저)**: sync agent가 모든 메시지를 서버로 전송합니다. 기기를
  초기화한 뒤 설정에서 기기 키로 sync agent를 설치하면 같은 계정으로 이어서
  집계됩니다 — 이전 이력은 그대로 유지됩니다.
- **로컬 백업**: `BACKUP_PATH`(선택적으로 `BACKUP_INTERVAL_HOURS`)를 설정하면
  원자적인 `VACUUM INTO` 스냅샷을 남기고 최근 10개만 자동 보관합니다.
- **초기화 후 전체 로컬 복구**: `bash scripts/restore-from-server.sh`가 호스팅
  서버에서 일관된 DB 스냅샷을 가져와 교체하고 재시작합니다. 로컬 JSONL은 그
  위에 다시 파싱되고(메시지 ID로 중복 제거), 업적도 과거 날짜 그대로 자동
  재계산됩니다.

## 문서

| 문서 | 내용 |
|---|---|
| [docs/API.md](docs/API.md) | 모든 라우트, 인증 방식, 파라미터 |
| [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) | 데이터 흐름, 모듈, 그리고 그 이면의 결정들 |
| [docs/METRICS.md](docs/METRICS.md) | 모든 숫자가 의미하는 것 — 예전에 틀렸던 정의들 포함 |
| [docs/CONFIGURATION.md](docs/CONFIGURATION.md) | 모든 환경 변수와, 의도적으로 설정 불가능하게 남겨둔 것 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 설치, 기본 규칙, 불가능한 업적을 만들지 않는 법 |
| [CHANGELOG.md](CHANGELOG.md) | 릴리스 이력 |
| [README_EN.md](README_EN.md) / [README_DE.md](README_DE.md) | 영문/독문 장문 매뉴얼 |

## 링크

- **써보기**: [tracker.celox.io](https://tracker.celox.io)
- **원저자**: [Martin Pfeffer](https://celox.io) | [GitHub](https://github.com/pepperonas)
- **라이선스**: [MIT](LICENSE)

---

<p align="center">
  <b>이 프로젝트가 유용하다면 개발 후원을 고려해 주세요:</b>
</p>

<p align="center">
  <a href="https://www.paypal.com/donate/?business=martinpaush@gmail.com&currency_code=EUR"><img src="https://img.shields.io/badge/Donate-PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white" alt="Donate via PayPal"></a>
</p>
