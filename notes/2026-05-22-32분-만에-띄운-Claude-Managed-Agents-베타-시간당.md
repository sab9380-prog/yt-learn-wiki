---
title: "32분 만에 띄운 Claude Managed Agents 베타, 시간당 0.08달러 가격 분석"
source_url: https://youtube.com/watch?v=TGSV1CGAGfw
video_id: TGSV1CGAGfw
source_type: youtube
lang: ko
analyzed: 2026-05-22
category: 일반학습
status: active
---
# 32분 만에 띄운 Claude Managed Agents 베타, 시간당 0.08달러 가격 분석

## 🧠 이해 (Understand)
- **Summary:** 앤스로픽이 클로드 매니지드 에이전트 베타를 공개했습니다. 기존에 에이전트를 프로덕션에 올리려면 샌드박스, 도구실행 레이어, 세션 상태 관리, 체크포인팅 등 5가지 인프라를 직접 구축해야 했지만, 매니지드 에이전트는 이 모든 것을 앤스로픽이 제공합니다. 핵심은 에이전트(직무기술서), 환경(사무실), 세션(출근한 사람), 이벤트(메시지) 4개 개념입니다. 베타 헤더 한 줄만 추가하면 32분 만에 첫 에이전트를 띄울 수 있으며, 가격은 시간당 0.08달러입니다. 장시간 비동기 워크플로우에는 유리하지만 빠른 동기형 채팅에는 기존 API가 더 효율적입니다.
- **Core Message:** 앤스로픽 매니지드 에이전트로 복잡한 에이전트 인프라 구축 없이 32분 만에 프로덕션급 에이전트를 띄울 수 있다.
> 제가 직접 신청하고 첫 에이전트를 띄우는 데까지 걸린 시간 정확히 32분입니다
> 모델만 빌렸쓰던 시대에서 모델 더하기 살림사리까지 통째로 빌리는 시대로 넘어간 거예요
> 한마디로 무거운 자동화에는 이득, 가벼운 채팅에는 손해
❗ 베타 헤더 한 줄만 추가하면 모든 API 계정에서 바로 사용 가능
❗ 시간당 0.08달러는 한국돈 100원짜리 동전 하나도 안 되는 금액
❗ 노션, 라쿠텐, 아사나 등 대기업들이 이미 베타에 참여해서 엔터프라이즈급 검증 완료

## 📚 핵심 용어
- **매니지드 에이전트:** 에이전트 실행에 필요한 모든 인프라를 앤스로픽이 제공하는 서비스 / 호텔처럼 침대, 청소, 룸서비스까지 모든 서비스가 준비된 곳에서 바로 업무를 시작하는 것 / 기존 메시지 API는 모델만 빌리는 것, 매니지드 에이전트는 모델+운영환경까지 통째로 빌리는 것
- **세션:** 에이전트가 환경에서 실제로 작업을 수행하는 한 번의 실행 단위 / 사무실(환경)에 직원(에이전트)이 출근해서 하루 일하는 것과 같다 / 에이전트는 설계도, 세션은 그 설계도로 만든 실제 작업자가 일하는 시간
- **액티브 런타임:** 에이전트가 실제로 도구를 실행하며 작업하는 시간만 과금되는 방식 / 택시 요금처럼 실제 운행 시간만 계산하고, 신호 대기는 별도 과금 없는 것 / 일반 서버는 켜져있는 모든 시간 과금, 액티브 런타임은 실제 작업 시간만 과금
- **비동기 워크플로우:** 사용자가 즉시 대기하지 않고 백그라운드에서 처리되는 장시간 작업 / 세탁소에 옷을 맡기고 나중에 찾아가는 것처럼, 결과를 기다리지 않고 다른 일을 하는 방식 / 동기형은 질문-즉시답변(채팅), 비동기형은 작업의뢰-나중에확인(이메일자동화)

## 🚀 실행 (Execute)
- [ ] 클로드 API 계정에 베타 헤더 추가하여 첫 매니지드 에이전트 테스트 실행
  - 담당: 나
  - 이유: 32분이면 실제 동작을 확인할 수 있고, 향후 자동화 프로젝트에 활용 가능성을 판단할 수 있음
