---
title: "하네스는 죽었다 — gstack·Superpowers 전부 지운 이유 (Opus 5.5)"
source_url: https://youtube.com/watch?v=kcwtzuGaB14
video_id: kcwtzuGaB14
source_type: youtube
lang: ko
analyzed: 2026-09-26
category: 일반학습
tags: ["주제/하네스", "개념/하네스/harness", "주제/스킬", "개념/스킬/claude-skill", "개념/지스택", "개념/슈퍼파워즈", "주제/클로드코드", "개념/클로드코드/hooks", "주제/토큰최적화", "개념/토큰최적화/token-optimization"]
key_concepts: ["하네스", "클로드 스킬", "지스택", "슈퍼파워즈", "훅스", "토큰 최적화"]
status: active
---
# 하네스는 죽었다 — gstack·Superpowers 전부 지운 이유 (Opus 5.5)

## 🧠 이해 (Understand)
- **Summary:** 클로드 코드용 하네스(지스택·슈퍼파워즈)는 모델이 서툴던 시절 필요했던 작업 규칙 묶음이다. 그러나 Claude Opus 4.5 수준에서는 방대한 스킬 문서(스킬 하나당 최대 4만 토큰)가 오히려 토큰을 낭비하고 속도를 떨어뜨리며 진짜 지시사항을 묻어버린다. 슈퍼파워즈는 1% 가능성만 있어도 스킬을 강제 호출하도록 명시해, 오타 수정 하나에 브레인스토밍·계획·체크리스트 절차를 모두 거치게 만든다. 선별 기준은 명확하다: 실제 기능(브라우저 도구 등)을 실행하는 것은 남기고, 모델에게 '어떻게 생각하라'고 가르치는 문서는 삭제한다. 프로젝트별 핵심 규칙만 10줄 이내로 압축해 직접 작성하는 것이 Opus 4.5를 제대로 활용하는 방법이다.
- **Core Message:** 강력해진 모델에게 낡은 하네스는 무기가 아니라 과속 방지턱이므로, 기능 도구만 남기고 '생각하는 법'을 강제하는 문서는 지워야 한다.
> 모델이 약하던 시절엔 이 강제가 안전 장치였습니다. 지금은 그냥 과속 방지턱입니다. 그것도 한 블록에 열 개씩 깔린 과속 방지턱이요.
> 똑똑한 신입한테 200쪽짜리 업무 매뉴얼을 쥐어 준 꼴입니다.
> 도구는 남기고 생각을 가르치는 문서는 지우세요.
❗ 지스택 패키지 하나의 용량이 1.1GB이며, 그 안에 스킬이 53개 포함되어 있다.
❗ 배포 담당 스킬 문서 하나가 168,000바이트(약 4만 토큰)에 달한다.
❗ 슈퍼파워즈 문서에는 '스킬이 적용될 가능성이 1%라도 있으면 반드시 불러라. 선택권은 없다. 협상 대상이 아니다'라고 대문자로 명시되어 있다.

## 📚 핵심 용어
- **하네스:** 클로드 코드에서 모델 위에 씌우는 작업 규칙·절차 문서 묶음. / 말에 채우는 마구처럼, AI가 엉뚱한 방향으로 가지 못하도록 절차를 강제하는 고삐다. / 클로드 스킬(개별 기능 단위)과 달리, 하네스는 여러 스킬과 훅을 묶어 전체 작업 흐름을 통제하는 상위 패키지다.
- **클로드 스킬:** 클로드 코드에서 특정 작업 방식을 정의한 개별 문서 단위. / 회사 업무 매뉴얼의 각 챕터처럼, 배포·리뷰·QA 등 작업마다 하나씩 따라 읽어야 할 설명서다. / MCP 도구는 실제 기능을 실행하지만, 스킬은 실행 없이 '어떻게 할지'를 텍스트로 지시하는 점이 다르다.
- **훅스:** 특정 이벤트(질문, 파일 저장 등) 발생 시 자동으로 실행되는 클로드 코드 설정. / 음식점 주문이 들어올 때마다 자동 울리는 알람처럼, 특정 동작에 묶어 둔 자동 실행 장치다. / 스킬을 지워도 훅은 설정 파일에 남아 계속 동작한다. 스킬은 내용, 훅은 실행 방아쇠라는 점이 다르다.
- **컨텍스트 부패:** 대화 앞부분이 불필요한 문서로 채워져 정작 중요한 지시사항이 묻히는 현상. / 보고서 첫 장부터 규정집 200쪽이 쌓이면 정작 사장 지시사항이 뒤에 묻히는 것과 같다. / 토큰 초과(한도 도달)와 달리, 컨텍스트 부패는 한도 내에서도 우선순위 밀림으로 핵심 지시를 누락시킨다.

