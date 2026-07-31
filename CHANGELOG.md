# 변경 기록

주간 서베이가 무엇을 바꿨는지 여기에 남깁니다. 최신이 위입니다.

## 2026-07-30 (7차: 신규 7건, 보강 5건 — CS 보안 계보의 빈 칸이 채워짐)

이번 실행의 소득은 새 논문 개수가 아니라 계보가 이어진 것입니다. CS의 PBR+RTT 결합이
어디서 왔고 누가 그 한계를 이미 지적했는지가 코퍼스 안에서 연결되었습니다.

### 신규 논문

- 신규: On the Performance and Security of Bluetooth Channel Sounding
  (IEEE Access 2026, vol. 14, pp. 109726–109741, 관련도 높음) — **본인 논문**.
  강화 ED/LC 공격으로 NADM EER을 11% 미만에서 43~49%까지 올린 결과.
  전문 확인 완료. Crossref 질의로 발견했습니다.
- 신규: Secure, Accurate, and Practical Narrow-Band Ranging System
  (TCHES 2021, 관련도 높음) — CS의 PBR+RTT 결합의 학술적 원형. imec/KU Leuven이
  규격보다 먼저 NXP KW36에 같은 논리를 구현했습니다. 전문 확인 완료.
- 신규: BLE Channel Sounding: Novel Method for Enhanced Ranging Accuracy in
  Vehicle Access (IEEE Access 2025, 관련도 높음) — 교차상관 기반 방어 논증의 실물 사례.
  전문 확인 완료.
- 신규: A high-accuracy phase-based ranging solution with BLE (WCNC 2019, 관련도 높음)
  — BLE MCPR의 뿌리. 인용 계보 상류 노드.
- 신규: Frequency Based Ranging (FBR) ... on a Single 2 MHz Channel (IoT 2025, 관련도 보통)
- 신규: Enhancing Bluetooth Channel Sounding Performance in Complex Indoor
  Environments (IEEE Sensors Letters 2024, 관련도 보통)
- 신규: HardaBLE: Hardening BLE Against Software Compromise (WiSec 2026, 관련도 낮음)

### 보강

- 보강: Secure Ranging with IEEE 802.15.4z HRP UWB — 미검증 → 전문확인.
  하드웨어(없음: 이론+수치 시뮬레이션), 소프트웨어, 결과 6항, 한계 5항.
  **핵심 소득**: 저자들이 SYNC의 CIR과 STS의 CIR을 비교해 탭을 검증하는 방식에
  보안 보장이 없다고 명시(6.1절)합니다. 같은 패킷의 두 관측을 교차대조하는 것이
  독립적 보안 증거가 아니라는 논증이며 CS의 PBR/RTT 교차검증에 그대로 옮겨 붙습니다.
- 보강: UWBAD — 미검증 → 전문확인. 게재지가 **ACM CCS 2024**로 확정(기존 "NDSS 추정",
  tier preprint → top4). 저자 12명, DOI, 장비(DW3210 + ESP32 + TQP3M9035), 결과 8항.
  상용 PKES가 옛 거리 데이터를 약 2분간 유지한다는 실측이 CS 배포에도 그대로 걸립니다.
- 보강: Data-driven Processing using Parametric Neural Network — 게재지 **ICASSP 2025** 확정,
  저자 4명, DOI. (기존 venue "확인 필요")
- 보강: High-Precision Ranging Fusion Using Neural Network — 게재지 WACSA → **WASA** 정정,
  저자 4명, 페이지.
- 보강: Study of BLE6 Ranging Performance in a Utility Basement — 저자 3명,
  게재지 IPIN-WCAL Workshop 확정. **연도 2026 → 2025 정정** (seo-2026의 참고문헌 [28] 근거).

### 인용 관계

48 → 54 → **72건**. 새 논문 7건의 인용을 넣은 것에 더해, 기존 논문 3건의 참고문헌을
다시 훑어 새 노드로 가는 간선을 채웠습니다. 안 하면 새 노드가 고립돼 보입니다.

- staat-2022 → abidin-2021, zand-2019
- schex-2026 → zand-2019, santra-2024
- wieme-2025 → santra-2024, suresh-2025

### 표준

