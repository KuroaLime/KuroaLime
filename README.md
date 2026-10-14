# DongHo Jung · KuroaLime

**Game Client Development**

C++와 Unreal Engine을 중심으로 게임 클라이언트 개발을 공부하고 있습니다.

멀티플레이 게임의 상태 동기화부터 전투 시스템, UI, DirectX 기반 렌더링까지 다양한 프로젝트를 경험했습니다. 최근에는 Unity와 Godot에서도 AI를 활용해 게임을 개발하며, 기획과 구현, 검증 과정을 기록하고 있습니다.

## About Me

- **게임플레이 시스템** — 전투, 스폰, 캐릭터 성장, 턴 진행과 게임 흐름 구현
- **멀티플레이** — 서버 권위 기반 상태 동기화와 리스폰 이후 데이터 유지
- **그래픽스** — DirectX 12, HLSL, 충돌 판정과 렌더링 학습
- **개발 과정** — 문제의 원인을 추적하고, 구현과 설계 결정을 문서로 정리

## Technologies

| 분야 | 사용 기술 |
| :--- | :--- |
| 주력 개발 | C++, Unreal Engine 5 |
| 그래픽스·Windows | DirectX 12, HLSL, Win32 API / GDI |
| 현재 프로젝트 | Unity / C#, Godot / GDScript |
| 학습·실습 | OpenGL, Python |
| 개발 도구 | Visual Studio, Git, GitHub |

## Featured Projects

### Dopamine Addiction
**4인 팀 · 클라이언트 프로그래머 | Unreal Engine 5 · C++**

TPS 전투, 전통 카드게임인 섯다, 상점 성장이 라운드마다 이어지는 온라인 멀티플레이 게임입니다. Dedicated Server 환경에서 게임플레이 시스템과 상태 동기화를 담당했습니다.

**주요 담당 내용**

- 서버 권위 기반 스폰 관리와 스폰 지점 점유 상태 복제
- 무기 발사·재장전·탄약 상태의 네트워크 동기화
- 리스폰 이후에도 유지돼야 하는 캐릭터 데이터를 `PlayerState`로 이관
- 기본 능력치와 성장·상점 효과를 합산하는 스탯 계산 구조 통합
- 체력 재생, 상점 UI와 성장 시스템 구현
- 황금 고블린의 등장 제어와 Behavior Tree 기반 행동 구현

**문제 해결 경험**

- 라운드가 반복되면 스폰 후보가 고갈되던 문제를 순회·재셔플 방식으로 개선
- 렌더링 부하를 유발하는 액터를 조사하고 Lumen 반영 범위를 조정
- 카드 배치 실패의 원인을 확인할 수 있도록 조건별 진단 로그 추가

