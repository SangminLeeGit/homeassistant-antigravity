# Home Assistant 대시보드 구성 리포트

**인스턴스**: `https://ha.nexusroid.org` | **버전**: 2026.2.3
**조회 시각**: 2026-03-03 11:23 KST | **총 대시보드**: 7개

> [!NOTE]
> 모든 대시보드는 Sections 레이아웃 사용 (HA 2024+ 신규 방식). Mushroom 커스텀 카드 적극 활용중.

---

## 대시보드 목록

| # | 이름 | URL Path | 아이콘 | 사이드바 | 관리자전용 | Views |
|---|------|----------|--------|----------|-----------|-------|
| 1 | Surveillance | `/dashboard-surveillance` | `mdi:camera` | ✅ | ✅ | 1 |
| 2 | _Home | `/dashboard-home` | — | ✅ | ❌ | 1 |
| 3 | YT | `/dashboard-yt` | `mdi:youtube` | ✅ | ❌ | 1 |
| 4 | IOT | `/dashboard-iot` | `mdi:bicycle-penny-farthing` | ✅ | ❌ | 1 |
| 5 | Printer | `/dashboard-printer` | `mdi:printer-3d` | ✅ | ❌ | 1 |
| 6 | Overview (Home & Car) | `/lovelace` | `mdi:view-dashboard` | ✅ | ❌ | 1 |
| 7 | **New (Nexusroid Home)** | `/dashboard-new` | — | ✅ | ❌ | **5** |

---

## 1. Surveillance (`dashboard-surveillance`)

**View**: Home | **Sections**: 1 | **카드**: 5

카메라 4대의 실시간 피드 표시 (Sections grid, 2-column span):

| 카드 | 타입 | 엔티티 |
|------|------|--------|
| 제목 | heading | "Surveillance" `mdi:camera-wireless` |
| Camera1 | picture-entity | `camera.camera1_camera1` |
| Camera2 | picture-entity | `camera.camera2_camera2` |
| Camera3 | picture-entity | `camera.camera3_camera3` |
| Camera4 | picture-entity | `camera.camera4_camera4` |

---

## 2. _Home (`dashboard-home`)

**View**: Home | **Sections**: 3 | **테마**: Metrology Fluent

### Section 1: Remote
| 카드 | 타입 | 엔티티 | 비고 |
|------|------|--------|------|
| LG TV | tile | `media_player.lg_webos_smart_tv` | |
| Last Opened | tile | `input_datetime.last_opened` | |
| E-GPU 전력 | gauge | `sensor.0xa4c1387338128c51_power` | 20-300W, 색상단계 |
| E-GPU 스위치 | tile | `switch.0xa4c1387338128c51` | |
| 12V Fan | tile | `switch.mosquito_plug` | |
| 선풍기 (Mi Fan 2) | mushroom-fan-card | `fan.dmaker_sg_811156575_p18_s_2_fan` | % + 회전 |
| 선풍기 속도 | mushroom-number-card | `number.dmaker_sg_811156575_p18_speed_level_p_2_10` | |
| 선풍기 (Lite) | mushroom-fan-card | `fan.dmaker_sg_455409575_1c_s_2_fan` | |

### Section 2: Room
| 카드 | 타입 | 엔티티 | 비고 |
|------|------|--------|------|
| 현관문 | tile | `binary_sensor.door_sensor_2_contact` | |
| 거실 창문 | tile | `binary_sensor.door_sensor_1_contact` | |
| 방 온도 | tile | `sensor.room_thermometer_temperature` | |
| 방 습도 | tile | `sensor.room_thermometer_humidity` | |
| 조명 스위치 | tile | `switch.remote_light_off` | |
| Ambient 2 | tile | `light.light_ambient2` | |
| Ambient 1 | tile | `light.light_ambient` | |
| 천장등 (Sonoff) | tile | `switch.sonoff_10022a9328` | |
| 베란다 팬 | tile | `switch.0xa4c138f4684ce498` | |
| Mosquitto | tile | `switch.chuangmi_cn_55300243_m1_on_p_2_1` | |
| PC WOL | tile | `button.wake_on_lan_e8_80_88_dc_7d_8a` | |

### Section 3: Remote_Power
| 카드 | 타입 | 엔티티 | 비고 |
|------|------|--------|------|
| 선풍기 Pro | mushroom-fan-card | `fan.dmaker_sg_811298141_p33_s_2_fan` | |
| 공기청정기 팬 | mushroom-number-card | `number.zhimi_cn_67287497_v6_favorite_fan_level_p_8_1` | |
| 3D 프린터 | tile | `switch.3d_printer` | |
| PM2.5 | tile | `sensor.zhimi_cn_67287497_v6_pm2_5_density_p_3_2` | |
| WAN 상태 | tile | `binary_sensor.efm_networks_iptime_ax1500sr_wan_status` | |
| 다운로드 속도 | tile | `sensor.efm_networks_iptime_ax1500sr_download_speed` | |
| 업로드 속도 | tile | `sensor.efm_networks_iptime_ax1500sr_upload_speed` | |
| 외부 IP | tile | `sensor.efm_networks_iptime_ax1500sr_external_ip` | |
| 공유기 트래커 | tile | `device_tracker.efm_networks_08_23_cc` | |

