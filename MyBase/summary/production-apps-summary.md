# 프로덕션 모바일 앱 활동 요약

## 기본 정보
- **활동 기간**: 2024년 3월 - 현재 (약 1년 9개월)
- **입사일**: 2024년 1월 24일
- **소속 기관**: LFin (엘핀)
- **역할**: 모바일 앱 개발자 (Android, iOS, React Native)
- **활동 유형**: 상용 모바일 앱 개발 및 데모 프로젝트
- **참고**: 모든 프로젝트는 입사 후 본인이 작업한 것

## 프로젝트 개요
다양한 산업 분야(금융, 공공교통, 근태관리, 네트워크 유틸리티)를 위한 프로덕션급 모바일 애플리케이션 개발. SDK 데모, WebView 하이브리드 앱, React Native 크로스 플랫폼 앱 등 다양한 아키텍처 경험.

## 프로젝트 목록

### 1. LPIN Android PLAC 데모 (미래에셋증권)
- **클라이언트**: 미래에셋증권 (Mirae Asset Securities)
- **유형**: SDK 데모 및 라이브러리
- **플랫폼**: Android
- **기간**: ~ 2021년 12월
- **버전**: 1.0.26

### 2. LPIN Android PLAC 데모 템플릿
- **유형**: 클라이언트용 SDK 통합 템플릿
- **플랫폼**: Android
- **기간**: 2025년 3월 - 2025년 6월
- **버전**: 1.0.5

### 3. LPIN 네트워크 유틸리티 앱
- **유형**: 사내 도구
- **플랫폼**: React Native (Android & iOS)
- **버전**: 1.3.0

### 4. PSRO Android 앱
- **클라이언트**: PSRO
- **유형**: 프로덕션 WebView 앱
- **플랫폼**: Android
- **기간**: 2024년 3월 - 2024년 6월
- **버전**: 1.0.6

### 5. 서울교통공사 무태그 모바일 앱
- **클라이언트**: 서울교통공사 (Seoul Metro)
- **유형**: 공공 부문 프로덕션 앱
- **플랫폼**: Android
- **버전**: Tagless 1.2.52, SrTagless 2.1.52

### 6. WorkPlus 앱
- **유형**: 상용 근태 관리 앱
- **플랫폼**: React Native (Android & iOS)
- **기간**: ~ 2025년 9월
- **버전**: 1.1.13

## 주요 활동 내용

### 금융 부문: 미래에셋증권 PLAC SDK

#### 레거시 데모 (2021)
- **목적**: PLAC (Place Authentication) SDK 시연
- **기술 스택**:
  - Kotlin, Koin (DI), RxJava2
  - Room Database
  - Microsoft AppCenter (Analytics, Crashes)
- **기능**:
  - 위치 기반 인증
  - Scanner 관리 스케줄러
  - 암호화 지원
  - Dev/Prod 환경 분리

#### 최신 템플릿 (2025)
- **목적**: 클라이언트가 LPinSDK를 쉽게 테스트하고 통합할 수 있는 템플릿
- **아키텍처**: Clean Architecture (data/domain/presentation layers)
- **기술 스택**:
  - Kotlin, Jetpack Compose
  - Hilt (DI), MVVM 패턴
  - Room Database, Coroutines
- **기능**:
  - PlacAuth (위치 인증)
  - LazyPlacAuth (백그라운드 자동 인증)
  - 인증 재시도 정책 설정
  - Beacon 캐시 데이터 관리
  - WiFi, Location, Beacon 스캔
  - 인증 결과 시각화
  - 설정 UI

**성과**: 미래에셋증권과 같은 대형 금융 기관에 SDK 솔루션 제공

### 공공 부문: 서울교통공사 무태그 앱

#### 프로젝트 개요
- **목적**: 통신 기지국 연동 기반 무태그 결제 플랫폼
- **대상**: 서울교통공사 직원 모바일 ID 앱

#### 핵심 기술
- **통합 SDK**:
  - T-Money STM SDK
  - T-Money VCMS SDK
  - LPin SDK v2
- **결제 시스템**: 무태그 결제 플랫폼
- **QR 코드**: ZXing 라이브러리
- **푸시 알림**: OneSignal
- **분석**: Microsoft AppCenter

#### 아키텍처
- **의존성 주입**: Jetpack Hilt
- **내비게이션**: Navigation Component with SafeArgs
- **데이터 바인딩**: DataBinding
- **네트워크**: Retrofit, OkHttp, Volley
- **이미지**: Coil
- **백그라운드**: WorkManager
- **보안**: EncryptedSharedPreferences, DataStore

#### Product Flavors
- **tagless**: 버전 1.2.52 (versionCode 1000000052)
- **srTagless**: 버전 2.1.52 (versionCode 2000000052)

**성과**: 공공 교통 부문 정부 프로젝트 성공적 수행

### 상용 제품: WorkPlus 근태 관리 앱

#### 프로젝트 개요
- **플랫폼**: React Native (Android & iOS)
- **버전**: 1.1.13
- **최근 업데이트**: 2025년 9월

