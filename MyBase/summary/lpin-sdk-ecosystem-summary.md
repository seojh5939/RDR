# LPIN SDK 에코시스템 활동 요약

## 기본 정보
- **활동 기간**: 2024년 2월 - 현재 (약 1년 10개월)
- **입사일**: 2024년 1월 24일
- **소속 기관**: LFin (엘핀)
- **역할**: SDK 개발자 / 소프트웨어 엔지니어
- **활동 유형**: SDK 개발 및 유지보수
- **참고**: MyBase의 SDK 프로젝트는 모두 입사 후 본인이 작업한 것임

## 프로젝트 개요
위치 기반 인증(Location-based Authentication)을 위한 멀티 플랫폼 SDK 에코시스템 개발. Wi-Fi, BLE 비콘, GPS, 기지국 데이터를 활용하여 사용자의 위치를 검증하는 보안 솔루션.

## 주요 활동 내용

### Android SDK 개발
**Period**: 2024년 2월 - 현재

#### Legacy SDK (v1) 유지보수
- **본인 작업 기간**: 2024년 2월 - 2024년 5월 (유지보수 및 개선)
- **특징**: 기존 통합형 모놀리식 아키텍처 유지보수
- **Git 기록**: 2024-02-02부터 2024-05-21까지 119개 커밋
- **기능**:
  - Wi-Fi, Beacon, GPS, 기지국 스캔 통합
  - 백그라운드 인증 (LazyPlacAuth)
  - 30초 데이터 캐싱
  - 자동 블루투스 활성화
- **기술**: Kotlin, Ktor HTTP 클라이언트, Gson, AltBeacon

#### Modern SDK v2 (v1.0.0)
- **본인 작업 기간**: 2024년 2월 - 현재 (주도적 개발)
- **Git 기록**: 2024-02-05부터 2025-12-16까지 283개 커밋 (develop 브랜치)
- **특징**: 모듈형 아키텍처로 전환 (본인이 설계 및 개발)
- **모듈 구성**:
  - **lpin-android-sdk-scanner**: 환경 데이터 수집
  - **lpin-android-sdk-encrypter**: 암호화/복호화
  - **lpin-android-sdk-requester**: HTTP 클라이언트 (의존성 충돌 방지)
  - **lpin-android-sdk-lzone**: 주소 해상도 변환
- **기술**: Kotlin, RxJava2, OkHttp, Google Play Services Location
- **성과**:
  - 모듈 분리로 유연성 향상
  - 클라이언트 앱 크기 최적화
  - 독립적 모듈 업데이트 가능

### iOS SDK 개발
**Period**: 2024년 4월 - 현재

- **본인 작업 기간**: 2024년 4월 - 현재
- **Git 기록**: 2024-04-08부터 현재까지 182개 커밋
- **버전**: 1.0.5 (지속적 업데이트)
- **아키텍처**: Swift Package Manager 기반, ServiceLocator 패턴 (본인이 설계)
- **핵심 기술**:
  - Swift 5.3+
  - RxSwift를 활용한 반응형 프로그래밍
  - Core Location, Core Bluetooth
- **주요 업데이트**:
  - Scanner 안정화 (1.0.1)
  - BeaconTTL 기능 추가 (1.0.3)
  - Wi-Fi 안정성 향상 (1.0.4)
  - EXC_BREAKPOINT 처리 (1.0.5)

### React Native SDK 개발
**Period**: 2025년 10월 - 현재

- **본인 작업 기간**: 2025년 10월 - 현재
- **Git 기록**: 2025-10-11부터 현재까지 107개 커밋
- **버전**: 1.0.3
- **혁신점**: React Native New Architecture (Turbo Module) 적용 (본인이 구현)
- **기술**:
  - TypeScript
  - JSI (JavaScript Interface)를 통한 네이티브 성능
  - Codegen을 통한 타입 안전성
- **특징**:
  - Android SDK v2 및 iOS SDK 래핑
  - React Hook (useGetCollectData) 제공
  - 크로스 플랫폼 통합 API

## 주요 성과 및 산출물

### 1. 멀티 플랫폼 SDK 에코시스템 구축
- **플랫폼**: Android, iOS, React Native 3개 플랫폼 지원
- **모듈**: 총 8개의 독립 모듈 개발
- **증빙**:
  - 📁 MyBase/lpin-android-sdk
  - 📁 MyBase/lpin-android-sdk-v2
  - 📁 MyBase/lpin-ios-sdk
  - 📁 MyBase/react-native-lpin-sdk

