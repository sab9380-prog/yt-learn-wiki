---
title: "https://youtube.com/watch?v=uVEA1SKmymg"
source_url: https://youtube.com/watch?v=uVEA1SKmymg
video_id: uVEA1SKmymg
source_type: youtube
lang: ko
analyzed: 2026-06-29
category: 일반학습
tags: ["개념/지식-그래프", "개념/갓노드", "개념/라이덴-커뮤니티-탐지-알고리즘", "개념/트리시터", "개념/신뢰도-태그", "개념/MCP-서버-연동"]
key_concepts: ["지식 그래프(Knowledge Graph)", "갓노드(God Node)", "라이덴 커뮤니티 탐지 알고리즘", "트리시터(Tree-sitter) 로컬 파싱", "신뢰도 태그(추출됨/추론됨/모호함)", "MCP 서버 연동"]
status: active
---
# https://youtube.com/watch?v=uVEA1SKmymg

## 🧠 이해 (Understand)
- **Summary:** Graphify는 코드베이스 전체를 단 한 번 파싱해 지식 그래프로 만드는 AI 코딩 보조 도구다. 기존 AI 어시스턴트가 질문마다 파일을 반복 읽어 토큰을 낭비하는 문제를 해결한다. 코드는 로컬에서만 파싱(API 호출 없음)하므로 보안 민감한 프로젝트에도 적용 가능하다. 라이덴 알고리즘으로 '갓노드(허브)'와 '의외의 연결'을 자동 탐지하며, 팀 전체가 깃 커밋으로 동일한 지식 그래프를 공유할 수 있다.
- **Core Message:** 코드베이스를 질문마다 다시 읽히지 말고, 한 번 지식 그래프로 만들어 두고 팀 전체가 질의하라.
> 코드베이스를 그래프로 매번 다시 읽지 말고 한번 지식 그래프로 만들어 두고 질의하라.
> 도구가 자기 확신의 수준을 솔직히 보여 줘야 우리가 그 위에서 결정을 내릴 수 있다.
> 새 동료도 첫날부터 같은 지도를 보죠.
❗ 2026년 4월 출시 후 두 달 만에 GitHub 스타 6만 개를 돌파했다.
❗ 코드만 다루는 프로젝트라면 API 키 없이 완전 오프라인으로 작동한다.
❗ Claude Code, Cursor, Codex, Gemini 등 20개 이상의 AI 도구와 연동을 지원한다.

## 📚 핵심 용어
- **지식 그래프(Knowledge Graph):** 코드의 함수·클래스·파일을 노드로, 호출·참조 관계를 엣지로 표현한 구조화된 지도. / 지하철 노선도처럼, 역(함수/파일)과 연결선(호출관계)으로 전체 코드 구조를 한눈에 보여준다. / 일반 코드 검색은 키워드로 파일을 하나씩 뒤지지만, 지식 그래프는 연결 관계 자체를 탐색한다.
- **갓노드(God Node):** 그래프에서 가장 많은 노드와 연결된 핵심 허브 파일 또는 함수. / 공항 환승 허브처럼, 이 노드를 거치지 않으면 다른 곳으로 가기 어려운 코드의 중심축이다. / 일반 파일과 달리 갓노드는 의존성이 집중돼 있어, 수정 시 전체 시스템에 파급 효과가 크다.
- **트리시터(Tree-sitter) 파싱:** 코드를 외부 서버 전송 없이 로컬 컴퓨터 안에서만 구문 분석하는 파서 기술. / 계산기처럼 인터넷 연결 없이 내 기기 안에서만 동작해, 코드가 외부로 나가지 않는다. / ChatGPT 등 클라우드 AI는 코드를 서버로 보내지만, 트리시터 파싱은 API 호출 자체가 없다.
- **신뢰도 태그:** 그래프의 각 관계가 코드에서 직접 추출됐는지, 의미 추론인지를 명시하는 레이블. / 의사 진단서의 '확진'과 '의심' 표기처럼, 확실한 사실과 추측을 항상 구분해 표시한다. / 신뢰도 태그가 없는 일반 AI 답변은 확신과 추측을 섞어 제공하지만, 이 태그는 근거 수준을 명시한다.

