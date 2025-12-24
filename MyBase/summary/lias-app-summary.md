# LIAS 앱 활동 요약

## 기본 정보
- **활동 기간**: 2025년 2월 - 2025년 8월 (약 6개월)
- **입사일**: 2024년 1월 24일
- **소속 기관**: LFin (엘핀)
- **클라이언트**: NHIS (국민건강보험공단)
- **역할**: Flutter 앱 개발자
- **활동 유형**: 모바일 앱 개발 (프로덕션)
- **Git 기록**: 2025-02-19부터 2025-08-14까지 75개 커밋 (본인 작업)

## 프로젝트 개요
NHIS(국민건강보험공단)를 위한 생체 인증 및 위치 기반 인증 시스템. 얼굴 인식과 공간 인식 기술을 결합하여 사용자 인증을 제공하는 Flutter 기반 크로스 플랫폼 애플리케이션.

## 주요 활동 내용

### 1. Flutter 크로스 플랫폼 앱 개발
- **기간**: 2022년 4월 - 2025년 8월
- **플랫폼**: Android (compileSdk 33, minSdk 24) 및 iOS (deployment target 13.0+)
- **현재 버전**: 2.0.0+4
- **코드 규모**: 약 2,873 라인의 Dart 코드

### 2. 생체 인증 시스템 통합
- **얼굴 인증**:
  - 사용자 얼굴 데이터 등록, 수정, 삭제
  - 얼굴 인증 수행 (검증)
  - FRR (False Rejection Rate) 테스트
  - FAR (False Acceptance Rate) 테스트
- **기술**:
  - Android: PyTorch Android 1.13.1, C++ 네이티브 모듈 (CMake, NDK)
  - iOS: LpinFaceRecognition.framework

### 3. 위치 기반 인증 시스템
- **공간/장소 인식 기능**:
  - 위치 데이터 등록, 검증, 삭제
  - Space/Place recognition 기반 인증
- **Android SDK**:
  - lpin-android-sdk-face-authenticator (1.0.44)
  - lpin-android-sdk-nhis (1.0.57)
  - lpin-android-sdk-scanner (1.0.17)
  - lpin-android-sdk-space-authenticator (1.0.63)
  - lpin-android-sdk-space-opencv
  - lpin-android-sdk-space-pixel-matching (1.0.5)
- **iOS Frameworks**:
  - LpinNhis.framework
  - LpinSpaceRecognition.framework

### 4. 네이티브 브릿지 구현
- **MethodChannel**: Flutter와 네이티브 플랫폼 간 양방향 통신
- **EventChannel**: 실시간 테스트 결과 스트리밍
- **플랫폼별 구현**:
  - Android: Kotlin (MainActivity.kt)
  - iOS: Swift (AppDelegate.swift)

### 5. 비동기 이미지 처리 시스템
- **Semaphore 기반 동시성 제어**: 8개 병렬 작업
- **실시간 스트리밍**: EventChannel을 통한 결과 전송
- **CSV 내보내기**: 테스트 결과 데이터 저장

## 주요 성과 및 산출물

### 1. 크로스 플랫폼 생체 인증 앱 출시
- **플랫폼**: Android 및 iOS
- **배포 버전**: 2.0.0+4
- **클라이언트**: 국민건강보험공단 (NHIS)
- **증빙**:
  - 📁 MyBase/LIAS-app/README.md
  - 📁 MyBase/LIAS-app/docs/LIAS_v1.0_API정의서.pdf
  - 📁 MyBase/LIAS-app/docs/LIAS_v1.0_제품설명서.pdf
  - 📁 MyBase/LIAS-app/docs/LIAS_브로슈어.pdf

### 2. 네이티브 SDK 통합
- **Android**: 6개 AAR 파일 (총 약 66MB)
- **iOS**: 3개 프레임워크
- **성과**: Flutter 앱에서 고성능 ML 모델 및 생체 인증 기능 사용 가능

### 3. 자동화 배포 파이프라인
- **도구**: Fastlane
- **플랫폼**: Android 및 iOS 동시 지원
- **성과**: 일관된 빌드 및 배포 프로세스

### 4. 보안 데이터 처리
- **암호화 유틸리티**: flutter_secure_storage (9.2.4), encrypt (5.0.3)
- **로컬 데이터베이스**: SQLite (sqflite 2.4.2)
- **성과**: 민감한 생체 정보 안전한 저장 및 처리

## 습득한 기술 및 역량

### 기술 스택

