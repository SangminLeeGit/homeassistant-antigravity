# Home Assistant 기기 및 자동화 현황 리포트

**인스턴스**: `https://ha.nexusroid.org` | **버전**: 2026.2.3 | **위치**: 집 (서울) | **상태**: RUNNING
**조회 시각**: 2026-03-03 11:18 KST | **총 엔티티**: 776개

---

## 자동화 (Automations) — 26개

| # | 이름 | 상태 | 마지막 실행 | 설명 |
|---|------|------|-------------|------|
| 1 | 5-Min Ventilation | ✅ on | 2026-01-02 | 5분 환기 |
| 2 | Airfryer_Ventilation | ✅ on | 2026-03-02 | 에어프라이어 사용 시 환기 |
| 3 | Ambient Light | ✅ on | 2026-03-02 | 엠비언트 조명 제어 |
| 4 | Auto printer off | ✅ on | 2025-07-07 | 프린터 자동 종료 |
| 5 | Auto Ventilation | ❌ off | 2025-10-08 | 자동 환기 (비활성) |
| 6 | 베란다 팬 켜졌는지 체크 | ✅ on | 2026-03-01 | 베란다 팬 상태 확인 |
| 7 | 에어프라이어off알림 | ✅ on | 2026-03-03 | 에어프라이어 꺼짐 알림 |
| 8 | eGPU 절전 | ✅ on | 2026-02-18 | eGPU 절전 모드 |
| 9 | Going Out | ✅ on | 2026-02-13 | 외출 모드 |
| 10 | 환풍기 소켓 전원 리셋 | ✅ on | (미실행) | 환풍기 소켓 리셋 |
| 11 | Light_button | ✅ on | 2026-02-02 | 조명 버튼 |
| 12 | Light Out | ✅ on | 2025-09-30 | 조명 끄기 |
| 13 | Light toggle button | ✅ on | 2026-03-02 | 조명 토글 버튼 |
| 14 | Lights Mod | ✅ on | 2026-01-02 | 조명 모드 변경 |
| 15 | Lights Mod2 | ✅ on | 2026-01-02 | 조명 모드 변경 2 |
| 16 | Livingroom Off | ✅ on | 2026-02-02 | 거실 전체 끄기 |
| 17 | 모기향_OFF | ❌ off | 2025-10-09 | 모기향 끄기 (비활성/계절) |
| 18 | 모기향_ON | ❌ off | 2025-12-13 | 모기향 켜기 (비활성/계절) |
| 19 | Morning | ✅ on | 2026-03-02 | 아침 루틴 |
| 20 | [PowerON] WOL with E-GPU | ✅ on | 2026-02-18 | WOL + eGPU 전원 |
| 21 | Printer Go(automation) | ✅ on | 2026-01-02 | 프린터 가동 |
| 22 | Printer OFF (automation) | ✅ on | 2025-06-29 | 프린터 종료 |
| 23 | Room vent toggle | ✅ on | 2025-09-28 | 방 환기 토글 |
| 24 | Last opened time | ✅ on | 2026-03-03 | 마지막 열림 시간 기록 |
| 25 | Veranda control | ✅ on | 2026-03-02 | 베란다 제어 |
| 26 | WOL 하면 eGPU도 같이 | ✅ on | 2026-02-18 | WOL 시 eGPU 동시 기동 |

> [!NOTE]
> **활성 23개** / **비활성 3개** (Auto Ventilation, 모기향_ON, 모기향_OFF)

---

## 주요 기기 현황

### 💡 조명 (Lights) — 10개

| 이름 | 상태 |
|------|------|
| Mosquitto Defuser Indicator Light | ✅ on |
| Mi Plug Mini Indicator Light | ⚠️ unavailable |
| Xiaomi Standing Fan 2 Pro Indicator Light | ✅ on |
| Light_ambient | ⬛ off |
| Light_Ambient2 | ⬛ off |
| Room Light | ⚠️ unavailable |
| Room Light2 | ⚠️ unavailable |
| Mi LED Desk Lamp | ⚠️ unavailable |
| Air purifier Indicator Light | ✅ on |
| Zigbee Light | ⚠️ unavailable |

---

### 🔌 스위치 (Switches) — 33개 (주요 항목)

