# MapMarker

**여행 동선을 지도 위에 보기 좋게 그리는 앱**

장소 포인트, 구간별 이동 수단, 사진을 한 번에 담은 여행 동선 페이지와 이미지를 만들고 공유합니다. 여행 전에는 계획을 세우고, 여행 중에는 현재 위치와 다음 장소를 확인하고, 여행 후에는 사진과 함께 회고합니다.

## 핵심 기능

| | 기능 | 상태 |
|---|---|---|
| 🗺️ | **동선 그리기**: 지도에 장소를 찍고, 직선이나 곡선으로 잇고, 구간마다 이동 수단을 표시 | ✅ 앱에서 동작 (서버 저장은 예정) |
| 🖼️ | **동선 이미지 내보내기**: 동선, 이동 수단, 사진이 담긴 한 장짜리 이미지 | 📅 예정 (기술 검증 완료) |
| 🔗 | **공유와 복사**: 친구가 공유한 여행을 보고, 내 여행으로 복사해서 수정 | 📅 예정 |
| 🤖 | **AI 동선 생성**: 여행지, 계절, 일정을 입력하면 AI가 동선 초안을 생성 | 📅 예정 |

지금은 1단계(MVP)를 진행하고 있습니다. 앱의 지도·동선 편집을 마쳤고, 다음은 서버 연동과 로그인입니다. 단계별 진행 상황은 [PLAN](https://github.com/mapmarker-dev/.github/blob/main/docs/PLAN.md)에 있습니다.

## 저장소

| 저장소 | 내용 | 기술 |
|---|---|---|
| [mapmarker-app](https://github.com/mapmarker-dev/mapmarker-app) | 모바일 앱 | Flutter |
| [mapmarker-server](https://github.com/mapmarker-dev/mapmarker-server) | API 서버 | NestJS, Prisma, PostgreSQL |
| [mapmarker-web](https://github.com/mapmarker-dev/mapmarker-web) | 정적 웹 페이지 | S3 + CloudFront |

## 인프라

AWS 단일 서버(EC2, RDS, S3, CloudFront)로 시작합니다. 이후 부하 테스트로 병목을 확인하고 ALB와 Auto Scaling으로 확장합니다. 단계마다 `문제 → 측정 → 설계 → 적용 → 검증`을 기록합니다.

## 문서

- [큰 그림 (OVERVIEW)](https://github.com/mapmarker-dev/.github/blob/main/docs/OVERVIEW.md)
- [단계별 계획 (PLAN)](https://github.com/mapmarker-dev/.github/blob/main/docs/PLAN.md)
