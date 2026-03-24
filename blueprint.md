# PulseBoard - Website Monitoring Suite

## Overview
PulseBoard는 웹사이트, API, 결제 플로우, 웹훅 엔드포인트의 가동 상태와 성능을 실시간으로 추적하는 현대적인 모니터링 대시보드입니다. 단일 페이지 애플리케이션(SPA) 스타일로 설계되어 사용자에게 직관적인 운영 현황을 제공합니다.

## Design & Features

### Style & Design (Aesthetics)
- **Visual Theme:** 깊이감 있는 어두운 계열(`--bg: #0b1020`) 배경에 네온 빛의 강조색(Primary Blue, Purple)을 사용한 프리미엄 다크 모드 디자인.
- **Layout:** 좌측 고정 사이드바와 우측 스크롤 가능한 메인 레이아웃의 2컬럼 구조. 반응형 그리드를 통해 태블릿 및 모바일 환경에 최적화.
- **Interactive UI:**
    - **Glassmorphism:** `backdrop-filter: blur(14px)`를 활용한 반투명 사이드바 및 카드 요소.
    - **Animations:** 실시간 가동을 상징하는 펄스(Pulse) 애니메이션 및 부드러운 호버 효과.
    - **Typography:** Inter 폰트를 기반으로 한 명확한 정보 계층 구조.
    - **Depth:** 다층 드롭 섀도우와 미세한 그라데이션 라인을 통해 요소 간의 입체감 부여.

### Key Features
1. **Core Metrics Summary:**
    - 전체 모니터 수, 평균 가동률(SLA), 평균 응답속도, 현재 장애 건수 실시간 집계.
    - 전일 대비 증감율(Delta) 표시.
2. **SLA & Health Overview:**
    - SVG 기반의 원형 가동률 링(SLA Ring).
    - 서비스군(Web, API, Payment, Webhook)별 상태 바.
3. **Response Trend Visualization:**
    - 최근 24시간 응답 속도 추이를 보여주는 커스텀 SVG 차트.
    - 주의(450ms+) 및 장애(900ms+) 구간 배경 강조.
4. **Alert & Event Management:**
    - 최근 발생한 긴급/주의/정보 알림 리스트.
    - 상태 변경 이력을 보여주는 타임라인.
    - 현재 상태 기반의 운영 권장 액션 가이드.
5. **Advanced Monitor Table:**
    - 상태(정상/주의/장애) 필터링 기능.
    - 검색 기능을 통한 빠른 서비스 탐색.
    - 각 서비스별 12단계 미니 추세 차트(Tiny Chart) 포함.
    - SSL 인증서 만료일 상태 표시.
6. **Live Simulation:**
    - '새로고침' 버튼 클릭 시 난수를 기반으로 응답 속도 및 가동률이 실시간으로 변하는 시뮬레이션 로직 포함.

## Current State & History

### v1.1 - PulseBoard 통합 구현 (현재)
- **변경 사항:** 기존의 분산된 파일 구조에서 단일 파일 내 고성능 CSS/JS를 포함한 통합 대시보드로 교체.
- **핵심 추가 사항:**
    - 모니터링 필터링 시스템 구현.
    - SVG 데이터 시각화(응답 속도 차트, 미니 차트) 추가.
    - 실시간 데이터 갱신 시뮬레이션 엔진 탑재.
- **상태:** 구현 완료 및 배포 준비.

## Implementation Steps
- [x] `index.html` 교체 및 통합 디자인 적용
- [x] 실시간 시뮬레이션 JS 로직 검증
- [x] 반응형 레이아웃 최적화
- [ ] Firebase를 통한 최종 배포
