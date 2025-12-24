# 전체 기술 역량 및 경력 요약

## 경력 개요
- **총 경력 기간**: 2024년 1월 24일 - 현재 (약 1년 11개월)
- **소속**: LFin (엘핀)
- **입사일**: 2024년 1월 24일
- **직무**: 모바일 소프트웨어 엔지니어 / SDK 개발자
- **전문 분야**: 크로스 플랫폼 모바일 개발, SDK 개발, 위치 기반 서비스

## 프로젝트 요약 (총 18개 프로젝트)

### SDK 개발 (8개 프로젝트)
- LPIN Android SDK (v1, v2)
- LPIN Android SDK Scanner
- LPIN Android SDK Encrypter
- LPIN Android SDK LZone
- LPIN Android SDK Requester
- LPIN iOS SDK
- React Native LPIN SDK
- **기간**: 2024년 2월 - 현재 (약 1년 10개월)

### 프로덕션 앱 (10개 프로젝트)
1. **LIAS 앱** (Flutter, NHIS) - 2025년 2월 ~ 8월
2. **WorkPlus 앱** (React Native) - 2025년 1월 ~ 현재 (운영 중)
3. **서울교통공사 무태그 앱** (Android) - 2024년 8월 ~ 현재 (운영 중)
4. **출석 관리 앱 3종** (Android, iOS) - 2024년 3월 ~ 9월
   - 제주대학교 Android (2024년 3월)
   - 제주대학교 iOS (2024년 3월)
   - 기독간호대학교 Android (2024년 9월)
5. **PSRO 앱** (Android) - 2024년 3월 ~ 6월
6. **PLAC 데모 앱 2종** (Android)
   - 템플릿: 2025년 2월 ~ 7월
   - 미래에셋: 2025년 6월 (유지보수)
7. **LPIN 네트워크 유틸리티 앱** (React Native) - 2024년 9월 ~ 현재

## 핵심 기술 스택

### 모바일 플랫폼
| 플랫폼 | 기술 | 프로젝트 수 | 숙련도 |
|--------|------|-------------|--------|
| **Android Native** | Kotlin, Java | 12개 | 전문가 |
| **iOS Native** | Swift | 3개 | 고급 |
| **React Native** | TypeScript | 3개 | 고급 |
| **Flutter** | Dart | 1개 | 중급 |

### 개발 역량 매트릭스

#### 1. SDK 개발 및 아키텍처 설계
**경험**: 1년 10개월 (2024년 2월 ~ 현재)
- **모놀리식 → 모듈형 전환**: Android SDK v1 → v2 (2024년 2월 시작)
- **멀티 플랫폼 SDK**: Android, iOS, React Native 3개 플랫폼
- **독립 모듈 설계**: 8개 독립 모듈 (Scanner, Encrypter, Requester, LZone 등)
- **API 디자인**: 플랫폼별 최적화, 일관된 API

**주요 성과**:
- LPIN SDK 에코시스템 전체 아키텍처 설계 및 개발
- 레거시 시스템을 Clean Architecture로 마이그레이션
- GitHub Package Registry 배포 및 버전 관리

#### 2. 위치 기반 서비스 (LBS)
**경험**: 1년 10개월 (2024년 2월 ~ 현재)
- **데이터 소스**: Wi-Fi AP, BLE 비콘, GPS, 기지국
- **위치 인증**: PlacAuth, LazyPlacAuth (백그라운드)
- **정확도 향상**: 다중 소스 결합 알고리즘

**프로젝트**:
- LPIN SDK 에코시스템 (전 프로젝트)
- LIAS 앱 (공간 인식)
- 출석 관리 앱 (BLE 비콘)

#### 3. BLE (Bluetooth Low Energy) 및 비콘
**경험**: 1년 7개월 (2024년 2월 ~ 현재)
- **프로토콜**: iBeacon
- **기능**: 스캐닝, 광고, RSSI 거리 계산
- **플랫폼**: Android (AltBeacon), iOS (Core Bluetooth)

**프로젝트**:
- LPIN SDK Scanner 모듈
- 출석 관리 앱 3종 (제주대, 기독간호대)

#### 4. 크로스 플랫폼 개발
**경험**: 1년 11개월 (2024년 2월 ~ 현재)
- **React Native**: Turbo Module, New Architecture, JSI
- **Flutter**: MethodChannel, EventChannel, 네이티브 SDK 통합
- **공통 코드 재사용**: 플랫폼별 최적화와 통합 API 균형