| 이름 | 상태 | 비고 |
|------|------|------|
| E-GPU | ✅ on | eGPU 전원 |
| Veranda Fan Control | ⬛ off | 베란다 환풍기 |
| 3D_Printer | ⬛ off | 3D 프린터 전원 |
| Mosquitto Defuser | ⬛ off | 모기 훈증기 |
| Mi Plug Mini | ⚠️ unavailable | — |
| Mi Smart Standing Fan 2 Lite | ⚠️ unavailable | — |
| Mi Smart Standing Fan 2 알림 | ⬛ off | — |
| Xiaomi Standing Fan 2 Pro 알림 | ✅ on | — |
| Overhead Light (Sonoff) | ⬛ off | 천장등 |
| Printer (IKEA Outlet) | ⚠️ unavailable | — |
| Lenovo (WOL) | ⬛ off | PC 전원 |
| Livingroom_AirFryer | ✅ on | 에어프라이어 소켓 |
| NVR Surveillance Home Mode | ⬛ off | NVR 홈 모드 |
| Zigbee2MQTT Permit Join | ⬛ off | 페어링 모드 |
| Air Purifier Alarm | ✅ on | 공기청정기 알림 |

---

### 🌀 선풍기/팬 (Fans) — 4개

| 이름 | 상태 |
|------|------|
| Mi Smart Standing Fan 2 | ⬛ off |
| Xiaomi Smart Standing Fan 2 Pro | ⬛ off |
| Mi Smart Standing Fan 2 Lite | ⚠️ unavailable |
| Air Purifier (공기청정기) | ✅ on |

---

### 📷 카메라 (Cameras) — 7개

| 이름 | 상태 |
|------|------|
| Camera1 ~ Camera4 | 🔴 recording (4대 녹화중) |
| ender3v3se Incam | idle |
| ender3v3se Thumbnail | idle |
| ender3v3se webcam | ⚠️ unavailable |

---

### 📺 미디어 플레이어 — 5개

| 이름 | 상태 |
|------|------|
| Google Home | ⬛ off |
| LG webOS Smart TV | ⚠️ unavailable |
| Mi TV | ⚠️ unavailable |
| Room Group | ⬛ off |

---

### 🤖 로봇청소기 — 2개

| 이름 | 상태 |
|------|------|
| 로봇청소기2 (Roborock S5) | ⚠️ unavailable |
| Robot vacuum (Roborock V1) | ⚠️ unavailable |

---

### 📍 기기 추적 — 7개

| 이름 | 상태 | IP/MAC |
|------|------|--------|
| EFM Networks (ipTIME) | 🏠 home | 192.168.1.1 |
| Espressif (ESP모듈) | 🏠 home | 192.168.1.12 |
| Lenovo PC | 🏠 home | 192.168.1.212 |
| Samsung Galaxy (S906N) | 📡 not_home | — |
| SM-S906N, SM-S906N_kak | ❓ unknown | — |

---

### 🎬 장면 (Scenes) — 16개

| 그룹 | 장면 |
|------|------|
| 에어컨 | Carrier 22℃ 냉방, 23℃ 냉방, 전원끄기 |
| 위니아(난방) | 24℃, 25℃, 26℃, 27℃, 끄기, 환기끄기 |
| TV | TV 켜기 (2개), 볼륨 UP/DOWN |
| 모니터 | Switch Monitor 1~3 |

---

### 🌡 주요 센서 (발췌)

| 카테고리 | 주요 값 |
|----------|---------|
| 방 온도 | **22.2°C** |
| 공기청정기 습도 | **50%** |
| E-GPU 전력 | **38W** |
| 에어프라이어 전력 | **0W** (대기) |
| SpeedTest 핑 | **33ms** |
| 외부 IP | **218.48.88.250** |
| 3D 프린터 (ender3v3se) | shutdown (익스트루더 57.38°C) |
| Door Sensor 1 (거실 창문) | 🟢 열림 |
| Door Sensor 2 (현관문) | 🔴 닫힘 |
| Zigbee2MQTT | v2.9.1 연결됨 |

---

### 📊 통합 모니터링 센서

| 항목 | 개수 | 비고 |
|------|------|------|
| YouTube 채널 센서 | ~27개 | VTuber/유튜버 채널 구독자·최신영상 |
| Twitch 센서 | ~40개 | 스트리머 온/오프라인 상태 |
| GitHub 리포 센서 | 4개 | whisper.cpp, stable-ts, whisperX, llm-subtrans, yt-dlp |
| Synology NAS (Home) | ~26개 | CPU, RAM, 디스크, 드라이브 건강 |
| Synology NAS (NVR) | ~20개 | NVR 전용 모니터링 |
| 모바일 앱 | 2대 | SM-S906N 배터리 63%, SM-S906N_kak 100% |

---

### 🔄 업데이트 필요 항목

| 기기/소프트웨어 | 현재 | 최신 |
|----------------|------|------|
| **Synology Home DSM** | 7.2.2-72806 U5 | **7.3.2-86009 U1** |
| **Synology NVR DSM** | 6.2.4-25556 U7 | **6.2.4-25556 U8** |

> [!IMPORTANT]
> Synology NAS 2대 모두 DSM 업데이트 대기 중

---

### 사용자 (Persons)

- **Nexusroid**: unknown
- **Yoo**: unknown
