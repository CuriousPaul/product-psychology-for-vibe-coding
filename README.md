# Product Psychology for Vibe Coding

> **PM이 바이브코딩으로 제품을 만들 때, 심리학 기반 설계 원칙을 자동 적용하는 Claude Code & OpenClaw 스킬**

---

## 한 줄 소개

Growth Design = Empathy Optimization. 사용자를 조종하는 게 아니라, 공감하는 설계를 한다.

---

## 5대 프레임워크

| 프레임워크 | 핵심 | 언제 사용? |
|-----------|------|-----------|
| **6P 스토리보드** | 고객 여정 맥락 파악 (Problem → Emotion → Action → Struggle → Attempt → Happy Ending) | 사용자 여정 설계, 페르소나 분석 |
| **BMAP** | 행동 = 동기(M) × 능력(A) × 자극(P) — 3가지 동시 충족 시에만 행동 발생 | 전환율 개선, 이탈 분석 |
| **B.I.A.S** | Block(필터 통과) → Interpret(가치 해석) → Act(행동 유도) → Store(기억 저장) | UI/UX 설계, 리뷰 |
| **Peak-End** | 경험의 "평균"이 아니라 "정점"과 "마지막"을 기억함 | 사용자 여정 최적화 |
| **윤리 체크** | Regret Test, Black Mirror Test, In Real-Life Test | 출시 전 검토 |

---

## 설치 방법

### OpenClaw 사용자

```bash
cd ~/.openclaw/skills/
git clone https://github.com/CuriousPaul/product-psychology-for-vibe-coding.git
```

### Claude Code 사용자

**방법 1: 프로젝트별 적용**
```bash
# 프로젝트 루트에 .claude 폴더 생성
mkdir -p your-project/.claude

# CLAUDE.md 파일로 복사
curl -o your-project/.claude/CLAUDE.md \
  https://raw.githubusercontent.com/CuriousPaul/product-psychology-for-vibe-coding/main/SKILL.md
```

**방법 2: 전역 룰로 적용**
```bash
# Claude Code 전역 룰 폴더에 저장
mkdir -p ~/.claude/rules

curl -o ~/.claude/rules/product-psychology.md \
  https://raw.githubusercontent.com/CuriousPaul/product-psychology-for-vibe-coding/main/SKILL.md
```

**방법 3: 커맨드로 등록**
```bash
# Claude Code 커맨드 폴더에 저장
mkdir -p ~/.claude/commands

curl -o ~/.claude/commands/ux-review.md \
  https://raw.githubusercontent.com/CuriousPaul/product-psychology-for-vibe-coding/main/references/review-checklist.md
```

이제 Claude Code에서 `/ux-review` 명령어로 바로 사용 가능!

---

## 파일 구조

```
product-psychology-for-vibe-coding/
├── SKILL.md                      # 메인 스킬 정의
├── README.md                     # 이 파일
├── LICENSE                       # MIT License
└── references/
    ├── bias-framework.md         # B.I.A.S 상세 가이드
    ├── review-checklist.md       # 통합 리뷰 체크리스트
    ├── ethics-checklist.md       # 윤리적 디자인 체크리스트
    └── prompt-templates.md       # PM용 프롬프트 템플릿
```

---

## 활용 시나리오

- **화면/컴포넌트 생성**: 랜딩페이지, 온보딩, 결제, 가격표 등
- **사용자 플로우 설계**: 회원가입, 구매, 기능 탐색 등의 흐름
- **문구/카피 작성**: CTA, 알림, 이메일, 에러 메시지 등
- **기획/분석**: 사용자 여정 분석, 전환율 개선 가설, A/B 테스트 설계
- **리뷰/피드백**: 기존 UI/UX에 대한 심리학 기반 리뷰

---

## Quick Review (5분)

1. **한 화면에 선택지가 6개를 넘지 않는가?** (Block - Hick's Law)
2. **혜택이 기능 설명보다 먼저 보이는가?** (Interpret - Clear Benefit)
3. **다음에 해야 할 행동이 명확한가?** (Act - Remove Options)
4. **행동 후 피드백이 즉시 나오는가?** (Store - Clear Feedback)
5. **이 화면을 사용자가 보고 있다면 후회할 것 같은 부분이 있는가?** (Ethics - Regret Test)

---

## 라이선스

MIT License - 자유롭게 사용, 수정, 배포 가능

---

## 만든이

**정성영 (Paul Jung)**
- 마켓핏랩 대표 (mfitlab.com)
- AI Agent 개발 & AX(Agent Experience) 컨설팅
- 그로스해킹, 마테크 15년+

---

**핵심 철학**: "논리로 만들고(System 2), 사용자는 본능으로 사용한다(System 1). 이 Gap을 메운다."
