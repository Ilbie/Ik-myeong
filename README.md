# Ik-myeong (잌명) - 중고등학생용 익명 SNS

> **안내**: 이 프로젝트는 개발 도중 갑작스럽게 중단되어 현재 상태로 공유합니다. 코드 분석 결과 아래 기능들이 구현되어 있습니다.

## 프로젝트 소개

Ik-myeong(잌명)은 중고등학생들이 익명으로 소통할 수 있는 소셜 네트워킹 서비스입니다. 학생들이 자유롭게 의견을 나누고 공감대를 형성할 수 있는 안전한 온라인 공간을 제공하는 것을 목표로 합니다.

## 구현된 기능

- **익명 소통**: 개인정보 없이 별명으로 활동
- **사용자 인증**: 회원가입, 로그인, JWT 기반 인증
- **프로필 관리**: 사용자 정보 조회 및 수정
- **소셜 피드**: 게시물 작성 및 조회
- **실시간 메시지**: Socket.io 기반 채팅 기능
- **반응형 디자인**: 모바일, 태블릿, 데스크톱 지원

## 프로젝트 구조

```
sns/
├── frontend/  # Next.js 클라이언트 (포트: 8000)
└── backend/   # NestJS 서버 (포트: 8888)
```

## 기술 스택

### 프론트엔드
- Next.js 15.1.6 / React 19
- TypeScript
- Tailwind CSS
- Socket.io-client

### 백엔드
- NestJS 10.x
- TypeORM / PostgreSQL
- JWT 인증
- Socket.io

## 간단한 설치 방법

### 백엔드

```bash
cd backend
cp .env.example .env  # 환경 변수 설정
npm install
npm run start:dev
```

### 프론트엔드

```bash
cd frontend
cp .env.example .env  # 환경 변수 설정
npm install
npm run dev
```

## 환경 변수 설정

각 디렉토리의 `.env.example` 파일을 참고하여 `.env` 파일을 생성하세요.

## 소스코드 분석

### 프론트엔드
- **인증 로직**: `src/app/context/auth` - JWT 토큰 관리 및 사용자 세션 유지
- **UI 컴포넌트**: `src/app/components` - 재사용 가능한 UI 요소
- **페이지**: 로그인, 회원가입, 프로필, 메인 피드 페이지 구현

### 백엔드
- **인증 모듈**: `src/auth` - 사용자 인증 및 보안
- **사용자 모듈**: `src/user` - 사용자 정보 관리
- **보안 기능**: CSRF 보호, 비밀번호 암호화, 요청 속도 제한 구현

## 프로젝트 상태

현재 이 프로젝트는 다음 상태로 중단되었습니다:
- 기본 인증 시스템 구현 완료
- 프로필 관리 기능 구현 완료
- 소셜 피드 기본 기능 구현
- 실시간 메시지 기능 부분적 구현
- UI/UX 개선 필요

## 라이센스

MIT 라이센스

## 기술 스택

### 프론트엔드
- **Next.js 15.1.6**: 풀스택 React 프레임워크로 서버 사이드 렌더링 지원
- **React 19.0.0**: 사용자 인터페이스 구축을 위한 최신 라이브러리
- **TypeScript**: 정적 타입 지원으로 개발 안정성 향상
- **Tailwind CSS**: 유틸리티 기반 CSS 프레임워크로 빠른 UI 개발 지원
- **Socket.io-client**: 실시간 양방향 통신을 위한 클라이언트 라이브러리
- **Framer Motion**: 부드러운 애니메이션 효과 구현 라이브러리
- **HeroIcons**: 디자인 시스템과 일관성 있는 아이콘 세트

### 백엔드
- **NestJS 10.x**: 확장 가능한 Node.js 서버 프레임워크
- **TypeORM**: 객체 관계형 매핑(ORM) 라이브러리
- **PostgreSQL**: 강력한 오픈소스 관계형 데이터베이스
- **JWT**: JSON Web Token 기반 인증 시스템
- **PassportJS**: 다양한 인증 전략을 지원하는 미들웨어
- **Mailgun**: 이메일 서비스 통합
- **Winston**: 강력한 로깅 시스템
- **Class Validator**: 데이터 유효성 검사
- **Helmet**: HTTP 헤더 보안 강화
- **Throttler**: API 요청 속도 제한

## 설치 및 실행 방법

### 사전 요구사항
- Node.js (v18 이상 권장)
- PostgreSQL 데이터베이스
- npm 또는 yarn 패키지 관리자

### 백엔드 설치 및 실행

```bash
# 백엔드 디렉토리로 이동
cd backend

# 환경 변수 설정
cp .env.example .env
# .env 파일을 편집하여 데이터베이스 설정을 구성하세요

# 의존성 설치
npm install

# 개발 모드로 실행
npm run start:dev

# 또는 프로덕션 빌드 후 실행
npm run build
npm run start:prod
```

