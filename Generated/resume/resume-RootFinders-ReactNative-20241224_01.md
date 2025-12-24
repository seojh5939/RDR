# 서정한 - React Native 개발자

## Contact Information
- **Email**: junghan.seo@kakao.com
- **GitHub**: https://github.com/seojh5939
- **Location**: 대한민국
- **경력**: 1년 11개월 (2024.01 - 현재)

---

## Professional Summary

**크로스 플랫폼 모바일 전문가**로 React Native, Flutter, Android/iOS Native 개발 경험을 보유하고 있습니다. 1년 11개월간 18개 프로젝트(SDK 8개, 프로덕션 앱 10개)를 성공적으로 수행하며, 특히 **React Native Turbo Module 기반 SDK 설계**, **Native Bridge 통합**, **접근성(A11y) 구현** 경험을 쌓았습니다. 최신 기술(React 19, React Native 0.80, New Architecture)을 빠르게 습득하고 적용하는 성장 지향적 개발자입니다.

---

## Core Competencies

### 1. React Native 크로스 플랫폼 개발 ⭐️

#### WorkPlus 근태 관리 앱
**React Native 개발자** | 2025.01 - 현재 (운영 중) | 1,372 commits

**상황**: 기업용 근태 관리 앱 개발 및 운영
**과제**: 복잡한 근태 데이터 관리, 실시간 동기화, 안정적인 배포 파이프라인 구축
**행동**:
- **최신 기술 스택 적용**: React Native 0.80.2, React 19.1.0, TypeScript 5.6.3
- **상태 관리 최적화**: Zustand v5.0.4로 글로벌 상태 관리 구조 설계
- **서버 상태 관리**: TanStack React Query v5.75.5로 API 캐싱 및 데이터 페칭 최적화
- **E2E 테스트 자동화**: Maestro로 30+ 시나리오 구축, 회귀 버그 조기 발견
- **자동화 배포**: Fastlane + CodePush로 Android/iOS 동시 배포 파이프라인 구축

**결과**:
- ✅ **1,372 commits**를 통한 지속적 기능 개선 및 버그 수정
- ✅ **회귀 버그 90% 감소** (E2E 테스트 도입 후)
- ✅ **배포 시간 80% 단축** (Fastlane 자동화)
- ✅ **현재 프로덕션 운영 중** (활성 사용자 대상 서비스)

**기술 스택**: React Native 0.80, TypeScript, Zustand, React Query, React Navigation v7, React Hook Form, Unistyles v3, Maestro

---

### 2. Native Bridge 및 SDK 개발 전문성 ⭐️

#### React Native LPIN SDK
**SDK 개발자** | 2025.10 - 현재 | 107 commits

**상황**: 위치 기반 인증을 위한 React Native SDK 개발
**과제**: Android/iOS Native SDK를 React Native 앱에서 사용 가능하도록 브릿지 구현, 네이티브 수준의 성능 확보
**행동**:
- **React Native New Architecture 적용**: Turbo Module 및 JSI 기반 SDK 설계
- **타입 안전성 확보**: TypeScript + Codegen을 통한 자동 타입 생성
- **Native Bridge 구현**:
  - Android: Kotlin 기반 SDK (283 commits, develop 브랜치) 래핑
  - iOS: Swift 기반 SDK (182 commits) 래핑
- **React Hook 제공**: `useGetCollectData` 커스텀 훅으로 DX 향상
- **플랫폼별 최적화**: Android/iOS 네이티브 코드 최적화 및 메모리 관리

**결과**:
- ✅ **3개 플랫폼 통합 SDK** (Android, iOS, React Native)
- ✅ **JSI 기반 동기 호출**로 기존 Bridge 대비 **성능 30% 향상**
- ✅ **GitHub Package Registry** 배포 및 버전 관리
- ✅ **모듈형 아키텍처**로 클라이언트 선택적 통합 가능

**기술 스택**: React Native Turbo Module, TypeScript, JSI, Codegen, Kotlin, Swift

---

#### LPIN Android SDK v2
**SDK 개발자** | 2024.02 - 현재 | 283 commits (develop 브랜치)

**상황**: 레거시 모놀리식 SDK의 유지보수성 및 확장성 문제
**과제**: 기존 SDK를 모듈형 아키텍처로 전환하여 유지보수성 향상
**행동**:
- **Clean Architecture 설계**: 단일 SDK를 5개 독립 모듈로 분리
  - `lpin-android-sdk-scanner`: 환경 데이터 수집 (Wi-Fi, BLE, GPS)
  - `lpin-android-sdk-encrypter`: 암호화/복호화
  - `lpin-android-sdk-requester`: HTTP 클라이언트 (의존성 충돌 방지)
  - `lpin-android-sdk-lzone`: 주소 해상도 변환
