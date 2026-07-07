---
title: "Anthropic 개발자가 직접 공개한 Claude Fable 5 사용법 (핵심은 언노운 찾기)"
source_url: https://youtube.com/watch?v=PNMBRgc0y2g
video_id: PNMBRgc0y2g
source_type: youtube
lang: ko
analyzed: 2026-07-07
category: 일반학습
tags: ["개념/언노운", "주제/컨텍스트관리", "개념/컨텍스트관리/context-engineering", "개념/블라인드스팟-패스", "개념/브레인스토밍-프로토타입", "개념/인터뷰-패턴", "개념/구현-노트", "주제/ANTHROPIC", "개념/ANTHROPIC/anthropic"]
key_concepts: ["언노운(Unknown)", "컨텍스트 엔지니어링", "블라인드스팟 패스", "브레인스토밍 프로토타입", "인터뷰 패턴", "구현 노트"]
status: active
---
# Anthropic 개발자가 직접 공개한 Claude Fable 5 사용법 (핵심은 언노운 찾기)

## 🧠 이해 (Understand)
- **Summary:** Anthropic의 Claude Code 개발자 Thariq가 Claude 5 사용법을 공개한 글을 분석한다. 핵심 개념은 '언노운(Unknown)' — AI가 추측으로 채워야 하는 나와 AI 사이의 정보 공백이다. Claude 5 시대에는 결과 품질이 모델 성능이 아니라 사용자가 언노운을 얼마나 빨리 발굴하느냐에 달려 있다. 구현 전(블라인드스팟 패스·브레인스토밍·인터뷰·레퍼런스·구현 계획서), 구현 중(구현 노트), 구현 후(피치 문서·퀴즈) 총 8가지 패턴으로 언노운을 줄이는 반복 과정이 핵심이다. 실제 Claude 5 공식 런칭 영상 편집 사례에서, 색보정 시안을 뽑기 전에 색보정 자체를 먼저 배운 장면이 이 전략의 본질을 보여준다.
- **Core Message:** AI 결과물의 품질은 모델 성능이 아니라 내가 '모른다는 것조차 모르는 것(언노운)'을 얼마나 빨리 발굴하느냐에 달려 있으므로, AI에게 더 시키기 전에 AI로 나 자신을 먼저 업그레이드하라.
> Fable 5는 결과물의 품질이 모델의 성능이 아니라, 내 언노운을 밝혀내는 능력에 발목 잡히는 첫 번째 모델이다.
> AI가 한 일을 내가 설명하지 못하면 아직 내 코드가 아니다.
> 브레인스토밍과 인터뷰, 프로토타입, 레퍼런스는 전부, 고치기 비싸지기 전에 내가 몰랐던 걸 알아내는 가장 싼 방법이다.
❗ Claude 5 공식 런칭 영상의 편집 전체가 Claude Code로 이루어졌으며, 개발자 본인에게 영상 편집은 완전히 처음인 분야였다.
❗ Anthropic 내부 개발자조차 '색보정 시안을 고르지 못했다'—도구를 만드는 사람도 자신의 언노운을 실시간으로 발견하며 일한다.
❗ 이 글은 X(트위터)에 올라온 지 며칠 만에 조회수 270만을 넘겼다.

## 📚 핵심 용어
- **언노운(Unknown):** 내가 모른다는 사실조차 인식하지 못해 AI가 혼자 추측으로 채워야 하는 정보 공백. / 요리사에게 '맛있게 해줘'라고만 하면 취향을 모르니 자기 기준으로 만드는 것처럼, AI도 내 공백을 자기 추측으로 채운다. / 프롬프트(내가 아는 것)는 지도, 언노운은 지도에 없는 실제 영토의 빈칸. 프롬프트를 잘 써도 언노운은 따로 발굴해야 한다.
- **블라인드스팟 패스:** 낯선 영역에서 작업 시작 전, AI에게 내가 모르는 것을 먼저 알려달라고 요청하는 사전 점검 프롬프트 패턴. / 처음 가는 등산로 전에 '이 코스에서 초보자가 자주 놓치는 위험 구간이 어디야?'라고 묻는 것과 같다. / 일반 질문이 '어떻게 해?'라면, 블라인드스팟 패스는 '내가 뭘 물어봐야 하는지 먼저 알려줘'—질문의 방향이 반대다.
- **구현 노트:** AI가 구현 중 계획에서 이탈하는 결정을 할 때 보수적 선택을 고르고 그 이유를 기록하는 임시 메모 파일. / 공사 현장에서 설계와 달라진 부분을 현장 일지에 적어두는 것처럼, AI의 변경 이유를 추적하는 로그다. / 커밋 메시지가 '무엇이 바뀌었는지' 기록이라면, 구현 노트는 '왜 계획에서 벗어났는지' 의사결정 이유를 기록한다.
- **퀴즈 패턴:** AI가 작업한 변경 내용을 보고서로 정리한 뒤, 사용자가 그 내용을 설명할 수 있는지 퀴즈로 확인하는 구현 후 검증 방식. / 수업 후 선생님이 낸 문제를 못 풀면 배웠다고 할 수 없듯, AI가 짠 코드를 내가 설명 못 하면 머지하지 않는다. / 코드 리뷰가 '결과물이 맞는가'를 보는 것이라면, 퀴즈 패턴은 '내가 그 결과물을 이해하는가'를 검증한다.