### 프론트엔드 설치 및 실행

```bash
# 프론트엔드 디렉토리로 이동
cd frontend

# 환경 변수 설정
cp .env.example .env

# 의존성 설치
npm install

# 개발 모드로 실행 (기본 포트: 8000)
npm run dev

# 또는 프로덕션 빌드 후 실행
npm run build
npm run start
```

## 환경 변수 설정

프로젝트 실행 전 각 디렉토리에 `.env` 파일을 설정해야 합니다. 보안을 위해 실제 프로젝트에서는 `.env` 파일을 Git에 커밋하지 마세요.

### 프론트엔드 (.env)
```
NEXT_PUBLIC_BACKEND_URL=http://localhost:8888
```

### 백엔드 (.env)
```
# 데이터베이스 설정
DATABASE_HOST=localhost
DATABASE_PORT=5432
DATABASE_USERNAME=your_username
DATABASE_PASSWORD=your_password
DATABASE_NAME=sns

# JWT 설정
JWT_SECRET=your_jwt_secret
JWT_EXPIRATION=30m
JWT_REFRESH_SECRET=your_refresh_secret
JWT_REFRESH_EXPIRATION=7d

# 환경 설정
NODE_ENV=development
FRONTEND_URL=http://localhost:8000

# 메일 서비스 설정 (선택사항)
MAILGUN_API_KEY=your_mailgun_api_key
MAILGUN_DOMAIN=your_mailgun_domain
```

## 주요 기능

### 사용자 인증
- 회원가입: 이메일 인증을 통한 안전한 회원가입 프로세스
- 로그인/로그아웃: JWT 기반 인증 시스템
- 비밀번호 재설정: 이메일을 통한 비밀번호 재설정

### 프로필 관리
- 사용자 프로필 조회 및 수정
- 프로필 이미지 업로드
- 개인 정보 관리

### 소셜 피드
- 게시물 작성, 수정, 삭제
- 이미지 첨부 기능
- 댓글 및 좋아요 기능
- 실시간 피드 업데이트

### 실시간 기능
- Socket.io를 활용한 실시간 메시지
- 실시간 알림
- 사용자 온라인 상태 표시

## 프로젝트 기여 방법

이 프로젝트에 기여하고 싶으시다면 다음 절차를 따라주세요:

1. 이 저장소를 포크(Fork)합니다
2. 새 브랜치를 생성합니다 (`git checkout -b feature/amazing-feature`)
3. 변경사항을 커밋합니다 (`git commit -m 'Add some amazing feature'`)
4. 브랜치에 푸시합니다 (`git push origin feature/amazing-feature`)
5. Pull Request를 생성합니다

### 코드 스타일 가이드

- **프론트엔드**: ESLint 규칙을 따르며, 컴포넌트는 함수형 컴포넌트로 작성합니다
- **백엔드**: NestJS 공식 스타일 가이드를 따릅니다
- **커밋 메시지**: 명확하고 간결하게 작성하며, 다음 형식을 권장합니다:
  - `feat:` 새로운 기능 추가
  - `fix:` 버그 수정
  - `docs:` 문서 변경
  - `style:` 코드 스타일 변경
  - `refactor:` 코드 리팩토링
  - `test:` 테스트 코드 추가/수정
  - `chore:` 빌드 프로세스 변경

### 이슈 보고

버그를 발견하거나 새로운 기능을 제안하고 싶다면 GitHub 이슈를 통해 보고해주세요. 이슈를 생성할 때는 다음 정보를 포함해주세요:

- 버그의 경우: 문제 현상, 재현 방법, 예상 결과, 실제 결과
- 기능 제안의 경우: 필요성, 구현 아이디어, 예상 효과

## 동작 화면 및 설명 추가하기

GitHub 리포지토리를 더 매력적으로 만들기 위해 동작 화면(스크린샷)과 설명을 추가하는 것이 좋습니다:

1. 주요 페이지의 스크린샷을 `screenshots` 폴더에 추가하세요.
2. 애플리케이션 사용 방법을 보여주는 GIF 또는 짧은 비디오를 추가하세요.
3. 각 주요 기능의 간략한 설명과 함께 스크린샷을 README에 포함하세요.

예시:
```markdown
### 메인 피드 화면
![메인 피드](screenshots/main-feed.png)
메인 피드에서는 사용자들의 게시물을 확인하고 댓글을 달 수 있습니다.

### 프로필 페이지
![프로필](screenshots/profile.png)
사용자 프로필 페이지에서는 개인 정보와 게시물을 관리할 수 있습니다.
```

## 연락처

프로젝트에 대한 문의나 기여하고 싶으시다면 GitHub 이슈를 등록해주세요. 