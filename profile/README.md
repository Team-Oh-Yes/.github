# 💰 GrowMoney (그로우머니)

> 경제 스토리와 퀴즈, NFT 거래로 배우는 청소년 경제 학습 플랫폼

![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.5-brightgreen)
![MySQL](https://img.shields.io/badge/MySQL-8.0-blue)
![Redis](https://img.shields.io/badge/Redis-latest-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📖 프로젝트 소개

**GrowMoney**는 경제 개념이나 투자 개념을 쉽게 배우고 싶은 학생들을 위한 경제 학습 서비스입니다.

기획재정부 조사에 따르면, 학년이 올라갈수록 경제이해력이 낮아지는 현상이 발생하고 있습니다. 초등학생 61.5점, 중학생 51.9점, 고등학생 51.7점으로 학생들의 경제교육 강화가 필요한 상황입니다.

저희는 이 문제를 해결하기 위해 **시각적인 그림과 흥미로운 경제 스토리**를 활용한 체험형 학습 서비스를 개발했습니다.

## ✨ 주요 기능

### 📚 경제 학습 로드맵
- 10개 테마, 50개 단원으로 구성된 체계적인 경제 교육 커리큘럼
- 시각적 그림과 스토리텔링 기반 자발적 체험형 학습
- 단계별 진행, 중간 중단 및 자유로운 학습 지원

### 🎯 퀴즈 시스템
- 학습 내용 기반 경제 퀴즈
- 포인트 보상 시스템
- 틀린 문제 복습 기능

### 🎨 NFT 도감 & 뽑기
- 학습 보상으로 획득하는 NFT 캐릭터
- 테마별 다양한 NFT 컬렉션
- 뽑기 시스템을 통한 재미 요소

### 💱 NFT 거래소
- 사용자 간 NFT 거래 기능
- 포인트 기반 경제 시뮬레이션
- 실제 경제 원리 체험

### 🏆 랭킹 시스템
- 사용자별 학습 진도 및 퀴즈 점수 기반 랭킹
- 경쟁을 통한 학습 동기 부여

## 🛠️ 기술 스택

### Backend
| 기술 | 버전 | 용도 |
|------|------|------|
| Java | 21 | 메인 언어 |
| Spring Boot | 3.5.5 | 백엔드 프레임워크 |
| Spring Security | - | 인증/인가 |
| Spring Data JPA | - | ORM |
| MySQL | 8.0+ | 메인 데이터베이스 |
| Redis | latest | 토큰 관리, 캐싱 |
| JWT | 0.12.5 | 토큰 기반 인증 |
| Swagger | 2.8.8 | API 문서화 |

### Frontend
| 기술 | 용도 |
|------|------|
| React | UI 프레임워크 |
| Vite | 빌드 도구 |
| React Router | 라우팅 |
| Axios | HTTP 통신 |
| Styled-components | 스타일링 |
| React Query | 서버 상태 관리 |

### DevOps
| 기술 | 용도 |
|------|------|
| AWS EC2 | 서버 호스팅 |
| GitHub Actions | CI/CD |
| Docker | 컨테이너화 |

## 📁 프로젝트 구조

```
grow-up-money-server/
├── .github/workflows/          # CI/CD 설정
├── src/main/java/com/ohyes/GrowUpMoney/
│   ├── domain/
│   │   ├── user/               # 사용자 인증/관리
│   │   ├── roadmap/            # 학습 로드맵
│   │   ├── quiz/               # 퀴즈 시스템
│   │   ├── nft/                # NFT 관리
│   │   ├── marketplace/        # 거래소
│   │   ├── point/              # 포인트 시스템
│   │   ├── ranking/            # 랭킹
│   │   └── admin/              # 관리자
│   └── global/
│       ├── config/             # 설정 (Security, JWT, CORS 등)
│       ├── exception/          # 예외 처리
│       └── util/               # 유틸리티
└── src/main/resources/
    └── application.yml         # 환경 설정
```

## 🚀 설치 및 실행

### 요구사항
- Java 21+
- MySQL 8.0+
- Redis
- Gradle

### 1. 레포지토리 클론
```bash
git clone https://github.com/Team-Oh-Yes/grow-up-money-server.git
cd grow-up-money-server
```

### 2. 환경 설정
`src/main/resources/application.properties` 파일을 생성하고 다음 내용을 설정합니다:
```properties
# Database
spring.datasource.url=jdbc:mysql://localhost:3306/growupmoney
spring.datasource.username=your_username
spring.datasource.password=your_password

# Redis
spring.data.redis.host=localhost
spring.data.redis.port=6379

# JWT
jwt.secret=your_jwt_secret_key
```

### 3. 빌드 및 실행
```bash
# 빌드
./gradlew clean build -x test

# 실행
./gradlew bootRun
```

### 4. API 문서 확인
서버 실행 후 Swagger UI에서 API 문서를 확인할 수 있습니다:
```
http://localhost:8080/swagger-ui.html
```

## 👥 팀 소개 (Team Oh!Yes)

| 이름 | 역할 | 담당 |
|------|------|------|
| **문채원** | 총괄 팀장 | 프론트엔드, 프로젝트 관리 |
| **배준하** | 개발 팀장 | 백엔드, Git 관리, ERD 설계 |
| **김민지** | 디자인 팀장 | 백엔드, UI/UX 가이드라인, 로드맵 |
| **홍준기** | 팀원 | 백엔드, 인증 시스템, ERD 설계 |
| **한석주** | 팀원 | 프론트엔드, NFT 디자인 |
| **안재민** | 팀원 | 프론트엔드, NFT 디자인 |
| **최현수** | 팀원 | 프론트엔드, UI/UX 디자인 |

### 커밋 메시지 규칙
- `feat`: 새로운 기능 추가
- `fix`: 버그 수정
- `docs`: 문서 수정
- `style`: 코드 포맷팅
- `refactor`: 코드 리팩토링
- `test`: 테스트 코드
- `chore`: 빌드, 설정 변경

## 📄 라이센스

이 프로젝트는 MIT 라이센스를 따릅니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

⭐ 이 프로젝트가 도움이 되셨다면 Star를 눌러주세요!