#### 핵심 기능
1. **인증**: 로그인/인증 시스템
2. **근태 관리**: 출퇴근 체크인/체크아웃
3. **방문 관리**: 방문 일정 시작/종료, 추가/수정/삭제
4. **일정 관리**: 휴가 신청, 캘린더 뷰
5. **지도**: Naver Map 통합 위치 서비스
6. **알림**: Notifee 푸시 알림
7. **OTA 업데이트**: CodePush

#### 기술 스택
- **코어**:
  - React Native 0.80.2
  - React 19.1.0
  - TypeScript 5.6.3
- **상태 관리**: Zustand v5.0.4
- **데이터 페칭**: TanStack React Query v5.75.5
- **내비게이션**: React Navigation v7 (Stack, Bottom Tabs)
- **폼**: React Hook Form + Zod/Yup 검증
- **스타일링**: React Native Unistyles v3
- **저장소**: MMKV (빠른 key-value 저장소)
- **HTTP**: Ky v1.7.5
- **날짜**: Dayjs

#### 개발 도구
- **테스팅**:
  - Maestro (E2E)
  - Jest (유닛 테스트)
- **CI/CD**:
  - Fastlane (배포 자동화)
  - Jenkins (웹훅 통합)
- **에러 모니터링**: Sentry v6.20.0
- **OTA**: CodePush (커스텀 포크 @chlee1001)

#### 환경 지원
- **환경**: mock, dev, prod
- **Node**: >=18
- **Ruby**: 3.0.5
- **JDK**: 21

#### 최근 주요 업데이트 (2025년)
- React Native 0.76.6 → 0.80.2 (8월)
- React 18.3.1 → 19.1.0 (8월)
- react-native-unistyles v2 → v3 (9월)

**성과**:
- 프로덕션 운영 중인 상용 앱
- 최신 기술 스택 지속적 업데이트
- E2E 테스트 자동화 구축

### 기타 프로젝트

#### PSRO Android 앱
- **유형**: WebView 기반 하이브리드 앱
- **기간**: 2024년 3월 - 6월 (버전 1.0.0 → 1.0.6)
- **기능**:
  - PSRO 웹사이트 표시
  - 로그인 인증 처리
  - 파일 다운로드/업로드
  - 다운로드 후 파일 실행
  - 전자세금계산서 통합 (Play Store 리다이렉트)
  - 카카오톡 상담 기능
  - 디버그 모드 (볼륨 다운 5회 → 엔드포인트 전환)
- **기술**: Kotlin, WebView, Material Design

#### LPIN 네트워크 유틸리티 앱
- **유형**: 사내 도구
- **플랫폼**: React Native
- **기능**:
  - LPin SDK 통합 (@l-fin/react-native-lpin-sdk)
  - 네트워크 정보 모니터링
  - 위치 서비스
  - 클립보드 기능
  - 디바이스 정보 접근
  - 파일 공유
- **기술**:
  - React Native 0.81.4
  - TypeScript 5.8.3
  - React Navigation
  - React Native Unistyles v3

## 주요 성과 및 산출물

### 1. 금융 부문 SDK 솔루션
- **클라이언트**: 미래에셋증권
- **성과**: PLAC SDK 라이브러리 및 통합 템플릿 제공
- **증빙**:
  - 📁 MyBase/lpin-android-plac-demo-mirae
  - 📁 MyBase/lpin-android-plac-demo-template

### 2. 공공 부문 프로젝트 수행
- **클라이언트**: 서울교통공사
- **성과**: 무태그 결제 시스템 직원용 앱 개발
- **증빙**: 📁 MyBase/seoul-metro-tagless-mobile-app

### 3. 상용 제품 개발 및 운영
- **제품**: WorkPlus 근태 관리 앱
- **성과**: 프로덕션 운영, 지속적 업데이트
- **증빙**: 📁 MyBase/work-plus-app

### 4. 다양한 아키텍처 경험
- **Clean Architecture**: LPIN 템플릿
- **MVVM**: Seoul Metro 앱
- **하이브리드 WebView**: PSRO 앱
- **React Native**: WorkPlus, 네트워크 유틸리티

### 5. CI/CD 파이프라인 구축
- **도구**: Fastlane, Jenkins, CodePush
- **성과**: 자동화된 빌드 및 배포 프로세스

### 6. E2E 테스트 자동화
- **프레임워크**: Maestro
- **프로젝트**: WorkPlus
- **성과**: 30개 이상의 E2E 테스트 시나리오 구축

## 습득한 기술 및 역량

### 기술 스택

#### Android 네이티브
- **언어**: Kotlin, Java
- **아키텍처**: Clean Architecture, MVVM
- **의존성 주입**: Hilt, Koin
- **UI**: Jetpack Compose, DataBinding, Material Design
- **데이터베이스**: Room
- **비동기**: Kotlin Coroutines, RxJava
- **네트워크**: Retrofit, OkHttp, Volley
- **보안**: EncryptedSharedPreferences