---

## 3. YT (`dashboard-yt`)

**View**: Home | **Sections**: 2

| Section | 카드 | 비고 |
|---------|------|------|
| Phasely | `sensor.phasely_subscribers` 구독자 수 그래프 (line) | Metro Orange 테마 |
| GitHub | `sensor.yt_dlp_yt_dlp_latest_release` 최신 릴리즈 | |

---

## 4. IOT (`dashboard-iot`)

**View**: Home | **Sections**: 2

| Section | 카드 | 비고 |
|---------|------|------|
| 공기청정기 | 온도 센서 그래프 + 팬 레벨 조절 | mushroom-number-card |
| 로봇청소기 | Roborock V1 + S5 vacuum-card | 2대 모두 표시 |

---

## 5. Printer (`dashboard-printer`)

**View**: Home | **Sections**: 2

### Section 1: 프린터 대시보드
| 카드 | 타입 | 비고 |
|------|------|------|
| 진행률 | gauge | Metro Green 테마 |
| 긴급 정지 | tile (button) | |
| 일시정지 | tile (button) | |
| 예상 완료 | tile (sensor) | |
| 취소 | tile (button) | |
| 베드 온도 | sensor (line graph) | 0-60°C, Fluent Blue |
| 익스트루더 온도 | sensor (line graph) | 0-200°C, Fluent Green |
| 모기향 플러그 | button | |
| 펌웨어 재시작 | button | Fluent Purple |

### Section 2: ender3v3se 제어
- Cancel/Emergency Stop/Firmware Restart/Pause/Resume 버튼
- Speed Factor 조절
- **Incam 라이브뷰** (picture-entity)

---

## 6. Overview (`/lovelace`)

**Title**: Home & Car | **테마**: Mushroom Square Shadow
- 빈 대시보드 (카드 없음)

---

## 7. New — Nexusroid Home (`dashboard-new`) ⭐ 메인 대시보드

**5개 View**: 홈, 보안, 서버, 제어, 에너지

### View 1: 홈 (`/home`)

**Mushroom 칩 바** (상단):
- 날씨 (`weather.forecast_home`)
- 사용자 (`person.nexusroid`)
- 현관문 상태 (색상 조건부)
- 거실 창문 상태 (색상 조건부)
- 태양 (`sun.sun`)
- 외부 IP (`sensor.efm_networks_iptime_ax1500sr_external_ip`)

**Quick Toggle 칩 바**:
- 천장등 / 무드등 / TV / E-GPU / PC WOL

**Quick Control 행**:
- 공기청정기 / 선풍기 / 로봇청소기

**자동화 상태 카드** (mushroom-template-card)

**환경 센서**:
- 방 온도/습도 (mushroom-entity-card, vertical)
- PM2.5 / 공기청정기 온도

**환경 그래프**:
- 온도 그래프 (mini-graph-card, 24시간)
- 습도 그래프 (mini-graph-card, 24시간)

**도어 센서**:
- 현관문 / 거실 창문 (조건부 색상)

### View 2~5: 보안/서버/제어/에너지
- Sections 레이아웃 사용
- 구체적 카드는 아직 미구성 (빈 views)

---

## 사용중인 커스텀 카드

| 카드 | 버전 | 용도 |
|------|------|------|
| Mushroom Cards | v5.1.1 | 엔티티/팬/넘버/템플릿/칩 카드 |
| Mushroom Dashboard Strategy | v2.5.0 | 대시보드 전략 |
| Mushroom Themes | v0.0.11 | 테마 |
| Bubble Card | v3.1.2 | — |
| auto-entities | v1.16.1 | 자동 엔티티 목록 |
| mini-graph-card | v0.13.0 | 인라인 그래프 |
| Vacuum Card | v2.12.0 | 로봇청소기 |
| button-card | v7.0.1 | 커스텀 버튼 |
| Slider Button Card | v1.13.0 | 슬라이더 |
| Horizon Card | v1.4.0 | 일출/일몰 |
| JB Battery Card | v1.0.2 | 배터리 |
| Vertical Stack In Card | v1.0.1 | 레이아웃 |
| Local Tuya | v5.2.5 | Tuya 로컬 |
| Sonoff LAN | v3.9.3 | Sonoff 로컬 |
| Xiaomi Home | v0.4.7 | Xiaomi 통합 |
| UI Lovelace Minimalist | v1.5.2 | 미니멀 UI |
| Metrology Themes | v1.9.1 | Metro/Fluent 테마 |