**프로젝트**:
- React Native LPIN SDK (Turbo Module)
- LIAS 앱 (Flutter)
- WorkPlus 앱 (React Native)
- LPIN 네트워크 유틸리티 (React Native)

#### 5. 생체 인증 및 ML 통합
**경험**: 6개월 (2025년 2월 ~ 8월)
- **얼굴 인식**: PyTorch Mobile, dlib, Armadillo
- **네이티브 통합**: C++ 모듈, CMake, NDK
- **성능 최적화**: Semaphore 기반 병렬 처리 (8개 동시 작업)

**프로젝트**:
- LIAS 앱 (NHIS 얼굴 인증)

#### 6. 금융 및 공공 부문 경험
**경험**: 1년 11개월 (2024년 1월 ~ 현재)
- **금융**: 미래에셋증권 PLAC SDK
- **공공**: 서울교통공사 무태그 결제 시스템
- **교육**: 제주대학교, 기독간호대학교 출석 시스템

**도메인 지식**:
- 금융 보안 요구사항
- 공공 부문 프로젝트 관리
- 교육 기관 커스터마이징

## 주요 기술 성과

### 아키텍처 및 설계
1. **모듈형 SDK 에코시스템 구축**
   - 8개 독립 모듈로 관심사 분리
   - 클라이언트 선택적 통합 가능
   - 독립적 버전 관리 및 배포

2. **Clean Architecture 적용**
   - LPIN Android SDK v2
   - PLAC 데모 템플릿
   - Data/Domain/Presentation 계층 분리

3. **멀티 플랫폼 통합 API**
   - Android, iOS, React Native 일관된 인터페이스
   - 플랫폼별 제약사항 문서화

### 성능 최적화
1. **병렬 처리**
   - Semaphore 기반 이미지 처리 (8 workers)
   - RxJava, RxSwift 반응형 프로그래밍
   - Kotlin Coroutines 비동기 작업

2. **데이터 캐싱**
   - 30초 캐시 메커니즘 (LPIN SDK v1)
   - Room Database 로컬 캐싱
   - MMKV 빠른 key-value 저장소

3. **React Native New Architecture**
   - Turbo Module 네이티브 성능
   - JSI 직접 메모리 접근
   - Codegen 타입 안전성

### 보안 및 암호화
1. **데이터 보호**
   - SHA256 해싱
   - AES 암호화/복호화
   - EncryptedSharedPreferences
   - Flutter Secure Storage

2. **생체 인증**
   - 얼굴 인식 FRR/FAR 테스트
   - 안전한 생체 데이터 저장

3. **Android 14 보안**
   - Conscrypt 보안 제공자
   - CA 인증서 수동 구현

### CI/CD 및 자동화
1. **배포 자동화**
   - Fastlane (Android, iOS, React Native)
   - Jenkins 웹훅 통합
   - CodePush OTA 업데이트

2. **테스트 자동화**
   - Maestro E2E 테스트 (30+ 시나리오)
   - Jest 유닛 테스트
   - GitHub Actions (CI)

3. **코드 품질**
   - SonarQube 정적 분석
   - ESLint, Prettier 린팅
   - ProGuard 난독화

## 협업 및 프로세스

### 버전 관리
- **Git**: 브랜칭 전략, Submodules
- **GitHub**: Package Registry, Pull Request
- **Semantic Versioning**: 체계적 버전 관리

### 코드 리뷰
- Pull Request Template 활용
- 코드 리뷰 문화
- 문서화 (README, CHANGELOG)

### 클라이언트 협업
- **B2B**: 미래에셋증권, 서울교통공사
- **B2G**: 교육 기관 (제주대, 기독간호대)
- **B2C**: NHIS (국민건강보험공단)

## 기술 트렌드 적용

### 최신 기술 도입
1. **React 19** (2025년 8월)
2. **React Native 0.80** (2025년 8월)
3. **Jetpack Compose** (2025년)
4. **React Native Unistyles v3** (2025년 9월)
5. **Swift Package Manager** (2024-2025)

### 모던 개발 패턴
- **MVVM**: ViewModel, LiveData/StateFlow
- **Clean Architecture**: 계층 분리
- **Dependency Injection**: Hilt, Koin, get_it
- **Reactive Programming**: RxJava, RxSwift, Coroutines
- **Type Safety**: TypeScript, Codegen

## 프로젝트별 핵심 기여

### LPIN SDK 에코시스템
- 전체 아키텍처 설계 및 개발
- 3개 플랫폼 SDK 개발 (Android, iOS, React Native)
- 8개 모듈형 컴포넌트 설계