#### React Native
- **언어**: TypeScript, JavaScript
- **상태 관리**: Zustand, React Query
- **내비게이션**: React Navigation v7
- **폼**: React Hook Form + Zod/Yup
- **스타일링**: React Native Unistyles v3
- **저장소**: MMKV, AsyncStorage
- **네트워크**: Ky, Axios
- **지도**: Naver Map

#### 개발 도구 및 서비스
- **CI/CD**: Fastlane, Jenkins, CodePush
- **테스팅**: Jest, Maestro
- **모니터링**: Sentry, AppCenter, OneSignal
- **버전 관리**: Git, Submodules
- **코드 품질**: SonarQube, ESLint, Prettier

#### SDK 통합
- **결제**: T-Money SDK (STM, VCMS)
- **위치**: LPin SDK, Naver Map
- **QR 코드**: ZXing
- **인증**: 생체 인식, 위치 인증

### 소프트 스킬

#### 1. 다양한 산업 도메인 경험
- **금융**: 미래에셋증권
- **공공**: 서울교통공사
- **SaaS**: WorkPlus
- **일반 비즈니스**: PSRO

#### 2. 아키텍처 설계 및 전환
- **경험**: 레거시 SDK를 모던 Clean Architecture로 재설계
- **성과**: PLAC 데모 1.0.26 → 템플릿 1.0.5 (Clean Architecture)

#### 3. 클라이언트 맞춤 솔루션
- **경험**: SDK 템플릿 제작으로 클라이언트 통합 지원
- **성과**: 빠른 프로토타이핑 및 커스터마이징

#### 4. 프로덕션 운영 및 유지보수
- **경험**: WorkPlus 앱 지속적 업데이트 (React 18 → 19, RN 0.76 → 0.80)
- **성과**: 안정적인 프로덕션 서비스 운영

#### 5. 테스트 자동화
- **경험**: Maestro로 30개 이상 E2E 테스트 작성
- **성과**: 회귀 테스트 자동화로 품질 보장

## 협업 및 네트워킹
- **조직**: LFin (엘핀) 개발팀
- **클라이언트**: 미래에셋증권, 서울교통공사, PSRO
- **협업 도구**: Git, GitHub, Jenkins
- **코드 리뷰**: Pull Request, Code Review
- **문서화**: README, DEVELOP.md, 다양한 템플릿

## 기술적 도전과 해결

### 1. 복잡한 SDK 통합 (Seoul Metro)
- **도전**: T-Money SDK, LPin SDK, QR 코드 동시 통합
- **해결**: Hilt를 활용한 의존성 관리, 모듈형 구조 설계

### 2. 멀티 Product Flavor 관리
- **도전**: Tagless 및 SrTagless 두 가지 버전 동시 관리
- **해결**: Gradle build flavor 구성, 버전 코드 체계화

### 3. React Native 최신 버전 마이그레이션
- **도전**: React 18 → 19, React Native 0.76 → 0.80
- **해결**: 단계적 업그레이드, 종속성 충돌 해결

### 4. E2E 테스트 자동화
- **도전**: 복잡한 사용자 플로우 (로그인, 출퇴근, 방문 관리)
- **해결**: Maestro로 30개 시나리오 작성, CI 통합

### 5. OTA 업데이트 관리
- **도전**: 앱스토어 배포 없이 빠른 업데이트
- **해결**: CodePush 통합, 환경별 배포 전략

## 프로젝트 타임라인

| 날짜 | 프로젝트 | 이벤트 |
|------|---------|--------|
| 2021-12-14 | PLAC 데모 (미래에셋) | 버전 1.0.25 |
| 2024-03-06 | PSRO Android | 프로젝트 시작 (v1.0.0) |
| 2024-06-25 | PSRO Android | 최종 업데이트 (v1.0.6) |
| 2025-03-07 | PLAC 템플릿 | 프로젝트 시작 (v1.0.0) |
| 2025-06-25 | PLAC 템플릿 | 최종 업데이트 (v1.0.5) |
| 2025-08-27 | WorkPlus | React Native 0.80.2, React 19 업그레이드 |
| 2025-09-19 | WorkPlus | Unistyles v3 업그레이드 |
| 현재 | Seoul Metro, WorkPlus, 네트워크 유틸리티 | 프로덕션 운영 중 |

## 원본 데이터 출처
- 📁 MyBase/lpin-android-plac-demo-mirae/README.md
- 📁 MyBase/lpin-android-plac-demo-template/README.md
- 📁 MyBase/lpin-network-util-app/README.md
- 📁 MyBase/lpin-network-util-app/package.json
- 📁 MyBase/psro-android/README.md
- 📁 MyBase/seoul-metro-tagless-mobile-app/README.md
- 📁 MyBase/seoul-metro-tagless-mobile-app/app/build.gradle.kts
- 📁 MyBase/work-plus-app/README.md
- 📁 MyBase/work-plus-app/package.json
- 📁 MyBase/work-plus-app/DEVELOP.md

---
*생성일: 2025-12-24*
*최종 수정일: 2025-12-24*