- 신규: **Channel Sounding Inline Phase Correction Term Transfer (IPT)** VSr01_PR 공개검토 초안.
  Reflector가 인라인 아날로그 위상 사전보상을 수행하고 PCT의 허수(Q) 성분을 HCI로
  보고하지 않습니다. 기능 추가가 아니라 **관측 가능성의 축소**로 읽어야 합니다 —
  seo-2026이 하드웨어 검증에 실패한 원인이 원시 지표 미노출이었는데, IPT는 Q 성분마저
  걷어냅니다. 관련도 높음.
- 갱신: IEEE 802.15.4ab — D03(2025-09) → **D04 SA 투표 단계** (LMSC 조건부 승인 2026-02).
  파형·보안 항목이 사실상 고정된 것으로 보아야 합니다.
- 확인만: Bluetooth Core 6.3이 여전히 최신 채택본. 신규 코어 릴리스 없음.

### 실패

- USENIX Security '25/'26 프로시딩 페이지가 usenix.org 전체 403. dblp 미러도
  세션 제목까지만 나오고 논문 제목이 잘렸습니다. 지난 실행 우선순위 1번이었는데
  또 못 했습니다. 다음에는 dblp XML API(`/rec/`)나 Crossref의 학회 필터로 우회할 것.
- dblp 검색 API가 3질의 후 500/레이트리밋. Crossref와 OpenAlex로 대체했고,
  결과적으로 초록·저자·DOI 확보에는 이쪽이 더 안정적이었습니다.
- ACM DL은 CC-BY 논문도 403 (FBR). IEEE Access OA는
  `stampPDF/getPDF.jsp?arnumber=` 경로로 받힙니다 — 이번에 확인한 우회로입니다.
- CCS 2026은 아직 채택 목록 미공개.

### 판단으로 넘긴 것

- WiSec 2026 "A Deep Dive into Wormhole Attacks in Underwater Acoustic Communication"은
  ToF 거리측정에 대한 중계 공격을 실증하지만 매체가 음향이라 물리가 다릅니다.
  추가하지 않고 여기에 남깁니다.
- Zenodo "Bluetooth Channel Sounding IQ Dataset Across Diverse Scenarios"는
  이미 wieme-2025의 `artifacts.dataset`(10.5281/zenodo.17347695)으로 기록되어 있어
  별도 항목을 만들지 않았습니다.

## 2026-07-29 (6차: Codex 교차검토 — 사실 오류 1건 정정)

연구주제와 인사이트를 Codex에 검토시켰습니다. 2라운드 토론했고, 사실 오류 하나와
구조적 약점 하나가 나왔습니다.

### 사실 오류 정정 (Codex가 맞았음)

Core 6.2에 **Channel Sounding Amplitude-based Attack Resilience**가 있습니다.
RTT 패킷 진폭 조작 공격 모델, DFT 기반 진폭 NADM, 90% 탐지 정확도 요구,
다단계 인증 시험, LL_CS_CAPABILITIES_REQ/RSP의 지원 비트까지 규정합니다.
제 표준 기록에는 Shorter Connection Interval만 있었고 관련도도 medium이었습니다.
critical로 올리고 내용을 채웠습니다.

이 정정이 제 주장 하나도 무너뜨립니다. "규격은 아무것도 정의하지 않는다"는 틀렸습니다.
정확히는 "거리 추정과 결합 정책은 Host에 맡기지만 탐지 지표와 인증 시험은 직접 규정한다"입니다.
그리고 NADM은 6.0의 위상 기반과 6.2의 진폭 기반이 별개라, 뭉뚱그리면 어느 버전을
공격하는지가 흐려집니다.

### 분류 축 교체

주제 6개를 **공격의 인과 사슬** 4개 + 연구 메모로 바꿨습니다.

1. 측정의 식별가능성 — 조작과 실제 거리가 구별되는가
2. 공격 실현가능성 — 공격자가 그 조건을 만들 수 있는가
3. 수신기와 판정 정책 — 추정되고 탐지를 통과하고 수락되는가
4. 시스템 구성과 영향 — 상위 계층과 유스케이스가 위험을 어떻게 바꾸는가

앞의 넷은 순서가 있습니다. 1이 참이어도 2가 거짓이면 위협이 아닙니다.

### 성숙도 태그 도입

