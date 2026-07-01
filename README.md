# 🛒 frontend

사내 구매 요청/승인 프로세스를 지원하는 Next.js 기반 커머스 플랫폼입니다.
상품 등록·조회부터 장바구니, 구매 요청, 예산 관리까지 조직 내 구매 흐름을 한 곳에서 처리합니다.

![Next.js](https://img.shields.io/badge/Next.js-App_Router-black?logo=next.js)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-black?logo=vercel)

**배포 링크:** [frontend042.vercel.app](https://frontend042.vercel.app/)

## 목차

- [팀원 구성](#팀원-구성)
- [기술 스택](#기술-스택)
- [시작하기](#시작하기)
- [파일 구조](#파일-구조)

## 팀원 구성

| 페이지 구분 | 인원 |
|------|-----------|
| 랜딩 · 로그인 · 회원가입 | 김민식 |
| 상품리스트 · 상품 상세 | 성재영 |
| 상품 등록 내역 | 주예송 |
| 장바구니 | 황인아 · 김민식 |
| 구매 요청 내역 | 이인창 |
| 구매 요청 관리 | 이인창 |
| 구매 내역 확인 | 이인창 · 김민식 |
| 회원관리 | 유찬혁 |
| 예산 관리 | 선태영 |

## 기술 스택

| 구분 | 사용 기술 |
|------|-----------|
| 프레임워크·언어 | **Next.js** (App Router), **React**, **TypeScript** |
| 스타일·UI | **Tailwind CSS**, **shadcn/ui**, **Radix UI**, **Storybook** |
| 상태 관리 | **Zustand** (클라이언트), **TanStack Query** (서버 상태·데이터 페칭) |
| 품질·도구 | **ESLint**, **Vitest** (테스트·Storybook 연동) |
| 배포 | **Vercel** |

자세한 도입 배경은 [`TECH_STACK.md`](./TECH_STACK.md)를 참고하세요.

## 시작하기

### 요구 사항

- `Node.js 20+`
- `npm`

### 설치 및 실행

```bash
# 의존성 설치
npm install

# 개발 서버 실행
npm run dev

# 프로덕션 빌드 / 실행
npm run build
npm run start
```

브라우저에서 [http://localhost:3000](http://localhost:3000) 으로 접속합니다.

### 그 외 스크립트

```bash
npm run lint              # 정적 검사
npm run storybook         # Storybook 개발 서버 (http://localhost:6006)
npm run build-storybook   # Storybook 정적 빌드
```

## 파일 구조

```text
frontend/
├── .cursor/                 # Cursor 규칙·설정
│   └── rules/
├── .storybook/              # Storybook 설정
├── github/                  # GitHub 관련 템플릿·워크플로(경로는 저장소 설정에 맞게 사용)
│   └── .github/
├── public/                  # 정적 자산(이미지·아이콘 등)
│   └── assets/
├── src/
│   ├── app/                 # App Router: 페이지·레이아웃·Route Handlers
│   │   ├── layout.tsx       # 루트 레이아웃
│   │   ├── page.tsx         # 홈(`/`)
│   │   ├── admin/           # 관리자(구매 이력·구매 관리 등)
│   │   ├── api/             # `route.ts` — 서버 API 라우트
│   │   │   ├── auth/
│   │   │   ├── budget/
│   │   │   ├── cart/
│   │   │   ├── expenses/
│   │   │   ├── invitations/
│   │   │   ├── purchase-requests/
│   │   │   └── seller/
│   │   ├── budget-mng/
│   │   ├── cart/
│   │   ├── guide/
│   │   ├── invite/
│   │   ├── invitations/
│   │   ├── login/
│   │   ├── members/
│   │   ├── product-register-history/
│   │   ├── productlist/
│   │   ├── products/
│   │   ├── profile/
│   │   ├── purchase-request-detail/
│   │   ├── purchase-requests/
│   │   └── signup/
│   ├── components/          # 공통 UI·레이아웃·도메인 컴포넌트
│   │   ├── auth/
│   │   ├── cart/
│   │   ├── header/
│   │   ├── layouts/
│   │   ├── menu/
│   │   └── ui/               # shadcn/ui 스타일 기반 프리미티브
│   ├── data/
│   ├── hooks/                # 공통 훅(`queries/` 등)
│   ├── lib/                  # 유틸·API 클라이언트·인증·장바구니 등
│   │   ├── api/
│   │   ├── auth/
│   │   ├── cart/
│   │   └── crypto/
│   ├── middleware.ts
│   ├── providers/            # React Provider 래퍼
│   ├── stores/               # Zustand 스토어
│   └── types/                # 공통 타입
├── components.json           # shadcn/ui 설정
├── eslint.config.mjs
├── next.config.ts
├── package.json
├── postcss.config.mjs
├── TECH_STACK.md             # 기술 스택·협업 참고
├── tsconfig.json
└── vitest.config.ts
```