## 🚀 실행 (Execute)
- [ ] 클로드 코드에서 '내 스킬 폴더랑 플러그인 목록 전부 보여줘'를 실행해 현재 설치된 하네스·스킬·훅 전수 파악 후, 직접 만들지 않은 대형 묶음(지스택·슈퍼파워즈 등)을 백업 폴더로 이동 — ⏰ 이번 주 내 · ⚡ 1~2시간
  - 담당: 나
  - 이유: 영상 기준 스킬 문서만 52,000자 이상이 매 대화 시작 시 자동 적재되어 토큰과 속도를 낭비하므로, 실태 파악이 정리의 선결 조건이다
- [ ] 훅스 설정 파일을 별도로 열어 하네스 관련 훅 제거 후, 프로젝트별 핵심 규칙을 10줄 이내 직접 작성한 CLAUDE.md로 교체 — ⏰ 2주 내 · ⚡ 2~3시간
  - 담당: 나
  - 이유: 스킬을 지워도 훅은 남아 계속 동작하며, 일반 규칙 문서 없이는 모델이 프로젝트 특화 맥락을 잃기 때문이다
- 자료: 지스택(G-Stack) GitHub 저장소 — 실제 설치 경로와 훅 위치 확인용 (검색 필요)
- 자료: 슈퍼파워즈(Superpower Claude) GitHub 저장소 — 훅 설정 파일 구조 확인용 (검색 필요)
- 자료: Claude Code 공식 문서 — CLAUDE.md 작성 가이드 (docs.anthropic.com, 확인 필요)
- Timeline: 1일차: 현황 파악 및 백업 폴더 이동 → 3일차: 훅 정리 → 1주일 사용 후 체감 속도·누락 여부 점검 → 이상 없으면 백업 폴더 삭제

## 🔗 연결
- 카테고리: [[_category-일반학습]]
- 주제: [[_topic-하네스]] · [[_topic-스킬]] · [[_topic-클로드코드]] · [[_topic-토큰최적화]]
- 핵심 개념: [[_concept-harness|하네스]] · [[_concept-claude-skill|클로드 스킬]] · [[_concept-지스택|지스택]] · [[_concept-슈퍼파워즈|슈퍼파워즈]] · [[_concept-hooks|훅스]] · [[_concept-token-optimization|토큰 최적화]]

