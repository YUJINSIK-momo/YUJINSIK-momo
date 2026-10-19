<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:3B82F6,100:111827&height=220&section=header&text=Jinsik%20Yu&fontSize=55&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=AI%20%C2%B7%20AX%20Backend%20%2F%20Infra%20Developer%20%7C%20Harness%20Engineering%20%7C%20AWS&descAlignY=58&descSize=16)

</div>

<div align="center">

### AI 가 일하는 길을 깔고, 사람이 결정하는 자리를 지키는 개발자

기획자가 Slack 에 적은 화면 요청이 코드 · 테스트 · 배포를 거쳐 **승인 버튼 하나로 끝나는 디자인 시스템 하네스**를 만들었고,  
상권 분석 서비스의 **AWS 인프라를 Terraform 으로 세워** GPT 리뷰 · Slack 결정 · 태그 배포로 이어지는 릴리스 하네스로 운영합니다.

모델에게는 판단만 맡기고, 반복 작업은 스크립트와 테스트가,  
되돌리기 어려운 일은 사람이 결정하도록 설계합니다.

<br/>

<a href="https://yujinsik-momo.github.io/Backend-Developer-Portfolio/">
  <img src="https://img.shields.io/badge/Portfolio-%EB%B0%94%EB%A1%9C%EA%B0%80%EA%B8%B0-2E6CF0?style=for-the-badge" />
</a>
<a href="https://yujinsik-momo.github.io/Design-Dev-Infra-Pipeline/">
  <img src="https://img.shields.io/badge/Harness%20Docs-%EC%83%88%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EC%A0%81%EC%9A%A9%EB%B2%95-7C5CE6?style=for-the-badge" />
</a>

</div>

<br/>

---

## 🧭 대표 작업 — 회사에서 운영 중

> 회사 저장소는 비공개라 코드 대신 설계 · 보안 · 운영 방식을 포트폴리오 상세 페이지에 정리했습니다.

### 디자인 시스템 하네스 · `AI · AX`

기획자가 Slack 폼에 화면 요청을 적으면 → 감시자가 집어 에이전트에게 넘기고 → 에이전트는 디자인 시스템 문서만 보고 화면 코드와 테스트를 만든 뒤 멈춥니다. PR · CI · 머지 · 배포 확인 · 결과 카드는 스크립트가 하고, 기획자는 배포된 화면을 보고 👍 승인 · 👎 반려 · 😕 개선을 누릅니다.

- 화면 요청 **27건 처리 · 27건 종료**, 요청 1건 11~15분
- 자동 테스트 **1,256개**, 문서 ↔ 코드 **30쌍** 자동 대조
- Figma 연동을 만들었다가 A/B 측정(요청과 어긋난 곳 4~5건 vs 0~1건) 뒤 처리 흐름에서 뺀 기록까지

`Claude Code Plugin · Skills` `launchd 러너` `Slack Socket Mode` `Next.js 16` `Base UI` `Tailwind v4`

