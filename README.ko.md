[English](README.md) | [한국어](README.ko.md)

# Cloth Simulation (옷감 시뮬레이션)

브라우저에서 직접 실행되는 고성능 대화형 물리 기반 옷감 시뮬레이션입니다. 이 프로젝트는 스프링, 제약 조건(constraints), 공기 역학적 드래그(drag) 모델을 사용하여 상호 연결된 점들의 그리드를 시뮬레이션함으로써 사실적인 직물 동작을 구현합니다.

## 주요 기능

- **사실적인 물리 엔진:** Verlet 적분 및 제약 조건 이완(constraint relaxation)을 사용하여 처음부터 직접 구축되었습니다. 질량, 강성(stiffness), 구조적 무결성과 같은 특성을 시뮬레이션합니다.
- **대화형 찢기(Tearing):** 클릭하고 드래그하여 옷감과 상호 작용할 수 있습니다. 너무 세게 당기면 천이 자연스럽게 찢어집니다.
- **재질 프리셋:** 고유한 물리적 특성을 가진 다양한 직물 유형 간에 전환할 수 있습니다:
  - **실크(Silk):** 가볍고 바람에 매우 민감하게 반응합니다.
  - **데님(Denim):** 뻣뻣하고 무거우며 잘 찢어지지 않습니다.
  - **린넨(Linen):** 실크와 데님 사이의 균형 잡힌 동작을 보여줍니다.
- **환경 제어:** 바람의 세기, 중력을 조절할 수 있으며, 마이크를 사용하여 옷감에 직접 바람을 불어넣을 수도 있습니다!
- **반응형 UI:** 데스크탑(HUD 사이드 패널 사용)과 모바일 기기(바텀 시트 사용) 모두에 최적화된 맞춤형 경험을 제공합니다.
- **다국어 지원:** UI에서 직접 영어와 한국어를 지원합니다.

## 기술 스택

- **코어:** HTML5 Canvas, Vanilla JavaScript (ES6+), Vanilla CSS.
- **아이콘:** Phosphor Icons.
- **폰트:** Pretendard, Noto Sans KR.
- **패키지 매니저:** `pnpm`.

## 시작하기

### 사전 요구 사항

[Node.js](https://nodejs.org/)와 [pnpm](https://pnpm.io/)이 설치되어 있는지 확인하세요.

### 설치 방법

1. 저장소를 클론하고 프로젝트 디렉토리로 이동합니다:
   ```bash
   cd Cloth-Sim-2026
   ```

2. 종속성을 설치합니다:
   ```bash
   pnpm install
   ```

### 로컬에서 실행하기

표준 정적 파일 서버를 사용하여 프로젝트를 실행할 수 있습니다. 예를 들어:
```bash
npx serve .
```
그런 다음, 브라우저에서 제공된 localhost URL을 열어 시뮬레이션을 확인하세요.

### 빌드 및 타입 검사

TypeScript 타입 검사를 실행하려면 (TypeScript 기능이나 라이브러리를 추가한 경우):
```bash
pnpm run typecheck
```

## 프로젝트 구조

- `index.html`: 메인 진입점. 전체 애플리케이션 레이아웃, HUD (Heads-Up Display), CSS 스타일링, 그리고 JavaScript로 작성된 전체 시뮬레이션 엔진을 포함하고 있습니다.
- `package.json` & `pnpm-workspace.yaml`: 프로젝트 메타데이터, 스크립트 명령어 및 작업 공간(workspace) 설정.
- `vercel.json`: Vercel 배포를 위한 설정 파일.

## 배포

이 프로젝트는 Vercel에 배포하도록 구성되어 있습니다. HTML에 포함된 `vercel.json` 및 `@vercel/analytics` 스크립트 태그를 통해 `vercel` CLI 명령어를 실행하거나 저장소를 Vercel 계정에 연결하여 쉽게 배포할 수 있습니다.

## 라이선스

MIT License
