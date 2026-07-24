---
type: synth
concept: graph-rag
---

# 🧭 그래프 RAG — 종합

> 자동 생성 · 3개 노트 종합 (수정 금지)

# 그래프 RAG (Graph RAG) — 종합 노트

## 핵심 공통 메시지

세 노트 모두 같은 문제를 지적합니다: **AI가 질문마다 전체 코드/문서를 반복해서 읽는 것은 토큰 낭비이자 비용 낭비**. 그래프 RAG는 이 반복 비용("rereading tax")을 없애기 위해, 문서나 코드를 **한 번만 읽어 관계 지도(그래프)로 만들어두고** 이후엔 그 지도를 질의하는 방식입니다 [[2026-06-29-youtube-com-watch-v-uVEA1SKmymg]] [[2026-06-11-Claude-Code-Graphify-Insane-Agentic-OS]] [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]].

---

## 각 노트의 강조점 차이

| 관점 | 강조 내용 | 출처 |
|------|-----------|------|
| **무엇인가** | 코드의 함수·파일을 노드로, 호출·참조를 엣지로 표현한 "지하철 노선도" | [[2026-06-29-youtube-com-watch-v-uVEA1SKmymg]] |
| **왜 쓰는가** | Naive RAG(단순 키워드 검색) 대비 성능 2배↑, 비용·시간 절감 | [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]] |
| **어디에 쓰는가** | 코드베이스 × Claude Code 결합 → 팀 전체 공유 "두뇌" | [[2026-06-11-Claude-Code-Graphify-Insane-Agentic-OS]] |

---

## 그래프 RAG만의 차별점

- **일반 RAG vs 그래프 RAG**: 일반 RAG는 키워드로 문서를 하나씩 찾는 것, 그래프 RAG는 문서들 *사이의 관계 자체*를 탐색 [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]
- **갓노드 자동 탐지**: 가장 많이 연결된 핵심 허브(수정 시 파급력 큰 파일)를 라이덴 알고리즘으로 자동 발견 [[2026-06-29-youtube-com-watch-v-uVEA1SKmymg]]
- **신뢰도 태그**: 각 관계가 "코드에서 직접 추출된 것"인지 "추론된 것"인지를 명시 → 불확실성을 숨기지 않음 [[2026-06-29-youtube-com-watch-v-uVEA1SKmymg]]
- **팀 공유**: 지식 그래프를 git에 커밋 → 신규 팀원도 첫날부터 동일한 지도 [[2026-06-11-Claude-Code-Graphify-Insane-Agentic-OS]]

---

## 주의점·상충

- **복잡도 주의**: 그래프 RAG는 설정이 복잡하므로, 문서가 적다면 Obsidian(레벨 4) 같은 단순한 방식이 오히려 99% 해결책 [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]
- **단계적 접근 권장**: "Level 7이 필요한지 명확하지 않다면, Obsidian부터 시작하라"는 조언 — 과도한 구현이 오히려 부담 [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]
- **보안 이점**: Graphify 구현체는 로컬 파싱(Tree-sitter) 방식으로 코드가 외부 서버에 나가지 않음 [[2026-06-29-youtube-com-watch-v-uVEA1SKmymg]]

---

## 실전 적용

1. **개인·소규모**: Obsidian부터 시작, 필요할 때 그래프 RAG로 업그레이드 [[2026-05-22-The-7-Levels-of-Claude-Code-RAG]]
2. **코드베이스 관리**: `graphify .` 한 번 실행 → 그래프 생성 → CI에 자동 재빌드 등록 [[2026-06-29-youtube-com-watch-v-uVEA1SKmymg]]
3. **팀 도입**: 지식 그래프를 git에 포함 → 온보딩 비용 절감, 컨텍스트 반복 설명 제거 [[2026-06-11-Claude-Code-Graphify-Insane-Agentic-OS]]

---

## 한 줄 정의

> **그래프 RAG**란, 문서·코드를 매번 처음부터 읽히는 대신 *관계 지도(그래프

---
- 개념 페이지: [[_concept-graph-rag]]
- [[INDEX]]