과대주장을 구조적으로 막는 축입니다. 문헌·추론, 시뮬레이션, 실측 trace 주입,
케이블 실측, 무선 실증, 상용 end-to-end 여섯 단계입니다.

현재 상태는 문헌·추론 9, 시뮬레이션 1, 실측 trace 주입 2입니다.
**trace-replay 위로는 아무것도 없습니다.** 이게 정직한 그림이고 전에는 안 보였습니다.

케이블 실측과 무선 실증을 나눈 것도 Codex 지적입니다. 케이블 실험은 "실제 칩셋에서
조작이 PBR과 RTT에 동시에 반영되는가"를 답하지만 "무선으로 FHSS를 실시간 추적할 수
있는가"는 답하지 못합니다.

### 표현 강등

- "FHSS가 CS를 지키는 유일한 것" → "채널 선택적 NGD 공격에서는 FHSS 추적이 실질적 병목"
  광대역 LTI 회로, 병렬 필터뱅크, 채널 예측, 강건 추정기를 배제하지 못했습니다.
- PBR 결과와 Anliker의 RTT 수치를 나란히 둔 것을 "동시 검증"으로 읽히게 쓰면 안 됩니다.
  장비·파형·수신기가 다르므로 교차 논증일 뿐입니다. 근거 구분을 앞에 명시했습니다.
- 커버리지 0.5 문턱은 물리 법칙이 아니라 이 정합 추정기의 bimodal capture 전환점입니다.

### 프레이밍 승격

핵심 인사이트를 "교차검증이 실패한다"에서 **"공통모드 경로 지연은 관측값만으로
실제 거리 변화와 식별되지 않는다"**로 올렸습니다. 두 센서가 같은 숨은 변수에 같은
방향으로 반응하면 교차검증은 독립적 보안 증거가 아니라는 일반 명제입니다.

그리고 Codex가 R1에서 부분 철회하며 더 중요한 것을 짚었습니다. 거리 바운딩이
원리적으로 주는 것은 거리의 **상한**입니다. 공격자가 신호를 지연시키면 그 관측은
실제로 더 먼 경우와 완전히 같고, 인증된 challenge도 "응답을 앞당기는 것"은 막지만
"임의로 늦추는 것"은 식별하지 못합니다. PBR의 합성 대역폭 약 80MHz로도 비모호
시간 분해능은 12.5ns, 편도 약 1.9m라 UWB식 판별과 다릅니다.

따라서 남는 방어는 둘뿐입니다. 신뢰된 회로·처리 지연 상한을 두거나, RF 관측모델
밖의 정보를 쓰는 것. 다중 안테나도 새 기하학적 제약을 실제로 더할 때만 독립 근거이고,
같은 신호를 비슷하게 받는 복제 관측은 독립 근거가 아닙니다.

### 강등

거리 확대 인사이트를 낮췄습니다. CCC Digital Key 공개 자료에서 "확대 시 약한 인증으로
폴백"하는 fail-open 정책을 확인하지 못했습니다. Release 3.0은 NFC를 하위호환과 배터리
부족 상황용 별도 인터페이스로 설명하며, 이는 "UWB 실패 시 무인증 unlock"을 뜻하지
않습니다. 축소는 보안 위반의 중심, 확대는 주로 가용성, 폴백 악용은 조건부 가설로
분리했습니다.

### 유지 (제 반론이 수용됨)

위험 평가 프레임은 독립 기여로 유지합니다. 다만 단순 곱이 아니라
P = 1 - (1 - p_eff)^N(T)로 쓰고, lockout과 재인증 때문에 둘이 독립이 아닐 수 있음을
명시해야 합니다. 그리고 "확률 x 반복"은 이미 거리경계 문헌에 있으므로 신규성을
거기 두면 안 됩니다. 기여는 의미가 다른 수치를 하나의 운영 위험 단위로 환산하는
절차에 있습니다.

### 신규 할 일 2건

1순위로 "동일 CS procedure에서 PBR·RTT·NADM·품질플래그·Host 최종거리 동시 기록"이
올라갔습니다. 현재 가장 위험한 지점이 여기입니다.
그리고 "정합도 탐지의 정상 LOS/NLOS ROC 곡선"이 추가됐습니다. 0.949 대 0.27의 분리만으로는
방어가 아니고 임계값에서 정상 측정이 얼마나 거부되는지를 함께 내야 합니다.


