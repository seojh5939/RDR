# 출석 관리 앱 활동 요약

## 기본 정보
- **활동 기간**: 2024년 3월 - 2024년 9월 (약 6개월)
- **입사일**: 2024년 1월 24일
- **소속 기관**: LFin (엘핀)
- **역할**: 모바일 앱 개발자 (Android & iOS)
- **활동 유형**: 교육 기관용 모바일 앱 개발
- **Git 기록**:
  - JNU Android: 2024-03-07 ~ 2024-03-12 (7개 커밋)
  - JNU iOS: 2024-03-12 ~ 2024-03-13 (8개 커밋)
  - CCN Android: 2024-09-03 (4개 커밋)

## 프로젝트 개요
교육 기관(대학교)을 위한 BLE 비콘 기반 출석 관리 시스템. 블루투스 저에너지(BLE) 비콘의 근접성 감지와 GPS 위치 추적을 결합하여 학생 출석을 자동으로 확인하는 하이브리드 모바일 애플리케이션.

## 클라이언트 및 프로젝트

### 1. 제주대학교 스마트출결 시스템
- **클라이언트**: 제주대학교 (Jeju National University)
- **플랫폼**: Android + iOS
- **기간**: 2022년 11월 - 2024년 3월
- **버전**:
  - Android: 1.1.2 (versionCode 12)
  - iOS: 1.1.3 (build 2)

### 2. 기독간호대학교 출석 시스템
- **클라이언트**: 기독간호대학교 (Christian College of Nursing)
- **플랫폼**: Android
- **기간**: 2023년 5월 - 2024년 9월
- **버전**: 5.0.2 (versionCode 6)

## 주요 활동 내용

### Android 앱 개발

#### 공통 기능 구현
1. **WebView 하이브리드 아키텍처**:
   - JavaScript Interface를 통한 웹-네이티브 통신
   - 파일 업로드/다운로드 지원
   - Cookie 관리 및 세션 유지

2. **BLE 비콘 출석 확인**:
   - BLE 비콘 스캐닝 (주변 비콘 감지)
   - BLE 비콘 광고 (디바이스를 비콘으로 전환)
   - RSSI (신호 강도) 기반 거리 계산

3. **GPS 위치 추적**:
   - 이중 프로바이더 (GPS + Network)
   - 위치 권한 관리
   - 위치 기반 출석 검증

4. **Firebase 통합**:
   - Firebase Cloud Messaging (FCM) 푸시 알림
   - Firebase Analytics 사용자 분석
   - Firebase Core

5. **멀티 환경 지원**:
   - 개발(Development) 환경
   - 프로덕션(Production) 환경
   - 환경 전환 설정 대화상자

#### 기독간호대학교 앱 특화 기능
- **Conscrypt 보안 제공자** (2024년 9월 추가):
  - Android 14 호환성
  - CA 인증서 수동 구현
- **compileSdk**: 34, **minSdk**: 26, **targetSdk**: 34

#### 제주대학교 Android 앱 특화 기능
- **앱 아이콘 및 이름 수정** (2024년 3월)
- **compileSdk**: 34, **minSdk**: 26, **targetSdk**: 34

### iOS 앱 개발 (제주대학교)

#### 핵심 기능
1. **WKWebView 기반 하이브리드 앱**:
   - JavaScript 브릿지
   - Cookie 관리 및 지속성
   - 버전 체크 및 자동 업데이트 안내

2. **BLE 비콘 통신**:
   - Core Bluetooth 활용
   - CBCentralManager (비콘 스캐닝)
   - CBPeripheralManager (비콘 광고)
   - RSSI 기반 거리 계산

3. **위치 서비스**:
   - Core Location (CLLocationManager)
   - GPS 위치 추적
   - 위치 권한 관리

4. **멀티 환경 URL 전환**:
   - Production: https://attend.jejunu.ac.kr/
   - Develop: https://at-jnu-dev.lfin.kr/
   - Local: http://at-jnu-local.lfin.kr:8080/

5. **특수 기능**:
   - 볼륨 버튼 감지 (개발자 모드 진입)
   - 마이크 권한 (2024년 3월 추가)

## 주요 성과 및 산출물

### 1. 멀티 플랫폼 출석 관리 솔루션
- **플랫폼**: Android (2개) + iOS (1개) = 총 3개 앱
- **클라이언트**: 2개 교육 기관
- **증빙**:
  - 📁 MyBase/ccn_attend_android
  - 📁 MyBase/jnu_attend_jeju_android
  - 📁 MyBase/jnu_attend_jeju_iOS

### 2. BLE 비콘 기반 근접성 출석 확인
- **기술**: Bluetooth Low Energy (BLE) iBeacon 프로토콜
- **정확도**: RSSI 신호 강도로 거리 측정
- **성과**: 학생이 강의실에 실제로 있는지 자동 확인

### 3. Android 14 호환성 업데이트
- **날짜**: 2024년 9월 (기독간호대학교)
- **내용**: Conscrypt 보안 제공자 통합
- **성과**: 최신 Android 버전 지원

### 4. 코드 재사용 가능한 아키텍처
- **공통성**: 두 Android 앱이 유사한 구조 공유
- **유틸리티 클래스**: Application.java, MainActivity.java, Beacon.java
- **성과**: 빠른 커스터마이징 및 배포