[🔗 사례 보기](https://yujinsik-momo.github.io/Backend-Developer-Portfolio/work/design-harness)

### 상권 프로젝트 · `인프라 · 운영` · 회사 프로젝트

지도 · 상권 리포트 · AI 어시스턴트를 갖춘 공개 상권 분석 서비스. 빈 저장소에서 시작해 **15일 동안 운영 릴리스 20개**.

- **AWS**: Terraform 으로 ECS Fargate · ALB · ECR · S3 · Secrets Manager · CloudWatch · EventBridge · SES 구성, 월 약 $59
- **보안**: 배포 경로에 장기 키 없음(GitHub OIDC), 최소 권한 배포 역할, 혼동된 대리인 방지, 로그 위생, AI 개인정보 가림
- **릴리스 하네스**: develop → main PR → Codex 리뷰(읽기 전용) → Slack 결정 → 사람이 발행한 태그로만 배포
- 자동 테스트 **3,059개** + Terraform test 50회, 마이그레이션 up/down/up 검사

`Terraform` `ECS Fargate` `GitHub OIDC` `NestJS` `Next.js` `Socket.IO` `Gemini` `Codex CLI`

[🔗 사례 보기](https://yujinsik-momo.github.io/Backend-Developer-Portfolio/work/trade-area)

### 상권 프로젝트 운영 대시보드 · `인프라 · 운영`

로그 · 배포 · 인프라 · 개발 흐름을 한 화면에서. 배포 중 파드가 뜨고 내려가는 모습을 ArgoCD 처럼 보여 준다. 외부 의존성 0, 읽기 전용 IAM, 루프백 + 사설망 공유, 테스트 510개.

[🔗 사례 · 배포 재생 화면](https://yujinsik-momo.github.io/Backend-Developer-Portfolio/work/ops-dashboard#demo)

<br/>

---

## 🤖 LLM 을 붙인 업무 자동화

| 프로젝트 | 내용 | 기술 | 링크 |
|---|---|---|---|
| **사내 HR · 업무 시스템** | 근태 · 연차 · 사내 채팅 · 디자인 요청. Gemini 로 한/영/일 번역(용어 사전 주입)과 시안 이미지 생성 | Express · Prisma · PostgreSQL(RDS) · S3 · Gemini | [데모](https://yujinsik-momo.github.io/HR-System-Portfolio/) · [GitHub](https://github.com/YUJINSIK-momo/HR-System-Portfolio) |
| **AI 가상 회사** | 역할별 Claude 에이전트 10명이 일일 보고, CTO 에이전트가 GitHub 커밋을 읽고 코드 리뷰 | Claude API · Express 5 · Supabase · React | [데모](https://yujinsik-momo.github.io/AI-Agent/) · [GitHub](https://github.com/YUJINSIK-momo/AI-Agent) |
| **일본 고객 LINE 상담 백엔드** | Dialogflow 의도 감지 → 신뢰도 낮으면 LLM 폴백 → 주문 · 결제 · 배송 담당자에게 Slack 연결 | Express 5 · Dialogflow · OpenAI 호환 LLM · Prisma · Redis | [GitHub](https://github.com/YUJINSIK-momo/momotyan) |
| **스포츠 채널 LINE 챗봇** | 야구 · 축구 · 농구 채널별 일본어 챗봇. FAQ 유사도가 높으면 FAQ 로, 낮으면 Gemini 로 넘기는 하이브리드 응답 | FastAPI · LangChain · Gemini · LINE API | [GitHub](https://github.com/YUJINSIK-momo/LangChain_TEST_yuyu) |
| **Slack 한↔일 업무 번역 봇** | 사내 메시지를 양식째 번역하고 상태 버튼 · 담당자 멘션으로 업무 흐름 관리 | Slack Bolt · OpenAI | 비공개 |
| **Rabbit Secretary** | 트레이 상주 데스크톱 비서. 저장소 자체가 Claude Code 작업 키트(agents · commands · phase) 예시 | Tauri 2 · Rust · React 19 | [GitHub](https://github.com/YUJINSIK-momo/Rabbit-Secretary) |
| **LINE 공식 계정 챗봇 · CRM** | 고객 · 대화 저장, 자동 응답 ↔ 상담원 모드 전환, 리치 메뉴 자동 등록 | Vercel Serverless · Supabase · LINE API | [사이트](https://chatbot-jinsik.vercel.app) · [💬 @118htpvo](https://line.me/R/ti/p/@118htpvo) |

더 보기: [프로젝트 전체 (분야별 필터)](https://yujinsik-momo.github.io/Backend-Developer-Portfolio/work) — Drink E-commerce(NestJS · Prisma), Travel Website, Shoe Store Simulator 등

<br/>

---

## 🧱 일하는 원칙

1. **모델은 판단만, 반복은 스크립트가** — 변환 · 검증 · 배포처럼 정해진 일은 모델이 운전하지 않게 한다
2. **되돌리기 어려운 일은 사람이 누른다** — 인프라 반영 · 운영 배포 · 마이그레이션은 에이전트가 실행할 수 없게 막는다
3. **권한은 좁게, 예외는 기록으로** — 임시 자격 증명과 읽기 전용 권한, 피할 수 없는 장기 키는 예외로 적고 주기적으로 바꾼다
4. **기록이 정본이 되게** — 결정 · 규칙 · 절차를 저장소 문서에 남기고, 문서와 코드가 어긋나면 검사로 잡는다

<br/>

---

## 🛠 Tech Stack

<div align="center">

### AI · Agent

<img src="https://img.shields.io/badge/Claude%20Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/Claude%20API-191919?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" />
<img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" />
<img src="https://img.shields.io/badge/Dialogflow-FF9800?style=for-the-badge&logo=dialogflow&logoColor=white" />
<img src="https://img.shields.io/badge/Figma%20MCP-F24E1E?style=for-the-badge&logo=figma&logoColor=white" />

<br/>

### AWS · Infra

<img src="https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white" />
<img src="https://img.shields.io/badge/Amazon%20ECS-FF9900?style=for-the-badge&logo=amazonecs&logoColor=white" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white" />

<br/>

### Backend · Database

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" />
<img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" />
<img src="https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" />
<img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />

<br/>

### Frontend · Integration

<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
<img src="https://img.shields.io/badge/LINE-00C300?style=for-the-badge&logo=line&logoColor=white" />
<img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" />
<img src="https://img.shields.io/badge/WooCommerce-96588A?style=for-the-badge&logo=woocommerce&logoColor=white" />
<img src="https://img.shields.io/badge/WordPress-21759B?style=for-the-badge&logo=wordpress&logoColor=white" />

</div>

<br/>

---

## 🌱 Currently Learning

- 멀티 에이전트 오케스트레이션과 검증 루프
- LangGraph · RAG(임베딩 검색) 시스템
- 로컬 LLM 서빙과 비용 설계
- AWS 보안 운영(WAF · 관측 · 비용 최적화)

<br/>

---

## 🌏 Language

<div align="center">

<img src="https://img.shields.io/badge/Korean-Native-111827?style=for-the-badge" />
<img src="https://img.shields.io/badge/Japanese-JLPT%20N1-DC2626?style=for-the-badge" />

</div>

<br/>

---

## 📊 GitHub Activity

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=yujinsik-momo&theme=tokyo-night&hide_border=true" />

</div>

<br/>

---

## 📫 Contact

<div align="center">

<a href="https://yujinsik-momo.github.io/Backend-Developer-Portfolio/">
  <img src="https://img.shields.io/badge/Portfolio-yujinsik--momo.github.io-2E6CF0?style=for-the-badge" />
</a>

<a href="https://github.com/yujinsik-momo">
  <img src="https://img.shields.io/badge/GitHub-yujinsik--momo-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

<a href="mailto:jinsik2036@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-jinsik2036%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
</a>

<a href="https://line.me/R/ti/p/@118htpvo">
  <img src="https://img.shields.io/badge/LINE-Chatbot%20Demo-00C300?style=for-the-badge&logo=line&logoColor=white" />
</a>

</div>

<br/>

<div align="center">

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:111827,100:3B82F6&height=120&section=footer)

</div>