## 2026-07-28 (5차: 주파수 의존 군지연)

4차의 "평탄한 군지연은 PBR과 RTT를 똑같이 움직인다"에 이어, 실제 회로처럼
주파수 의존성이 있을 때 어떻게 되는지 쟀습니다. 결과가 이분법으로 갈립니다.

기준 정합도 0.949 (35m 실외, 깨끗한 신호)

| 조건 | PBR 이동 | 정합도 | 판정 |
|---|---|---|---|
| FHSS 추적 성공 (대역폭 0.5~20MHz 모두) | -18.590 m | 0.949 | 완벽, 무흔적 |
| 고정 LO (대역폭 0.5~80MHz 모두) | 통제 불능 | 0.23~0.39 | 추정 붕괴 |

추적하면 회로 대역폭과 무관하게 정확히 `c·τ`만큼 이동하고 정합도가 기준값
그대로입니다. 추적 못 하면 거짓 거리를 만드는 게 아니라 측정을 망가뜨립니다.
스푸핑이 아니라 서비스 거부입니다.

### 결론이 바뀝니다

CS를 실제로 지키는 것은 PBR-RTT 교차검증이 아니라 FHSS 추적의 난이도입니다.
교차검증은 4차에서 이미 순수 군지연을 못 잡는 것으로 나왔고, 이번에는
공격 성립의 진짜 문턱이 채널 추적임이 드러났습니다.

그런데 Anliker 2026은 FHSS 동기화를 "범위 밖의 공학적 과제"로 명시하고
USRP X310 급 광대역 SDR과 FPGA 폴리페이즈 필터뱅크가 필요하다고만 적었습니다.
즉 CS를 지키고 있는 유일한 것이 아무도 실증하지 않은 부분입니다.

새 인사이트: `fhss-tracking-is-the-real-barrier`

### 방법론 정정

첫 시도의 잔차 지표가 틀렸습니다. 위상 언랩 기반이라 분산이 아니라 언랩 품질을
재고 있었고, 평탄 주입 후 잔차가 오히려 줄어드는 모순이 나왔습니다.
언랩이 필요 없는 정합도(정규화 상호상관 계열)로 교체했습니다.
이 지표는 CS 규격의 NADM과 같은 계열이지만, NADM은 RTT 쪽만 규정하므로
PBR 톤의 정합도를 보는 지표는 규격에 없습니다. 값싼 방어 후보입니다.

재현 코드: `experiments/dispersive_ngd.py`

## 2026-07-28 (4차: 2단 공격기 실험 — 3차 결론 철회)

### 철회

3차에서 낸 "하나의 NGD 회로로는 PBR과 RTT가 9m 어긋나므로 CS 교차검증이 작동한다"는
예비 결론을 철회합니다. **틀렸습니다.**

원인은 `sample_1_meter.csv` 한 파일에서 8π 관례를 확정한 것입니다. 그 파일은
`data.zip` 안의 `distance_2/LOS/1_meter.csv`와 다른 별개 데이터였고(20행 대 100행,
내용도 다름), 올바른 4π로 읽으면 파일명과 달리 약 1.96m가 나옵니다.
Zenodo 최상위에 따로 놓인 맛보기 파일이며 기준으로 삼으면 안 됩니다.

### 확정

실외 시리즈 30개 거리(1~72m, 다중경로 없음)로 관례를 확정했습니다.

- 올바른 관례는 4π. 기울기 비 1.0051, 잔차는 거리에 무관한 +0.86m 고정 바이어스
  (케이블·안테나·처리 지연)
- 실내 창고 데이터는 다중경로로 언랩 기반 추정기가 무너집니다(평균 오차 3.5m).
  Wieme가 보고한 이상치 문제와 같은 현상입니다. 언랩이 필요 없는 정합필터로 바꾸면
  실외에서 1~40m 전 구간이 깨끗합니다.

### 실험 결과

경로에 놓인 회로의 군지연 τ는 PBR 거리를 `c·τ`만큼 움직입니다. RTT도 왕복 시간이
2τ 바뀌어 `c·(2τ)/2 = c·τ`로 같습니다. 실측 주입에서 다섯 조건 모두 예측과
6mm 이내로 일치했습니다.