## 🚀 실행 (Execute)
- [ ] 다음 AI 작업의 첫 프롬프트를 '이 작업에서 내 언노운부터 찾아줘 (블라인드스팟 패스)'로 시작하고, 그 결과를 메모해 기존 방식과 결과물 품질을 비교한다. — ⏰ 오늘~이번 주 첫 AI 작업 시 · ⚡ 5분 (프롬프트 변경) + 작업 후 10분 회고
  - 담당: 나
  - 이유: 언노운 발굴이 결과 품질의 병목임을 직접 체감해야 이후 8가지 패턴 도입의 동기가 생긴다.
- [ ] 긴 AI 세션 후 '변경 내용을 맥락과 함께 정리하고 맨 아래에 퀴즈를 내줘' 프롬프트를 추가해 퀴즈 만점 전 결과물 적용을 보류하는 규칙을 도입한다. — ⏰ 이번 주 · ⚡ 세션당 10~15분 추가
  - 담당: 나
  - 이유: AI 산출물을 그대로 쓰다가 내용을 모르는 채 축적되면 나중에 수정·설명이 불가능해지는 리스크를 사전 차단할 수 있다.
- [ ] 원글(Thariq의 'Fable Field Guide') 영문 원문을 직접 읽고, 영상에서 다루지 않은 세부 프롬프트 예시와 코드베이스 레퍼런스 활용 방식을 확인한다. — ⏰ 이번 주 · ⚡ 30~60분
  - 담당: 나
  - 이유: 영상은 8가지 패턴을 요약했지만 원문에는 실제 프롬프트 문구와 Remotion·ffmpeg 연동 같은 구체적 구현 예시가 포함되어 있어 실행력이 높아진다.