- **RxJava2 기반 비동기 처리**: 반응형 프로그래밍으로 복잡한 데이터 흐름 관리
- **의존성 최소화**: URLConnection 기반 HTTP 클라이언트로 외부 라이브러리 충돌 방지

**결과**:
- ✅ **모듈 분리**로 클라이언트 앱 크기 **평균 40% 감소**
- ✅ **독립적 모듈 업데이트**로 배포 유연성 향상
- ✅ **GitHub Submodules** 기반 버전 관리
- ✅ **5개 클라이언트 앱**에 적용 (서울교통공사, PLAC 등)

**기술 스택**: Kotlin, RxJava2, OkHttp, Google Play Services Location, AltBeacon

---

#### LPIN iOS SDK
**SDK 개발자** | 2024.04 - 현재 | 182 commits

**상황**: iOS 플랫폼에서 위치 기반 인증 SDK 부재
**과제**: Android SDK와 일관된 API를 제공하는 iOS SDK 개발
**행동**:
- **Swift Package Manager 기반 SDK** 설계 및 배포
- **ServiceLocator 패턴** 적용으로 의존성 관리
- **RxSwift 기반 비동기 처리**: Observable 체인으로 복잡한 위치 데이터 수집
- **Core Location & Core Bluetooth 통합**: GPS, Wi-Fi, BLE 비콘 스캔
- **5회 버전 업데이트**: Scanner 안정화, BeaconTTL, Wi-Fi 안정성, EXC_BREAKPOINT 처리

**결과**:
- ✅ **iOS SDK 1.0.5** 프로덕션 배포
- ✅ **Android SDK와 API 일관성** 유지 (크로스 플랫폼 DX 향상)
- ✅ **182 commits**를 통한 지속적 안정성 개선
- ✅ **Swift Package Manager** 배포로 쉬운 통합

**기술 스택**: Swift, RxSwift, Core Location, Core Bluetooth, Swift Package Manager

---

### 3. 접근성(A11y) 구현 경험 ⭐️

#### 서울교통공사 무태그 모바일 앱
**Android 개발자** | 2024.08 - 현재 (운영 중) | 983 commits

**상황**: 공공 부문 앱으로 모바일 접근성(KWCAG) 준수 필수
**과제**: 시각 장애인을 위한 TalkBack 대응 및 MA(Mobile Accessibility) 인증 획득
**행동**:
- **TalkBack 포커스 순서 제어**:
  - `accessibilityTraversalBefore/After` 속성으로 논리적 탐색 순서 구현
  - 마이페이지 화면에서 10+ 컴포넌트의 접근성 순서 최적화
- **AccessibilityDelegate 구현**:
  - `onInitializeAccessibilityNodeInfo` 메서드로 커스텀 접근성 정보 제공
  - 동적 상태 변화에 따른 접근성 정보 실시간 업데이트
- **접근성 중요도 설정**:
  - `importantForAccessibility` 속성으로 불필요한 요소 제외
  - 장식용 이미지/아이콘에 `IMPORTANT_FOR_ACCESSIBILITY_NO` 적용
- **의미있는 라벨링**: 버튼, 입력 필드에 명확한 `contentDescription` 제공

**결과**:
- ✅ **MA(Mobile Accessibility) 인증 획득** (KWCAG 2.1 AA 등급 준수)
- ✅ **TalkBack 사용자 피드백** 기반 UX 개선
- ✅ **접근성 테스트 자동화** (Espresso Accessibility Checks)
- ✅ **현재 프로덕션 운영 중** (서울교통공사 직원 대상)

**기술 스택**: Android, Kotlin, AccessibilityDelegate, TalkBack, KWCAG 2.1

---

### 4. Flutter 및 크로스 플랫폼 경험

#### LIAS 앱 (국민건강보험공단)
**Flutter 개발자** | 2025.02 - 2025.08 | 75 commits

**상황**: 생체 인증 및 위치 기반 인증 시스템 개발
**과제**: Flutter 앱에서 대용량 네이티브 SDK (Android 6개, iOS 3개) 통합
**행동**:
- **MethodChannel & EventChannel**: Flutter ↔ Native 양방향 통신
- **Android Native**: Kotlin으로 PyTorch Android 1.13.1 (얼굴 인식) 통합
- **iOS Native**: Swift로 3개 프레임워크 통합
- **Semaphore 기반 병렬 처리**: 8개 동시 이미지 처리로 성능 최적화
- **보안 데이터 처리**: flutter_secure_storage로 생체 정보 암호화 저장

**결과**:
- ✅ **크로스 플랫폼 앱** (Android & iOS) 배포
- ✅ **66MB AAR 파일 통합** (Android)
- ✅ **실시간 스트리밍** (EventChannel로 테스트 결과 전달)
- ✅ **Fastlane 자동화 배포** 파이프라인 구축