## 📝 자막 전문
- [0:00](https://youtube.com/watch?v=kcwtzuGaB14&t=0) 결론부터 말씀드리겠습니다. 지스택이든
- [0:02](https://youtube.com/watch?v=kcwtzuGaB14&t=2) 슈퍼파워즈든 깔려 있는 한네스 지금
- [0:04](https://youtube.com/watch?v=kcwtzuGaB14&t=4) 다 지우세요. 저도 이번 주에 제
- [0:06](https://youtube.com/watch?v=kcwtzuGaB14&t=6) 컴퓨터에 깔린 걸 전부 열어봤습니다.
- [0:08](https://youtube.com/watch?v=kcwtzuGaB14&t=8) 지스택 하나가 차지하는 용량만 1.1
- [0:10](https://youtube.com/watch?v=kcwtzuGaB14&t=10) 기가였습니다. 그 안에 들어 있는
- [0:12](https://youtube.com/watch?v=kcwtzuGaB14&t=12) 스킬이 쉰세계입니다. 배포 스킬
- [0:14](https://youtube.com/watch?v=kcwtzuGaB14&t=14) 하나의 설명서가 3,000줄이
- [0:15](https://youtube.com/watch?v=kcwtzuGaB14&t=15) 넘습니다. 한 때는 이게
- [0:16](https://youtube.com/watch?v=kcwtzuGaB14&t=16) 무기였습니다. 모델이 서툴던 시절에는
- [0:18](https://youtube.com/watch?v=kcwtzuGaB14&t=18) 옆에서 절차를 쥐여 줘야 했으니까요.
- [0:20](https://youtube.com/watch?v=kcwtzuGaB14&t=20) 그런데 지금은 그 절차가 오히려
- [0:22](https://youtube.com/watch?v=kcwtzuGaB14&t=22) 발목을 잡습니다. 토큰은 토큰대로
- [0:24](https://youtube.com/watch?v=kcwtzuGaB14&t=24) 먹고 속도는 속도대로 느려집니다.
- [0:26](https://youtube.com/watch?v=kcwtzuGaB14&t=26) 그리고 정작 제가 시킨 일은
- [0:27](https://youtube.com/watch?v=kcwtzuGaB14&t=27) 빠뜨립니다. 특히 오퍼스 5.5로 로
- [0:29](https://youtube.com/watch?v=kcwtzuGaB14&t=29) 넘어오고 나서 이게 확심해졌습니다.
- [0:31](https://youtube.com/watch?v=kcwtzuGaB14&t=31) 오늘은 제가 직접 젠 숫자로 왜
- [0:33](https://youtube.com/watch?v=kcwtzuGaB14&t=33) 지워야 하는지 보여 드리겠습니다.
- [0:35](https://youtube.com/watch?v=kcwtzuGaB14&t=35) 그리고 그래도 남겨 둘게 뭔지도 같이
- [0:37](https://youtube.com/watch?v=kcwtzuGaB14&t=37) 정리하겠습니다. 먼저 하네스가
- [0:39](https://youtube.com/watch?v=kcwtzuGaB14&t=39) 뭔지부터 짚고 가겠습니다. 하네스는
- [0:41](https://youtube.com/watch?v=kcwtzuGaB14&t=41) 원래 말에 채우는 마구입니다. 말이
- [0:43](https://youtube.com/watch?v=kcwtzuGaB14&t=43) 엉뚱한 대로 못 가게 방향을 잡아주는
- [0:44](https://youtube.com/watch?v=kcwtzuGaB14&t=44) 장치죠. 클로드 코드에서 한스라고
- [0:46](https://youtube.com/watch?v=kcwtzuGaB14&t=46) 하면 모델 위에 더 씌우는 작업 규칙
- [0:49](https://youtube.com/watch?v=kcwtzuGaB14&t=49) 묶음을 말합니다. 대표적인게 두 개
- [0:51](https://youtube.com/watch?v=kcwtzuGaB14&t=51) 있습니다. 하나는 지스택입니다.
- [0:53](https://youtube.com/watch?v=kcwtzuGaB14&t=53) 기획, 리뷰, 배포, QA까지 개발전
- [0:55](https://youtube.com/watch?v=kcwtzuGaB14&t=55) 과정을 스킬로 쪼개 놓은 묶음입니다.
- [0:57](https://youtube.com/watch?v=kcwtzuGaB14&t=57) 다른 하나는 슈퍼파워즈입니다.
- [0:59](https://youtube.com/watch?v=kcwtzuGaB14&t=59) 브레인스토밍 테스트 먼저 짝기,
- [1:01](https://youtube.com/watch?v=kcwtzuGaB14&t=61) 디버인 같은 작업 방식을 강제하는
- [1:03](https://youtube.com/watch?v=kcwtzuGaB14&t=63) 묶음입니다. 둘 다 기터브에서 별을
- [1:05](https://youtube.com/watch?v=kcwtzuGaB14&t=65) 엄청나게 받은 프로젝트입니다. 저도
- [1:07](https://youtube.com/watch?v=kcwtzuGaB14&t=67) 둘 다 깔아서 몇 달을 썼습니다.
- [1:09](https://youtube.com/watch?v=kcwtzuGaB14&t=69) 처음엔 확실히 좋았습니다. 모델이
- [1:10](https://youtube.com/watch?v=kcwtzuGaB14&t=70) 알아서 계획을 안 세우니까 계획
- [1:12](https://youtube.com/watch?v=kcwtzuGaB14&t=72) 세우는 법을 문서로 넣어 준
- [1:14](https://youtube.com/watch?v=kcwtzuGaB14&t=74) 거였거든요. 문제는 모델이 바뀌었는데
- [1:16](https://youtube.com/watch?v=kcwtzuGaB14&t=76) 문서는 그대로라는 겁니다. 느낌으로
- [1:18](https://youtube.com/watch?v=kcwtzuGaB14&t=78) 말하면 반박당하니까 숫자로
- [1:20](https://youtube.com/watch?v=kcwtzuGaB14&t=80) 가겠습니다. 제 클로드 스킬 폴더를
- [1:22](https://youtube.com/watch?v=kcwtzuGaB14&t=82) 열어봤습니다. 폴더가 162개
- [1:24](https://youtube.com/watch?v=kcwtzuGaB14&t=84) 있었습니다.이 스킬들의 설명만 합쳐도
- [1:26](https://youtube.com/watch?v=kcwtzuGaB14&t=86) 52,000자입니다.이 목록은 대화를
- [1:29](https://youtube.com/watch?v=kcwtzuGaB14&t=89) 열 때마다 먼저 깔립니다. 제가 아무
- [1:31](https://youtube.com/watch?v=kcwtzuGaB14&t=91) 말도 안 했는데 이미 그만큼 읽고
- [1:32](https://youtube.com/watch?v=kcwtzuGaB14&t=92) 시작하는 겁니다. 이번엔 지스택 안을
- [1:34](https://youtube.com/watch?v=kcwtzuGaB14&t=94) 열어봤습니다. 배포를 맞는 쉽킬
- [1:36](https://youtube.com/watch?v=kcwtzuGaB14&t=96) 문서가 16만8,000바트였습니다.
- [1:39](https://youtube.com/watch?v=kcwtzuGaB14&t=99) 영어 기준으로 대략 4만 토큰입니다.
- [1:41](https://youtube.com/watch?v=kcwtzuGaB14&t=101) 기획 리뷰 스킬은
- [1:42](https://youtube.com/watch?v=kcwtzuGaB14&t=102) 13만7,000바입니다.
- [1:43](https://youtube.com/watch?v=kcwtzuGaB14&t=103) QA 스킬도 74,000바입니다.
- [1:45](https://youtube.com/watch?v=kcwtzuGaB14&t=105) 스킬 하나를 부를 때마다 이만한
- [1:47](https://youtube.com/watch?v=kcwtzuGaB14&t=107) 문서가 통째로 들어옵니다. 두 세
- [1:49](https://youtube.com/watch?v=kcwtzuGaB14&t=109) 개만이어서 불러도 대화 앞부분이
- [1:51](https://youtube.com/watch?v=kcwtzuGaB14&t=111) 설명서로 꽉 찹니다. 그러면 정작
- [1:53](https://youtube.com/watch?v=kcwtzuGaB14&t=113) 코드가 들어갈 자리가 줄어듭니다.
- [1:55](https://youtube.com/watch?v=kcwtzuGaB14&t=115) 그리고 이건 스킬만의 문제가
- [1:56](https://youtube.com/watch?v=kcwtzuGaB14&t=116) 아닙니다. 지스텍은 질문 도구에
- [1:58](https://youtube.com/watch?v=kcwtzuGaB14&t=118) 후까지 걸어 놨습니다. 모델이 저한테
- [2:00](https://youtube.com/watch?v=kcwtzuGaB14&t=120) 뭘 물어볼 때마다 그 앞뒤로 지스텍
- [2:02](https://youtube.com/watch?v=kcwtzuGaB14&t=122) 스크립트가 먼저 돕니다. 이런게 몇
- [2:04](https://youtube.com/watch?v=kcwtzuGaB14&t=124) 개나 걸려 있는지 저도 열어보기 전에
- [2:06](https://youtube.com/watch?v=kcwtzuGaB14&t=126) 몰랐습니다. 슈퍼파워즈는 더
- [2:08](https://youtube.com/watch?v=kcwtzuGaB14&t=128) 노골적입니다. 시작. 스킬 문서에
- [2:10](https://youtube.com/watch?v=kcwtzuGaB14&t=130) 이런 문장이 대문자로 박혀 있습니다.
- [2:12](https://youtube.com/watch?v=kcwtzuGaB14&t=132) 스킬이 적용될 가능성이 1%라도
- [2:14](https://youtube.com/watch?v=kcwtzuGaB14&t=134) 있으면 반드시 불러라. 선택권은
- [2:16](https://youtube.com/watch?v=kcwtzuGaB14&t=136) 없다. 협상 대상이 아니다. 심지어
- [2:18](https://youtube.com/watch?v=kcwtzuGaB14&t=138) 질문을 하기 전에도 스킬부터
- [2:20](https://youtube.com/watch?v=kcwtzuGaB14&t=140) 확인하라고 적혀 있습니다. 단순한
- [2:22](https://youtube.com/watch?v=kcwtzuGaB14&t=142) 질문이라고 생각하면 그게 핑계라고까지
- [2:24](https://youtube.com/watch?v=kcwtzuGaB14&t=144) 써 놨습니다. 이게 무슨 뜻이냐면요.
- [2:26](https://youtube.com/watch?v=kcwtzuGaB14&t=146) 오타 하나 고쳐 달라고 해도 모델은
- [2:28](https://youtube.com/watch?v=kcwtzuGaB14&t=148) 먼저 스킬 목록을 뒤집니다.
- [2:29](https://youtube.com/watch?v=kcwtzuGaB14&t=149) 브레인스토밍 스킬을 부르고 계획
- [2:31](https://youtube.com/watch?v=kcwtzuGaB14&t=151) 스킬을 부르고 체크리스트를 만듭니다.
- [2:33](https://youtube.com/watch?v=kcwtzuGaB14&t=153) 그다음에야 오타를 고칩니다. 1초면
- [2:35](https://youtube.com/watch?v=kcwtzuGaB14&t=155) 끝날 일에 분 단위가 걸립니다.
- [2:37](https://youtube.com/watch?v=kcwtzuGaB14&t=157) 모델이 약하던 시절엔이 강제가 안전
- [2:39](https://youtube.com/watch?v=kcwtzuGaB14&t=159) 장치였습니다. 지금은 그냥 과속
- [2:41](https://youtube.com/watch?v=kcwtzuGaB14&t=161) 방지턱입니다. 그것도 한 블록에 열
- [2:43](https://youtube.com/watch?v=kcwtzuGaB14&t=163) 개씩 깔린 과속 방지턱이요. 그럼 왜
- [2:45](https://youtube.com/watch?v=kcwtzuGaB14&t=165) 하필 오퍼스 5점 왜서 심해졌을까요?
- [2:48](https://youtube.com/watch?v=kcwtzuGaB14&t=168) 제 체감으로는 모델이 말을 너무 잘
- [2:49](https://youtube.com/watch?v=kcwtzuGaB14&t=169) 듣게 됐기 때문입니다. 예전 모델은
- [2:51](https://youtube.com/watch?v=kcwtzuGaB14&t=171) 긴 규칙을 대충 흘려들었습니다.
- [2:53](https://youtube.com/watch?v=kcwtzuGaB14&t=173) 그래서 3,000줄짜리 문서를 넣어도
- [2:55](https://youtube.com/watch?v=kcwtzuGaB14&t=175) 필요한 부분만 골랐었습니다. 그런데
- [2:57](https://youtube.com/watch?v=kcwtzuGaB14&t=177) 오퍼스 5.5는 적힌 걸 정말 끝까지
- [2:59](https://youtube.com/watch?v=kcwtzuGaB14&t=179) 지키려고 합니다. 체크리스트가
- [3:01](https://youtube.com/watch?v=kcwtzuGaB14&t=181) 20개면 20개를 다 돕니다. 절차에
- [3:03](https://youtube.com/watch?v=kcwtzuGaB14&t=183) 질문하라고 적혀 있으면 굳이 안
- [3:05](https://youtube.com/watch?v=kcwtzuGaB14&t=185) 물어도 될 걸 묻습니다. 그리고이
- [3:07](https://youtube.com/watch?v=kcwtzuGaB14&t=187) 모델은 원래 스스로 계획을 씁니다.
- [3:09](https://youtube.com/watch?v=kcwtzuGaB14&t=189) 스스로 파일을 찾아보고 스스로
- [3:10](https://youtube.com/watch?v=kcwtzuGaB14&t=190) 검증하고 스스로 나눠서 일합니다.
- [3:12](https://youtube.com/watch?v=kcwtzuGaB14&t=192) 거기에 한네스가 자기 절차를 하나 더
- [3:14](https://youtube.com/watch?v=kcwtzuGaB14&t=194) 얹습니다. 절차가 두 벌이 되는
- [3:16](https://youtube.com/watch?v=kcwtzuGaB14&t=196) 겁니다. 모델 머릿속 계획이랑 문서에
- [3:18](https://youtube.com/watch?v=kcwtzuGaB14&t=198) 적힌 계획이 서로 싸웁니다. 그러면
- [3:20](https://youtube.com/watch?v=kcwtzuGaB14&t=200) 모델은 대부분 문서 쪽을 따릅니다.
- [3:22](https://youtube.com/watch?v=kcwtzuGaB14&t=202) 문서가 대문자로 반드시라고 소리치고
- [3:24](https://youtube.com/watch?v=kcwtzuGaB14&t=204) 있으니까요. 결과는 느리고 비싸고
- [3:26](https://youtube.com/watch?v=kcwtzuGaB14&t=206) 엉뚱한데 공을 드린 결과물입니다.
- [3:27](https://youtube.com/watch?v=kcwtzuGaB14&t=207) 똑똑한 신입한테 200쪽짜리 업무
- [3:29](https://youtube.com/watch?v=kcwtzuGaB14&t=209) 매뉴얼을 쥐어 준 꼴입니다. 제일
- [3:31](https://youtube.com/watch?v=kcwtzuGaB14&t=211) 아픈 건 속도나 돈이 아닙니다. 정작
- [3:33](https://youtube.com/watch?v=kcwtzuGaB14&t=213) 챙겨야 할 걸 놓친다는 겁니다.
- [3:35](https://youtube.com/watch?v=kcwtzuGaB14&t=215) 한네스는 일론입니다. 세상 모든
- [3:37](https://youtube.com/watch?v=kcwtzuGaB14&t=217) 프로젝트에 맞게 쓰인 문서라는
- [3:39](https://youtube.com/watch?v=kcwtzuGaB14&t=219) 뜻입니다. 그런데 제 프로젝트에는 제
- [3:41](https://youtube.com/watch?v=kcwtzuGaB14&t=221) 규칙이 따로 있습니다.이 폴더는
- [3:42](https://youtube.com/watch?v=kcwtzuGaB14&t=222) 건드리지 마라.이 작업은 이순서로
- [3:44](https://youtube.com/watch?v=kcwtzuGaB14&t=224) 해라. 같은 것들이요. 한네스 문서가
- [3:46](https://youtube.com/watch?v=kcwtzuGaB14&t=226) 길어질수록 제 규칙은 그 사이에
- [3:48](https://youtube.com/watch?v=kcwtzuGaB14&t=228) 묻입니다. 모델은 체크리스트를 다
- [3:50](https://youtube.com/watch?v=kcwtzuGaB14&t=230) 채우고 뿌듯해야 하는데요. 제가
- [3:51](https://youtube.com/watch?v=kcwtzuGaB14&t=231) 처음에 부탁한 한 줄은 빠져
- [3:53](https://youtube.com/watch?v=kcwtzuGaB14&t=233) 있습니다.이 영상을 만든 세션에서도
- [3:55](https://youtube.com/watch?v=kcwtzuGaB14&t=235) 그랬습니다. 같은 모드 안내문이
- [3:57](https://youtube.com/watch?v=kcwtzuGaB14&t=237) 시작하자마자 두 번 연달아
- [3:58](https://youtube.com/watch?v=kcwtzuGaB14&t=238) 들어왔습니다. 누가 켰는지도 모르는
- [4:00](https://youtube.com/watch?v=kcwtzuGaB14&t=240) 규칙이 제 대화맨 앞을 차지하고 있던
- [4:03](https://youtube.com/watch?v=kcwtzuGaB14&t=243) 겁니다. 규칙끼리 부딪히는 것도
- [4:04](https://youtube.com/watch?v=kcwtzuGaB14&t=244) 문제입니다. 한네스는 이렇게 하라고
- [4:06](https://youtube.com/watch?v=kcwtzuGaB14&t=246) 하고 제 설정 파일은 저렇게 하라고
- [4:08](https://youtube.com/watch?v=kcwtzuGaB14&t=248) 합니다. 둘 중 뭘 따를지 모델이
- [4:10](https://youtube.com/watch?v=kcwtzuGaB14&t=250) 매번 추측합니다. 추측이 틀리면 그
- [4:12](https://youtube.com/watch?v=kcwtzuGaB14&t=252) 비용은 전부 제가 냅니다. 공정하게
- [4:14](https://youtube.com/watch?v=kcwtzuGaB14&t=254) 반대편 얘기도 하겠습니다. 하네스가
- [4:16](https://youtube.com/watch?v=kcwtzuGaB14&t=256) 여전히 쓸모 있는 자리가 있습니다.
- [4:18](https://youtube.com/watch?v=kcwtzuGaB14&t=258) 첫째 팀으로 일할 때입니다. 열명이
- [4:20](https://youtube.com/watch?v=kcwtzuGaB14&t=260) 같은 방식으로 리뷰하고 배포해야
- [4:22](https://youtube.com/watch?v=kcwtzuGaB14&t=262) 한다면 문서로 묶어 두는게 맞습니다.
- [4:24](https://youtube.com/watch?v=kcwtzuGaB14&t=264) 둘째, 처음 시작하는 분들입니다.
- [4:26](https://youtube.com/watch?v=kcwtzuGaB14&t=266) 좋은 작업 순서를 한번 구경하는
- [4:28](https://youtube.com/watch?v=kcwtzuGaB14&t=268) 교재로는 훌륭합니다. 셋째, 진짜
- [4:30](https://youtube.com/watch?v=kcwtzuGaB14&t=270) 기능이 들어 있는 도구입니다.
- [4:32](https://youtube.com/watch?v=kcwtzuGaB14&t=272) 지스택의 브라우저 도구처럼 실제로
- [4:33](https://youtube.com/watch?v=kcwtzuGaB14&t=273) 뭔가를 실행하는 건 프롬프트가 아니라
- [4:35](https://youtube.com/watch?v=kcwtzuGaB14&t=275) 도구입니다. 이건 지우면 기능이
- [4:37](https://youtube.com/watch?v=kcwtzuGaB14&t=277) 사라집니다. 그래서 선을 이렇게
- [4:39](https://youtube.com/watch?v=kcwtzuGaB14&t=279) 긋습니다. 모델이 무언가를 할 수
- [4:41](https://youtube.com/watch?v=kcwtzuGaB14&t=281) 있게 해 주는 건 남깁니다. 모델한테
- [4:43](https://youtube.com/watch?v=kcwtzuGaB14&t=283) 어떻게 생각하라고 가르치는 건
- [4:44](https://youtube.com/watch?v=kcwtzuGaB14&t=284) 지웁니다. 생각하는 법은 이제 모델이
- [4:46](https://youtube.com/watch?v=kcwtzuGaB14&t=286) 우리보다 잘합니다. 그리고 제 말도
- [4:48](https://youtube.com/watch?v=kcwtzuGaB14&t=288) 그대로 믿지 마시고 지우기 전으로
- [4:50](https://youtube.com/watch?v=kcwtzuGaB14&t=290) 직접 재보세요. 그럼 실제로 어떻게
- [4:52](https://youtube.com/watch?v=kcwtzuGaB14&t=292) 정리하는지 보겠습니다. 어렵지
- [4:54](https://youtube.com/watch?v=kcwtzuGaB14&t=294) 않습니다. 클로드 데스크탑 앱에서
- [4:55](https://youtube.com/watch?v=kcwtzuGaB14&t=295) 말로 시키면 됩니다. 첫째, 지금
- [4:57](https://youtube.com/watch?v=kcwtzuGaB14&t=297) 뭐가 깔려 있는지부터 보여 달라고
- [4:59](https://youtube.com/watch?v=kcwtzuGaB14&t=299) 합니다. 내 스킬 폴더랑 플러그인
- [5:01](https://youtube.com/watch?v=kcwtzuGaB14&t=301) 목록 전부 보여 줘.이 이 한 마디면
- [5:03](https://youtube.com/watch?v=kcwtzuGaB14&t=303) 됩니다. 둘째, 내가 직접 만든게
- [5:05](https://youtube.com/watch?v=kcwtzuGaB14&t=305) 아닌 묶음을 고릅니다. 지스택
- [5:07](https://youtube.com/watch?v=kcwtzuGaB14&t=307) 슈퍼파워즈처럼 남이 만든 대형 묶음이
- [5:09](https://youtube.com/watch?v=kcwtzuGaB14&t=309) 1순위입니다. 셋째, 훅을
- [5:10](https://youtube.com/watch?v=kcwtzuGaB14&t=310) 확인합니다. 설정 파일에 걸린 훅은
- [5:12](https://youtube.com/watch?v=kcwtzuGaB14&t=312) 스킬을 지워도 남아 있을 수
- [5:14](https://youtube.com/watch?v=kcwtzuGaB14&t=314) 있습니다. 그래서 설정에 걸린 훅도
- [5:15](https://youtube.com/watch?v=kcwtzuGaB14&t=315) 같이 정리해 달라고 따로 말해야
- [5:17](https://youtube.com/watch?v=kcwtzuGaB14&t=317) 합니다. 넷째, 바로 지우지 말고 한
- [5:19](https://youtube.com/watch?v=kcwtzuGaB14&t=319) 군데로 옮겨 두라고 합니다. 백업
- [5:21](https://youtube.com/watch?v=kcwtzuGaB14&t=321) 폴더로 빼두는 겁니다. 일주일 써
- [5:23](https://youtube.com/watch?v=kcwtzuGaB14&t=323) 보고 아쉬운게 없으면 그때 지웁니다.
- [5:25](https://youtube.com/watch?v=kcwtzuGaB14&t=325) 다섯째, 남길 규칙은 한 장으로
- [5:26](https://youtube.com/watch?v=kcwtzuGaB14&t=326) 줄입니다. 프로젝트마다 꼭 지켜야 할
- [5:28](https://youtube.com/watch?v=kcwtzuGaB14&t=328) 것만 열줄 안팎으로 적어 두면
- [5:30](https://youtube.com/watch?v=kcwtzuGaB14&t=330) 됩니다. 나머지는 모델한테 맡기세요.
- [5:32](https://youtube.com/watch?v=kcwtzuGaB14&t=332) 그게 오퍼스 5.5를 제대로 쓰는
- [5:34](https://youtube.com/watch?v=kcwtzuGaB14&t=334) 방법입니다. 정리하겠습니다. 한에
- [5:36](https://youtube.com/watch?v=kcwtzuGaB14&t=336) 쓰는 모델이 서툴던 시절에 보조
- [5:38](https://youtube.com/watch?v=kcwtzuGaB14&t=338) 바퀴였습니다. 지금 모델은 이미 두
- [5:40](https://youtube.com/watch?v=kcwtzuGaB14&t=340) 발로 달립니다. 보조 바퀴를 단체로
- [5:42](https://youtube.com/watch?v=kcwtzuGaB14&t=342) 달리면 느려지고 커브에서 오히려
- [5:44](https://youtube.com/watch?v=kcwtzuGaB14&t=344) 넘어집니다. 토크은 설명서가 먹고
- [5:46](https://youtube.com/watch?v=kcwtzuGaB14&t=346) 시간은 체크리스트가 먹습니다. 그리고
- [5:48](https://youtube.com/watch?v=kcwtzuGaB14&t=348) 정작 내가 시킨 일은 문서에
- [5:50](https://youtube.com/watch?v=kcwtzuGaB14&t=350) 묻입니다. 도구는 남기고 생각을
- [5:51](https://youtube.com/watch?v=kcwtzuGaB14&t=351) 가르치는 문서는 지우세요. 여러분
- [5:53](https://youtube.com/watch?v=kcwtzuGaB14&t=353) 컴퓨터에는 스킬이 몇 개나 깔려
- [5:55](https://youtube.com/watch?v=kcwtzuGaB14&t=355) 있는지 댓글로 알려 주세요. 지우고
- [5:57](https://youtube.com/watch?v=kcwtzuGaB14&t=357) 나서 얼마나 빨라졌는지도 같이 적어
- [5:59](https://youtube.com/watch?v=kcwtzuGaB14&t=359) 주시면 다음 영상에서 모아보겠습니다.