## 🚀 실행 (Execute)
- [ ] 가장 익숙한 레포에서 `uv tool install graphify` 설치 후 `/graphify.` 명령 실행해 그래프 리포트 확인 — ⏰ 오늘 · ⚡ 30분
  - 담당: 나
  - 이유: 비용·API 키 없이 즉시 실행 가능하며, 코드 구조의 '의외의 연결'을 처음 발견하는 경험이 도구 가치를 체감하는 가장 빠른 방법이다.
- [ ] 팀 레포에 graphify out 폴더를 깃 커밋 규칙에 포함시키고, CI에서 매 커밋마다 자동 재빌드 설정 — ⏰ 이번 주 · ⚡ 2시간
  - 담당: 나 또는 팀 리드
  - 이유: 한 번 설정하면 팀 전체가 동일한 코드 지식 그래프를 공유해 온보딩 비용과 반복 컨텍스트 설명을 줄일 수 있다.
- 자료: Graphify 공식 GitHub 저장소 (검색: 'graphify knowledge graph AI coding' — 정확한 URL은 확인 필요)
- 자료: Tree-sitter 공식 문서: https://tree-sitter.github.io/tree-sitter/
- 자료: Leiden 커뮤니티 탐지 알고리즘 논문 (검색: 'Leiden algorithm community detection')
- 자료: MCP(Model Context Protocol) 서버 개념: Anthropic 공식 문서 확인 필요
- Timeline: 1일차: 개인 레포에 설치·체험 → 3일차: 팀 공유 방식 검토 → 1주차: CI 자동화 설정 완료

## 🔗 연결
- 카테고리: [[_category-일반학습]]
- 핵심 개념: [[_concept-지식-그래프|지식 그래프]] · [[_concept-갓노드|갓노드]] · [[_concept-라이덴-커뮤니티-탐지-알고리즘|라이덴 커뮤니티 탐지 알고리즘]] · [[_concept-트리시터|트리시터]] · [[_concept-신뢰도-태그|신뢰도 태그]] · [[_concept-MCP-서버-연동|MCP 서버 연동]]