### LIAS 앱
- Flutter 크로스 플랫폼 앱 개발
- 네이티브 SDK 통합 (Android 6개, iOS 3개)
- 생체 인증 및 위치 인증 구현

### WorkPlus 앱
- React Native 프로덕션 앱 개발
- E2E 테스트 자동화 (Maestro)
- CI/CD 파이프라인 구축

### 서울교통공사 무태그 앱
- 복잡한 SDK 통합 (T-Money, LPin)
- 멀티 Product Flavor 관리
- 공공 부문 프로젝트 수행

### 출석 관리 앱
- BLE 비콘 기반 출석 시스템
- 멀티 플랫폼 개발 (Android, iOS)
- 클라이언트 맞춤화 (2개 교육 기관)

## 도메인 지식

### 산업 분야
- **금융 (FinTech)**: 미래에셋증권
- **공공 (GovTech)**: 서울교통공사
- **교육 (EduTech)**: 제주대학교, 기독간호대학교
- **헬스케어**: 국민건강보험공단 (NHIS)
- **HR Tech**: WorkPlus 근태 관리

### 기술 도메인
- **위치 기반 서비스 (LBS)**
- **생체 인증 (Biometric Authentication)**
- **모바일 결제 (Mobile Payment)**
- **IoT (BLE 비콘, 센서 데이터)**
- **머신러닝 (얼굴 인식, PyTorch)**

## 언어 및 커뮤니케이션
- **프로그래밍 언어**: Kotlin, Swift, TypeScript, Dart, Java
- **문서화 언어**: 한국어 (주), 영어
- **기술 문서**: README, API 문서, 사용자 가이드

## 통계 요약

### 프로젝트 통계
- **총 프로젝트**: 18개
- **SDK 프로젝트**: 8개
- **프로덕션 앱**: 10개
- **활성 프로젝트**: 3개 (WorkPlus, Seoul Metro, 네트워크 유틸리티)

### 플랫폼 분포
- **Android Native**: 12개
- **iOS Native**: 3개
- **React Native**: 3개
- **Flutter**: 1개

### 클라이언트 분포
- **금융**: 1개 (미래에셋증권)
- **공공**: 1개 (서울교통공사)
- **교육**: 2개 (제주대, 기독간호대)
- **헬스케어**: 1개 (NHIS)
- **사내/상용**: 3개 (WorkPlus, 네트워크 유틸리티, PSRO)

## 지속적 학습 및 성장

### 기술 진화 추적 (LFin 입사 후)
- **2024년 1월-2월**: 입사 및 SDK 개발 시작 (Android SDK v1/v2, Scanner)
- **2024년 3월-8월**: iOS SDK 개발 시작, 다양한 프로덕션 앱 개발
- **2024년 9월-12월**: React Native 전환, 서울교통공사 프로젝트
- **2025년 1월-현재**: WorkPlus 대형 프로젝트, React Native New Architecture, LIAS Flutter 앱

### 버전 업그레이드 경험
- React Native 0.76 → 0.80
- React 18 → 19
- Unistyles v2 → v3
- Android SDK v1 → v2 (아키텍처 재설계)

## 강점 및 차별점

### 1. 풀스택 모바일 개발자
Android, iOS, React Native, Flutter 모든 주요 플랫폼 경험

### 2. SDK 설계 및 개발 전문성
단순 앱 개발을 넘어 재사용 가능한 라이브러리 설계

### 3. 위치 기반 서비스 전문가
6년 이상 LBS 도메인 경험, 다중 소스 위치 인증

### 4. 아키텍처 설계 역량
레거시 시스템 모더나이제이션, Clean Architecture 적용

### 5. 프로덕션 운영 경험
단순 개발을 넘어 CI/CD, 모니터링, 유지보수까지

### 6. 다양한 산업 도메인
금융, 공공, 교육, 헬스케어 도메인 이해

## 향후 발전 방향

### 기술적 목표
- **서버 사이드**: 백엔드 API 개발 역량 강화
- **클라우드**: AWS/GCP 인프라 경험 확대
- **AI/ML**: 모바일 ML 모델 최적화 심화

### 커리어 목표
- **리더십**: 모바일 팀 리드 역할
- **오픈소스**: SDK 오픈소스화
- **글로벌**: 해외 프로젝트 참여

## 연락처 및 포트폴리오
- **GitHub**: https://github.com/l-fin
- **Email**: david.seo@lfin.kr (추정)
- **회사**: LFin (엘핀)

---
*생성일: 2025-12-24*
*최종 수정일: 2025-12-24*
*분석 기준: MyBase 폴더 전체 프로젝트 (18개)*
