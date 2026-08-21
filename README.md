# 김유민

회사에서는 C++로 무인 보관함 키오스크 소프트웨어를 만들고, 퇴근 후에는 게임을 만듭니다.
필요한 건 직접 만들어 보는 편입니다.

- GitHub: [rladbals0129](https://github.com/rladbals0129)
- Blog: [season97.tistory.com](https://season97.tistory.com/)
- Email: rladbals0129@naver.com

## 실무 경력

### 유비라커 산업(주) · Windows MFC/C++ 소프트웨어 개발자

`2025.03 ~ 재직중`

무인 보관함의 보관, 찾기, 결제, 원격 제어를 수행하는 키오스크 소프트웨어를 개발합니다. 포트폴리오에 정리된 범위는 C++/MFC 기반 메인 키오스크, 카드 결제 서버 프로그램, 10인치 파생 키오스크, 현장 설치 자동화입니다.

| 영역 | 다룬 것 |
| --- | --- |
| 키오스크 본체 | C++/MFC, Win32 API, GDI+ 기반 UI. `CUI_Page` 상속 구조, 더블 버퍼링, 프레임 캐싱, 1080x1920 동적 레이아웃, 저자세 모드 좌표 변환 |
| 결제 | `CPaymentManager` 단일 진입점으로 카드, 현금, 카카오페이 흐름 통합. 카드 결제는 TCP, 현금 장비는 RS-232 시리얼, 카카오페이는 서버 연동 |
| 서버 통신 | MQTT 기반 관제 통신, 오프라인 DB 큐 재전송, 자동 재연결, 초기 핸드셰이크 동기화 |
| 하드웨어 제어 | RS-232로 보관함 보드, 지폐기, 동전기 제어. 보드 리셋, 헬스체크, 재시도 흐름 포함 |
| 접근성 | 고대비, 저자세, 돋보기, 음성 안내 기능을 UI 전반에 적용 |
| 운영 | `TaskManager`로 결제 프로세스 감시, 일일 작업, 새벽 자동 재부팅, 로그 관리 |
| 배포 | PowerShell, Batch, JSON 설정 기반 현장 설치 자동화. 파티션 생성, OS 설정, 런타임, DB, 드라이버, 키오스크 프로그램 배포까지 17개 단계를 silent install로 실행 |

#### 실무 프로젝트 단위로 보면

- `Locker_Kiosk_Korail_Ver2_NewUI` / `Locker_10Inch`
  - C++/MFC 키오스크 프로그램.
  - 메인 키오스크 엔진과 10인치 소형 디스플레이용 경량 파생 버전.
  - 결제, 통신, 하드웨어 제어 코어를 공유하는 구조.
- `UbiAnyCard_V2`
  - 키오스크와 ED-785 카드 단말기 사이를 중계하는 TCP 서버 프로그램.
  - 결제, 취소, ping 명령을 받고 시리얼 통신으로 카드 단말기와 교신.
  - 교통카드, 이비카드, 리얼패스 프로토콜 파싱 포함.
- `ServiceServerDlg`
  - C 기반 Windows service server.
  - 400+ 키오스크가 연결된 프로덕션 운영 서버.
- 그 외 private repo로 확인되는 실무 작업
  - `locker-app` TypeScript
  - `UExpress_WEB` Classic ASP
  - `AutoStart`, `Updater_UBI`, `UBILockerPlatfromApp`, `UBIKorail_doc`

규모로 확인되는 숫자는 메인 C++ 프로젝트 56,000+ LOC / 145 source files, 현장 자동 설치 17단계, 운영 서버 400+대 키오스크 연결입니다.

## 게임 포트폴리오

실무 경력과 별도로, 퇴근 후에는 Unity와 Unreal 기반 게임 프로젝트를 진행합니다. 공개 저장소가 있는 항목만 링크를 걸었습니다.

| 프로젝트 | 기술 | 요약 | 링크 |
| --- | --- | --- | --- |
| The Others Inside | Unreal Engine 5.7+, C++ | 정상/이상현상을 판별하는 1인칭 공포 루프물. DataTable, GameplayTag, `UAnomalyManager`, `UAnomalyTargetComponent` 기반 이상현상 시스템을 C++ 중심으로 구현 중 | WebPortfolio 문서(비공개) |
| AI 로봇 키우기 | Unity 6, C# | 3인 팀 방치형 RPG 모바일 게임. 코어 아키텍처, 전투, 스킬, 스탯/재화/업그레이드, CSV to ScriptableObject 데이터 파이프라인, 에디터 툴 담당 | [AI_Robot_Raising](https://github.com/rladbals0129/AI_Robot_Raising) |
| 굴러가유 알 (Rolling Egg) | Unity 6, C# | 2D 러닝 퍼즐 & 육성 시뮬레이션. 코어 아키텍처, 육성 시스템, 데이터 파이프라인, Unity Localization 기반 다국어 지원 담당 | [RollingEgg_Portfolio](https://github.com/rladbals0129/RollingEgg_Portfolio) |
| Diary of Lucie | C++, WinAPI | 4인 팀 로그라이크 탄막 슈팅. 몬스터 AI, 보스 패턴, 이펙트 렌더링 담당 | PDF 문서(비공개) |
| KUNAI | C++, WinAPI | 액션 플랫포머 개인 포트폴리오 | PDF 문서(비공개) |
| 감염된 도시 탈출 | Unreal Engine 5, Blueprint | 호러 서바이벌 FPS 개인 포트폴리오. AI Behavior Tree, Geometry Collection, Animation Blueprint, Sequencer 활용 | PDF 문서(비공개) |

## 기술

프로젝트나 저장소명으로 근거가 있는 것만 적습니다.

- **C / C++**: MFC, Win32 API, GDI+, Winsock TCP/IP, RS-232 Serial, MQTT, multithreading, synchronization
- **C# / Unity**: Unity 6, UniTask, Addressables, ScriptableObject data pipeline, Unity Localization, editor tooling
- **Unreal**: Unreal Engine 5, C++, Blueprint, DataTable, GameplayTag
- **Web / 운영 도구**: TypeScript, Classic ASP, PowerShell, Batch script, JSON config

## 지금 관심 있는 쪽

- 운영 중인 키오스크처럼 오래 켜져 있어야 하는 소프트웨어
- 게임에서 데이터와 툴이 콘텐츠 제작 속도를 밀어주는 구조
- 작은 팀에서 바로 써먹을 수 있는 자동화