[Repository](https://github.com/KuroaLime/dopamine_addiction) · [Gameplay Video](https://youtu.be/Gi9b-EheNaE)

### DirectX 12 · 헬기 전투 데모
**개인 프로젝트 | C++ · DirectX 12 · HLSL**

지형 위를 비행하며 타깃을 조준하고 미사일 전투를 진행하는 3D 액션 데모입니다. 렌더링과 충돌 판정, 게임플레이 로직을 함께 다뤘습니다.

- Hull / Domain Shader를 활용한 거리 기반 지형 테셀레이션
- GJK / EPA 기반 충돌 판정과 공간 분할 그리드
- Shadow Mapping과 PCF를 활용한 실시간 그림자
- 스텐실 버퍼를 활용한 거울 반사
- 헬기 조종, 타깃 락온, 미사일 발사·폭발
- 1인칭·3인칭·자유 시점 카메라

[Repository](https://github.com/KuroaLime/DirectX12_3DProgramming)

### Tales of the Dark Throne
**2인 팀 · 스테이지·턴 시스템·UI 담당 | C++ · Win32 API / GDI**

던전 탐색과 그리드 기반 전투를 다루는 Windows 게임 프로젝트입니다. 게임 진행을 구성하는 스테이지와 턴 순서, 플레이어의 행동을 연결하는 UI를 담당했습니다.

- 타일 데이터를 사용하는 스테이지 구성과 화면 전환
- 캐릭터 속도에 따른 턴 순서 관리
- 전투 행동 선택과 턴 진행을 위한 UI
- 게임 상태와 캐릭터 정보를 전달하는 화면 구성

[Repository](https://github.com/KuroaLime/Tales_of_the_Dark_Throne)

## Currently Building

### Jelly Sling
**2인 팀 · 게임 진행·UI·기믹·환경 담당 | Unity · C#**

파쿠르와 고무손 이동을 결합해 개인 완주 기록을 단축하는 3인칭 타임어택 게임을 개발하고 있습니다. AI를 활용해 설계를 구체화하고 기능을 구현하며, 팀원의 캐릭터·물리 시스템과 연결하고 있습니다.

**현재 구현한 내용**

- 타이틀, 허브, 플레이, 결과 화면으로 이어지는 진행 흐름
- 수동·자동 저장과 불러오기, 손상된 저장 파일의 복구 처리
- 카운트다운, 런 타이머, 골인과 결과 처리
- 체크포인트와 낙하 후 복귀
- 밀리초 단위 완주 기록과 개인 기록 순위
- 여러 스테이지에 배치할 수 있는 진행 컴포넌트

**설계 중인 내용**

- 열기구를 이용한 스테이지 선택과 입장 연출
- 게임 분위기에 맞는 허브·환경·UI 구성

### The Way of the Immortals
**개발 중 · AI 활용 프로젝트 | Godot · GDScript**

선협 세계관에서 수련과 탐험, 턴제 카드 전투를 통해 성장하는 게임입니다. 현재 플레이 가능한 프로토타입을 바탕으로 시스템과 UI를 확장하고 있습니다.

- 카드 드래그와 대상 선택, 술법 준비·융합·덱 편성
- 수련과 돌파, 부상과 회복을 연결한 성장 구조
- 7일 단위 일정 편성과 활동 실행
- 세계 지도 탐험, 문파 교류, 비경 진행
- 재료 수집과 제작, 시설 성장
- 캐릭터 생성, 자동 저장·이어하기
- 게임 규칙과 화면 처리를 분리하고 데이터로 수치 관리

## More Projects

### END OF THE LINE
**2인 개발 프로젝트 | Unreal Engine 5 · C++**

오염된 도심의 지하철망을 배경으로 한 탑다운 액션 로그라이크 프로젝트입니다.

절차적 던전 생성, 방별 전투 흐름, 캐릭터·스킬·아이템 데이터 구조와 UI를 포함하며, 전투와 성장 시스템을 함께 설계하고 있습니다.

[Repository](https://github.com/KuroaLime/END_OF_THE_LINE)

### Another Tail
**게임 시스템 기획 프로젝트**

턴제 JRPG의 전투와 성장, 세계관을 구체적인 시스템 문서로 정리한 프로젝트입니다.

적응형 전투 AI, 카르마·명성·관계도, 전투 공식과 밸런스, 퀘스트 분기, UI와 데이터 구조를 다루며 시스템 사이의 연결과 일관성을 검토했습니다.

[Repository](https://github.com/KuroaLime/Game_Design-Another_Tail)

### No Body Knows
**기획 단계 · 작업명**

플레이어가 직접 만든 행적을 바탕으로 사건을 추리하는 2D 멀티플레이 머더 미스터리를 기획하고 있습니다.

관계와 개인 목표를 매 판 다르게 배정하는 구조를 검토하며, AI의 제안과 제작자의 선택·수정 이유를 기록하고 있습니다.

### 2D Magic School RPG
**기획 프로젝트**

마법학교의 한 해를 보내며 수강 선택, 자습과 탐험으로 전문 분야를 키우는 육성 RPG입니다.

한정된 활동 기회 안에서 성장 방향을 선택하고, 배운 주문을 실전에서 사용해 상위 마법으로 이어가는 구조를 설계했습니다.

## Learning Archive

| 프로젝트 | 내용 |
| :--- | :--- |
| [Shader Programming](https://github.com/KuroaLime/ShaderProgramming) | 셰이더 프로그래밍 실습 |
| [2D Game Project](https://github.com/KuroaLime/2DGP_Project) | Python 기반 2D 게임 제작, 캐릭터·카메라·UI 구성 |
| [2D Programming Drill](https://github.com/KuroaLime/2021180037_2DGP_DRILL) | 2D 게임 프로그래밍과 충돌 처리 실습 |
| Computer Graphics | OpenGL 기반 도형 표현, 변환과 입력 처리 학습 |
| Problem Solving | C++ 기반 알고리즘 문제 풀이 |
| Deep Learning | 신경망, 분류와 CNN 학습 |

## Working with AI

게임 기획과 프로토타입 제작, 구현 검토와 문서화에 AI를 활용하고 있습니다.

- 만들고 싶은 플레이 경험과 요구사항을 먼저 정의합니다.
- 제안된 방법을 비교하고 프로젝트에 맞게 선택·수정합니다.
- 구현 결과는 테스트와 실제 플레이 흐름으로 확인합니다.
- 결정 이유와 시행착오, 남은 문제를 개발 기록에 남깁니다.