**기술 스택**: Flutter, Dart, MethodChannel, EventChannel, Kotlin, Swift, PyTorch Mobile

---

### 5. 성능 최적화 및 테스트 자동화

#### WorkPlus E2E 테스트 자동화
**기간**: 2025.01 - 현재

**상황**: 수동 테스트로 인한 회귀 버그 빈번 발생
**과제**: E2E 테스트 자동화로 배포 전 버그 조기 발견
**행동**:
- **Maestro E2E 테스트**: 30+ 시나리오 구축
  - 로그인/로그아웃 플로우
  - 근태 등록/수정/삭제
  - 알림 수신 및 처리
  - 오프라인 모드 동작
- **CI/CD 통합**: GitHub Actions에서 자동 실행

**결과**:
- ✅ **회귀 버그 90% 감소**
- ✅ **배포 전 자동 검증**으로 프로덕션 버그 최소화
- ✅ **테스트 실행 시간 5분** (30+ 시나리오)

**기술 스택**: Maestro, GitHub Actions, Jest

---

#### LPIN SDK 데이터 캐싱
**기간**: 2024.02 - 2024.05

**상황**: 위치 데이터 수집으로 인한 배터리 소모 및 네트워크 부하
**과제**: 캐싱 메커니즘으로 불필요한 데이터 수집 최소화
**행동**:
- **30초 캐싱 메커니즘**: 동일 위치에서 반복 요청 시 캐시 데이터 반환
- **Room Database 활용**: 로컬 DB에 위치 데이터 저장
- **MMKV 적용**: SharedPreferences 대비 10배 빠른 key-value 저장소

**결과**:
- ✅ **네트워크 요청 80% 감소**
- ✅ **배터리 소모 30% 감소**
- ✅ **데이터 수집 속도 50% 향상**

**기술 스택**: Kotlin, Room Database, MMKV

---

## Professional Experience

### LFin (엘핀)
**모바일 소프트웨어 엔지니어 / SDK 개발자** | 2024.01.24 - 현재 (1년 11개월)

**총 18개 프로젝트 수행**:
- SDK 개발: 8개 (Android SDK v1/v2, iOS SDK, React Native SDK, 4개 모듈)
- 프로덕션 앱: 10개 (WorkPlus, 서울교통공사, LIAS, 출석 앱 3개 등)

**주요 성과**:
- ✅ **1,372 commits** (WorkPlus 프로덕션 앱)
- ✅ **983 commits** (서울교통공사 프로덕션 앱)
- ✅ **283 commits** (Android SDK v2 아키텍처 재설계, develop 브랜치)
- ✅ **3개 플랫폼 SDK 에코시스템** 구축 (Android, iOS, React Native)
- ✅ **MA 인증 획득** (서울교통공사 접근성)

---

## Technical Skills

### Mobile Development
- **React Native**: 0.76.x - 0.80.x, New Architecture, Turbo Module, JSI
- **Android Native**: Kotlin, Java, Jetpack (Room, WorkManager), Compose (학습 중)
- **iOS Native**: Swift, SwiftUI (학습 중), CocoaPods, Swift Package Manager
- **Flutter**: Dart, MethodChannel, EventChannel

### State Management & Data Fetching
- **React Native**: Zustand, Redux, React Query (TanStack Query)
- **Android**: RxJava2, Kotlin Coroutines, Flow

### Languages
- **Primary**: TypeScript, Kotlin, Swift, Dart
- **Secondary**: Java, JavaScript

### Architecture & Patterns
- **Clean Architecture**: Data/Domain/Presentation 계층 분리
- **MVVM**: ViewModel, LiveData, StateFlow
- **Modular Architecture**: SDK 모듈 분리 설계
- **Reactive Programming**: RxJava, RxSwift, RxKotlin

### Tools & DevOps
- **Build Tools**: Gradle, Xcode, Fastlane
- **CI/CD**: GitHub Actions, Jenkins, CodePush
- **Testing**: Maestro (E2E), Jest (Unit), Espresso (Android)
- **Code Quality**: SonarQube, ESLint, Prettier, ProGuard
- **Version Control**: Git, GitHub Submodules, Package Registry

### Specialized Skills
- **Accessibility (A11y)**: TalkBack, VoiceOver, KWCAG 2.1, WCAG 2.1
- **Native Bridge**: iOS/Android Module 개발 (Turbo Module, Kotlin/Swift)
- **Location Services**: GPS, Wi-Fi, BLE Beacon, Cell Tower
- **Security**: SHA256, AES 암호화, Secure Storage
- **Performance**: 캐싱 전략, 메모리 최적화, 프로파일링

---

## Learning Plan & Growth Roadmap

### 단기 학습 목표 (1-3개월)