#### Flutter 및 Dart
- **Flutter**: 3.19.0+
- **Dart SDK**: 3.0.0+
- **핵심 패키지**:
  - dio 5.4.1 (HTTP 클라이언트)
  - sqflite 2.4.2 (SQLite 데이터베이스)
  - flutter_secure_storage 9.2.4 (보안 저장소)
  - get_it 8.0.3 (의존성 주입)
  - permission_handler 12.0.0 (권한 관리)
  - csv 6.0.0 (CSV 내보내기)
  - share_plus 11.0.0 (공유 기능)

#### Android 네이티브
- **언어**: Kotlin
- **빌드 도구**: Gradle
- **SDK**: Android API 24-33
- **ML**: PyTorch Android 1.13.1
- **네이티브 빌드**: CMake, NDK 25.1.8937393

#### iOS 네이티브
- **언어**: Swift
- **의존성 관리**: CocoaPods
- **SDK**: iOS 13.0+
- **프레임워크**: Core Location, Core Bluetooth (추정)

#### 아키텍처 및 패턴
- **의존성 주입**: get_it
- **비동기 프로그래밍**: Dart async/await, Semaphore
- **플랫폼 채널**: MethodChannel, EventChannel
- **데이터베이스**: SQLite 로컬 데이터 관리
- **보안**: Secure Storage, Encryption

### 소프트 스킬

#### 1. 크로스 플랫폼 개발
- **경험**: Flutter로 Android 및 iOS 앱 동시 개발
- **성과**: 단일 코드베이스로 두 플랫폼 지원

#### 2. 네이티브 통합
- **경험**: 복잡한 네이티브 SDK를 Flutter 앱에 통합
- **성과**:
  - Android 6개 AAR 라이브러리 통합
  - iOS 3개 프레임워크 통합
  - MethodChannel 및 EventChannel을 통한 양방향 통신

#### 3. 머신러닝 SDK 통합
- **경험**: PyTorch Mobile을 Android 앱에 통합
- **성과**: 디바이스 내 얼굴 인식 기능 구현

#### 4. 동시성 및 성능 최적화
- **경험**: Semaphore를 활용한 병렬 이미지 처리 (8개 동시 작업)
- **성과**: 실시간 스트리밍으로 테스트 결과 전달

#### 5. CI/CD 및 배포
- **경험**: Fastlane을 활용한 자동화 배포
- **성과**: Android 및 iOS 일관된 릴리스 프로세스

## 협업 및 네트워킹
- **조직**: LFin (엘핀) 개발팀
- **클라이언트**: 국민건강보험공단 (NHIS)
- **협업 도구**: Git (https://github.com/l-fin/LIAS-app.git)
- **문서화**: API 정의서, 제품 설명서, 브로슈어 제작

## 기술적 도전과 해결

### 1. 대용량 네이티브 라이브러리 통합
- **도전**: Android AAR 파일 총 66MB, iOS 프레임워크 통합
- **해결**: 플랫폼별 네이티브 모듈 분리, 효율적인 빌드 설정

### 2. 실시간 이미지 처리
- **도전**: 다수의 이미지를 동시에 처리하면서 UI 블로킹 방지
- **해결**: Semaphore로 8개 병렬 작업 제어, EventChannel로 실시간 결과 스트리밍

### 3. 보안 데이터 처리
- **도전**: 생체 정보 및 위치 데이터의 안전한 저장
- **해결**: flutter_secure_storage와 encrypt 패키지를 활용한 암호화 저장

### 4. 멀티 환경 지원
- **도전**: 개발, 스테이징, 프로덕션 환경 분리
- **해결**: 환경별 설정 파일 및 빌드 flavor 구성

## 원본 데이터 출처
- 📁 MyBase/LIAS-app/README.md
- 📁 MyBase/LIAS-app/pubspec.yaml
- 📁 MyBase/LIAS-app/android/app/src/main/kotlin/io/lpin/app/lias/lias/MainActivity.kt
- 📁 MyBase/LIAS-app/ios/Runner/AppDelegate.swift
- 📁 MyBase/LIAS-app/lib/main.dart
- 📁 MyBase/LIAS-app/lib/lias.dart
- 📁 MyBase/LIAS-app/ios/LpinNhis/README.md
- 📄 MyBase/LIAS-app/docs/LIAS_v1.0_API정의서.pdf
- 📄 MyBase/LIAS-app/docs/LIAS_v1.0_제품설명서.pdf
- 📄 MyBase/LIAS-app/docs/LIAS_브로슈어.pdf

---
*생성일: 2025-12-24*
*최종 수정일: 2025-12-24*