| τ (ns) | PBR 실측 변화 | 예측 c·τ | 불일치 |
|---|---|---|---|
| -62 | -18.590 m | -18.587 m | 3 mm |
| -30 | -8.990 m | -8.994 m | 4 mm |
| -10 | -3.000 m | -2.998 m | 2 mm |
| +10 | +3.000 m | +2.998 m | 2 mm |
| +30 | +9.000 m | +8.994 m | 6 mm |

-62ns에서 PBR -18.590m는 Anliker 2026이 RTT에서 측정한 -18.35m와 같습니다.
**두 측정이 같은 거짓 거리를 보고하므로 교차검증에 걸리지 않습니다.**
공격자는 자유도를 추가할 필요조차 없고, 2단 공격기는 불필요합니다.

### 남은 질문 (더 좋아짐)

이 계산은 통과 대역에서 평탄한 군지연을 가정합니다. Anliker의 회로는 1MHz 폭
CS 채널에 맞춰 설계됐는데 PBR은 2402~2476MHz의 72개 채널을 씁니다.
74MHz 전체에 평탄한 음의 군지연을 유지하는 것이 실제 제약일 가능성이 높습니다.

방어로 뒤집으면, CS가 PBR 톤과 RTT 패킷을 의도적으로 멀리 떨어진 채널에 배치하면
공격자에게 광대역 평탄 NGD를 요구하게 되어 난이도가 올라갑니다.
규격 개정 없이 스케줄링만으로 가능한 방어 후보입니다.

선행 확인 사항: CS가 실제로 PBR과 RTT를 수치 비교하는지, 허용오차가 얼마인지를
규격에서 아직 확인하지 않았습니다. 이 논증의 전제이므로 먼저 해야 합니다.

재현 코드: `experiments/two_stage_attacker.py`, `experiments/pbr_from_iq.py`

## 2026-07-28 (3차: Wieme 데이터셋 검증)

인사이트 `spec-vs-implementation-debate`가 걸어둔 전제 조건을 실제로 확인했습니다.
데이터가 원시 수준인지 집계된 거리값인지에 따라 그 연구 줄기가 성립하거나 무너지는
상황이었는데, 성립합니다.

데이터셋 실체

- Zenodo 10.5281/zenodo.17347695, CC-BY-4.0, 28 MB, 250개 이상 시나리오
- 원시 per-step 복소 I/Q. 측정 N행 x step 159열, 셀마다 8개 정수
  (플래그2, 채널인덱스, 0, I1, Q1, I2, Q2)
- 채널 2~76 중 고유 72개. CS 규격의 "79개 중 최대 72개"와 정확히 일치
- `mapping.csv`가 initiator/reflector 3D 좌표를 mm로 제공 (MoCap ground truth)

복원 검증

- 한쪽 I/Q만으로는 거리가 안 나옵니다. 두 복소값을 곱해야 주파수에 선형인 위상이 나옵니다.
- `d = -c * (dphi/df) / (8*pi)`. 8pi인 이유는 양쪽 I/Q가 각각 왕복 위상을 담고 있어서입니다.
- MoCap 실측 1.0093 m에 대해 단순 slope 추정기로 0.9795 m 복원. 오차 3 cm.
- 재현 코드: `experiments/pbr_from_iq.py`

예비 발견 (가설과 반대 방향)

같은 -62 ns 군지연을 이 원시 데이터에 주입하면 PBR 거리가 약 -9.3 m 움직입니다
(왕복 경로 2회 통과 기준). 그런데 Anliker 2026은 같은 회로가 CS RTT에서 -18.35 m를
만든다고 보고했습니다. 즉 하나의 NGD 회로만으로는 두 측정이 약 9 m 어긋나므로,
CS의 교차검증이 이 공격에 대해서는 실제로 작동합니다.

`dual-defense-not-independent` 인사이트를 이에 맞춰 고쳤습니다. 질문이 죽은 게 아니라
날카로워졌습니다. 진짜 질문은 공격자가 자유도를 하나 더 쓰면 되는가입니다.
NGD로 RTT를 앞당기면서 별도 소자로 PBR을 그에 맞추는 2단 공격기가 성립하는지가 핵심이고,
성립하지 않으면 왜 불가능한지가 CS 설계의 강점으로 정리됩니다.