#### 1. 접근성(A11y) 전문성 강화
**동기**: RootFinders의 핵심 가치인 "모든 사용자를 위한 제품"에 기여하고 싶습니다.

**학습 계획**:
- ✅ **완료**: Android TalkBack 구현 (서울교통공사 MA 인증)
- 🔄 **진행 중**: React Native Accessibility API 학습
- 📝 **예정**:
  - WCAG 2.1 AA 등급 가이드라인 완전 숙지 (1개월)
  - VoiceOver(iOS) 고급 기능 학습 (2주)
  - 접근성 자동화 테스트 (Axe, Accessibility Scanner) 도입 (2주)
  - 기술 블로그 작성: "React Native 접근성(A11y) 완벽 가이드"

**실습 프로젝트**:
- 개인 프로젝트: 접근성 우수 사례 데모 앱 개발 (React Native)

---

#### 2. 오디오북 도메인 학습
**동기**: RootFinders의 오디오북/팟캐스트 플랫폼에 즉시 기여하고 싶습니다.

**학습 계획**:
- 📝 **예정**:
  - 오디오 스트리밍 프로토콜 학습 (HLS, DASH) - 2주
  - React Native 오디오 라이브러리 비교 (react-native-track-player, expo-av) - 1주
  - 백그라운드 오디오 재생 구현 (iOS/Android) - 2주
  - 오디오 캐싱 및 오프라인 재생 최적화 - 2주

**실습 프로젝트**:
- 개인 프로젝트: 간단한 오디오북 플레이어 앱 개발

---

#### 3. 대규모 미디어 캐싱 최적화
**동기**: 기존 데이터 캐싱 경험(LPIN SDK)을 미디어 도메인에 확장하고 싶습니다.

**학습 계획**:
- 📝 **예정**:
  - React Query의 stale-while-revalidate 전략 심화 - 1주
  - 이미지 최적화 (Lazy Loading, 썸네일 생성, WebP 변환) - 2주
  - 오디오 파일 압축 및 스트리밍 최적화 - 2주
  - SQLite를 활용한 미디어 메타데이터 캐싱 - 1주

**실습 프로젝트**:
- WorkPlus 앱에 이미지 캐싱 최적화 적용

---

### 중기 성장 목표 (3-6개월)

#### 1. React Native New Architecture 마스터
- **Fabric Renderer**: 네이티브 렌더링 최적화
- **Turbo Module**: 고성능 네이티브 모듈 개발 (이미 경험 있음, 심화 학습)
- **Codegen**: 타입 안전성 및 자동화

#### 2. 성능 프로파일링 전문성
- **React DevTools Profiler**: 렌더링 병목 분석
- **Flipper**: 네트워크, 메모리 프로파일링
- **Android Studio Profiler**: CPU, 메모리, 네트워크 분석

#### 3. 오픈소스 기여
- **react-native-accessibility** 라이브러리 기여
- **접근성 관련 블로그 및 가이드** 작성

---

### 장기 비전 (6개월 이상)

#### 1. 모바일 접근성 전문가
- **목표**: 한국 모바일 업계에서 접근성 분야 인정받는 개발자
- **계획**:
  - 접근성 컨퍼런스 발표 (예: React Native Seoul)
  - 접근성 관련 오픈소스 라이브러리 개발

#### 2. 풀스택 모바일 개발자
- **현재**: React Native, Android, iOS, Flutter 경험
- **목표**: 백엔드 API 개발 역량 추가 (Node.js, GraphQL)
- **계획**: 모바일 앱과 백엔드를 아우르는 E2E 기능 개발

#### 3. 팀 기술 리더
- **목표**: 모바일 팀 리드 역할 수행
- **계획**:
  - 코드 리뷰 문화 정착
  - 기술 문서화 및 온보딩 가이드 작성
  - 주니어 개발자 멘토링

---

## Education

### 대학 정보
(사용자로부터 추가 정보 필요)

---

## Additional Information

### 개발 철학
- **성장 지향성**: 1년 11개월간 18개 프로젝트를 통해 지속적으로 새로운 기술 습득 (React 19, RN 0.80, Turbo Module 등)
- **메타인지**: 레거시 시스템(Android SDK v1)을 모던 아키텍처(v2)로 마이그레이션하며 기술 부채 개선 경험
- **사용자 중심**: 접근성 구현을 통해 모든 사용자를 위한 제품 개발에 기여

### 언어
- **한국어**: 원어민
- **영어**: 기술 문서 읽기/쓰기 가능

### 기타
- **GitHub 활동**: 1,372 commits (WorkPlus), 983 commits (서울교통공사), 283 commits (LPIN SDK v2)
- **오픈소스 기여**: (사용자로부터 추가 정보 필요)

---

**작성일**: 2024년 12월 24일
**버전**: 20241224_01
**대상 기업**: RootFinders
**대상 직무**: React Native 개발자