- [ ] 현재 진행 중인 업무에서 비동기 자동화가 가능한 워크플로우 식별
  - 담당: 나
  - 이유: 매니지드 에이전트가 가장 효과적인 장시간/백그라운드 작업을 미리 파악해서 ROI 극대화
- 자료: 앤스로픽 매니지드 에이전트 공식 문서
- 자료: 핑거(pingda.io) - 영상 제작 도구
- 자료: 매니지드 에이전트 핵심 가이드 PDF (출처: 영상 제공 링크)
- Timeline: 1단계: 이번 주 내 베타 테스트로 기능 확인 → 2단계: 2주 내 적용 가능한 워크플로우 식별 → 3단계: 가장 ROI가 높은 자동화부터 단계적 적용

## 🔗 연결
- 카테고리: [[_category-일반학습]]

## 📝 자막 전문
- [0:00](https://youtube.com/watch?v=TGSV1CGAGfw&t=0) 에이전트 한번 만들어 보겠다고
- [0:01](https://youtube.com/watch?v=TGSV1CGAGfw&t=1) 랭체인 MCP 샌드박스 세션
- [0:04](https://youtube.com/watch?v=TGSV1CGAGfw&t=4) 관리까지 일주일 동안 헤매신 분
- [0:06](https://youtube.com/watch?v=TGSV1CGAGfw&t=6) 계시죠? 저도 그랬어요. 그런데
- [0:08](https://youtube.com/watch?v=TGSV1CGAGfw&t=8) 어제부로 그거 안 해도 됩니다.
- [0:10](https://youtube.com/watch?v=TGSV1CGAGfw&t=10) 앤스로픽이 어제 클로드 매니지
- [0:12](https://youtube.com/watch?v=TGSV1CGAGfw&t=12) 에이전트 베타를 공개했거든요. 제가
- [0:14](https://youtube.com/watch?v=TGSV1CGAGfw&t=14) 직접 신청하고 첫 에이전트를 띄우는
- [0:16](https://youtube.com/watch?v=TGSV1CGAGfw&t=16) 데까지 걸린 시간 정확히
- [0:18](https://youtube.com/watch?v=TGSV1CGAGfw&t=18) 32분입니다. 영상을 끝까지 보시고
- [0:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=21) 좋아요와 댓글 구독해 주시면 매니지드
- [0:24](https://youtube.com/watch?v=TGSV1CGAGfw&t=24) 에이전트 핵심 가이드 PDF를 받으실
- [0:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=26) 수 있는 링크를 말씀드리겠습니다.
- [0:28](https://youtube.com/watch?v=TGSV1CGAGfw&t=28) 자, 이게 왜 중요하냐? 그동안
- [0:30](https://youtube.com/watch?v=TGSV1CGAGfw&t=30) 에이전트를 진짜 프로덕션에 올리려면
- [0:32](https://youtube.com/watch?v=TGSV1CGAGfw&t=32) 샌드박스 만들고 도구실행 레이어 짜고
- [0:35](https://youtube.com/watch?v=TGSV1CGAGfw&t=35) 세션 상태 관리하고 체크포인팅까지
- [0:38](https://youtube.com/watch?v=TGSV1CGAGfw&t=38) 직접 해야 했어요. 다섯 가지
- [0:39](https://youtube.com/watch?v=TGSV1CGAGfw&t=39) 인프라를 다 짜야 했단 거죠.
- [0:41](https://youtube.com/watch?v=TGSV1CGAGfw&t=41) 매니지드 에이전트는 그 다섯 개를
- [0:43](https://youtube.com/watch?v=TGSV1CGAGfw&t=43) 통째로 엔스로픽이 들고가
- [0:45](https://youtube.com/watch?v=TGSV1CGAGfw&t=45) 버렸습니다.이 영상에서 다룰 건 세
- [0:47](https://youtube.com/watch?v=TGSV1CGAGfw&t=47) 가지예요. 첫째 매니지드 에이전트가
- [0:50](https://youtube.com/watch?v=TGSV1CGAGfw&t=50) 정확히 뭘 대신해 주는지. 둘째 어제
- [0:53](https://youtube.com/watch?v=TGSV1CGAGfw&t=53) 막픈 베타로 첫 에이전트 띄우는
- [0:55](https://youtube.com/watch?v=TGSV1CGAGfw&t=55) 30분 가이드. 셋째 시간당
- [0:58](https://youtube.com/watch?v=TGSV1CGAGfw&t=58) 0.08달러. 08달러 가격 모델.
- [1:00](https://youtube.com/watch?v=TGSV1CGAGfw&t=60) 어떤 워크로드일 때 진짜 이득인지.
- [1:03](https://youtube.com/watch?v=TGSV1CGAGfw&t=63) 먼저 매니지드 에이전트가 정확히
- [1:04](https://youtube.com/watch?v=TGSV1CGAGfw&t=64) 뭐냐? 한 줄로 정리해 볼게요.
- [1:06](https://youtube.com/watch?v=TGSV1CGAGfw&t=66) 엔스로픽 공식 문서에는 클로드를 쓰는
- [1:09](https://youtube.com/watch?v=TGSV1CGAGfw&t=69) 두 가지 방법이 나와 있어요. 첫째는
- [1:11](https://youtube.com/watch?v=TGSV1CGAGfw&t=71) 메시지스 API. 그러니까 우리가
- [1:13](https://youtube.com/watch?v=TGSV1CGAGfw&t=73) 평소에 쓰는 모델 직접 호출
- [1:15](https://youtube.com/watch?v=TGSV1CGAGfw&t=75) 방식이에요. 채 만들 때 쓰는
- [1:17](https://youtube.com/watch?v=TGSV1CGAGfw&t=77) 그거요. 둘째가 어제 새로 나온
- [1:19](https://youtube.com/watch?v=TGSV1CGAGfw&t=79) 매니지드 에이전트인데 이건 사전에
- [1:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=81) 미리 빌드된 에이전트 한네스의
- [1:23](https://youtube.com/watch?v=TGSV1CGAGfw&t=83) 인프라까지 통째로 묶여 있는
- [1:25](https://youtube.com/watch?v=TGSV1CGAGfw&t=85) 형태입니다. 한마디로 모델만 빌렸쓰던
- [1:27](https://youtube.com/watch?v=TGSV1CGAGfw&t=87) 시대에서 모델 더하기 살림사리까지
- [1:30](https://youtube.com/watch?v=TGSV1CGAGfw&t=90) 통째로 빌리는 시대로 넘어간 거예요.
- [1:32](https://youtube.com/watch?v=TGSV1CGAGfw&t=92) 그럼 그 통째로 빌려 준다는게 뭘
- [1:34](https://youtube.com/watch?v=TGSV1CGAGfw&t=94) 빌려 준다는 거냐? 외울 건 딱네
- [1:36](https://youtube.com/watch?v=TGSV1CGAGfw&t=96) 개입니다. 에이전트, 환경, 세션,
- [1:39](https://youtube.com/watch?v=TGSV1CGAGfw&t=99) 그리고 이벤트. 일상 비유로 풀어
- [1:42](https://youtube.com/watch?v=TGSV1CGAGfw&t=102) 볼게요. 첫째 에이전트는 직무
- [1:44](https://youtube.com/watch?v=TGSV1CGAGfw&t=104) 기술서예요. 어떤 모델 쓰고, 어떤
- [1:46](https://youtube.com/watch?v=TGSV1CGAGfw&t=106) 시스템 프롬프트 쓰고, 어떤 도구랑
- [1:49](https://youtube.com/watch?v=TGSV1CGAGfw&t=109) MCP 서버랑 스킬을 줄지 한번
- [1:51](https://youtube.com/watch?v=TGSV1CGAGfw&t=111) 정의해 두면 아이디 하나가 발급돼요.
- [1:53](https://youtube.com/watch?v=TGSV1CGAGfw&t=113) 다음부터는 그 아이디만 부르면
- [1:55](https://youtube.com/watch?v=TGSV1CGAGfw&t=115) 됩니다. 회사로 치면 영업 사원 직무
- [1:58](https://youtube.com/watch?v=TGSV1CGAGfw&t=118) 기술서를 한번 써 두면 세원 뽑을
- [2:00](https://youtube.com/watch?v=TGSV1CGAGfw&t=120) 때마다 그 문서만 꺼내 쓰는 거랑
- [2:02](https://youtube.com/watch?v=TGSV1CGAGfw&t=122) 똑같아요. 둘째 환경은 사무실이에요.
- [2:04](https://youtube.com/watch?v=TGSV1CGAGfw&t=124) 파이썬이 미리 깔린 책상. 외부
- [2:07](https://youtube.com/watch?v=TGSV1CGAGfw&t=127) 인터넷 접속이 되는지 안 되는지 같은
- [2:09](https://youtube.com/watch?v=TGSV1CGAGfw&t=129) 네트워크룰, 미리 마운트해 놓은
- [2:11](https://youtube.com/watch?v=TGSV1CGAGfw&t=131) 파일들 이런 걸 다 포함한 클라우드
- [2:13](https://youtube.com/watch?v=TGSV1CGAGfw&t=133) 컨테이너 템플릿입니다. 셋째 세션은
- [2:15](https://youtube.com/watch?v=TGSV1CGAGfw&t=135) 그 사무실에 오늘 출근한 그
- [2:17](https://youtube.com/watch?v=TGSV1CGAGfw&t=137) 사람이에요. 환경이라는 사무실에
- [2:19](https://youtube.com/watch?v=TGSV1CGAGfw&t=139) 에이전트라는 직무를 가진 인스턴스가
- [2:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=141) 들어와서 실제로 일하는 한 번의
- [2:23](https://youtube.com/watch?v=TGSV1CGAGfw&t=143) 실행이죠. 마지막 넷째 이벤트는 그
- [2:25](https://youtube.com/watch?v=TGSV1CGAGfw&t=145) 사람이랑 우리가 주고받는
- [2:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=146) 메시지입니다. 사용자 메시지, 도구
- [2:29](https://youtube.com/watch?v=TGSV1CGAGfw&t=149) 실행 결과, 상태 업데이트가 다
- [2:31](https://youtube.com/watch?v=TGSV1CGAGfw&t=151) 이벤트로 흘러가요.이네 개만 외우시면
- [2:33](https://youtube.com/watch?v=TGSV1CGAGfw&t=153) 매니지드 에이전트의 거의 모든게
- [2:35](https://youtube.com/watch?v=TGSV1CGAGfw&t=155) 설명됩니다. 아참이 영상은 핑거로
- [2:38](https://youtube.com/watch?v=TGSV1CGAGfw&t=158) 만들었습니다. 이런 영상을 딸각으로
- [2:40](https://youtube.com/watch?v=TGSV1CGAGfw&t=160) 만드시려면 핑다 아이오에 접속해
- [2:42](https://youtube.com/watch?v=TGSV1CGAGfw&t=162) 보세요. 설명란에 링크가 있습니다.
- [2:45](https://youtube.com/watch?v=TGSV1CGAGfw&t=165) 제가 직접 녹음하고 편집해 하루 종일
- [2:47](https://youtube.com/watch?v=TGSV1CGAGfw&t=167) 만든 영상은 조회수가 1천도 안
- [2:48](https://youtube.com/watch?v=TGSV1CGAGfw&t=168) 나왔는데 딸깍 만든 영상들은 몇만의
- [2:51](https://youtube.com/watch?v=TGSV1CGAGfw&t=171) 조회수가 나오면서 영상마다 몇 만
- [2:53](https://youtube.com/watch?v=TGSV1CGAGfw&t=173) 원의 조회수 수익, 수십만 원의 강의
- [2:56](https://youtube.com/watch?v=TGSV1CGAGfw&t=176) 판매 수익이 있습니다. 판매하시는
- [2:58](https://youtube.com/watch?v=TGSV1CGAGfw&t=178) 전문 서비스나 상품이 있다면 딸각으로
- [3:00](https://youtube.com/watch?v=TGSV1CGAGfw&t=180) 만든 영상으로 내 서비스를 홍보할 수
- [3:02](https://youtube.com/watch?v=TGSV1CGAGfw&t=182) 있어요. 자, 이제 본격적으로 첫
- [3:05](https://youtube.com/watch?v=TGSV1CGAGfw&t=185) 에이전트 띄우는 가이드로 들어가
- [3:06](https://youtube.com/watch?v=TGSV1CGAGfw&t=186) 볼게요. 사전 준비는 정말
- [3:08](https://youtube.com/watch?v=TGSV1CGAGfw&t=188) 단순합니다. 클로드 AP 하나만
- [3:11](https://youtube.com/watch?v=TGSV1CGAGfw&t=191) 있으면 돼요. 그다음에 베타 헤더 한
- [3:13](https://youtube.com/watch?v=TGSV1CGAGfw&t=193) 줄만 추가하면 끝납니다. 헤더 이름은
- [3:15](https://youtube.com/watch?v=TGSV1CGAGfw&t=195) 화면에 띄어 드릴 테니 그대로
- [3:17](https://youtube.com/watch?v=TGSV1CGAGfw&t=197) 복사하시면 돼요. 모든 API 계정의
- [3:19](https://youtube.com/watch?v=TGSV1CGAGfw&t=199) 기본으로 활성화돼 있어서 따로 신청
- [3:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=201) 절차도 없어요. 단, 결과정이나
- [3:24](https://youtube.com/watch?v=TGSV1CGAGfw&t=204) 멀티에 같은 연구 프리뷰 기능은
- [3:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=206) 별도로 신청이 필요합니다. 다음은 첫
- [3:29](https://youtube.com/watch?v=TGSV1CGAGfw&t=209) 에이전트를 정의하는 단계예요. 코드는
- [3:31](https://youtube.com/watch?v=TGSV1CGAGfw&t=211) 아주 간단합니다. 어떤 모델을 쓸지,
- [3:34](https://youtube.com/watch?v=TGSV1CGAGfw&t=214) 어떤 시스템 프롬프트를 줄지, 어떤
- [3:36](https://youtube.com/watch?v=TGSV1CGAGfw&t=216) 도구를 붙일지 한 번에 적어서 보내면
- [3:39](https://youtube.com/watch?v=TGSV1CGAGfw&t=219) 아이디가 돌아옵니다. 예를 들어
- [3:41](https://youtube.com/watch?v=TGSV1CGAGfw&t=221) 기터브 이슈가 올라올 때마다 자동으로
- [3:43](https://youtube.com/watch?v=TGSV1CGAGfw&t=223) 분류해서 라벨을 붙이는 에이전트를
- [3:44](https://youtube.com/watch?v=TGSV1CGAGfw&t=224) 만든다고 해 볼게요. 시스템
- [3:46](https://youtube.com/watch?v=TGSV1CGAGfw&t=226) 프롬프트에 너는 기터브 이슈기다라고
- [3:48](https://youtube.com/watch?v=TGSV1CGAGfw&t=228) 적고 독구로는 웹 검색이랑 기타
- [3:51](https://youtube.com/watch?v=TGSV1CGAGfw&t=231) MCP 서버를 붙입니다. 호출 한
- [3:53](https://youtube.com/watch?v=TGSV1CGAGfw&t=233) 번이면 아이디가 발급되고 다음부터는
- [3:55](https://youtube.com/watch?v=TGSV1CGAGfw&t=235) 그 아이디만 부르면 같은 에이전트가
- [3:58](https://youtube.com/watch?v=TGSV1CGAGfw&t=238) 매번 불려 나와요. 다음은 환경
- [4:00](https://youtube.com/watch?v=TGSV1CGAGfw&t=240) 그러니까 사무실 만들기예요. 매니지드
- [4:02](https://youtube.com/watch?v=TGSV1CGAGfw&t=242) 에이전트는 컨테이너 템플릿을 미리
- [4:05](https://youtube.com/watch?v=TGSV1CGAGfw&t=245) 골라서 쓸 수 있어요. 파이썬 노드고
- [4:07](https://youtube.com/watch?v=TGSV1CGAGfw&t=247) 같은 주요 런타임이 사전 설치된
- [4:09](https://youtube.com/watch?v=TGSV1CGAGfw&t=249) 옵션이 있고 거기에 네트워크 룰을
- [4:11](https://youtube.com/watch?v=TGSV1CGAGfw&t=251) 토글로 설정합니다.이 에이전트는 외부
- [4:14](https://youtube.com/watch?v=TGSV1CGAGfw&t=254) 인터넷 접속 가능 또는 안됨.이
- [4:17](https://youtube.com/watch?v=TGSV1CGAGfw&t=257) 폴더만 쓰기 가능 또는 전체 가능
- [4:19](https://youtube.com/watch?v=TGSV1CGAGfw&t=259) 이런 식으로 권한을 잘게 쪼개는
- [4:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=261) 거죠. 어제 영상에서 강조했던 권한
- [4:23](https://youtube.com/watch?v=TGSV1CGAGfw&t=263) 화이트리스트가 여기서 자동으로
- [4:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=266) 강제돼요. 이제 진짜 실행입니다.
- [4:28](https://youtube.com/watch?v=TGSV1CGAGfw&t=268) 세션 시작 코출 한 번이면 에이전트가
- [4:30](https://youtube.com/watch?v=TGSV1CGAGfw&t=270) 환경 안에서 일을 시작해요. 결과는
- [4:33](https://youtube.com/watch?v=TGSV1CGAGfw&t=273) 서버센터 이벤트라는 스트리밍 방식으로
- [4:35](https://youtube.com/watch?v=TGSV1CGAGfw&t=275) 실시간으로 봤습니다. 에이전트가
- [4:38](https://youtube.com/watch?v=TGSV1CGAGfw&t=278) 도구를 호출할 때마다 결과가 나올
- [4:40](https://youtube.com/watch?v=TGSV1CGAGfw&t=280) 때마다 이벤트가 한 줄씩 흘러나와요.
- [4:42](https://youtube.com/watch?v=TGSV1CGAGfw&t=282) 그리고 진짜 좋은 건 도중에 사용자
- [4:45](https://youtube.com/watch?v=TGSV1CGAGfw&t=285) 이벤트를 보내서 방향을 바꿀 수도
- [4:47](https://youtube.com/watch?v=TGSV1CGAGfw&t=287) 있다는 거예요. 에이전트가 엉뚱한
- [4:49](https://youtube.com/watch?v=TGSV1CGAGfw&t=289) 길로 가는게 보이면 잠깐 다른 거
- [4:51](https://youtube.com/watch?v=TGSV1CGAGfw&t=291) 먼저 해 줘 하고 끼어들 수 있는
- [4:53](https://youtube.com/watch?v=TGSV1CGAGfw&t=293) 거죠. 세션이 끝나도 만들어 둔
- [4:55](https://youtube.com/watch?v=TGSV1CGAGfw&t=295) 파일은 그대로 남아 있고 그게 영속
- [4:57](https://youtube.com/watch?v=TGSV1CGAGfw&t=297) 파일 시스템이에요. 베타에더 추가,
- [4:59](https://youtube.com/watch?v=TGSV1CGAGfw&t=299) 에이전트 정의, 환경 선택, 세션
- [5:02](https://youtube.com/watch?v=TGSV1CGAGfw&t=302) 시작. 여기까지 정확히 32분
- [5:05](https://youtube.com/watch?v=TGSV1CGAGfw&t=305) 걸렸습니다. 여기까지 보시고 가장
- [5:07](https://youtube.com/watch?v=TGSV1CGAGfw&t=307) 궁금하신게 가격이실 텐데요. 매니지드
- [5:10](https://youtube.com/watch?v=TGSV1CGAGfw&t=310) 에이전트의 가격 구조는 의외로
- [5:12](https://youtube.com/watch?v=TGSV1CGAGfw&t=312) 정직합니다. 두 축이에요. 첫 번째
- [5:14](https://youtube.com/watch?v=TGSV1CGAGfw&t=314) 축은 우리가 늘 쓰던 표준 클로드
- [5:17](https://youtube.com/watch?v=TGSV1CGAGfw&t=317) 토큰 요금 변화 없습니다. 두 번째
- [5:19](https://youtube.com/watch?v=TGSV1CGAGfw&t=319) 축이 새로 추가된 부분인데 세션당
- [5:22](https://youtube.com/watch?v=TGSV1CGAGfw&t=322) 시간당 0.08달러예요.
- [5:24](https://youtube.com/watch?v=TGSV1CGAGfw&t=324) 그것도 그냥 시간당이 아니라 액티브
- [5:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=326) 런타임. 그러니까 에이전트가 실제로
- [5:28](https://youtube.com/watch?v=TGSV1CGAGfw&t=328) 도구를 실행하면서 일하는 시간만
- [5:31](https://youtube.com/watch?v=TGSV1CGAGfw&t=331) 과금됩니다. 가만히 대기 중인 세션은
- [5:33](https://youtube.com/watch?v=TGSV1CGAGfw&t=333) 시간 비용이 거의 안 붙어요.
- [5:35](https://youtube.com/watch?v=TGSV1CGAGfw&t=335) 100원짜리 동전 하나가 안 되는
- [5:36](https://youtube.com/watch?v=TGSV1CGAGfw&t=336) 금액이라는 거죠. 그래서 누가
- [5:38](https://youtube.com/watch?v=TGSV1CGAGfw&t=338) 이득이고 누가 손해냐 이득 보시는
- [5:41](https://youtube.com/watch?v=TGSV1CGAGfw&t=341) 분은 명확합니다. 한시간씩 또는
- [5:44](https://youtube.com/watch?v=TGSV1CGAGfw&t=344) 백그라운드 자동화, 다수 도구를
- [5:46](https://youtube.com/watch?v=TGSV1CGAGfw&t=346) 연속으로 호출해야 하는 워크플로우,
- [5:48](https://youtube.com/watch?v=TGSV1CGAGfw&t=348) 상태가 계속 유지돼야 하는 작업.
- [5:50](https://youtube.com/watch?v=TGSV1CGAGfw&t=350) 이런 비동기 워크로드면 매니지드
- [5:52](https://youtube.com/watch?v=TGSV1CGAGfw&t=352) 에이전트가 거의 무조건 이득이에요.
- [5:55](https://youtube.com/watch?v=TGSV1CGAGfw&t=355) 직접 인프라 짜는데 한 달 걸릴 걸
- [5:57](https://youtube.com/watch?v=TGSV1CGAGfw&t=357) 시간당 0.08달러로 08달러로
- [5:58](https://youtube.com/watch?v=TGSV1CGAGfw&t=358) 끝내니까요. 반대로 손해 보시는 분도
- [6:01](https://youtube.com/watch?v=TGSV1CGAGfw&t=361) 있어요. 사용자가 옆에서 보면서 즉시
- [6:03](https://youtube.com/watch?v=TGSV1CGAGfw&t=363) 답을 받아야 하는 동기형 채포이라면
- [6:05](https://youtube.com/watch?v=TGSV1CGAGfw&t=365) 일반 메세지스 API가 여전히 더
- [6:07](https://youtube.com/watch?v=TGSV1CGAGfw&t=367) 쌉니다. 그리고 에이전트 루프 자체를
- [6:10](https://youtube.com/watch?v=TGSV1CGAGfw&t=370) 직접 만지고 싶은 연구 개발
- [6:12](https://youtube.com/watch?v=TGSV1CGAGfw&t=372) 케이스에도 안 맞아요. 한마디로
- [6:14](https://youtube.com/watch?v=TGSV1CGAGfw&t=374) 무거운 자동화에는 이득, 가벼운
- [6:16](https://youtube.com/watch?v=TGSV1CGAGfw&t=376) 체스에는 손해. 혹시 이거 인디
- [6:18](https://youtube.com/watch?v=TGSV1CGAGfw&t=378) 개발자용 작은 베타 아니냐 하실 수도
- [6:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=381) 있는데 사실 정반대예요. 이미 노션,
- [6:24](https://youtube.com/watch?v=TGSV1CGAGfw&t=384) 라쿠텐 아사나 바이브코드 센트리
- [6:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=386) 같은 회사들이 베타에 합류해서 코드
- [6:29](https://youtube.com/watch?v=TGSV1CGAGfw&t=389) 자동화 생산성 인사 재무
- [6:32](https://youtube.com/watch?v=TGSV1CGAGfw&t=392) 워크플로우에 통합하고 있습니다. 즉
- [6:35](https://youtube.com/watch?v=TGSV1CGAGfw&t=395) 1인 개발자용 장난감 베타가 아니라
- [6:37](https://youtube.com/watch?v=TGSV1CGAGfw&t=397) 엔터프라이즈가 이미 검증하고 있는
- [6:39](https://youtube.com/watch?v=TGSV1CGAGfw&t=399) 인프라는 뜻이에요. 우리가 지금 만져
- [6:42](https://youtube.com/watch?v=TGSV1CGAGfw&t=402) 보는게 곧 표준이 될 가능성이 높다는
- [6:44](https://youtube.com/watch?v=TGSV1CGAGfw&t=404) 거죠. 그래서 베타라는 이유로 미루지
- [6:46](https://youtube.com/watch?v=TGSV1CGAGfw&t=406) 마시고 오늘 한번 띄어 보시는 걸
- [6:48](https://youtube.com/watch?v=TGSV1CGAGfw&t=408) 추천드립니다. 정리해 볼게요.
- [6:50](https://youtube.com/watch?v=TGSV1CGAGfw&t=410) 매니지드 에이전트는 한 줄로 말해
- [6:53](https://youtube.com/watch?v=TGSV1CGAGfw&t=413) 에이전트 인프라의 무거운 짐 다섯
- [6:54](https://youtube.com/watch?v=TGSV1CGAGfw&t=414) 개를 엔스로픽이 통째로 들고 간
- [6:57](https://youtube.com/watch?v=TGSV1CGAGfw&t=417) 서비스입니다. 외울 건네 개.
- [6:59](https://youtube.com/watch?v=TGSV1CGAGfw&t=419) 에이전트 환경 세션 이벤트. 베타
- [7:02](https://youtube.com/watch?v=TGSV1CGAGfw&t=422) 헤더 한 줄만 추가하면 오늘 당장 첫
- [7:04](https://youtube.com/watch?v=TGSV1CGAGfw&t=424) 세션을 띄울 수 있어요. 장시간
- [7:06](https://youtube.com/watch?v=TGSV1CGAGfw&t=426) 비동기 워크로드에는 거의 무조건
- [7:08](https://youtube.com/watch?v=TGSV1CGAGfw&t=428) 이득이고 빠른 동기형 채포에는 일반
- [7:11](https://youtube.com/watch?v=TGSV1CGAGfw&t=431) API가 여전히 더 쌉니다. 영상이
- [7:13](https://youtube.com/watch?v=TGSV1CGAGfw&t=433) 도움되셨다면 좋아요와 구독 그리고
- [7:15](https://youtube.com/watch?v=TGSV1CGAGfw&t=435) 댓글에 만들고 싶은 에이전트 시나리오
- [7:17](https://youtube.com/watch?v=TGSV1CGAGfw&t=437) 한 줄만 남겨 주세요. 다른 분들
- [7:19](https://youtube.com/watch?v=TGSV1CGAGfw&t=439) 댓글이 분명히 영감이 될 거예요.
- [7:21](https://youtube.com/watch?v=TGSV1CGAGfw&t=441) 약속드린 대로 매니지드 에이전트 핵심
- [7:24](https://youtube.com/watch?v=TGSV1CGAGfw&t=444) 가이드 PDF는.ai/팁스에서
- [7:26](https://youtube.com/watch?v=TGSV1CGAGfw&t=446) AI/팁에서 받으실 수