주의: 제 PBR 복원은 단순 slope 추정기이고 Anliker의 RTT 수치는 전체 CS 수신기
시뮬레이션에서 나온 것이라, 두 숫자를 나란히 놓는 데는 한계가 있습니다.
예비 관찰로만 취급해야 합니다.

## 2026-07-28 (2차: 미완료분 처리)

1차에서 막혔던 USENIX Security를 dblp 검색 API로 우회했습니다.
논문 32 → 33건, 4대 학회 11 → 13건, 원문 대조 7 → 10건.

서지정보 정정 1건 (중요)

- **Secure Ranging with IEEE 802.15.4z HRP UWB**가 실제로는 **IEEE S&P 2024** 게재작이었습니다.
  기존 기록은 학회 미확인에 tier가 `other`였습니다. 저자는 Xiliang Luo, Cem Kalkanli,
  Hao Zhou, Pengcheng Zhan, Moche Cohen. 이 논문은 Ghost Peak에 대한 사실상의 반론으로,
  802.15.4z의 취약성이 표준 결함이 아니라 수신기 구현 문제라고 논증합니다.
  분류를 `defense`, 관련도를 높음으로 올렸습니다.

신규 논문 1건

- LEO-Range (USENIX Security 2025). 저자가 Coppola, Camurati, Singh, Capkun으로
  Anliker 2026과 겹칩니다. OFDM 호환 물리계층 보안 거리측정 설계.

원문 대조 3건 완료

- **Wieme 2025 (IEEE Access)** — nRF54L15 DK, NCS 2.9.1, Zephyr, 단일 subevent 160 step,
  MoCap 밀리미터 ground truth. 공개 데이터셋 zenodo 10.5281/zenodo.17347695.
  거리 구간에 따라 최적 알고리즘이 뒤바뀝니다. 1~10 m는 MUSIC이 80% 정확,
  20 m까지는 slope 기반이 87%에서 2.5 m 미만인데 같은 백분위 MUSIC은 8 m.
- **MTAC (IEEE S&P 2020)** — 실기기 없는 이론·시뮬레이션 논문임을 확인.
  상관 피크 기반 검증은 안전하지 않다는 논증이 핵심.
- **V-Range (NDSS 2022)** — USRP 도터보드 2개로 동기 공격자 구성, 지하실 15 m,
  mm-wave는 벡터 신호 발생기. 에너지 분산 기반 무결성 검사로 거리 확대 탐지.

신규 인사이트 2건

- **MTAC이 2020년에 상관 기반 검증은 안전하지 않다고 논증했고, CS의 NADM이 정확히 그것이다.**
  두 논문 모두 이 연결을 짓지 않았습니다. NADM 3종이 전부 상관 기반이고 Anliker 2026이
  셋 다 우회했으니, 2020년의 예측이 2026년 CS에서 실현된 셈입니다. 방어 방향도 여기서 나옵니다.
  MTAC이 안전하다고 본 것은 상관이 아니라 분산 기반 판별이었고, V-Range가 5G-NR에서
  정확히 그것으로 거리 확대를 잡았습니다.
- **표준이 취약한가 구현이 취약한가라는 논쟁이 UWB에서 이미 벌어졌고 CS에서 반복된다.**
  Ghost Peak와 Luo 외(S&P 2024)가 상반된 결론으로 각각 4대 학회에 실렸습니다.
  CS 공격을 제안하면 받을 첫 반론이 이것이므로, 단일 수신기가 아니라 수신기 계열에 대해
  평가해야 합니다. Wieme 데이터셋으로 하드웨어 없이 가능합니다.

## 2026-07-28 (1차 서베이 실행)

프로시딩 목차 전수 훑기를 처음 제대로 돌렸습니다. 논문 27 → 32건, 4대 학회 8 → 11건.

신규 논문 5건

- **BLERP: BLE Re-Pairing Attacks and Defenses** (NDSS 2026, 관련도 높음) — 원문 대조 완료.
  표준 v6.1 재페어링에서 설계 취약점 6개(신규 4개)를 찾아 0-click/1-click으로 임퍼소네이션과
  MitM을 실증. 보안수준을 LSC + JustWorks까지 강등 가능. 22종 평가, CVE-2025-62235,
  nRF52840 + NimBLE 기반 공개 툴킷.