## 습득한 기술 및 역량

### 기술 스택

#### Android 네이티브
- **언어**: Java
- **빌드 도구**: Gradle 8.0.2
- **SDK**: Android API 26-34
- **핵심 기술**:
  - WebView with JavaScript Interface
  - Bluetooth Low Energy (BLE)
  - Location Services (GPS + Network)
  - Firebase (Analytics, Messaging, Core)
  - AndroidX WorkManager
  - Conscrypt Security Provider

#### iOS 네이티브
- **언어**: Swift
- **의존성 관리**: CocoaPods
- **SDK**: iOS 13.0+
- **핵심 기술**:
  - WKWebView
  - Core Location (CLLocationManager)
  - Core Bluetooth (CBCentralManager, CBPeripheralManager)
  - Firebase (Core, Messaging, Analytics)
  - Alamofire 4.9.1

#### 공통 기술
- **아키텍처**: 하이브리드 WebView 기반
- **통신**: JavaScript Bridge (WebView ↔ Native)
- **권한 관리**: TedPermission (Android), Core Permission APIs (iOS)
- **푸시 알림**: Firebase Cloud Messaging
- **분석**: Firebase Analytics

### 소프트 스킬

#### 1. 멀티 플랫폼 개발
- **경험**: 동일한 기능을 Android와 iOS에서 구현
- **성과**: 제주대학교 앱은 Android 및 iOS 모두 지원

#### 2. BLE 프로토콜 구현
- **경험**: iBeacon 프로토콜 스캔 및 광고 구현
- **성과**: RSSI 기반 근접성 감지로 출석 확인 자동화

#### 3. 하이브리드 앱 개발
- **경험**: WebView를 통한 웹 콘텐츠 표시, 네이티브 기능은 플랫폼별 구현
- **성과**: 빠른 UI 업데이트 (웹) + 고성능 네이티브 기능

#### 4. 클라이언트 맞춤화
- **경험**: 2개 기관의 브랜딩 (앱 이름, 아이콘, 패키지 ID)
- **성과**: 재사용 가능한 코드베이스에서 빠른 커스터마이징

#### 5. 보안 및 호환성 업데이트
- **경험**: Android 14 보안 요구사항 대응 (Conscrypt)
- **성과**: 최신 OS 버전 지원 유지

## 협업 및 네트워킹
- **개발자**: EoApps 팀 (패키지명 및 저작권 표시 기반)
- **조직**: LFin (엘핀)
- **클라이언트**: 제주대학교, 기독간호대학교
- **협업 도구**: Git, Android Studio, Xcode

## 기술적 구현 세부사항

### BLE 비콘 구현
- **스캐닝**: 주변 비콘 UUID, Major, Minor, RSSI 수집
- **광고**: 디바이스를 비콘으로 전환하여 출석 확인
- **거리 계산**: RSSI 값으로 근접성 판단

### GPS 위치 추적
- **이중 프로바이더**: GPS_PROVIDER와 NETWORK_PROVIDER 동시 사용
- **위치 권한**: 런타임 권한 요청 (Android 6.0+)
- **정확도**: 위치 기반으로 캠퍼스 내 출석 확인

### Firebase 푸시 알림
- **FCM 토큰**: 디바이스별 고유 토큰 생성
- **알림 수신**: 출석 확인, 공지사항 등 실시간 알림
- **분석**: 사용자 행동 및 앱 사용 통계

### 멀티 환경 지원
- **환경 전환**: 개발 서버와 프로덕션 서버 간 전환
- **iOS**: Constance.swift 파일로 환경별 URL 관리
- **Android**: 빌드 flavor 또는 설정 대화상자

## 개발 타임라인

| 날짜 | 프로젝트 | 이벤트 |
|------|---------|--------|
| 2022-11-07 | 제주대학교 (Android) | 프로젝트 시작 |
| 2022-11-07 | 제주대학교 (iOS) | 프로젝트 시작 |
| 2023-05-30 | 기독간호대학교 (Android) | 프로젝트 시작 |
| 2024-03-12 | 제주대학교 (Android) | 앱 아이콘 및 이름 수정 (최종 업데이트) |
| 2024-03-13 | 제주대학교 (iOS) | 마이크 권한 추가 (최종 업데이트) |
| 2024-09-03 | 기독간호대학교 (Android) | Conscrypt 보안 제공자 추가 (최종 업데이트) |

## 원본 데이터 출처
- 📁 MyBase/ccn_attend_android/build.gradle
- 📁 MyBase/ccn_attend_android/app/build.gradle
- 📁 MyBase/ccn_attend_android/app/src/main/java/kr/ac/ccn/attend/
- 📁 MyBase/jnu_attend_jeju_android/build.gradle
- 📁 MyBase/jnu_attend_jeju_android/app/build.gradle
- 📁 MyBase/jnu_attend_jeju_android/app/src/main/java/com/eoapps/jejunu/
- 📁 MyBase/jnu_attend_jeju_iOS/Podfile
- 📁 MyBase/jnu_attend_jeju_iOS/abydos/AppDelegate.swift
- 📁 MyBase/jnu_attend_jeju_iOS/abydos/ViewController.swift
- 📁 MyBase/jnu_attend_jeju_iOS/abydos/Constance/Constance.swift

---
*생성일: 2025-12-24*
*최종 수정일: 2025-12-24*
