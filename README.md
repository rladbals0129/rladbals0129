# 김유민

회사에서는 C++로 무인 보관함 키오스크 소프트웨어를 만들고, 퇴근 후에는 게임을 만듭니다.
구조부터 짜고, 막히면 뚫고, 없으면 만들고, 귀찮으면 자동화합니다.

- **웹 포트폴리오: [kymportfolio.netlify.app](https://kymportfolio.netlify.app/)** — 소개·기술·경력에 프로젝트별 기술 문서 페이지까지
- Blog: [season97.tistory.com](https://season97.tistory.com/)
- Email: rladbals0129@naver.com

## 실무 경력

### 유비라커 산업(주) · Windows MFC/C++ 소프트웨어 개발자

`2025.03 ~ 재직 중`

무인 보관함의 보관, 찾기, 결제, 원격 제어를 담당하는 키오스크 소프트웨어를 개발합니다. C++/MFC 메인 키오스크, 카드 결제 서버 프로그램, 10인치 파생 키오스크, 현장 설치 자동화까지 맡았습니다.

상세 내용은 [경력 기술 문서](https://kymportfolio.netlify.app/경력기술/)에 정리해 놨습니다.

| 영역 | 다룬 것 |
| --- | --- |
| 키오스크 본체 | C++/MFC, Win32 API, GDI+ 기반 UI. `CUI_Page` 상속 구조, 더블 버퍼링, 프레임 캐싱, 1080x1920 동적 레이아웃, 저자세 모드 좌표 변환 |
| 결제 | `CPaymentManager` 하나로 카드·현금·카카오페이 흐름을 통합. 카드는 TCP, 현금 장비는 RS-232 시리얼, 카카오페이는 서버 연동 |
| 서버 통신 | MQTT 관제 통신, 오프라인 DB 큐 재전송, 자동 재연결, 초기 핸드셰이크 동기화 |
| 하드웨어 제어 | RS-232로 보관함 보드, 지폐기, 동전기 제어. 보드 리셋과 헬스체크, 재시도 흐름까지 |
| 접근성 | 고대비, 저자세, 돋보기, 음성 안내를 UI 전반에 적용 |
| 운영 | `TaskManager`로 결제 프로세스 감시, 일일 작업, 새벽 자동 재부팅, 로그 관리 |
| 배포 | PowerShell·Batch·JSON 설정 기반 현장 설치 자동화. 파티션 생성, OS 설정, 런타임, DB, 드라이버, 프로그램 배포까지 17단계를 silent install로 실행 |

#### 프로젝트 단위로 보면

- `Locker_Kiosk_Korail_Ver2_NewUI` / `Locker_10Inch`
  - C++/MFC 키오스크 프로그램.
  - 메인 키오스크 엔진과 10인치 소형 디스플레이용 경량 파생 버전.
  - 결제, 통신, 하드웨어 제어 코어를 공유하는 구조.
- `UbiAnyCard_V2`
  - 키오스크와 ED-785 카드 단말기 사이를 중계하는 TCP 서버 프로그램.
  - 결제, 취소, ping 명령을 받아 시리얼로 카드 단말기와 교신.
  - 교통카드, 이비카드, 리얼패스 프로토콜 파싱 포함.
- `ServiceServerDlg`
  - C 기반 Windows service server.
  - 키오스크 400대 이상이 붙어 있는 운영 서버.
- 그 외 비공개 저장소로 관리하는 작업
  - `locker-app` TypeScript
  - `UExpress_WEB` Classic ASP
  - `AutoStart`, `Updater_UBI`, `UBILockerPlatfromApp`, `UBIKorail_doc`

규모로 보면 메인 C++ 프로젝트가 56,000줄 남짓, 소스 파일 145개입니다. 현장 설치는 17단계 자동화로 돌아가고, 운영 서버에는 키오스크 400대 이상이 연결돼 있습니다.

## 게임 프로젝트

퇴근 후에는 Unity와 Unreal로 게임을 만듭니다. 기술 문서 페이지가 있는 것은 사이트로, 소스가 공개된 것은 저장소로 링크를 걸었습니다.

| 프로젝트 | 기간 | 기술 | 맡은 것 | 링크 |
| --- | --- | --- | --- | --- |
| The Others Inside | `2026.02 ~ 2026.03` (개발 종료) | Unreal Engine 5.7+, C++ | 8인 팀 1인칭 공포 루프물. DataTable, GameplayTag, `UAnomalyManager`, `UAnomalyTargetComponent` 기반 이상현상 시스템과 스테이지 흐름을 C++로 구현. PM 역할 겸임 | [기술 문서](https://kymportfolio.netlify.app/Portfolio_TheOthersInside/) |
| AI 로봇 키우기 | `2025.12 ~ 2026.03` | Unity 6, C# | 3인 팀 방치형 RPG 모바일 게임. 코어 아키텍처, 전투, 스킬, 스탯·재화·업그레이드, CSV to ScriptableObject 데이터 파이프라인, 에디터 툴 | [기술 문서](https://kymportfolio.netlify.app/Portfolio_AI로봇키우기/) · [소스](https://github.com/rladbals0129/AI_Robot_Raising) |
| 굴러가유 알 (Rolling Egg) | `2025.08 ~ 2025.12` | Unity 6, C# | 2D 러닝 퍼즐 & 육성 시뮬레이션. 코어 아키텍처, 육성 시스템, 데이터 파이프라인, Unity Localization 다국어 지원 | [기술 문서](https://kymportfolio.netlify.app/Portfolio_RollingEgg/) · [소스](https://github.com/rladbals0129/RollingEgg_Portfolio) |
| Diary of Lucie | `2023.09` | C++, WinAPI | 4인 팀 로그라이크 탄막 슈팅. 몬스터 AI, 보스 패턴, 이펙트 렌더링 | [PDF](https://kymportfolio.netlify.app/루시의일기.pdf) |
| KUNAI | `2023.07 ~ 2023.08` | C++, WinAPI | 액션 플랫포머 개인 포트폴리오 | [PDF](https://kymportfolio.netlify.app/KUNAI.pdf) |
| 감염된 도시 탈출 | `2023.10` | Unreal Engine 5, Blueprint | 호러 서바이벌 FPS 개인 포트폴리오. AI Behavior Tree, Geometry Collection, Animation Blueprint, Sequencer | [PDF](https://kymportfolio.netlify.app/언리얼포폴_개별기술문서.pdf) |

## AI를 붙여서 하는 일

코딩에만 쓰지는 않습니다. 업무 전반에 붙여서 씁니다.

- 조사가 필요한 작업은 먼저 대화로 계획을 세우고 md 파일로 남깁니다. 그 파일을 새 대화에 읽혀서 이어가면 맥락은 유지되고 토큰은 덜 씁니다.
- 반복되는 업무 문서는 Python 템플릿 스크립트로 뽑고, 현장 설치는 Batch·PowerShell 17단계 자동화로 돌립니다.
- Google Sheets에 있는 기획 데이터를 CSV를 거쳐 ScriptableObject로 변환하는 파이프라인을 만들어 손으로 옮기던 작업을 없앴습니다.
- RS-232 통신 누락으로 깨진 DB는 누락 패턴을 분석해 정합성 검증·복구 로직을 넣고 예외처리를 보강했습니다.
- 도구는 Cursor, Claude, Gemini, MCP 서버, AI Agent 멀티스텝 자동화를 씁니다. 위 포트폴리오 사이트와 기술 문서 페이지도 이 방식으로 만들었습니다.

## 기술

써본 것만 적었습니다.

- **C / C++**: MFC, Win32 API, GDI+, Winsock TCP/IP, RS-232 Serial, MQTT, multithreading, synchronization
- **C# / Unity**: Unity 6, UniTask, Addressables, ScriptableObject 데이터 파이프라인, Unity Localization, 에디터 툴
- **Unreal**: Unreal Engine 5, C++, Blueprint, DataTable, GameplayTag
- **Web / 운영 도구**: TypeScript, Classic ASP, PowerShell, Batch script, JSON config
- **협업**: Git, SVN, Azure DevOps

## 요즘 관심

- 키오스크처럼 오래 켜져 있어야 하는 소프트웨어
- 데이터와 툴이 콘텐츠 제작 속도를 밀어주는 구조
- 작은 팀에서 바로 써먹을 수 있는 자동화