## 📝 자막 전문
- [0:00](https://youtube.com/watch?v=uVEA1SKmymg&t=0) 당신의 AI 코딩 어시스턴트는 질문할
- [0:03](https://youtube.com/watch?v=uVEA1SKmymg&t=3) 때마다 코드베이스를 처음부터 다시
- [0:05](https://youtube.com/watch?v=uVEA1SKmymg&t=5) 읽습니다. 그래하고 파일 열고 또
- [0:09](https://youtube.com/watch?v=uVEA1SKmymg&t=9) 그래하고 매번 똑같은 일을 반복하죠.
- [0:12](https://youtube.com/watch?v=uVEA1SKmymg&t=12) 그러는 사이 컨텍스트 창은 가득 차고
- [0:15](https://youtube.com/watch?v=uVEA1SKmymg&t=15) 파일과 파일의 연결은 놓칩니다.
- [0:18](https://youtube.com/watch?v=uVEA1SKmymg&t=18) 그래피파이는이 방식을 뒤집습니다.
- [0:21](https://youtube.com/watch?v=uVEA1SKmymg&t=21) 코드 전체를 단 한 번 질리 가능한
- [0:24](https://youtube.com/watch?v=uVEA1SKmymg&t=24) 지식 그래프로 바꿉니다.이
- [0:26](https://youtube.com/watch?v=uVEA1SKmymg&t=26) 도구는 2026년 4월의 세상에
- [0:29](https://youtube.com/watch?v=uVEA1SKmymg&t=29) 나와서 두 달 만에 기터브 스타 6만
- [0:32](https://youtube.com/watch?v=uVEA1SKmymg&t=32) 개를 넘겼습니다. Y 콤비네이터도
- [0:34](https://youtube.com/watch?v=uVEA1SKmymg&t=34) 투자했죠. 오늘은 이게 왜 AI
- [0:37](https://youtube.com/watch?v=uVEA1SKmymg&t=37) 코딩의 다음 단계인지 그리고 당신
- [0:40](https://youtube.com/watch?v=uVEA1SKmymg&t=40) 내포에 지금 바로 어떻게 적용하는지
- [0:43](https://youtube.com/watch?v=uVEA1SKmymg&t=43) 끝까지 풀어 드립니다. AI
- [0:45](https://youtube.com/watch?v=uVEA1SKmymg&t=45) 어시스턴트는 당신의 코드베이스를
- [0:47](https://youtube.com/watch?v=uVEA1SKmymg&t=47) 통째로 기억하지 않습니다. 그래서
- [0:50](https://youtube.com/watch?v=uVEA1SKmymg&t=50) 인증이 데이터베이스랑 어떻게 연결돼?
- [0:53](https://youtube.com/watch?v=uVEA1SKmymg&t=53) 같은 질문마다 파일을 뒤지고 스니펫을
- [0:56](https://youtube.com/watch?v=uVEA1SKmymg&t=56) 다시 익죠. 문제는 세 가지예요.
- [0:59](https://youtube.com/watch?v=uVEA1SKmymg&t=59) 첫째, 같은 컨텍스트를 반복해서
- [1:02](https://youtube.com/watch?v=uVEA1SKmymg&t=62) 토큰으로 태우니 느리고 비쌉니다.
- [1:05](https://youtube.com/watch?v=uVEA1SKmymg&t=65) 둘째, 파일을 하나씩 보다 보면
- [1:07](https://youtube.com/watch?v=uVEA1SKmymg&t=67) 모듈에 흩어진 연결을 놓칩니다.
- [1:10](https://youtube.com/watch?v=uVEA1SKmymg&t=70) 셋째, 사람이 매번이 파일도 봐, 저
- [1:13](https://youtube.com/watch?v=uVEA1SKmymg&t=73) 함수도 봐 하고 떠먹여 줘야 하죠.
- [1:16](https://youtube.com/watch?v=uVEA1SKmymg&t=76) 리뷰 한 번, 디버깅 한 번마다 같은
- [1:18](https://youtube.com/watch?v=uVEA1SKmymg&t=78) 설명을 반복하니 생각보다 큰
- [1:20](https://youtube.com/watch?v=uVEA1SKmymg&t=80) 비용입니다. 그래피파이의 사용법은
- [1:23](https://youtube.com/watch?v=uVEA1SKmymg&t=83) 놀랄만큼 단순합니다. 어시스턴트
- [1:26](https://youtube.com/watch?v=uVEA1SKmymg&t=86) 안에서 슬러시그래피파이.이
- [1:29](https://youtube.com/watch?v=uVEA1SKmymg&t=89) 한 줄이면 끝이에요. 그러면
- [1:31](https://youtube.com/watch?v=uVEA1SKmymg&t=91) 프로젝트를 분석해 세 개의 파일을
- [1:33](https://youtube.com/watch?v=uVEA1SKmymg&t=93) 만들어 줍니다. 그래프.html은
- [1:36](https://youtube.com/watch?v=uVEA1SKmymg&t=96) 노드를 클릭하고 검색하는 인터랙티브
- [1:39](https://youtube.com/watch?v=uVEA1SKmymg&t=99) 시각화고요. 그래프리포트.md는
- [1:41](https://youtube.com/watch?v=uVEA1SKmymg&t=101) MD는 핵심 개념과 의외의 연결,
- [1:44](https://youtube.com/watch?v=uVEA1SKmymg&t=104) 추천 질문을 정리해 줍니다. 그래프.
- [1:47](https://youtube.com/watch?v=uVEA1SKmymg&t=107) 제이스는 한 번 만들면 파일을 다시
- [1:50](https://youtube.com/watch?v=uVEA1SKmymg&t=110) 파싱하지 않고 언제든 물어볼 수 있는
- [1:52](https://youtube.com/watch?v=uVEA1SKmymg&t=112) 본체죠. 그럼이 그래프 안에는 뭐가
- [1:55](https://youtube.com/watch?v=uVEA1SKmymg&t=115) 들어갈까요? 그래피파이는 코드를
- [1:58](https://youtube.com/watch?v=uVEA1SKmymg&t=118) 노드와 엣지로 바꿉니다. 함수와
- [2:01](https://youtube.com/watch?v=uVEA1SKmymg&t=121) 클래스, 파일이 노드가 되고 호출과
- [2:04](https://youtube.com/watch?v=uVEA1SKmymg&t=124) 참조가 엣지가 되죠. 그런데 코드만이
- [2:07](https://youtube.com/watch?v=uVEA1SKmymg&t=127) 아닙니다. 문서와 PDF, 이미지,
- [2:10](https://youtube.com/watch?v=uVEA1SKmymg&t=130) 심지어 영상과 유튜브 링크까지 같은
- [2:13](https://youtube.com/watch?v=uVEA1SKmymg&t=133) 그래프로 들어옵니다. 정말 똑똑한
- [2:16](https://youtube.com/watch?v=uVEA1SKmymg&t=136) 부분은 이거예요. 노트, Y, 핵
- [2:19](https://youtube.com/watch?v=uVEA1SKmymg&t=139) 같은 주석과 독스트링을 따로 노드로
- [2:21](https://youtube.com/watch?v=uVEA1SKmymg&t=141) 뽑아냅니다. 코드가 무엇을 하는짓뿐
- [2:24](https://youtube.com/watch?v=uVEA1SKmymg&t=144) 아니라 왜 그렇게 짰는지까지 그래프에
- [2:27](https://youtube.com/watch?v=uVEA1SKmymg&t=147) 남는 거죠.
- [2:29](https://youtube.com/watch?v=uVEA1SKmymg&t=149) 앱코드와 DB 스키마, 인프라가 한
- [2:31](https://youtube.com/watch?v=uVEA1SKmymg&t=151) 그래프에 모이면 어시스턴트가 전체
- [2:34](https://youtube.com/watch?v=uVEA1SKmymg&t=154) 그림을 봅니다. 많은 분들이 가장
- [2:36](https://youtube.com/watch?v=uVEA1SKmymg&t=156) 궁금해하는 보안을 짚고 갈게요.
- [2:39](https://youtube.com/watch?v=uVEA1SKmymg&t=159) 그래피파이는 코드를 트리시터라는
- [2:42](https://youtube.com/watch?v=uVEA1SKmymg&t=162) 파서로 당신 컴퓨터 안에서만
- [2:44](https://youtube.com/watch?v=uVEA1SKmymg&t=164) 파싱합니다.
- [2:46](https://youtube.com/watch?v=uVEA1SKmymg&t=166) 28개 언어 문법을 지원하죠. 코드
- [2:49](https://youtube.com/watch?v=uVEA1SKmymg&t=169) 추출에는 API 호출이 단 한 번도
- [2:51](https://youtube.com/watch?v=uVEA1SKmymg&t=171) 없습니다. 코드만 다루는 프로젝트라면
- [2:55](https://youtube.com/watch?v=uVEA1SKmymg&t=175) API 키조차 필요 없이 완전히
- [2:57](https://youtube.com/watch?v=uVEA1SKmymg&t=177) 오프라인으로 돌아갑니다.
- [2:59](https://youtube.com/watch?v=uVEA1SKmymg&t=179) 모델은 문서나 PDF, 영상처럼
- [3:02](https://youtube.com/watch?v=uVEA1SKmymg&t=182) 의미를 해석할 자료에만 당신 이골은
- [3:05](https://youtube.com/watch?v=uVEA1SKmymg&t=185) 백엔드로 호출되고요.
- [3:07](https://youtube.com/watch?v=uVEA1SKmymg&t=187) 즉 보안 민감한 코드를 웹로 보내지
- [3:09](https://youtube.com/watch?v=uVEA1SKmymg&t=189) 않고도 전체 구조 분석을 받는
- [3:11](https://youtube.com/watch?v=uVEA1SKmymg&t=191) 겁니다. 도이퍼들이 확 낮아지죠.
- [3:14](https://youtube.com/watch?v=uVEA1SKmymg&t=194) 이제 그래피파이가 진짜 빛나는
- [3:16](https://youtube.com/watch?v=uVEA1SKmymg&t=196) 부분입니다. 단순히 그래프만 그리는게
- [3:19](https://youtube.com/watch?v=uVEA1SKmymg&t=199) 아니라 라이덴이라는 커뮤니티 탐지
- [3:22](https://youtube.com/watch?v=uVEA1SKmymg&t=202) 알고리즘으로 그래프를 분석합니다.
- [3:24](https://youtube.com/watch?v=uVEA1SKmymg&t=204) 그러면 두 가지가 드러나요. 첫째,
- [3:27](https://youtube.com/watch?v=uVEA1SKmymg&t=207) 갓노드. 가장 많이 연결된 허브들이라
- [3:30](https://youtube.com/watch?v=uVEA1SKmymg&t=210) 어디부터 이해해야 할지 한 눈에
- [3:32](https://youtube.com/watch?v=uVEA1SKmymg&t=212) 보입니다. 둘째, 의외의 연결. 서로
- [3:36](https://youtube.com/watch?v=uVEA1SKmymg&t=216) 다른 파일에 흩어져 있는데도 강하게
- [3:38](https://youtube.com/watch?v=uVEA1SKmymg&t=218) 엮긴 관계를 얼마나 뜻바인지 순위까지
- [3:41](https://youtube.com/watch?v=uVEA1SKmymg&t=221) 먹겨 보여주죠. 사람이 다 읽어도 안
- [3:44](https://youtube.com/watch?v=uVEA1SKmymg&t=224) 보이던 숨은 의존성을 그래프가
- [3:46](https://youtube.com/watch?v=uVEA1SKmymg&t=226) 구조적으로 찾아냅니다. 그래프가
- [3:49](https://youtube.com/watch?v=uVEA1SKmymg&t=229) 똑똑한만큼 함정도 있습니다. 출론한
- [3:52](https://youtube.com/watch?v=uVEA1SKmymg&t=232) 관계를 사실처럼 믿어 버리면
- [3:54](https://youtube.com/watch?v=uVEA1SKmymg&t=234) 위험하죠.
- [3:56](https://youtube.com/watch?v=uVEA1SKmymg&t=236) 그래피파인은 이걸 정직하게
- [3:58](https://youtube.com/watch?v=uVEA1SKmymg&t=238) 처리합니다. 모든 출론된 관계에
- [4:01](https://youtube.com/watch?v=uVEA1SKmymg&t=241) 신뢰도 태그를 붙여요. 추출됨,
- [4:04](https://youtube.com/watch?v=uVEA1SKmymg&t=244) 추론됨, 모호함. 코드에서 직접 뽑은
- [4:08](https://youtube.com/watch?v=uVEA1SKmymg&t=248) 건 추출됨. 의미로 미루어 연결한 건
- [4:11](https://youtube.com/watch?v=uVEA1SKmymg&t=251) 추론됨으로 표시되죠.
- [4:13](https://youtube.com/watch?v=uVEA1SKmymg&t=253) 그래서 확실히 찾은 것과 그래프가
- [4:16](https://youtube.com/watch?v=uVEA1SKmymg&t=256) 추측한 것을 항상 구분할 수
- [4:18](https://youtube.com/watch?v=uVEA1SKmymg&t=258) 있습니다. 도구가 자기 확신의 수준을
- [4:21](https://youtube.com/watch?v=uVEA1SKmymg&t=261) 솔직히 보여 줘야 우리가 그 위에서
- [4:24](https://youtube.com/watch?v=uVEA1SKmymg&t=264) 결정을 내릴 수 있으니까요. 그래프를
- [4:26](https://youtube.com/watch?v=uVEA1SKmymg&t=266) 만들었으면 이제 그랩 대신 질문하면
- [4:29](https://youtube.com/watch?v=uVEA1SKmymg&t=269) 됩니다. 어시스턴트에서 그래피파이
- [4:32](https://youtube.com/watch?v=uVEA1SKmymg&t=272) 쿼리 그리고 자연어로 물으세요.
- [4:35](https://youtube.com/watch?v=uVEA1SKmymg&t=275) 인증과 데이터베이스를 잇는게 뭐야?
- [4:38](https://youtube.com/watch?v=uVEA1SKmymg&t=278) 처럼요. 두 노드 사이 경로가
- [4:40](https://youtube.com/watch?v=uVEA1SKmymg&t=280) 궁금하면 그래피파이 패스. 특정 개념
- [4:44](https://youtube.com/watch?v=uVEA1SKmymg&t=284) 설명이 필요하면 그래피파이
- [4:46](https://youtube.com/watch?v=uVEA1SKmymg&t=286) 익스플레인. 그래프를 MCP 서버로
- [4:49](https://youtube.com/watch?v=uVEA1SKmymg&t=289) 띄우면 어시스턴트가 구조화된 도구로
- [4:52](https://youtube.com/watch?v=uVEA1SKmymg&t=292) 직접 접근할 수도 있죠. 여기까지
- [4:54](https://youtube.com/watch?v=uVEA1SKmymg&t=294) 오셨다면이 채널이 마음에 드실
- [4:56](https://youtube.com/watch?v=uVEA1SKmymg&t=296) 거예요. 매주 이런 실전 개발 도구를
- [4:59](https://youtube.com/watch?v=uVEA1SKmymg&t=299) 다루니 구독해 주세요. 자,이어서
- [5:02](https://youtube.com/watch?v=uVEA1SKmymg&t=302) 팀으로 넘어갑니다. 개인으로도 좋지만
- [5:05](https://youtube.com/watch?v=uVEA1SKmymg&t=305) 진짜 힘은 팀에서 나옵니다.
- [5:07](https://youtube.com/watch?v=uVEA1SKmymg&t=307) 그래피파이 아웃폴더를 기세 커밋하도록
- [5:10](https://youtube.com/watch?v=uVEA1SKmymg&t=310) 설계돼 있어요. 한 사람이 만들어
- [5:12](https://youtube.com/watch?v=uVEA1SKmymg&t=312) 커밋하면 나머지는 풀만 받아도
- [5:15](https://youtube.com/watch?v=uVEA1SKmymg&t=315) 어시스턴트가 곧장 그 그래프를
- [5:17](https://youtube.com/watch?v=uVEA1SKmymg&t=317) 익습니다. 커밋을 걸면 매 커밋마다
- [5:20](https://youtube.com/watch?v=uVEA1SKmymg&t=320) 자동으로 다시 빌드 코드는 AS만
- [5:24](https://youtube.com/watch?v=uVEA1SKmymg&t=324) 다시 뽑으니 API 비용도 없죠.
- [5:27](https://youtube.com/watch?v=uVEA1SKmymg&t=327) 거기에 깃 머지 드라이버까지 있어서
- [5:29](https://youtube.com/watch?v=uVEA1SKmymg&t=329) 두 명이 동시에 커밋해도 충돌 마커
- [5:31](https://youtube.com/watch?v=uVEA1SKmymg&t=331) 없이 합쳐집니다. 한마디로
- [5:34](https://youtube.com/watch?v=uVEA1SKmymg&t=334) 코드베이스에 대한 공유된 기억 메모리
- [5:36](https://youtube.com/watch?v=uVEA1SKmymg&t=336) 레이어가 생기는 겁니다. 새 동료도
- [5:39](https://youtube.com/watch?v=uVEA1SKmymg&t=339) 첫날부터 같은 지도를 보죠. 오늘
- [5:41](https://youtube.com/watch?v=uVEA1SKmymg&t=341) 내용을 실모 체크리스트로 정리할게요.
- [5:45](https://youtube.com/watch?v=uVEA1SKmymg&t=345) 첫째, 설치. UV툴 인스톨러로
- [5:48](https://youtube.com/watch?v=uVEA1SKmymg&t=348) 그래피파이를 깔면 됩니다. 패키지
- [5:51](https://youtube.com/watch?v=uVEA1SKmymg&t=351) 이름엔 Y가 하나 더 붙고 명령어는
- [5:53](https://youtube.com/watch?v=uVEA1SKmymg&t=353) 그냥 그래피파이예요.
- [5:56](https://youtube.com/watch?v=uVEA1SKmymg&t=356) 둘째, 그래피파이 인스톨러로
- [5:58](https://youtube.com/watch?v=uVEA1SKmymg&t=358) 어시스턴트에 등록하세요. 클로드
- [6:01](https://youtube.com/watch?v=uVEA1SKmymg&t=361) 코드 커서 코덱스 제미나이까지
- [6:04](https://youtube.com/watch?v=uVEA1SKmymg&t=364) 20개가 넘는 도구를 지원합니다.
- [6:07](https://youtube.com/watch?v=uVEA1SKmymg&t=367) 셋째, 레포 안에서 슬래시
- [6:09](https://youtube.com/watch?v=uVEA1SKmymg&t=369) 그래피파이점을 돌려 보세요. 코드만
- [6:12](https://youtube.com/watch?v=uVEA1SKmymg&t=372) 있다면 비용도 키도 없이 끝납니다.
- [6:15](https://youtube.com/watch?v=uVEA1SKmymg&t=375) 넷째, 문서나 PDF까지 넣고 싶을
- [6:18](https://youtube.com/watch?v=uVEA1SKmymg&t=378) 때만 모델 백엔드를 붙이면 됩니다.
- [6:21](https://youtube.com/watch?v=uVEA1SKmymg&t=381) 정리하면 오늘 핵심은 한 문장입니다.
- [6:24](https://youtube.com/watch?v=uVEA1SKmymg&t=384) 코드베이스를 그래프로 매번 다시 읽지
- [6:27](https://youtube.com/watch?v=uVEA1SKmymg&t=387) 말고 한번 지식 그래프로 만들어 두고
- [6:30](https://youtube.com/watch?v=uVEA1SKmymg&t=390) 지리하라. 그래피파이는 코드를
- [6:32](https://youtube.com/watch?v=uVEA1SKmymg&t=392) 로컬에서 그래프로 바꾸고 감로드와
- [6:35](https://youtube.com/watch?v=uVEA1SKmymg&t=395) 숨은 연결을 드러내고 그 지도를 팀
- [6:38](https://youtube.com/watch?v=uVEA1SKmymg&t=398) 전체가 공유하게 해 줍니다. 오늘 딱
- [6:41](https://youtube.com/watch?v=uVEA1SKmymg&t=401) 하나만 해 보세요. 가장 잘하는
- [6:43](https://youtube.com/watch?v=uVEA1SKmymg&t=403) 레포의 슬래시 그래피파이 점을 한번
- [6:46](https://youtube.com/watch?v=uVEA1SKmymg&t=406) 돌려 보는 겁니다. 리포트의 의외에
- [6:49](https://youtube.com/watch?v=uVEA1SKmymg&t=409) 연결해서 이게 여기 엮겨 있었어 하는
- [6:52](https://youtube.com/watch?v=uVEA1SKmymg&t=412) 순간을 분명히 만나실 거예요. 이런
- [6:55](https://youtube.com/watch?v=uVEA1SKmymg&t=415) 실전 도구의 설이 유용하셨다면 구독
- [6:57](https://youtube.com/watch?v=uVEA1SKmymg&t=417) 부탁드립니다. 그리고 댓글로 알려
- [7:00](https://youtube.com/watch?v=uVEA1SKmymg&t=420) 주세요. 여러분은 새 코드이를 파악할
- [7:03](https://youtube.com/watch?v=uVEA1SKmymg&t=423) 때 가장 먼저 무엇부터 보시나요?
