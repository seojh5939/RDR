# MyBase 요약 문서 디렉토리

이 디렉토리는 MyBase 폴더의 모든 프로젝트를 분석하여 생성된 요약 문서를 포함합니다.

## 생성 정보
- **생성일**: 2025년 12월 24일
- **분석 대상**: MyBase 폴더 내 18개 프로젝트
- **분석 방법**: 4개 병렬 서브 에이전트를 통한 자동 분석
- **문서 수**: 5개

## 요약 문서 목록

### 1. LPIN SDK 에코시스템 요약
📄 **파일**: `lpin-sdk-ecosystem-summary.md`

**포함 프로젝트**:
- lpin-android-sdk (레거시)
- lpin-android-sdk-v2
- lpin-android-sdk-scanner
- lpin-android-sdk-encrypter
- lpin-android-sdk-lzone
- lpin-android-sdk-requester
- lpin-ios-sdk
- react-native-lpin-sdk

**주요 내용**:
- 6년 이상의 SDK 개발 경험
- 모놀리식 → 모듈형 아키텍처 전환
- Android, iOS, React Native 3개 플랫폼 지원
- 위치 기반 인증 기술 (Wi-Fi, BLE, GPS, 기지국)

---

### 2. LIAS 앱 요약
📄 **파일**: `lias-app-summary.md`

**포함 프로젝트**:
- LIAS-app

**주요 내용**:
- Flutter 크로스 플랫폼 개발
- NHIS (국민건강보험공단) 클라이언트
- 생체 인증 (얼굴 인식) 및 위치 기반 인증
- 네이티브 SDK 통합 (Android 6개, iOS 3개)
- PyTorch Mobile ML 통합

---

### 3. 출석 관리 앱 요약
📄 **파일**: `attendance-apps-summary.md`

**포함 프로젝트**:
- ccn_attend_android (기독간호대학교)
- jnu_attend_jeju_android (제주대학교)
- jnu_attend_jeju_iOS (제주대학교)

**주요 내용**:
- BLE 비콘 기반 출석 확인 시스템
- 멀티 플랫폼 개발 (Android, iOS)
- 교육 기관 맞춤형 솔루션
- GPS 위치 추적 및 Firebase 통합

---

### 4. 프로덕션 앱 요약
📄 **파일**: `production-apps-summary.md`

**포함 프로젝트**:
- lpin-android-plac-demo-mirae (미래에셋증권)
- lpin-android-plac-demo-template
- lpin-network-util-app
- psro-android
- seoul-metro-tagless-mobile-app (서울교통공사)
- work-plus-app

**주요 내용**:
- 금융 부문: 미래에셋증권 PLAC SDK
- 공공 부문: 서울교통공사 무태그 결제 시스템
- 상용 제품: WorkPlus 근태 관리 앱
- React Native, Android 네이티브 개발
- CI/CD 및 E2E 테스트 자동화

---

### 5. 전체 기술 역량 요약
📄 **파일**: `overall-technical-summary.md`

**주요 내용**:
- **총 경력**: 2019년 6월 - 2025년 11월 (약 6년 5개월)
- **총 프로젝트**: 18개
- **플랫폼 경험**: Android, iOS, React Native, Flutter
- **도메인**: 금융, 공공, 교육, 헬스케어
- **핵심 역량**: SDK 개발, 위치 기반 서비스, 크로스 플랫폼 개발
- **기술 스택 매트릭스** 및 **프로젝트 통계**

## 활용 방법

### 이력서 작성 시
1. `overall-technical-summary.md`에서 전체 경력 개요 확인
2. 각 프로젝트별 요약에서 구체적인 기술 성과 추출
3. "습득한 기술 및 역량" 섹션을 기술 스택 리스트로 활용

### 포트폴리오 작성 시
1. 프로젝트별 요약에서 "주요 성과 및 산출물" 섹션 참조
2. "기술적 도전과 해결" 섹션을 프로젝트 스토리로 활용
3. "원본 데이터 출처"를 통해 증빙 자료 확인

### 면접 준비 시
1. 도메인별 프로젝트 경험 정리 (금융, 공공, 교육 등)
2. 기술별 깊이 있는 경험 사례 확인
3. 프로젝트 타임라인으로 경력 흐름 파악

## 프로젝트 분류 체계

### 플랫폼별
- **Android Native**: 12개 프로젝트
- **iOS Native**: 3개 프로젝트
- **React Native**: 3개 프로젝트
- **Flutter**: 1개 프로젝트

### 유형별
- **SDK 개발**: 8개 프로젝트
- **프로덕션 앱**: 10개 프로젝트

### 도메인별
- **금융 (FinTech)**: 미래에셋증권 PLAC SDK
- **공공 (GovTech)**: 서울교통공사 무태그 앱
- **교육 (EduTech)**: 출석 관리 앱 3종
- **헬스케어**: LIAS 앱 (NHIS)
- **HR Tech**: WorkPlus 앱

## 핵심 기술 키워드

### 모바일 개발
`Android` `iOS` `React Native` `Flutter` `Kotlin` `Swift` `TypeScript` `Dart`

### 아키텍처
`Clean Architecture` `MVVM` `Modular Architecture` `SDK Development` `Dependency Injection`

### 위치 기반 서비스
`BLE Beacon` `iBeacon` `GPS` `Wi-Fi Scanning` `Cell Tower` `Location Authentication`

### 기타 핵심 기술
`RxJava` `RxSwift` `Coroutines` `PyTorch Mobile` `Firebase` `Fastlane` `CI/CD` `E2E Testing`

## 데이터 정확성

모든 요약 문서는 다음 원칙에 따라 작성되었습니다:
- ✅ **사실 기반**: 실제 파일 내용만 사용
- ✅ **추측 배제**: 불확실한 정보는 제외하거나 명시
- ✅ **증빙 가능**: 모든 정보에 대한 출처 파일 경로 제공
- ✅ **날짜 정확성**: Git 커밋 로그 및 빌드 파일 기준

## 업데이트 이력

| 날짜 | 변경 내용 |
|------|----------|
| 2025-12-24 | 초기 생성 - 18개 프로젝트 분석 완료 |

## 추가 분석이 필요한 경우

새로운 프로젝트가 MyBase에 추가되었거나 기존 프로젝트가 업데이트된 경우, `/rdr:mybase-init` 명령어를 다시 실행하여 요약 문서를 갱신할 수 있습니다.

---
*생성일: 2025-12-24*
*마지막 분석: 2025-12-24*