- Formal Analysis of BLE Secure Connection Pairing / PE Confusion Attack (NDSS 2026)
- One Tap to Hijack Them All: Google Fast Pair 보안 분석 (IEEE S&P 2026)
- The Zen of Bluetooth Security (WiSec 2026 기조)
- Vehicular Wireless Positioning: A Survey (arXiv 2601.20547)

표준 변경 2건

- IEEE 802.15.4ab: 초안 P802.15.4ab/D03(2025-09) 확인, 코어 기능 확정, 2026년 완료 예상.
  ST가 Narrowband Assist 통합 첫 칩 계열 출시. 기존 기록의 "진행 중"을 구체화.
- Bluetooth Core 6.3 Technical Overview 추가. CS 결과 데이터 최적화가 RAS/RAP 전달에
  미치는 영향이 여기 정리되어 있음.

신규 인사이트 1건

- **CS의 난수화는 페어링 키에 얹혀 있고, 그 페어링은 0-click으로 강등된다.**
  CS Security Start가 본딩 PK에서 sounding sequence와 마커 배치를 유도하므로, BLERP의
  보안수준 강등이 CS 난수의 예측 가능성에 영향을 주는지가 곧바로 연구 질문이 된다.
  물리계층 회로 없이 CS를 무너뜨리는 경로다.

계보 인사이트 갱신

- 이 분야가 두 계보로 갈려 있고 서로 인용하지 않는다는 것이 드러났다. 물리계층은
  Capkun 계보(ETH/CISPA), 페어링 계층은 Antonioli 계보(EURECOM). CS는 두 계층에 동시에
  걸쳐 있으므로 둘을 잇는 연구는 양쪽 모두에게 새롭다.

인프라

- 인용 관계 추출을 손으로 관리하던 제목 프로브 표에서 자동 생성으로 교체
  (`scripts/extract-cites.mjs`). 손으로 놓쳤던 인용 3건을 잡아 48 → 51건.
- `data/refs.bib` 생성 (`scripts/export-bib.mjs`).

접근 실패

- USENIX Security 채택논문 페이지가 403. dblp 경유도 목록이 잘려 확인 불가.
  다음 실행에서 다른 경로 필요.
- NDSS 2026의 PE Confusion과 S&P 2026의 Fast Pair는 원문 URL을 찾지 못해 미검증 상태.

다음 실행 우선순위

1. USENIX Security 2024~2026 프로시딩 전수 (이번에 못 함)
2. Wieme 2025(IEEE Access) 원문 대조 — 관련도 높음인데 아직 일부확인
3. MTAC(S&P 2020), V-Range(NDSS 2022) 원문 대조 — 방어 논증 언어의 근거

## 2026-07-28 (초기 구축)

- 코퍼스 구축: 논문 27건, 표준 16건, 인용 관계 48건, 인사이트 8건
- 보안 4대 학회 8건 (IEEE S&P 1, USENIX Security 3, ACM CCS 2, NDSS 2)
- 원문 대조 완료 6건

주요 발견

- Anliker et al. WiSec 2026이 Bluetooth CS의 RTT를 직접 겨냥해 최대 18 m 거리 축소를
  실증하고, CS 규격이 요구하는 NADM 지표 3종(NCC, PMSE, DFT)을 모두 우회했다.
  제목에 Bluetooth도 Channel Sounding도 없어 키워드 검색으로는 잡히지 않았다.
- 서베이 절차를 두 번 고쳤다. 키워드 검색 전에 학회 채택논문 목록을 전수로 훑도록 했고,
  WebFetch가 PDF를 파싱하지 못하는 문제를 `curl` + `pdftotext`로 우회하게 했다.
- CCS 2023 논문의 제목을 검색 스니펫에서 잘못 추정했던 것을 목차 대조로 정정했다.
  실제 제목은 "Protecting HRP UWB Ranging System Against Distance Reduction Attacks"
  (Joo, Lee, Jeong, Choi). 검증 플래그가 이 오류를 잡았다.
- 참고문헌 캐기로 UWB-ED(USENIX Security 2019) 등 검색에 안 걸린 3건을 발견했다.