- 자료: Thariq의 원글 'Fable Field Guide: Finding My Unknowns' — X(트위터) 또는 본인 블로그 검색 (확인 필요: 정확한 URL은 영상에 미언급)
- 자료: Remotion — 코드로 영상을 만드는 React 기반 도구 (https://www.remotion.dev, 실제 존재 확인됨)
- 자료: Whisper — OpenAI의 오픈소스 음성 인식 모델 (https://github.com/openai/whisper, 실제 존재 확인됨)
- 자료: ffmpeg — 영상·음성 처리 CLI 도구 (https://ffmpeg.org, 실제 존재 확인됨)
- 자료: Claude Code 공식 문서 — 에이전틱 코딩 워크플로우 참고 (https://docs.anthropic.com, 실제 존재 확인됨)
- Timeline: 1일차: 블라인드스팟 패스 첫 적용 → 3일차: 퀴즈 패턴 도입 → 1주차: 원문 정독 후 인터뷰·구현 노트 패턴 순차 적용 → 2주차: 8가지 패턴 전체를 한 프로젝트에 통합 적용해 체화

## 🔗 연결
- 카테고리: [[_category-일반학습]]
- 주제: [[_topic-컨텍스트관리]] · [[_topic-ANTHROPIC]]
- 핵심 개념: [[_concept-언노운|언노운]] · [[_concept-context-engineering|컨텍스트 엔지니어링]] · [[_concept-블라인드스팟-패스|블라인드스팟 패스]] · [[_concept-브레인스토밍-프로토타입|브레인스토밍 프로토타입]] · [[_concept-인터뷰-패턴|인터뷰 패턴]] · [[_concept-구현-노트|구현 노트]] · [[_concept-anthropic|Anthropic]]

## 📝 자막 전문
- [0:00](https://youtube.com/watch?v=PNMBRgc0y2g&t=0) Anthropic에서 Claude Code를 만드는
개발자가,
- [0:03](https://youtube.com/watch?v=PNMBRgc0y2g&t=3) 자기들이 만든 Fable 5를 실제로 어떻게 쓰는지
공략집을 통째로 공개했습니다.
- [0:08](https://youtube.com/watch?v=PNMBRgc0y2g&t=8) 며칠 전 X에 올라와 조회수 270만을 넘긴
글인데요.
- [0:14](https://youtube.com/watch?v=PNMBRgc0y2g&t=14) 모델을 만든 사람들은 대체 뭘 다르게 하는지,
오늘 이 글을 처음부터 끝까지 풀어드릴게요.
- [0:19](https://youtube.com/watch?v=PNMBRgc0y2g&t=19) 결과를 가르는 핵심 개념 하나,
그리고 작업 전과 중,
- [0:23](https://youtube.com/watch?v=PNMBRgc0y2g&t=23) 후에 쓰는 프롬프트 패턴 여덟 가지를 보여드리고,
마지막에는 글쓴이가 Fable 5 공식 런칭 영상을
- [0:31](https://youtube.com/watch?v=PNMBRgc0y2g&t=31) 만들면서 이 방법을 그대로 쓴 실제 사례까지
보여드립니다.
- [0:35](https://youtube.com/watch?v=PNMBRgc0y2g&t=35) 특히 그 사례 끝에,
이 글 전체를 한 장면으로 요약하는 반전이 하나
- [0:40](https://youtube.com/watch?v=PNMBRgc0y2g&t=40) 있어요.
- [0:41](https://youtube.com/watch?v=PNMBRgc0y2g&t=41) 이 글을 쓴 사람은 Anthropic의 Claude
Code 팀에서 일하는 Thariq라는 개발자예요.
- [0:47](https://youtube.com/watch?v=PNMBRgc0y2g&t=47) 글의 제목은 페이블 필드 가이드,
나의 언노운 찾기입니다.
- [0:51](https://youtube.com/watch?v=PNMBRgc0y2g&t=51) 글은 지도는 영토가 아니다라는 오래된 말로
시작하는데요.
- [0:55](https://youtube.com/watch?v=PNMBRgc0y2g&t=55) 여기서 지도는 내가 AI에게 건네는 것,
그러니까 프롬프트와 스킬, 컨텍스트예요.
- [1:02](https://youtube.com/watch?v=PNMBRgc0y2g&t=62) 반대로 영토는 실제로 일이 벌어지는 곳,
진짜 코드베이스와 현실의 제약 조건이죠.
- [1:08](https://youtube.com/watch?v=PNMBRgc0y2g&t=68) 아무리 지도를 정성껏 그려도,
지도에 없는 것이 영토에는 반드시 있습니다.
- [1:14](https://youtube.com/watch?v=PNMBRgc0y2g&t=74) 바로 그 지도와 영토의 차이를, 그는 언노운,
그러니까 내가 모르는 것들이라고 부릅니다.
- [1:21](https://youtube.com/watch?v=PNMBRgc0y2g&t=81) Claude가 일하다가 언노운을 만나면,
내가 뭘 원하는지 스스로 추측해서 결정을 내려야
- [1:27](https://youtube.com/watch?v=PNMBRgc0y2g&t=87) 해요.
- [1:28](https://youtube.com/watch?v=PNMBRgc0y2g&t=88) 시키는 일이 커질수록 이런 추측의 순간도 늘어나죠.
- [1:31](https://youtube.com/watch?v=PNMBRgc0y2g&t=91) 그런데 여기서 그가 아주 중요한 말을 합니다.
- [1:34](https://youtube.com/watch?v=PNMBRgc0y2g&t=94) Fable 5는 결과물의 품질이 모델의 성능이
아니라,
- [1:38](https://youtube.com/watch?v=PNMBRgc0y2g&t=98) 내 언노운을 밝혀내는 능력에 발목 잡히는 첫 번째
모델이라는 거예요.
- [1:44](https://youtube.com/watch?v=PNMBRgc0y2g&t=104) 다시 말해 이제 아쉬운 결과가 나오면,
모델이 부족해서가 아니라 내가 못 알려줘서일
- [1:50](https://youtube.com/watch?v=PNMBRgc0y2g&t=110) 가능성이 크다는 겁니다.
- [1:52](https://youtube.com/watch?v=PNMBRgc0y2g&t=112) 더 무서운 얘기도 있어요.
- [1:53](https://youtube.com/watch?v=PNMBRgc0y2g&t=113) 미리 계획을 잘 세운다고 언노운이 다 잡히는 게
아니라는 겁니다.
- [1:57](https://youtube.com/watch?v=PNMBRgc0y2g&t=117) 구현 한복판에서 튀어나오기도 하고,
언노운을 따라가다 보니 문제를 아예 다른 방식으로
- [2:03](https://youtube.com/watch?v=PNMBRgc0y2g&t=123) 풀어야 한다는 결론이 나오기도 해요.
- [2:06](https://youtube.com/watch?v=PNMBRgc0y2g&t=126) 그래서 그는 Fable과 일하는 과정 자체를,
구현 전과 구현 중,
- [2:11](https://youtube.com/watch?v=PNMBRgc0y2g&t=131) 구현 후에 걸쳐 내 언노운을 계속 발굴하는 반복
과정이라고 정의합니다.
- [2:17](https://youtube.com/watch?v=PNMBRgc0y2g&t=137) 그런데 언노운을 찾으려면,
먼저 언노운에도 종류가 있다는 걸 알아야 해요.
- [2:23](https://youtube.com/watch?v=PNMBRgc0y2g&t=143) 그가 문제를 받았을 때 머릿속에서 돌리는 네 가지
분류가 있습니다.
- [2:27](https://youtube.com/watch?v=PNMBRgc0y2g&t=147) 첫째는 아는 것을 아는 상태입니다.
- [2:30](https://youtube.com/watch?v=PNMBRgc0y2g&t=150) 내가 원하는 걸 알고 있고,
프롬프트에 적어서 전달하는 것들이죠.
- [2:35](https://youtube.com/watch?v=PNMBRgc0y2g&t=155) 둘째는 모른다는 걸 아는 상태예요.
- [2:38](https://youtube.com/watch?v=PNMBRgc0y2g&t=158) 아직 답을 정하지 못했지만,
정해야 한다는 건 인식하고 있는 부분입니다.
- [2:43](https://youtube.com/watch?v=PNMBRgc0y2g&t=163) 셋째가 재미있는데, 안다는 걸 모르는 상태예요.
- [2:47](https://youtube.com/watch?v=PNMBRgc0y2g&t=167) 나한테는 너무 당연해서 굳이 적을 생각조차 못
하지만,
- [2:51](https://youtube.com/watch?v=PNMBRgc0y2g&t=171) 결과물을 보면 바로 이게 아닌데 하고 알아차리는
것들입니다.
- [2:55](https://youtube.com/watch?v=PNMBRgc0y2g&t=175) 넷째가 가장 위험한,
모른다는 것조차 모르는 상태예요.
- [3:00](https://youtube.com/watch?v=PNMBRgc0y2g&t=180) 아예 고려해 본 적이 없는 영역,
심지어 결과물이 얼마나 좋아질 수 있는지 그 기준
- [3:06](https://youtube.com/watch?v=PNMBRgc0y2g&t=186) 자체를 모르는 상태죠.
- [3:08](https://youtube.com/watch?v=PNMBRgc0y2g&t=188) 글에서 그는 에이전틱 코딩을 잘하는 사람들의
공통점을 이렇게 말합니다.
- [3:13](https://youtube.com/watch?v=PNMBRgc0y2g&t=193) 언노운이 애초에 적고,
그러면서도 언노운이 남아 있다고 가정한다는 거예요.
- [3:19](https://youtube.com/watch?v=PNMBRgc0y2g&t=199) 언노운을 줄이고 대비하는 것 자체가 에이전틱 코딩의
실력이라는 거죠.
- [3:24](https://youtube.com/watch?v=PNMBRgc0y2g&t=204) 지시가 너무 구체적이면 Claude는 방향을 트는
게 나은 순간에도 지시를 그대로 따르고,
- [3:30](https://youtube.com/watch?v=PNMBRgc0y2g&t=210) 너무 모호하면 내 상황에 안 맞는 업계의 일반적인
관행으로 빈칸을 채워버립니다.
- [3:35](https://youtube.com/watch?v=PNMBRgc0y2g&t=215) 양쪽 모두 언노운을 계산에 넣지 않아서 생기는
실패예요.
- [3:40](https://youtube.com/watch?v=PNMBRgc0y2g&t=220) 다행인 건,
이 언노운 찾기를 Claude가 도와줄 수 있다는
- [3:43](https://youtube.com/watch?v=PNMBRgc0y2g&t=223) 겁니다.
- [3:44](https://youtube.com/watch?v=PNMBRgc0y2g&t=224) Claude는 코드베이스와 인터넷을 나보다 훨씬
빨리 뒤지고, 웬만한 주제는 나보다 많이 알고,
- [3:50](https://youtube.com/watch?v=PNMBRgc0y2g&t=230) 실패했을 때 다시 시도하는 속도도 빠르니까요.
- [3:53](https://youtube.com/watch?v=PNMBRgc0y2g&t=233) 대신 조건이 하나 있는데,
내 출발점을 컨텍스트로 줘야 한다는 거예요.
- [3:58](https://youtube.com/watch?v=PNMBRgc0y2g&t=238) 내가 지금 어디까지 생각했는지,
이 문제와 코드베이스에 얼마나 익숙한지 솔직하게
- [4:04](https://youtube.com/watch?v=PNMBRgc0y2g&t=244) 밝히고, 생각의 파트너처럼 같이 일하는 겁니다.
- [4:07](https://youtube.com/watch?v=PNMBRgc0y2g&t=247) 이걸 기억하면서,
이제 그가 실제로 쓰는 여덟 가지 패턴을 구현 전,
- [4:13](https://youtube.com/watch?v=PNMBRgc0y2g&t=253) 구현 중, 구현 후 순서로 하나씩 보시죠.
- [4:16](https://youtube.com/watch?v=PNMBRgc0y2g&t=256) 구현 전 첫 번째 패턴은 블라인드스팟 패스,
사각지대 점검입니다.
- [4:21](https://youtube.com/watch?v=PNMBRgc0y2g&t=261) 낯선 코드베이스에서 기능을 만들거나 익숙하지 않은
작업을 시작할 때는, 뭘 물어봐야 하는지,
- [4:28](https://youtube.com/watch?v=PNMBRgc0y2g&t=268) 뭐가 좋은 건지,
어떤 함정을 피해야 하는지조차 모르는 상태잖아요.
- [4:33](https://youtube.com/watch?v=PNMBRgc0y2g&t=273) 이럴 때 Claude에게 대놓고 부탁하는 거예요.
- [4:36](https://youtube.com/watch?v=PNMBRgc0y2g&t=276) 그는 블라인드스팟 패스와 언노운 언노운이라는 단어를
문자 그대로 프롬프트에 쓴다고 합니다.
- [4:43](https://youtube.com/watch?v=PNMBRgc0y2g&t=283) 예를 들면 이런 식이에요.
- [4:44](https://youtube.com/watch?v=PNMBRgc0y2g&t=284) 새 인증 기능을 붙여야 하는데 이 코드베이스의 인증
모듈은 하나도 몰라,
- [4:49](https://youtube.com/watch?v=PNMBRgc0y2g&t=289) 블라인드스팟 패스를 해서 내가 모르는 걸 알려주고
너한테 더 잘 지시할 수 있게 도와줘.
- [4:55](https://youtube.com/watch?v=PNMBRgc0y2g&t=295) 심지어 코딩이 아니어도 됩니다.
- [4:57](https://youtube.com/watch?v=PNMBRgc0y2g&t=297) 컬러 그레이딩이 뭔지 모르는데 이 영상을 보정해야
해,
- [5:01](https://youtube.com/watch?v=PNMBRgc0y2g&t=301) 내가 더 잘 지시할 수 있게 컬러 그레이딩부터
가르쳐줘, 이런 프롬프트도 글에 그대로 나와요.
- [5:09](https://youtube.com/watch?v=PNMBRgc0y2g&t=309) 여기서 잠깐,
직접 만들긴 막막하고 외주 견적은 부담스러워
- [5:13](https://youtube.com/watch?v=PNMBRgc0y2g&t=313) 망설이셨다면,
헤이제임스의 1:1 외주 제작 패키지를 추천드려요.
- [5:18](https://youtube.com/watch?v=PNMBRgc0y2g&t=318) 85억 매출 개발 에이전시를 운영한 23년차
개발자가, 단 4시간 만에 로그인과 결제,
- [5:24](https://youtube.com/watch?v=PNMBRgc0y2g&t=324) 관리자 페이지는 물론 SaaS와 플랫폼, 앱,
그리고 보안 검토까지 갖춘 서비스를 실서버에 직접
- [5:32](https://youtube.com/watch?v=PNMBRgc0y2g&t=332) 출시해 드리고,
사업성 검토와 창업·마케팅 전략 컨설팅까지 함께
- [5:36](https://youtube.com/watch?v=PNMBRgc0y2g&t=336) 봐드려요.
- [5:38](https://youtube.com/watch?v=PNMBRgc0y2g&t=338) 세션이 끝난 뒤에도 직접 운영할 수 있도록 교육
자료를 드리고,
- [5:42](https://youtube.com/watch?v=PNMBRgc0y2g&t=342) 진행이 만족스럽지 않으면 100% 환불해 드립니다.
- [5:46](https://youtube.com/watch?v=PNMBRgc0y2g&t=346) 게다가 업계 최저가도 보장해요.
- [5:49](https://youtube.com/watch?v=PNMBRgc0y2g&t=349) 다른 개발사의 견적서를 보여주시면 그보다 더
저렴하게 만들어 드립니다.
- [5:55](https://youtube.com/watch?v=PNMBRgc0y2g&t=355) 신청 링크는 설명란에 있어요.
- [5:57](https://youtube.com/watch?v=PNMBRgc0y2g&t=357) 좋아요와 구독도 부탁드리고, 자,
다시 본론으로 돌아갈게요.
- [6:01](https://youtube.com/watch?v=PNMBRgc0y2g&t=361) 두 번째 패턴은 브레인스토밍과 프로토타입입니다.
- [6:05](https://youtube.com/watch?v=PNMBRgc0y2g&t=365) 보면 알겠는데 말로는 설명하지 못하는 것들,
아까 말한 안다는 걸 모르는 영역에서 쓰는
- [6:11](https://youtube.com/watch?v=PNMBRgc0y2g&t=371) 방법이에요.
- [6:12](https://youtube.com/watch?v=PNMBRgc0y2g&t=372) 이런 건 구현이 끝난 뒤에 발견하면 비용이 커요.
- [6:16](https://youtube.com/watch?v=PNMBRgc0y2g&t=376) 스펙이 조금만 바뀌어도 코드는 완전히 다른 모양이
될 수 있으니까요.
- [6:20](https://youtube.com/watch?v=PNMBRgc0y2g&t=380) 그래서 백엔드를 연결하기 전에,
가짜 데이터를 넣은 HTML 한 장으로 화면부터
- [6:26](https://youtube.com/watch?v=PNMBRgc0y2g&t=386) 만들어 보고 반응하는 겁니다.
- [6:28](https://youtube.com/watch?v=PNMBRgc0y2g&t=388) 그가 쓰는 프롬프트도 아주 구체적이에요.
- [6:31](https://youtube.com/watch?v=PNMBRgc0y2g&t=391) 이 데이터로 대시보드를 만들고 싶은데 나는 디자인
감각이 없다,
- [6:36](https://youtube.com/watch?v=PNMBRgc0y2g&t=396) 완전히 다른 네 가지 디자인 방향으로 HTML
페이지를 만들어줘, 내가 보고 반응할게,
- [6:42](https://youtube.com/watch?v=PNMBRgc0y2g&t=402) 이런 식이죠.
- [6:44](https://youtube.com/watch?v=PNMBRgc0y2g&t=404) 그는 거의 모든 코딩 세션을 이런 탐색이나
브레인스토밍으로 시작한다고 해요.
- [6:49](https://youtube.com/watch?v=PNMBRgc0y2g&t=409) 작업 범위를 너무 좁지도 너무 넓지도 않게 잡는 데
이만한 방법이 없다는 겁니다.
- [6:56](https://youtube.com/watch?v=PNMBRgc0y2g&t=416) 세 번째 패턴은 인터뷰입니다.
- [6:58](https://youtube.com/watch?v=PNMBRgc0y2g&t=418) 브레인스토밍을 충분히 해도 언노운은 남거든요.
- [7:02](https://youtube.com/watch?v=PNMBRgc0y2g&t=422) 이럴 때 그는 거꾸로 Claude에게 질문을
시킵니다.
- [7:05](https://youtube.com/watch?v=PNMBRgc0y2g&t=425) 애매한 게 있으면 나를 인터뷰해줘,
한 번에 하나씩만 물어보고,
- [7:09](https://youtube.com/watch?v=PNMBRgc0y2g&t=429) 내 대답에 따라 아키텍처가 바뀔 질문부터 우선으로,
이렇게요.
- [7:14](https://youtube.com/watch?v=PNMBRgc0y2g&t=434) 우리가 AI에게 질문하는 게 아니라 AI가 우리를
인터뷰하게 만든다는 발상의 전환이 포인트예요.
- [7:22](https://youtube.com/watch?v=PNMBRgc0y2g&t=442) 내 머릿속에만 있던 결정 사항들이,
질문에 대답하는 사이에 전부 프롬프트가 되는
- [7:27](https://youtube.com/watch?v=PNMBRgc0y2g&t=447) 셈이죠.
- [7:28](https://youtube.com/watch?v=PNMBRgc0y2g&t=448) 네 번째 패턴은 레퍼런스입니다.
- [7:30](https://youtube.com/watch?v=PNMBRgc0y2g&t=450) 원하는 걸 말로 다 설명할 수 없을 때가 있잖아요.
- [7:33](https://youtube.com/watch?v=PNMBRgc0y2g&t=453) 표현할 언어가 없거나,
설명하자면 한나절 걸리는 경우요.
- [7:37](https://youtube.com/watch?v=PNMBRgc0y2g&t=457) 이럴 때 최고의 답은 참고 자료를 던져주는 건데,
다이어그램이나 문서,
- [7:42](https://youtube.com/watch?v=PNMBRgc0y2g&t=462) 그림도 좋지만 그가 꼽는 최고의 레퍼런스는 단연
소스코드입니다.
- [7:47](https://youtube.com/watch?v=PNMBRgc0y2g&t=467) 마음에 드는 방식으로 구현된 라이브러리나 디자인
컴포넌트가 있으면,
- [7:51](https://youtube.com/watch?v=PNMBRgc0y2g&t=471) 그 폴더를 Fable에게 가리키면서 뭘 봐야 하는지
알려주면 돼요.
- [7:56](https://youtube.com/watch?v=PNMBRgc0y2g&t=476) 심지어 프로그래밍 언어가 달라도 됩니다.
- [7:59](https://youtube.com/watch?v=PNMBRgc0y2g&t=479) 글의 예시는 이래요.
- [8:01](https://youtube.com/watch?v=PNMBRgc0y2g&t=481) 이 Rust 라이브러리가 내가 원하는 재시도 동작을
정확히 구현하고 있으니,
- [8:05](https://youtube.com/watch?v=PNMBRgc0y2g&t=485) 읽고 나서 같은 로직을 우리 TypeScript
클라이언트에 다시 구현해줘.
- [8:10](https://youtube.com/watch?v=PNMBRgc0y2g&t=490) 구현 전 마지막,
다섯 번째 패턴은 구현 계획서입니다.
- [8:14](https://youtube.com/watch?v=PNMBRgc0y2g&t=494) 이제 만들 준비가 됐다 싶으면,
그는 바로 코드를 시키는 대신 리뷰용 구현 계획을
- [8:20](https://youtube.com/watch?v=PNMBRgc0y2g&t=500) 먼저 받아요.
- [8:21](https://youtube.com/watch?v=PNMBRgc0y2g&t=501) 핵심은 순서인데,
바뀔 가능성이 큰 것부터 앞에 놓게 합니다.
- [8:26](https://youtube.com/watch?v=PNMBRgc0y2g&t=506) 데이터 모델 변경과 새 타입 인터페이스,
사용자에게 보이는 부분을 맨 위로 올리고,
- [8:31](https://youtube.com/watch?v=PNMBRgc0y2g&t=511) 기계적인 리팩토링은 네가 알아서 해도 되니 맨
아래로 내려달라고 하는 거죠.
- [8:36](https://youtube.com/watch?v=PNMBRgc0y2g&t=516) 검토하는 내 시간과 주의력을,
실제로 뒤집힐 수 있는 결정에만 쓰겠다는 겁니다.
- [8:42](https://youtube.com/watch?v=PNMBRgc0y2g&t=522) 여기까지가 구현 전이고, 이제 구현 중입니다.
- [8:45](https://youtube.com/watch?v=PNMBRgc0y2g&t=525) 계획이 만족스러우면 그는 새 세션을 열고,
스펙 파일과 프로토타입 같은 산출물을 넘겨서 구현을
- [8:51](https://youtube.com/watch?v=PNMBRgc0y2g&t=531) 시작해요.
- [8:52](https://youtube.com/watch?v=PNMBRgc0y2g&t=532) 그런데 아무리 계획해도 언노운은 어딘가에 숨어
있다고 했잖아요.
- [8:57](https://youtube.com/watch?v=PNMBRgc0y2g&t=537) 에이전트가 일하다가 코드에서 예상하지 못한 케이스를
만나, 계획과 다른 길로 가야 할 수도 있습니다.
- [9:03](https://youtube.com/watch?v=PNMBRgc0y2g&t=543) 그래서 여섯 번째 패턴,
그는 구현 노트라는 임시 메모 파일을 하나 만들게
- [9:08](https://youtube.com/watch?v=PNMBRgc0y2g&t=548) 시켜요.
- [9:09](https://youtube.com/watch?v=PNMBRgc0y2g&t=549) 계획에서 벗어나는 결정을 하게 되면 보수적인 쪽을
선택하고,
- [9:13](https://youtube.com/watch?v=PNMBRgc0y2g&t=553) 그 내용을 이탈 항목에 기록한 다음 계속 진행해,
이렇게 지시하는 겁니다.
- [9:18](https://youtube.com/watch?v=PNMBRgc0y2g&t=558) 이 파일이 쌓이면 다음 시도에서 배울 수 있는
자산이 되고요.
- [9:22](https://youtube.com/watch?v=PNMBRgc0y2g&t=562) 구현이 끝난 뒤의 두 가지도 재미있습니다.
- [9:24](https://youtube.com/watch?v=PNMBRgc0y2g&t=564) 일곱 번째 패턴은 피치 문서예요.
- [9:26](https://youtube.com/watch?v=PNMBRgc0y2g&t=566) 뭔가를 출시하려면 결국 동료와 리뷰어의 승인을
받아야 하는데, 프로토타입과 스펙,
- [9:32](https://youtube.com/watch?v=PNMBRgc0y2g&t=572) 구현 노트를 하나의 문서로 묶어서 슬랙에 바로 올릴
수 있게 포장해달라고 시키는 겁니다.
- [9:39](https://youtube.com/watch?v=PNMBRgc0y2g&t=579) 리뷰어도 나와 같은 언노운에서 출발하니까,
내가 겪은 과정을 보여주면 이해도 승인도 빨라진다는
- [9:46](https://youtube.com/watch?v=PNMBRgc0y2g&t=586) 거죠.
- [9:46](https://youtube.com/watch?v=PNMBRgc0y2g&t=586) 그리고 여덟 번째 패턴이 퀴즈인데,
이 글에서 특히 인상적인 부분이에요.
- [9:50](https://youtube.com/watch?v=PNMBRgc0y2g&t=590) 긴 세션이 끝나면 Claude는 내가 생각한 것보다
훨씬 많은 일을 해놨을 때가 많잖아요.
- [9:57](https://youtube.com/watch?v=PNMBRgc0y2g&t=597) 코드 변경분만 읽어서는 무슨 일이 있었는지 다 알기
어렵습니다.
- [10:02](https://youtube.com/watch?v=PNMBRgc0y2g&t=602) 그래서 변경 내용을 맥락과 함께 정리한 보고서를
받고, 맨 아래에 퀴즈를 내달라고 해요.
- [10:10](https://youtube.com/watch?v=PNMBRgc0y2g&t=610) 그리고 이 퀴즈에서 만점을 받기 전에는 머지하지
않는다고 합니다.
- [10:15](https://youtube.com/watch?v=PNMBRgc0y2g&t=615) AI가 한 일을 내가 설명하지 못하면 아직 내
코드가 아니라는 원칙인 셈이죠.
- [10:20](https://youtube.com/watch?v=PNMBRgc0y2g&t=620) 자, 이제 약속드린 실제 사례입니다.
- [10:24](https://youtube.com/watch?v=PNMBRgc0y2g&t=624) Fable 5의 공식 런칭 영상,
그러니까 Anthropic이 이 모델을 발표할 때
- [10:30](https://youtube.com/watch?v=PNMBRgc0y2g&t=630) 쓴 그 영상은,
편집 전체가 Claude Code로 이루어졌다고
- [10:34](https://youtube.com/watch?v=PNMBRgc0y2g&t=634) 그는 밝혔어요.
- [10:35](https://youtube.com/watch?v=PNMBRgc0y2g&t=635) 영상 편집은 그에게 완전히 처음인 분야였습니다.
- [10:39](https://youtube.com/watch?v=PNMBRgc0y2g&t=639) 그래서 아는 것에서 시작했어요.
- [10:42](https://youtube.com/watch?v=PNMBRgc0y2g&t=642) Claude가 코드로 영상을 자르고 받아 적을 수
있다는 건 알았으니,
- [10:47](https://youtube.com/watch?v=PNMBRgc0y2g&t=647) 먼저 Whisper 같은 음성 인식 기술이 어떻게
동작하는지,
- [10:51](https://youtube.com/watch?v=PNMBRgc0y2g&t=651) 말버릇이나 긴 침묵을 편집 도구인 ffmpeg로
정확히 잘라낼 수 있는지부터 설명해달라고 했죠.
- [10:58](https://youtube.com/watch?v=PNMBRgc0y2g&t=658) 다음에는 말하는 단어에 맞춰 화면 그래픽이 뜨는
연출이 가능한지 확신이 없어서,
- [11:04](https://youtube.com/watch?v=PNMBRgc0y2g&t=664) Remotion이라는 도구로 프로토타입 영상부터
만들어 봤습니다.
- [11:08](https://youtube.com/watch?v=PNMBRgc0y2g&t=668) 여기까지는 앞에서 본 패턴 그대로죠.
- [11:12](https://youtube.com/watch?v=PNMBRgc0y2g&t=672) 그런데 마지막에 진짜 언노운이 나타납니다.
- [11:14](https://youtube.com/watch?v=PNMBRgc0y2g&t=674) 완성된 영상의 색감이 어딘가 칙칙했던 거예요.
- [11:17](https://youtube.com/watch?v=PNMBRgc0y2g&t=677) 색보정,
그러니까 컬러 그레이딩의 문제라는 건 알겠는데,
- [11:21](https://youtube.com/watch?v=PNMBRgc0y2g&t=681) 그게 정확히 뭔지는 몰랐죠.
- [11:23](https://youtube.com/watch?v=PNMBRgc0y2g&t=683) 처음에는 우리가 늘 하던 대로 했습니다.
- [11:26](https://youtube.com/watch?v=PNMBRgc0y2g&t=686) Claude에게 몇 가지 시안을 만들게 하고
고르려고 한 거죠.
- [11:30](https://youtube.com/watch?v=PNMBRgc0y2g&t=690) 그런데 시안을 아무리 봐도 고를 수가 없었어요.
- [11:34](https://youtube.com/watch?v=PNMBRgc0y2g&t=694) 좋은 색보정이 뭔지,
그 기준 자체를 자기가 모른다는 걸 깨달은 겁니다.
- [11:39](https://youtube.com/watch?v=PNMBRgc0y2g&t=699) 아까 말한 네 번째 언노운,
모른다는 것조차 모르는 상태였던 거예요.
- [11:43](https://youtube.com/watch?v=PNMBRgc0y2g&t=703) 그래서 시안 뽑기를 멈추고,
Claude에게 컬러 그레이딩을 가르쳐달라고
- [11:49](https://youtube.com/watch?v=PNMBRgc0y2g&t=709) 했습니다.
- [11:50](https://youtube.com/watch?v=PNMBRgc0y2g&t=710) 도구에게 더 시키기 전에,
나를 먼저 업그레이드한 거죠.
- [11:55](https://youtube.com/watch?v=PNMBRgc0y2g&t=715) 이 글 전체가 이 한 장면에 들어 있어요.
- [11:58](https://youtube.com/watch?v=PNMBRgc0y2g&t=718) AI에게 더 시키는 게 아니라,
AI로 내가 모르는 걸 먼저 밝히는 것.
- [12:03](https://youtube.com/watch?v=PNMBRgc0y2g&t=723) 그게 페이블 시대의 사용법이라는 겁니다.
- [12:06](https://youtube.com/watch?v=PNMBRgc0y2g&t=726) 정리할게요.
- [12:07](https://youtube.com/watch?v=PNMBRgc0y2g&t=727) 지도는 영토가 아니고, 그 차이가 언노운입니다.
- [12:11](https://youtube.com/watch?v=PNMBRgc0y2g&t=731) 이제는 모델의 성능이 아니라,
내가 언노운을 얼마나 빨리 찾느냐가 결과를
- [12:16](https://youtube.com/watch?v=PNMBRgc0y2g&t=736) 가릅니다.
- [12:17](https://youtube.com/watch?v=PNMBRgc0y2g&t=737) 그래서 구현 전에는 블라인드스팟 패스와
브레인스토밍, 인터뷰, 레퍼런스,
- [12:22](https://youtube.com/watch?v=PNMBRgc0y2g&t=742) 구현 계획으로 언노운을 줄이고,
구현 중에는 구현 노트로 이탈을 기록하고,
- [12:27](https://youtube.com/watch?v=PNMBRgc0y2g&t=747) 구현 후에는 피치 문서와 퀴즈로 확인하는 거예요.
- [12:31](https://youtube.com/watch?v=PNMBRgc0y2g&t=751) 글쓴이의 마지막 문장이 좋아서 그대로 전해드릴게요.
- [12:34](https://youtube.com/watch?v=PNMBRgc0y2g&t=754) 브레인스토밍과 인터뷰, 프로토타입,
레퍼런스는 전부,
- [12:38](https://youtube.com/watch?v=PNMBRgc0y2g&t=758) 고치기 비싸지기 전에 내가 몰랐던 걸 알아내는 가장
싼 방법이다.
- [12:44](https://youtube.com/watch?v=PNMBRgc0y2g&t=764) 오늘 당장 해볼 액션 아이템은 하나입니다.
- [12:47](https://youtube.com/watch?v=PNMBRgc0y2g&t=767) 다음 작업을 시작할 때 첫 프롬프트로 이렇게
쳐보세요.
- [12:51](https://youtube.com/watch?v=PNMBRgc0y2g&t=771) 이 작업에서 내 언노운부터 찾아줘.
- [12:54](https://youtube.com/watch?v=PNMBRgc0y2g&t=774) 마지막으로 궁금한 게 있어요.
- [12:56](https://youtube.com/watch?v=PNMBRgc0y2g&t=776) 여러분은 AI에게 일을 시킬 때 계획부터 세우는
쪽인가요, 일단 시키고 고치는 쪽인가요.
- [13:02](https://youtube.com/watch?v=PNMBRgc0y2g&t=782) A는 계획부터, B는 일단 시키고,
댓글에 A나 B로만 남겨주세요.
- [13:08](https://youtube.com/watch?v=PNMBRgc0y2g&t=788) 좋아요와 구독은 이런 글을 더 빨리 찾아오는 데 큰
힘이 됩니다.