### 2. 아키텍처 진화
- **레거시**: 모놀리식 구조에서 모듈형 구조로 전환
- **성과**: 유지보수성 향상, 독립적 배포 가능
- **증빙**: 📁 MyBase/lpin-android-sdk-v2/README.md

### 3. 위치 기반 인증 기술
- **데이터 소스**: Wi-Fi AP, BLE 비콘, GPS, 기지국 정보
- **정확도**: 다중 데이터 소스 결합으로 신뢰도 향상
- **보안**: SHA256 해싱, 데이터 암호화

### 4. 프로덕션 배포
- **배포 방식**: GitHub Package Registry
- **버전 관리**: Semantic Versioning
- **문서화**: 한국어 README, 에러 코드 체계

## 습득한 기술 및 역량

### 기술 스택

#### Mobile Development
- **Android**: Kotlin, Java, Gradle
- **iOS**: Swift, Swift Package Manager, CocoaPods
- **React Native**: TypeScript, New Architecture (Turbo Module)

#### 프레임워크 및 라이브러리
- **반응형 프로그래밍**: RxJava2, RxKotlin, RxAndroid, RxSwift, RxCocoa
- **네트워킹**: OkHttp, Ktor, URLConnection
- **의존성 주입**: Koin (언급됨, 다른 프로젝트)
- **위치 서비스**: Google Play Services Location, Core Location
- **블루투스**: AltBeacon, Core Bluetooth

#### 아키텍처 패턴
- **Modular Architecture**: 관심사 분리 (암호화, 네트워킹, 스캔, 권한)
- **Singleton Pattern**: SDK 인스턴스 관리
- **ServiceLocator Pattern**: iOS SDK
- **Reactive Programming**: 비동기 작업 처리

### 소프트 스킬

#### 1. 시스템 설계
- **경험**: 레거시 시스템을 모던 아키텍처로 마이그레이션
- **성과**: 단일 SDK를 5개 독립 모듈로 분리하여 유연성 확보

#### 2. 크로스 플랫폼 개발
- **경험**: Android, iOS, React Native 3개 플랫폼에서 일관된 API 제공
- **성과**: 플랫폼별 제약사항을 문서화하고 최적화

#### 3. 기술 문서화
- **경험**: 각 SDK별 상세 README 작성 (한국어)
- **성과**: 에러 코드 체계화, 사용 예제 제공

#### 4. 버전 관리 및 배포
- **경험**: GitHub Submodules, Package Registry 활용
- **성과**: 독립적 모듈 버전 관리, 지속적 업데이트 (iOS SDK 5회, 8일 전 React Native SDK 업데이트)

## 협업 및 네트워킹
- **조직**: LFin (엘핀) 개발팀
- **협업 도구**: Git, GitHub (Submodules, Package Registry)
- **코드 리뷰**: Pull Request Template 활용 (iOS, React Native SDK)
- **라이선스**: Copyright LFin. All rights reserved.

## 기술적 혁신

### 1. 다중 데이터 소스 위치 검증
Wi-Fi AP, BLE 비콘, GPS, 기지국 정보를 결합하여 단일 소스보다 높은 정확도와 신뢰도 달성

### 2. 모듈형 SDK 아키텍처
클라이언트가 필요한 기능만 선택적으로 통합 가능한 구조 설계

### 3. React Native New Architecture 적용
Turbo Module과 JSI를 활용하여 네이티브 수준의 성능 제공

### 4. 의존성 충돌 방지
URLConnection 기반 HTTP 클라이언트 구현으로 외부 라이브러리 충돌 최소화

### 5. 백그라운드 인증
LazyPlacAuth를 통한 사용자 개입 없는 자동 인증 구현

## 원본 데이터 출처
- 📁 MyBase/lpin-android-sdk/README.md
- 📁 MyBase/lpin-android-sdk-v2/README.md
- 📁 MyBase/lpin-android-sdk-scanner/README.md
- 📁 MyBase/lpin-android-sdk-encrypter/README.md
- 📁 MyBase/lpin-android-sdk-requester/README.md
- 📁 MyBase/lpin-android-sdk-lzone/README.md
- 📁 MyBase/lpin-ios-sdk/README.md
- 📁 MyBase/lpin-ios-sdk/Package.swift
- 📁 MyBase/react-native-lpin-sdk/README.md
- 📁 MyBase/react-native-lpin-sdk/package.json

---
*생성일: 2025-12-24*
*최종 수정일: 2025-12-24*
