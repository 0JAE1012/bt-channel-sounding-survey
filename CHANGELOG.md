# 변경 기록

주간 서베이가 무엇을 바꿨는지 여기에 남깁니다. 최신이 위입니다.

## 2026-09-05 (26차: 신규 5건 — ED/LC·거리 바운딩 계보의 뿌리 Hancke–Kuhn 2005·2008 과 첫 무선 rapid-bit-exchange 구현 Tippenhauer WiSec'15 전문 편입, Kuhn WPNC'10·Lu JPCS'21 허브 문헌 partial 편입, 인용 56건 추가)

어제 25차 직후라 신규 발행분은 없었고(arXiv cs.CR/eess.SP RSS·pastweek 목록 무해당, Crossref 9-01 이후 등록분에서
관련 신규 없음 — "channel sounding" 질의는 Sounding Out! 팟캐스트 DOI 로 오염, S2 429·OpenAlex 검색 클러스터 정지),
캐시된 전문 89건의 참고문헌을 스크립트로 훑어 코퍼스에 없는 피인용 상위 문헌을 골랐습니다. 결과는 거리 바운딩 계보의
뿌리 — 코퍼스 20건이 인용하는 Hancke–Kuhn 2005 와 10건이 인용하는 Hancke–Kuhn 2008(late-commit 첫 실증) — 가
빠져 있었다는 것입니다. Kuhn 의 Cambridge 홈페이지와 Tippenhauer 의 scy-phy 서버에서 OA PDF 를 받았습니다.

- 신규 (전문 확인): **Attacks on Time-of-Flight Distance Bounding Channels** (Hancke·Kuhn, ACM WiSec 2008, 관련도
  **높음**, `verified`). Clulow 2006 의 late-commit 을 상용 수신기에 처음 구현 — Maxim MAX1471 433.92 MHz ASK/FSK
  수신기는 저역 데이터 필터 때문에 응답 시작 후 20–22 µs(6.6 km) 뒤에 값을 바꿔도 정상 복조, NXP MF RC531 ISO 14443A
  리더는 상관기 임계 전까지 2–2.5 µs(750 m). 수신기가 필터 차단 주파수(9.6/4.8 kHz) 이상의 15 kbit/s 데이터도 복조한다는
  관찰, 적분기 입력 V_m/2 유지 최적 전략, 13.56 MHz 반송파 +1/+2 MHz 오버클럭으로 토큰 응답 최대 15/30 µs 앞당김,
  HF RFID 전용 채널 3종(Munilla·Reid·Hancke–Kuhn UWB) 비교. Anliker 2026 이 "Clulow 의 긴 심볼 문제가 RFID/433 MHz
  [13] 등 공격의 기반" 이라고 계보에 넣은 문헌이라 relation extends(anliker-2026·olafsdottir-2017 → 이 논문) 추가.
- 신규 (전문 확인): **An RFID Distance Bounding Protocol** (Hancke·Kuhn, IEEE/CreateNet SecureComm 2005, 관련도
  보통, `verified`, tier other). "Hancke–Kuhn 구조" 의 원전 — nonce 로 R0·R1 을 미리 계산, 1 비트 챌린지에 비동기
  룩업 즉답, 추측 확률 3/4, n 중 k 판정의 pFA·pFR 식, 분해능 r ≈ c/B(ISO 14443A 300 kHz → km 급) 논증, 13.56 MHz
  반송파 영교차 + UWB BPM 펄스 채널 구상. 구현 없음(향후 과제 명시).
- 신규 (전문 확인): **UWB Rapid-Bit-Exchange System for Distance Bounding** (Tippenhauer·Luecken·Kuhn·Capkun, ACM
  WiSec 2015, 관련도 보통, `verified`, category defense). 무선 rapid-bit-exchange 첫 완전 구현 — Tekmicro Triton VXS-5
  ×2(Virtex-5 ×3, 2 GS/s ADC/DAC), Mini-Circuits 3.5–4 GHz 프런트엔드(부품 번호 전부 확보), 펄스 2 ns·적분창 4 ns·
  심볼 512 ns, prover 임계 경로 12 사이클 × 8 ns = 96 ns(Table 1 블록별 지연), 30–255 cm 16 지점 × 1,000 회 평균 오차
  10.9 cm·BER 2.72 %(Table 2 전체), 최대 거리 이득 악의적 prover 15.6 m·외부 공격자 1.2 m 산식, "distance commitment"
  (프리앰블 타이밍 = 거리 약속) 개념. cites 8건, relation implements → kuhn-2010·hancke-2005·poturalski-2011(EDD 4 ns 창),
  complementary → rasmussen-2010.
- 신규 (초록 + Tippenhauer 2015 의 2차 서술, `partial`): **UWB Impulse Radio Based Distance Bounding** (Kuhn·Luecken·
  Tippenhauer, WPNC 2010, 관련도 보통). 코퍼스 6건이 인용하는 처리지연 최소화 아날로그 UWB 트랜시버 구상 — 단일 IC 시
  δB ≤ 4 ns(distance fraud 3.6 m). 유료(Unpaywall·OpenAlex closed).
- 신규 (초록만, `partial`): **Indoor Positioning Experiment Based on Phase Ranging with BLE** (Lu·Yin·Zhao·Wei, J. Phys.:
  Conf. Ser. 1971, 2021, 관련도 낮음). Nikodem 2025·Sheikh 2023 이 인용하는 CS 이전 BLE 다중반송파 PBR 실측(Dialog
  DA14695). CC-BY OA 이지만 IOP 사이트가 Radware 봇 차단이고 Wayback 스냅샷 없음 — 전문 미확보.
- 인용: 56건 추가 (410 → 466). 캐시 전문의 정규화 제목 대조 + 저자명 확인으로 역방향 인용 46건(hancke-2005 18건,
  hancke-2008 10건, tippenhauer-2015 10건, kuhn-2010 6건, lu-2021 2건) 과 신규 노드의 정방향 10건.
- 보강: `partial` → `verified` 상향 없음. Nishikawa ICC'26·Andreadis IPIN'25·Rashidi IoT-J'25·Fujii ICST/GCCE'25·Boer
  VTC'20(TU/e 포털 403)·Stanciu MWSCAS'21(NXP, OA 없음)의 arXiv·기관 사본을 WebSearch 로 재확인했으나 전부 없음.
  기존 항목은 인용·관계 갱신(olafsdottir-2017·anliker-2026 relation 추가, 20건 last_checked)만.
- 표준: 변경 없음 — Bluetooth SIG 규격 목록에 6.3 이후 신규 없음(Inline PCT Transfer 는 여전히 VSr01_PR 초안), IEEE
  P802.15.4ab 는 SA 페이지상 Active PAR(PAR 2021-09-23) 유지, CCC 신규 릴리스 없음.
- 실패: Lu 2021 전문(IOP Radware 차단·Wayback 없음); Kuhn WPNC 2010 전문(유료); 부수 후보 "Bluetooth Signal Transient
  Start Detection Based on Fast AIC"(Franklin Open, 2026-08)는 Elsevier linkinghub 리다이렉트만 돌아와 초록 미확인 —
  ToA 검출인지 RF 지문인지 판단 불가라 미등재.

## 2026-09-04 (25차: 신규 2건 — CS 자세 오차 첫 실측 arXiv 신간 전문 편입 + Dialog BLE ToF 석사논문(TU/e) 편입, 보강 3건 — Schröder IPIN 2019·2018 을 저자 박사학위논문(LEOPARD OA, Wayback)으로 장비·수치 확정, Pelka 학위논문 확인, 인용 11건 추가)

어제 24차 직후라 신규 발행분은 arXiv 1건뿐이었고(cs.CR/eess.SP RSS·Crossref 9-01 이후 등록분·CCS 2026 accepted
papers·USENIX Sec '26 목차 재확인, NDSS 2027·S&P 2027 목록은 아직 없음, S2 는 여전히 429/500), 나머지는 계보와
우회 경로 발굴에 썼습니다. 새 경로 둘 — **DNB SRU API**(`services.dnb.de/sru/dnb?query=per="성, 이름"`)로 독일
박사학위논문의 OA URL 을 바로 찾을 수 있고, TU Braunschweig **LEOPARD** 리포지터리는 PDF 요청에 JS 작업증명
챌린지(`/pow-challenge`)를 걸지만 REST API(`/api/v1/objects/<id>/derivates/…/contents`)로 파일명을 알아낸 뒤
**Wayback `id_` 경로**로 원본을 받을 수 있었습니다. TU/e `pure.tue.nl` 의 기밀 해제된 석사논문도 열려 있습니다.

- 신규 (전문 확인): **IMU-Aided Correction of Orientation-Induced Ranging Error in Bluetooth Channel Sounding on
  Commercial Hardware** (Bapat·Nagaraj, arXiv 2609.00650, 2026-09-01, 관련도 **보통**, `verified`). Silicon Labs
  EFR32xG24 CS DK(BRD2606A, ICM-40627 IMU) 2 대, PBR + 이중 안테나 편파 다이버시티, 복도 9 거리 × 9 자세
  44,576 측정. 같은 0.61 m 에서 자세만 바꿔 MAE 9.3 → 44.6 cm(5 배), roll 축이 pitch 축보다 1.24 배 나쁨,
  roll left 90° 는 거리와 함께 발산. Random Forest 가 LOOO 에서 MAE 74.6 % 감소, LODO 는 16.1 %. 자연 자세 오차
  대역이 탐지 임계값 하한을 올린다는 점과 RF 밖 센서가 거리 판정에 개입하는 첫 CS 사례라는 점을 relevance_note 에
  적음. cites 10건(wieme·zand·gunia·nikodem·pnn·santra·wacsa·bintariq·vanmarter·suresh), relation implements →
  wieme-2025(Wieme 의 IMU 향후 과제 실행).
- 신규 (전문 확인): **Algorithms and Simulation set-up for realizing Bluetooth Low Energy based ranging**
  (Ramachandran, TU/e 석사논문 · Dialog Semiconductor, 2016, 관련도 보통, `verified`, tier `thesis`). CS 8 년 전
  Dialog DA14681 로 시도한 BLE ToF·2 주파 위상 거리측정의 실패 기록 — 비대칭 단일채널은 광고 간격 ≥100 ms 로
  클럭 보상 불가(ToF σ 50~60 ns), 대칭 단일채널은 σ 5~6 ns ≈ 2 m 이나 AGC 단계별 군지연 편차 30 ns 보정표 필요,
  2 채널 위상차는 프랙셔널-N PLL 의 채널별 임의 시작 위상으로 실측 붕괴(2.5~15 m 가 전부 9~11 m). CS 가
  마이크로초급 타이밍·양방향 교환·위상 연속성을 규격화한 이유의 하드웨어 실증이고, 수신 전력 의존 군지연은
  RTT 조작 가설의 근거. cites 1건(pelka-2014), relation extends → pelka-2014.
- 보강 (`partial` 유지, 장비·소프트웨어 verified·수치 전면 교체): **schroeder-2019-multipath-pbr** — 박사논문 4.3 절
  (저자가 "이 논문에 기반"이라고 명시)로 InPhase 노드(ATmega1284P + AT86RF233), 공원 화이트보드 반사면 + 30°
  Yagi-Uda, 플라자 테스트베드 10 노드·45 링크·90,000 측정(Leica 토탈스테이션 GT), LOS 24 / Multipath 48 / NLOS 18
  링크 분류, MP iCDE 임계식 t = γ + (DQI − γ)·β 와 격자 탐색 파라미터(97 백분위, β 0.37), Table 4.7~4.10 전체
  (전체 MAE 7.714 → 5.572 m, LOS 0.430 → 0.384, NLOS 26.4 → 21.6, Multipath 4.347 → 2.138), 허상 봉우리(25/55/70 m)
  의 AR 원리 설명, 최악 오차의 원인(동기화 프레임 유실)까지 확보. 논문 본문 PDF 자체와 참고문헌은 여전히
  미확보라 `verified` 로 올리지 않음.
- 보강 (`partial` 유지, 장비·소프트웨어 verified·수치 보완): **schroeder-2018-cde** — 박사논문 3.5·4.1 절로 INGA +
  AT86RF233, 레이저 거리계 GT(±1 mm), d_offset 1.09 m, 4 장면 환경 설명, CDE 정의식·B = 4096(잡음 σ 25.7 LSB
  시뮬레이션, 분해능 73.2 mm)·iCDE 512 빈, DQI Youden 임계 0.289, 폐기 측정 표(Table 4.2), 4 장면 표의 나머지
  칸(RDE/ESSR 최대값) 확보. 박사논문은 이 절을 TOSN 2022 기반으로 적고 있어 IPIN 2018 본문 고유 서술은 미확인.
- 보강 (메모): **pelka-2014-phase-multi-frequency** — DNB 로 찾은 저자 박사논문(Lübeck 2017, OA)은 이 논문을
  배경 인용만 하고 재수록하지 않음. Schröder 박사논문이 인용한 2 차 수치(PMU 잡음 σ 32.25 LSB, 무반향실 근거리
  실험, 언랩 + 선형회귀) 를 출처 표기해 추가.
- 인용: 11건 추가 (399 → 410). 신규 두 노드는 최신·비공개 문헌이라 역방향 인용 없음(캐시 전문 grep 확인).
- 표준: 변경 없음 — Bluetooth SIG 규격 목록에 신규 없음(6.3 이 최신), IEEE P802.15.4ab 는 여전히 Active PAR
  (SA 투표 진행), CCC 는 Digital Key 4 plugfest(2026-06) 이후 신규 릴리스 없음.
- 실패: Schröder IPIN 2019·2018 본문 PDF(유료, IBR 에 슬라이드만, LEOPARD 는 박사논문만); Pelka IPIN 2014
  본문(학위논문에 미수록); Sheikh VCC 2025·Xie TCOM 2026·Kumbul IPIN 2025 는 arXiv/기관 사본 없음; Boshoff TII
  2026 은 경로 없음. IBR(TU-BS) 서버는 오늘 복구됐지만 새 파일은 없음.

## 2026-09-03 (24차: 신규 3건 — 협대역 PBR 계보의 뿌리 InPhase 원형(INFOCOM'16) 전문 편입 + Pelka IPIN'14·Schröder IPIN'18 허브 문헌 편입, 보강 1건 — WCL 신간 초록 확보, 인용 25건 추가)

어제(23차) 직후라 신규 발행분은 없었고(arXiv cs.CR/eess.SP 신규 목록 무해당, Crossref 8-28 이후
등록분에서 관련 신규 없음, S2 는 여전히 429, arXiv API 는 빈 응답), 23차가 남긴 Gunia 참고문헌 계보
후보 3건을 처리했습니다. TU Braunschweig IBR 서버가 오늘 ECONNREFUSED 라 **Wayback Machine
보존본**(`web.archive.org/web/<ts>id_/<url>`)으로 PDF 를 받았고, IEEE Xplore 는 `rest/document/<arnumber>/abstract`
엔드포인트가 브라우저 UA 로 JSON 초록·소속·키워드를 주는 것을 확인해 유료 논문 3건의 초록을 채웠습니다.

- 신규 (전문 확인 1건): **No-Cost Distance Estimation Using Standard WSN Radios** (von Zengen·Schröder·
  Rottmann·Büsching·Wolf, IEEE INFOCOM 2016, 관련도 **보통**, `verified`, IBR OA 사본의 Wayback 보존본).
  InPhase 계보의 출발점 — AT86RF233 PMU + Active Reflector 를 Contiki 에 구현, 2400–2500 MHz 500 kHz
  스텝(d_max 150 m), 자기상관+FFT 의 PSD 봉우리로 거리·DQF. 네 환경 중앙값 오차 0.40 m(무필터)/0.30 m
  (DQF 임계 21) vs Atmel RTB 0.59/0.45 m; DQF 는 1 m 초과 오차 분류에서 민감도 0.79·특이도 0.83·PPV 0.94
  (Youden 0.62 vs RTB 0.33). "PMU 는 측정 신호와 다른 전파를 구별 못 한다"는 저자 명시가 receiver-policy
  축의 근거. cites 1건(Pelka), relation extends → pelka-2014.
- 신규 (초록만, `partial`): **Accurate radio distance estimation by phase measurements with multiple
  frequencies** (Pelka·Bollmeyer·Hellbrück, IPIN 2014, 관련도 보통). 코퍼스 11건이 인용하는 협대역
  다주파수 PBR 의 이론 뿌리 — PMU 분해능 → 정확도 요구조건 도출. 유료(ielx7 202), OA 없음.
- 신규 (초록 + 저자 슬라이드, `partial`): **Accurate and Precise Distance Estimation from Phase-based Ranging
  Data** (Schröder·Reimers·Wolf, IPIN 2018, 관련도 보통). CDE 알고리즘(복소 위상응답 FFT → 최대 봉우리 =
  거리, 높이 = DQI). Wayback 보존 슬라이드 표를 이미지로 읽어 4 장면 수치 확보 — 공원 CDE MAE 0.149 m·
  σ 0.104 m vs RDE 0.706/4.292(최소 −69 m) vs ESSR 2.555/19.653(최대 +283 m); 사무실 복도 CDE 0.550/0.738;
  잡음 하 FFT 4096 빈에서 MAE ~3 cm 바닥. relation extends → vonzengen-2016.
- 보강 (unverified → `partial`): **wang-2026-svt-ifft-music-ble** (IEEE WCL) — Xplore REST abstract 로
  초록·소속·키워드 확보: SVT 저계수 CFR 완성으로 빠진·왜곡 톤 복원 후 IFFT 안내 국소 탐색 + 실수값
  고유분해 MUSIC, 실측 BLE 다중경로에서 정확도 약 39.5 % 개선. sheikh-2023 "빠진 톤" 계보 확정.
- 인용: 25건 추가 (373 → 399) — 세 신규 노드로 향하는 역방향 인용을 전문 텍스트 참고문헌에서 대조
  (vanmarter-2023 은 학위논문 장 본문 [4] 사용 확인). relations 3건 추가(schroeder-2022 → 2016·2018,
  schroeder-2019 → 2018).
- 표준: 변경 없음.
- 실패: Boshoff TII 2026 은 Unpaywall closed·CityU Scholars 가 curl 도 403(Cloudflare) 으로 바뀜; IBR
  서버 다운으로 Schröder IPIN 2019·2018 본문은 여전히 미확보(Wayback 에는 슬라이드만); Pelka 2014 는
  TH Lübeck 에 PDF 없음.

## 2026-09-02 (23차: 신규 2건 — Gunia RSS 융합 후속작 전문 편입 + WCL 후보 unverified 등재, 보강 2건 — UTD 학위논문 재수록 장으로 UTD·TI 계보 전문 확인, 인용 12건 추가)

S2 API 는 오늘도 429, OpenAlex 검색은 "클러스터 복구 중"이라 둘 다 못 썼고, Crossref
`works?query.title=…&filter=from-created-date:2026-08-15` 로 대체해 IEEE 신간을 잡았습니다.
arXiv cs.CR/eess.SP 신규 목록, CCS 2026 accepted papers, USENIX Sec '26 목차(curl+UA)는 해당
없음(USENIX 의 PrivacyShield 는 BLE 비콘 릴레이지만 거리측정이 아니라 제외). 보강은 유료
IEEE 경로가 전부 막힌 상태에서 **저자 박사학위논문의 IEEE 재수록 장**이라는 새 우회로로 뚫었습니다.

- 신규 (전문 확인 1건): **Decimetre-Accurate Positioning Using Channel Sounding and UWB: Does RSS
  Still Play a Role?** (Gunia·Ellinger, IEEE Access 2026-08-24, 관련도 **보통**, `verified`,
  ielx8 경로). gunia-2026-cs-metrological 의 3층(칼만 융합·추적) 후속 — Table 2: UWB 단독 실내
  0.30 m → +Bluetooth RSS 0.26 m, 네 시스템 융합 0.23/0.72 m(평균/최대), RSS 융합으로 평균이
  나빠진 경우 없음. 여기서도 "CS" 는 AT86RF233 PBR 대용. RSS 가 위상·시간과 직교하는 독립
  정보라는 저자 논리는 수신기 판정 정책의 재료이고, 고정 R 의 칼만 추적은 단발 조작을 묻는
  대신 지속 조작에 무방비라는 점을 relevance_note 에 적음.
- 신규 (제목·서지만, `unverified`): **Accurate and Efficient BLE Ranging in Multipath Environments
  Using SVT-Based Channel Completion and IFFT-MUSIC** (Wang 외, Tongji, IEEE WCL Early Access
  2026-08-31, 관련도 보통 — 잠정). Xplore 페이지·REST metadata·Crossref·OpenAlex 어디서도 초록을
  못 얻어 배지가 붉게 남도록 등재. sheikh-2023 의 "빠진 톤" 계보로 추정.
- 보강 (partial → `verified` 2건): UT Dallas 리포지터리(DSpace REST API)에서 저자 박사학위논문을
  받아 "©IEEE Reprinted, with permission" 장으로 확인.
  - **vanmarter-2023-svr-ble-ranging** — 장비(75 ch × 1 MHz two-way CFR, 4×1/1×4/2×2, 주차장
    룸미러·도어핸들 + 실내 주거, 705 trial·14,100 측정), SVR 파라미터(ε = 4·10⁻⁴, C = 20, γ = 0.3,
    N = 30), 결과(룸미러 전체 RMSE MUSIC 1.681/0.749 m vs SVR 0.766/0.585 m, NLOS 편향 +1.203 →
    +0.116 m, 차 안 1.494 → 0.296 m), cites 5건, relation extends → shoudha-2022.
  - **bintariq-2024-dl-ble-ranging** — RLA-SepCNN 구조(필터 10-10-40-20, dropout 0.1), 744 trial·
    14,880 측정·J = 6 leave-one-environment-out, 결과(IE1 0.68/0.96 m vs SVR 0.98/1.43 m, IE2
    0.37/0.68 m, 실외 DH 0.51/0.74 m), cites 5건, relation extends → vanmarter-2023.
- 인용: 12건 추가 (361 → 373) — 학위논문 참고문헌은 전체 공용이라 장 본문에서 실제 인용된 번호만
  대조해 넣음.
- 표준: 변경 없음 — Core 6.3 최신, IPT 여전히 VSr01_PR Draft, 802.15.4ab Active PAR(2021-09-23
  승인, 미발행), CCC 3.0/4.x 그대로.
- 실패: partial 잔여 IEEE 18건 ielx8 재시도 전부 202 빈 응답(재확인, last_checked 만 갱신);
  Eriksson VNC 포스터는 Google 색인 iel8 직링크도 202·TUM 강좌 페이지(echord.info) 404; Andreadis
  IPIN 2025 는 dblp 상 closed; Schröder IPIN 2019 는 IBR 개인 페이지에 PDF 없음.
- 참고문헌 계보 후보 (Gunia 전문): Pelka 2014 IPIN "Accurate radio distance estimation by phase
  measurements with multiple frequencies", von Zengen 2016 INFOCOM "No-cost distance estimation
  using standard WSN radios", Schröder 2018 IPIN "Accurate and precise distance estimation from
  phase-based ranging data" — 비-Bluetooth PBR 계보(`other`), 다음 실행에서 판단.

## 2026-09-01 (22차: 신규 2건 — DB 이론 허브 문헌 편입, 인용 18건 추가)

어제(21차) 직후라 신규 발행분은 없었고(arXiv cs.CR/eess.SP 최신 목록 무해당,
S2 재조회도 신규 0), CityU Scholars 계보를 한 층 더 파서 두 건을 전문으로 편입했습니다.
CityU 포털 검색 페이지는 이제 Cloudflare 챌린지가 걸리지만, Google이 색인한
`portalfiles` 직링크는 여전히 curl+UA로 받힙니다.

- 신규 (전문 확인 2건):
  - **Persistent Distance Bounding for Mobile Provers** (Nkrow·Boshoff·Silva·Liu·Hancke,
    IEEE CNS 2024, 관련도 **보통**, `verified`). DB의 '순간 검증' 빈틈을 다룬 첫 논문 —
    CIR 특징 8종 지문(λ)으로 세션 중 경계 이탈을 감시하다 의심 시에만 재측距를 트리거
    (PiBiF). DWM1001 2대, 환경 1 민감도 1.0/특이도 최악 0.80. 경계 안 프록시(mafia/
    terrorist fraud)와 CIR 스푸핑은 못 잡는다고 저자가 명시 — receiver-policy 축 근거.
  - **Security of Distance-Bounding: A Survey** (Avoine 외 15인, ACM CSUR 2018, 관련도
    **보통**, `verified`, Oxford ORA 기탁본). 코퍼스 전문 확보 논문 12건이 인용하는 DB
    이론의 허브인데 코퍼스에 없어 인용 그래프에 구멍이 나 있었음. mafia/distance/terrorist
    fraud 통일 정의와 (1/2)^n vs (3/4)^n 성공확률 프레임의 표준 출처.
- 인용: 18건 추가 (343 → 361) — avoine-2018을 인용하는 기확보 전문 12건(aad-2026,
  abidin-2021, anliker-2023, bogner-2026, coppola-2024/2025, leu-2021, nkrow-2024-tof,
  secure-ranging-4z, singh-2021, tschirschnitz-2026, uwb-sv-2023) 전부 grep+저자명 대조로
  확정, 신규 2건의 cites 6건.
- 표준: 변경 없음 — SIG Inline PCT Transfer 여전히 Draft(VSr01_PR), 802.15.4ab 미발행,
  CCC·Core 6.3 기존 그대로.
- 실패: partial 잔여분 보강 시도 전패 — OpenAlex 재조회 11건 전부 closed(기존 메모리와
  일치), boshoff-2026(TII)은 CityU 미기탁·UPSpace 없음·TechRxiv 없음, xie-2026(TCOMM)은
  arXiv 판 없음(같은 그룹의 VAA 논문만 존재), vanmarter-2023은 TI 재직 저자라 기관
  리포지터리 없음, schroeder-2019는 TU-BS LeoPARD가 PoW 챌린지로 차단. 해당 8건
  `last_checked`만 갱신.

## 2026-08-31 (21차: 신규 9건 — 20차가 남긴 참고문헌 계보 후보 일괄 편입, 전문 5건 확인, qi 전문 확보로 초록 수치 반증)

20차 참고문헌에서 나온 계보 후보(UTD·TI / imec / JSI / NXP 군)를 이번에 팠습니다.
Crossref `link` → `ielx7/ielx8` + 브라우저 UA 경로가 **2022·2023년 골드 OA에도 통해서**
IEEE Access 4건의 전문을 바로 받았고(Shoudha 3.2 MB·Helwa 2 MB·Simončič 2025/2026),
CityU Scholars 포털은 WebFetch 403이지만 curl+UA로 열려 Nkrow CNS 2024 기탁 원고를
얻었습니다. S2 검색 API는 25초 백오프 6회에도 하루 종일 429라 이번엔 못 썼습니다.

- 신규 (전문 확인 5건):
  - **Reduced-Complexity Decimeter-Level Bluetooth Ranging in Multipath Environments**
    (Shoudha 외, UT Dallas·TI, IEEE Access 2022, 관련도 **보통**, `verified`). UTD·TI 계보
    시조격 — 차량 주차장 실측(도어핸들·룸미러, 0.84~7 m)에서 단일 안테나 MUSIC 1.53 m →
    다중안테나·희소 OMP 0.61~0.75 m. Burg 대역폭 외삽으로 80 MHz를 가상 확장하는 단계는
    "측정에 없는 대역을 모델로 지어내는" 추정기라 조작 민감도 질문거리. 장비 모델명은
    본문에 없음(TI 사사뿐).
  - **Bridging the Performance Gap Between Two-Way and One-Way CSI-Based 5 GHz WiFi
    Ranging** (Helwa 외, UT Dallas·TI, IEEE Access 2023, 관련도 **보통**, `verified`, tech
    `wifi`). two-way CFR 제곱이 망가뜨리는 것을 정량화(탭 2배·LoS 상대전력 1/4)하고
    제곱근+언래핑+deep fade π 보정으로 one-way에 1~10 cm 차까지 복원 — **±분기 선택이
    morano-2026의 분기 뒤집기 조작 지점과 동일 구조**임을 Wi-Fi 쪽에서 보여주는 교차
    자료. USRP 실측 LoS 중앙값 13 cm.
  - **Optimizing Frequency Switching Pattern to Reduce Asynchronization Effect in MCPD
    Ranging Systems** (Simončič 외, Jožef Stefan Inst., IEEE Access 2025, 관련도 **보통**,
    `verified`, tech `other`). 채널 순서 자체가 편향을 만든다 — 순차 호핑은 CFO·클럭
    오프셋 위상항이 거리 기울기와 같은 모양으로 쌓여 160캐리어 1.6 m, 구조적 재배열로
    2 cm 미만. **정확도 최적 패턴은 결정론적 순서라 CS의 무작위 호핑과 정면 상충**,
    BLE 호핑 알고리즘 #1의 비동기 한계는 81.2 ppm. AT86RF215 케이블 실측.
  - **Mitigating Frequency Dependent Carrier Frequency Offset in MCPD Ranging Through
    Timing Diagram Design** (Simončič 외, IEEE Access 2026-02-16, 관련도 **높음**,
    `verified`, tech `other`). PLL 합성에서 CFO가 반송파 주파수에 선형 비례(4대 실측
    확인)하고, 두 기기의 CFO 기울기 차(CFOSD)가 **거리 기울기와 구별 불가능한 편향**
    (10 Hz/MHz·ΔTo 120 µs → 약 18 cm)을 만든다는 모델. M=76·1 MHz 구성을 BLE CS와
    일치한다고 명시. 완화책(시간차 보정·역할 교대)은 전부 CS 표준에 없는 타이밍
    재설계라 현행 CS는 노출 — 클럭 특성 조작만으로 예측 가능한 편향을 넣는 경로의
    물리적 근거.
  - **Building ToF Resiliency Into UWB-Based Secure Distance Bounding Protocols**
    (Nkrow·Boshoff·Silva·Liu·Hancke, CityU, IEEE CNS 2024, 관련도 **보통**, `verified`).
    NLOS가 ToF를 부풀려 정직한 prover가 거부되는 FRR 문제에 CIR 특징 기반 LOS/NLOS
    분류·보정을 제안하고, **보정 자체가 새 공격면임을 스스로 실증** — 4 m LOS 공격자가
    저장한 2 m NLOS CIR 재생으로 근거리 수락(위조 CIR Pearson 0.90), 오토인코더 탐지
    FAR 최악 28%. CS의 NADM·ML 보정 논의에 그대로 이식되는 구도. DWM1001 × 2,
    1~15 m × 500회. boshoff-2026 TII 서베이와 같은 그룹.
- 신규 (초록만, `partial` 4건): **Support Vector Regression for Bluetooth Ranging**
  (Van Marter 외, IoT-J 2023, 보통 — 코퍼스 5편이 인용하는 ML 보정 허브, ielam AAM
  경로는 HTML만 반환); **Performance of High-Accuracy Phase-Based Ranging in Multipath
  Environments** (Boer 외, imec, VTC2020-Spring, 보통 — 코퍼스 8편이 인용하는 one-way
  재구성 원류, ielx7 0바이트·Unpaywall closed); **Accurate Distance Measurement Using
  Narrowband Systems** (Stanciu 외, NXP, MWSCAS 2021, 보통 — 초록에 relay attack
  prevention을 응용으로 명시한 벤더 논증의 이른 사례, wu-2026·nikodem-2025가 인용);
  **Reduced Complexity Deep Learning Approach for Bluetooth Ranging** (Bin Tariq 외,
  Sensors J. 2024, 낮음 — DL 보정의 일반화·임베디드 비용 한계를 벤더 계보 스스로
  명시, morano-2026·schex-2026이 인용).
- 보강: **qi-2026-cs-hadm-iot** `partial` → `verified` — Unpaywall에서 bronze OA 발견,
  전문 60 KB 확보. **초록의 LOS ±1~3 cm 주장은 지면 어디에서도 수치로 뒷받침되지
  않음을 확정**: 본문 유일의 정량 그림이 자유공간 RMSE 0.5~1.2 m·실내 1~3 m로 두
  자릿수 차이, 표 1은 ±5~10 cm로 자기모순, 기술 사실 오류 다수(BLE 79채널, BLE SoC의
  FiRa/802.15.4z 인증, nRF54H20에 NCS 2.0.0). 수치 인용 금지 판단을 전문 확인으로 확정.
- 인용: 신규 전문 6편의 참고문헌에서 22건 + 역방향(기존 11편 → 신규 5편) 21건으로
  총 300 → 343건. 전부 원문 참고문헌 대조. 역방향은 기존 캐시 전문 grep 후 참고문헌
  항목 원문 확인.
- 표준: 변경 없음 — arXiv 최근 목록(cs.CR 해당 없음, eess.SP는 D-MIMO 측위뿐)·NDSS
  2027 목차 미공개. 뉴스로는 Silicon Labs BG2B(코인셀용 CS SoC, 2026-08-04 발표)가
  눈에 띄나 표준 문서가 아니라 미등재.
- 실패: Van Marter IoT-J·Boer VTC·Stanciu MWSCAS·Bin Tariq Sensors J. 전문 — IEEE 유료
  (ielx 0바이트/202, Unpaywall·OpenAlex closed). Boshoff TII 서베이 — CityU Scholars에
  항목 페이지는 있으나 파일 미기탁, 다음 실행에서 재확인. S2 API 하루 종일 429.
- 주의: Simončič 2026의 정식 제목은 "… Through Timing Diagram Design"까지. Nkrow는
  IoT-J가 아니라 CNS 2024 학회 논문(5인 저자, Zhe Liu 포함).

## 2026-08-30 (20차: 신규 16건 — Semantic Scholar API 로 IEEE 저널·학회의 CS 논문 무더기 발굴, 전문 6건 확보)

이번 실행의 소득은 접근 경로 하나입니다. 지금까지 WebSearch·arXiv 로는 안 잡히던
**IEEE Xplore 쪽 CS/PBR 논문이 Semantic Scholar 검색 API(`/graph/v1/paper/search`,
`year=2025-2026`)로 한 번에 20 건 넘게 나왔습니다.** arXiv API 는 연속 호출에 429 를
뱉어 이번엔 못 썼고(6 초 간격으로도 막힘), S2 도 초당 1 회 이상이면 429 지만 `/paper/batch`
로 초록을 한 번에 받으면 됩니다. 두 번째 소득: **IEEE Access·OJVT 같은 골드 OA 논문은
Crossref 의 `link` 필드가 주는 `ielx8/.../NNNN.pdf?arnumber=NNNN` 경로를 브라우저 UA 로
받으면 전문이 열립니다**(`stamp.jsp`·`document/` 는 여전히 202 빈 응답). 유료 논문은
같은 경로로도 202. 이 두 경로는 메모리에 남겼습니다.

- 신규 (전문 확인 6건):
  - **A Novel Method for Two-Way Ranging to Mitigate Phase Offset in Bluetooth Channel
    Sounding** (Wu·Gunia·Figueroa·Ellinger, Metirionic·TU Dresden, IEEE Access 2026-08-14,
    관련도 **높음**, `verified`). 한 톤 교환 안에서 송수신 순서를 뒤집은 Mirrored Tone
    Exchange 를 정규 교환과 4 회 짝지어 발진기 오프셋 잔류항을 p(k+1) 스케일에서 Δp
    스케일로 떨어뜨림(cm → µm). 대가로 비모호 거리 150 → 75 m, 이를 기존 TWR 의 거친
    창으로 푸는 하이브리드 — **'거친 창 → 정밀값' 구조는 창만 밀면 정밀값이 따라오는
    공격 패턴**. Dialog DA14699 DK + RIGOL DG4162 외부 클럭으로 ±20 ppm 스윕, 케이블
    0.12 → 0.02 m, 실내 σ 0.14 → 0.11 m, 총 에너지 무반향실 −89 % / 실내 +32 %.
  - **Interference Mitigation in One-Way Channel Reconstruction for Robust Phase-Based
    Ranging** (Morano 외, Jožef Stefan Inst., IEEE Access 2026, 관련도 **높음**, `verified`,
    tech `other`). 양방향 CFR 은 채널의 제곱이라 탭이 L(L+1)/2 개로 불고 제곱근의 ±1
    분기를 골라야 하는데, 간섭 톤 하나가 위상 언래핑을 뒤집어 8 m 이상 오차를 낸다는
    관찰이 핵심 — **톤 한두 개만 덮어써서 분기를 뒤집는 저비용 조작 벡터**의 근거.
    AT86RF215 TSCH 회의실 실측(SIR −3 dB) 에서 제안 CR-BS 적중률 99.8 % vs 언래핑 84.5 %.
    정렬 보정 τ − T0/2 규칙은 긴 지연을 짧은 거리로 접는 경로.
  - **Digital-Only Phase Compensation for Secure Phase-Based Ranging in Vehicular RKE
    Systems** (Nishikawa·Otaka·Seto·Otsuki, Keio·Toshiba, IEEE OJVT 2026-08-05, 관련도
    **보통**, `verified`, tech `other`). 920 MHz 사설 RKE 라디오. 송수신 홉마다 깨지는
    fractional-N PLL 초기 위상을 ΣΔ 1 단 적분기 복제로 디지털 보상(RTL 시뮬레이션
    ±0.27° ≈ ±1.6 cm). 보안 논증은 "정확한 거리 + 임계값" 그대로이고 olafsdottir-2017·
    staat-2022 미인용 — 산업계 PBR 이 여전히 증폭 릴레이만 위협모델로 삼는 사례.
  - **Experimental Evaluation of Multicarrier Phase Difference Localization in Bluetooth
    Low Energy** (Nikodem 외, Wrocław·ULPGC, IEEE Sensors J. 25(1) 2025, 관련도 **보통**,
    `verified`, ULPGC 리포지터리 저자판). nRF52840 DK × 5 + NDML, 100 m² 사무실 4 앵커 ×
    101 지점 × 100 회. IFFT 거리 MAE 앵커별 0.59~1.02 m, 95 백분위 1.62~2.79 m, 앵커별 편향
    0.09~1.44 m; 측위 0.98 m 가 AoA 1.26 m 를 앞섬. **가장 가까운 앵커 3 개만 쓰면 IFFT 가
    25~30 % 나빠짐** — gunia-2026 의 최단거리 채택 권고와 정면 충돌하는 실측. 벽 반사
    1·2 회의 0.9 / 3.3 m 이봉 히스토그램. schex-2026·wieme-2025 가 이미 인용하던 논문.
  - **Exploration of Device-Free Sensing Ability Based on Bluetooth 6.0 Channel Sounding**
    (Wang·Cao·Gong·Chang, HKUST-GZ, UbiComp Companion 2025, 관련도 **보통**, `verified`).
    nRF54L15 + SDK 2.9.1 에서 서브이벤트별 local/peer I/Q 를 꺼내는 절차가 그대로 있고,
    **2·3 m RF 케이블 직결 시 16 채널 위상 변동 ±0.05 rad 이내** — 케이블 실험의 정상
    위상 잡음 바닥값. seo-2026 이 인용. 거리 오차 수치는 없음.
  - **SoK: Stealing Cars Since Remote Keyless Entry Introduction and How to Defend From
    It** (Bianchi·Brighente·Pavan·Conti, Padova, USENIX VehicleSec 2025, 관련도 **보통**,
    `verified`). 공격 35 건·방어 13 건 체계화. 릴레이 대응 6 건이 전부 비용 N/A, 15 년간
    공격 유형 불변. **CS·위상 거리측정·distance bounding 형식 프로토콜을 전혀 안 다룸**
    ('channel sounding'·'phase' 0 회) — 그 빈칸이 내 서베이의 기여 여지.
- 신규 (초록만, `partial` 10건): **Secure and Reliable Indoor Ranging: An Analysis of
  Industry Protocols, Attacks, and Defences** (Boshoff·Nkrow·Silva·Hancke, IEEE TII 22(8)
  2026-08, 관련도 **높음** — Bluetooth·UWB·Wi-Fi 보안 거리측정만 다루는 첫 서베이라
  주장, 내 코퍼스의 대조군·신규성 검사 대상. CityU·THEi 리포지터리·arXiv 에 없음);
  **Multipath ToA Estimation for BLE Ranging With Binary Phase Ambiguity** (Xie 외, IEEE
  TCOM 74, 보통 — xie-2026-vaa 의 모체, 원자 노름 + 헝가리안 + MaxCut SDP); **RANSAC-
  Integrated Root-MUSIC for BLE CS** (Nie 외, IWSA 2025, 보통 — MVDR 대비 PE90 −74 %);
  **Simulation Study on PBR for Dual-Antenna CS** (Fujii 외, ICST 2025, 보통 — NLoS 첫 경로
  오검출 2.0 %); **Experimental Study on Improving PBR Accuracy Indoors** (Fujii 외, GCCE
  2025, 보통 — 중앙값 0.35 m, 잠정 거리 게이팅 구조); **Indoor Localization with BLE
  Utilizing Different Ranging Methods** (Kumbul·Sheikh·Dolmans, imec, IPIN 2025, 보통 —
  측위 오차 12 cm 이내); **Robust Phase-based BLE Localization with a Single Multi-Antenna
  Receiver and ML** (Andreadis 외, IPIN 2025, 낮음); **Comprehensive Study of Indoor
  Positioning Methods in BLE and UWB** (Rashidi·Chinara, IEEE IoT-J 2025, 낮음 —
  droemmer-2026 이 인용); **High Accuracy Distance Measurements Method with Channel
  Sounding for IoT** (Qi 외, Journal of Computers 2026, 낮음 — LOS ±1~3 cm 주장은 코퍼스
  실측과 어긋나 검증 전 인용 금지); **Low-Overhead PBR for Sub-GHz Systems Using
  Fractional-N PLL** (Nishikawa 외, ICC 2026, 낮음 — OJVT 판의 학회판, 계보 연결용).
- 인용: 전문 6 편의 참고문헌에서 코퍼스 내 인용 22 건 + 역방향 4 건(schex-2026·
  wieme-2025 → nikodem-2025, seo-2026 → wang-2025, droemmer-2026 → rashidi-2025) 으로
  총 274 → 300 건. 전부 `grep -a` 로 원문 확인. 참고문헌에서 코퍼스에 없는 계보 후보:
  Boer·Romme·Govers·Dolmans "Performance of High-Accuracy Phase-Based Ranging in Multipath
  Environments" (VTC 2020, 세 편이 인용), Shoudha 외 "Reduced-complexity decimeter-level
  Bluetooth ranging in multipath environments" (IEEE Access 2022, 골드 OA, TI·UT Dallas),
  Van Marter 외 SVR Bluetooth ranging (IoT-J 2023), Simončič 외 "Optimizing frequency
  switching pattern … MCPD" (IEEE Access 2025, OA), Helwa 외 two-way/one-way CSI Wi-Fi
  ranging (IEEE Access 2023, CR-PU 기준선), Pelka 2014 IPIN. 다음 실행에서 OA 인 것부터.
- 보강: 없음 — 기존 `partial` 7 건은 메모리대로 재시도하지 않았고, 이번 신규 전문 6 건이
  보강 몫을 대신함. 기존 항목은 인용 추가로 `last_checked` 만 갱신(4 건).
- 표준: **CCC Digital Key** — 사양 다운로드 페이지가 V3.1.4 와 V4.1.0 을 제공(신청 필요),
  2026-06 Plugfest #18 에서 Version 4 시험 진행. 항목 제목·날짜·요약 갱신. Core 6.4 미공개,
  Inline PCT Transfer 페이지 여전히 VSr01_PR 공개검토 초안, IEEE P802.15.4ab 여전히 Active
  PAR(초안 번호·완료일 미표시). 변경 없음.
- 실패: TII 서베이(Boshoff)·TCOM(Xie)·IWSA·ICST·GCCE·IPIN × 2·IoT-J·ICC 전문 — IEEE 유료
  (`ielx8` 경로 202). 목차 훑기는 같은 날 19 차에서 끝냈으므로 arXiv `pastweek` 목록만
  다시 봄(cs.CR 해당 없음, eess.SP 는 D-MIMO·서브 THz 측위뿐). arXiv API 429.
- 주의: Nikodem 논문의 원 제목은 "Multi-Carrier" 표기이나 IEEE 게재 제목(Multicarrier) 을
  따름. SoK 는 arXiv 판에 4 번째 저자 Edoardo Pavan 이 있어 S2 메타데이터(3 인) 와 다름.

## 2026-08-30 (19차: 신규 6건 — USENIX Security '26 목차 드디어 확보, 참고문헌 캐기로 계보 2건 편입)

이번 실행의 소득은 접근 경로 둘입니다. 첫째, 지난 세 차례 403 이던 **USENIX Security '26
technical sessions 페이지가 브라우저 User-Agent 를 붙인 `curl` 로는 열립니다**(1.4 MB).
WebFetch 는 여전히 403 이므로 다음 실행부터는 curl 로 받아 키워드 필터를 돌릴 것.
전수 확인 결과 거리측정 관련 신규는 없었고(BLE Theft Auto 는 이미 등재, PrivacyShield 는
추적 방지용 비콘 릴레이라 범위 밖), CCS 2025·WiSec 2026 목차(dblp)도 마찬가지였습니다.
둘째, 새로 확보한 전문의 참고문헌에서 코퍼스에 없던 계보 논문 2 건을 찾았습니다 —
staat-2022 의 전사인 escar 2020 논문(RUB 리포지터리에 공개)과 zand-2019 의 자매 논문
PIMRC 2019(유료). 후자는 이미 코퍼스의 3 편(schex-2026·suresh-2025-cs·schroeder-2022)이
인용하고 있었는데 빠져 있었습니다.

- 신규: **Securing Phone as a Key Against Relay Attacks** (Staat·Jansen·Zenger·Paar,
  escar Europe 2020, 관련도 **보통**, `verified`). staat-2022-analog-relay 의 저자가 2 년 전
  방어 쪽에서 쓴 제안 논문. BLE 반송파 위상 거리측정에 대한 릴레이 공격자가 넘어야 할 네
  관문(저지연 양방향 전달·물리계층 일관성·위상 조작·호핑 아래 동기화)을 나열하고 "이를
  동시에 실시간으로 만족하기는 매우 어렵다"고 썼는데, 같은 저자가 2022 년에 아날로그
  릴레이로 스스로 반증했습니다. 채널 상호성 + RF 지문의 하이브리드 IDS 제안은 NADM 의
  전신 격. 평가 실험은 없음.
- 신규: **Mitigating Relay Attacks in Vehicle Access Systems Using BLE and UWB**
  (Suresh·Joshi·Parandkar, ETASR 15(5), 2025-10, 관련도 **보통**, `verified`).
  suresh-2025-cs-vehicle-access 와 같은 저자진의 UWB 판. BLE 는 인증과 RSSI 트리거(≈2 m)만,
  거리 판정은 UWB — Lock 1.6 m / Unlock 0.5 m / 사이는 no-care zone 이라는 **실제 판정
  정책값**이 기록돼 있고, "UWB 가 켜지기 전 구간이 릴레이에 노출된다"고 저자가 인정합니다.
  릴레이 공격 실증도 UWB 정확도 수치도 없어 산업계 논증의 전형으로 대조 자료.
- 신규: **RadioRange: An Open-Source Digital Twin-based Ranging Simulator for UWB, Wi-Fi,
  and 5G** (Lyu·Chen·Hsu·Zhang, PolyU, arXiv 2606.23708, 관련도 **보통**, `verified`).
  Sionna 레이트레이싱 위에 하드웨어 비이상성 11 종을 토글로 주입하는 공개 시뮬레이터.
  **공격 없이 결함만으로** 첫 경로 검출이 얼마나 흔들리는지의 기준값 — 11 종 중 8 종은
  DSP 가 1% 미만으로 누르고 I/Q 불일치·ADC 지터·ADC 양자화만 유의미, 전부 켜면 UWB −28.6%
  / Wi-Fi −23.0% / 5G −9.1%. I/Q 불일치가 만드는 거울상 유령 경로는 Ghost Peak 과 구분해야
  할 자연 봉우리. 첫 경로 검출기 5 종 비교표와 코드(GitHub) 공개, QM33120WDK1 실측 검증.
- 신규: **Learning-Based Phase Estimation for Multi-Frequency Carrier Phase Ranging under
  Structured Multipath Conditions** (Bonczyk·Nikonowicz·Matuszewski, Poznan UT, arXiv
  2606.11332 v2, 관련도 **보통**, `verified`). 5G PRS 다중 부반송파 위상차 거리측정에서
  3GPP 채널의 결정론적 다중경로가 위상 분포를 비대칭·다봉으로 만들어 원형 평균이
  체계적으로 편향됨을 QuaDRiGa 로 정량화. UMi 에서 MAE 0.034 vs 0.067 rad(절반),
  InF 최악 조건 2.61 → 1.85 m. CS 의 PCT 위상을 원형 평균으로 뭉개는 파이프라인의
  정상 상태 꼬리를 먼저 알아야 탐지 임계값을 정할 수 있다는 근거. 시뮬레이션 전용.
- 신규: **Performance comparison of 802.11mc and 802.11az Wi-Fi Fine Time Measurement
  protocols** (Rajendran 외, Arista, arXiv 2511.17935, 관련도 **낮음**, `verified`).
  비교군 기준값용. 무보정 응답기가 6 m 를 20/40/80 MHz 에서 71.9/47.9/66.1 m 로 보고하고
  보정 후에도 11.0/7.5/6.4 m — 1 ns ≈ 0.3 m 가 상용 장비에서 어떻게 나타나는지의 실례.
- 신규: **A high-accuracy concurrent phase-based ranging for large-scale dense BLE network**
  (Zand·Duzen·Romme·Govers·Bachmann·Philips, imec, PIMRC 2019, 관련도 **보통**, `partial`).
  일대일 PBR 을 그룹 랑잉으로 확장(소요 시간 ≈ n−1 배 단축), COD 보정, 연결형·비연결형
  링크 계층 결합 제안 — schex-2026 PAwR 연결 없는 CS 의 직접 선행. 유료 벽이라 초록만.
- 인용: 신규 5 편의 참고문헌에서 코퍼스 내 인용 10 건 추가(총 274 건). staat-2020 →
  clulow-2006·francillon-2011·joo-2020·olafsdottir-2017, suresh-2025-ble-uwb → olafsdottir-2017·
  staat-2020·suresh-2025-cs, 그리고 schex-2026·suresh-2025-cs·schroeder-2022 → zand-2019-concurrent.
  **주의**: `scripts/extract-cites.mjs` 를 그대로 돌리면 부제 앞 머리제목이 흔한 구("Channel
  Sounding:", "BLE phase-based ranging:", "BLE Channel Sounding:")인 논문 3 편이 10 여 곳에
  오탐으로 붙고, 18 차에서 손으로 잡은 20 건이 다시 사라집니다. 이번에는 직전 상태를
  복원한 뒤 원문 grep 으로 확인한 것만 더했습니다. 스크립트 수정은 사람 판단 사항으로 남김.
- 보강: 없음. 유료 `partial` 7 건(WCNC·PIMRC·Sensors Letters·VNC·ICASSP·WASA·VCC)을
  OpenAlex·Semantic Scholar 로 다시 조회했으나 **전부 closed**, TU/e 리포지터리에도 파일
  없음, ResearchGate 는 403. 캐시 전문이 있는 `software_verified: false` 항목 4 건은 원문에
  툴 이름이 정말 없는 것이라 올릴 수 없음.
- 표준: 변경 없음. Core 6.4 미공개(6.3 이 최신), IEEE P802.15.4ab 는 여전히 Active PAR,
  Channel Sounding Inline PCT Transfer 는 아직 VSr01_PR 공개검토 초안. bluetooth.com 규격
  목록 페이지는 로그인 리다이렉트라 자동 확인 불가.
- 실패: WiSec 2026 공식 accepted 페이지 404(dblp 로 대체), CCS 2026 accepted 미공개,
  S&P 2026·NDSS 2026 은 신규 없음. arXiv 검색 UI 는 정상.

## 2026-08-27 (18차: 신규 2건, 보강 1건 — 발표 슬라이드로 유료 논문 우회, 인용 20건 보강)

이번 실행의 소득은 두 가지 우회 경로입니다. 첫째, **IEEE 유료 논문이라도 저자가
학회 발표 슬라이드를 기관 페이지에 올려둔 경우가 있습니다.** `schroeder-2019` 는
전문 접근이 계속 막혔지만 TU Braunschweig IBR 의 InPhase 프로젝트 페이지에
IPIN 2019 발표 슬라이드(30 MB)가 그대로 공개돼 있었고, 여기서 장비명·실험 규모·
오차 표를 모두 얻었습니다. 다만 슬라이드 PDF 는 폰트 서브셋 때문에 `pdftotext` 가
**숫자를 통째로 버립니다** — PyMuPDF 의 `get_text()` 로 페이지별로 뽑아야 수치가
나옵니다. 다음 실행에서 슬라이드를 만나면 이 함정을 먼저 기억할 것.
둘째, 캐시된 전문 56 건을 코퍼스 제목 전체와 정규화 대조해 **누락된 인용 20 건**을
찾았습니다. 신규 논문을 넣을 때마다 이 스캔을 돌려야 그래프에 고립 노드가 안 생깁니다.

- 신규: **Smartphones with UWB: Evaluating the Accuracy and Reliability of UWB Ranging**
  (Heinrich·Krollmann·Putz·Hollick, TU Darmstadt SEEMOO, arXiv 2303.11220, 2023,
  관련도 **보통**, `verified`). 이미 코퍼스의 `seo-2026` 과 `aad-2026` 이 인용하고
  있던 논문인데 빠져 있었습니다. 핵심은 **공격자가 없어도 상용 기기가 수 m 짜리
  음의 이상치를 낸다**는 실측입니다 — 실제 5 m 지점에서 보고된 거리가 0 m ~ 7.79 m,
  간섭 없는 옥외에서도 −3 m, Samsung 은 실험실에서 반복적으로 0 m. 무보정 RMSE 는
  DW3000 16.03 cm / Pixel 14.98 cm / S21 Ultra 15.65 cm / iPhone 17.68 cm 로
  제조사 광고치 ±10 cm 를 재현하지 못합니다. 저자들의 네 가지 수신기 권고
  (DS-TWR, 10~15 회 슬라이딩 윈도 평균, 음수값 폐기, **음수값 빈발을 공격 신호로
  카운트**)는 CS 의 판정 정책 설계에 그대로 옮길 수 있습니다.
- 신규: **Multipath Error Correction in Radio Interferometric Positioning Systems**
  (Zhang·Qi·Wei·Chang·Zhao, arXiv 1702.07624, 2017, 관련도 **보통**, `verified`).
  2.4 GHz 협대역에서 **위상만 쓰던 관행을 깨고 진폭으로 다중경로 프로파일을 추정해
  위상 오차를 되돌립니다.** CS 의 PCT 는 톤마다 I/Q 를 주므로 진폭을 이미 갖고 있는데
  대부분의 파이프라인이 위상 기울기나 IFFT 봉우리만 봅니다. 시뮬레이션에서 q-range
  75 m 기준 중앙값 0.33 → 0.05 m, 95 백분위 7.4 → 0.38 m 로 꼬리가 20 배 줄었고,
  경로 지연차가 10 ns 를 넘어야 잘 듣습니다(실내 근거리 CS 가 정확히 그 아래 영역).
  보안 쪽 함의가 더 큽니다 — 진폭과 위상이 함께 일관해야 한다면 **위상만 조작하는
  공격자는 진폭 프로파일과의 불일치를 남긴다**는 탐지 가설이 여기서 나옵니다.
- 보강: **Investigation of Multipath Effects on Phase-based Ranging** (schroeder-2019)
  — 저자 IPIN 2019 발표 슬라이드로 `hardware`(PMU 를 가진 AT86RF233, 2400~2500 MHz,
  통제실험 직접 10 m + 반사 40 m 각 1000 회, 실환경 노드 10 대 × 링크 9 × 1000 회
  ≈ 9만 측정), `results`(Multipath 조건 MAE 4.347 → 2.138 m, 중앙값 1.863 → 0.524 m,
  표준편차 6.518 → 3.834 m), `limitations` 를 채우고 `hardware_verified: true`.
  **가장 쓸모 있는 발견은 부록 표의 최악값입니다** — 51% 개선 뒤에도 오차 범위가
  iCDE −8.576~155.616 m, MP iCDE −10.108~152.760 m 로 거의 그대로입니다. 자연
  다중경로의 극단 이상치가 공격이 만드는 이상치와 같은 크기 대역에 있다는 뜻이라,
  임계값 기반 탐지의 상한을 이 숫자가 직접 정합니다. 본문은 여전히 미확보라
  `verification` 은 `partial` 유지.
- 인용: 캐시 전문 대조로 **20 건 추가**. `leu-2022-ghost-peak` → singh-2021·flury-2010,
  `wieme-2025` → zand-2019·sheikh-2023, `anliker-2026` → leu-2021,
  `ranganathan-2012` 를 인용하던 4 편(singh-2019-uwb-pr·leu-2020-mtac·singh-2022-v-range·
  coppola-2025), `seo-2026`·`aad-2026` → heinrich-2023 등. 총 인용 264 건.
- 표준: 변경 없음. Bluetooth Core 6.3(2026-05-06)은 이미 등재돼 있고 신규 릴리스 없음.
- 실패: 유료 벽에 막힌 `partial` 6 건은 이번에도 뚫지 못했습니다 — Unpaywall 로
  DOI 7 건을 일괄 조회했으나 **전부 `is_oa: false`** 였습니다(IPIN·WCNC·Sensors
  Letters·VNC·ICASSP·WASA·VCC). 학회 목차 훑기도 소득 없음: NDSS 2027 accepted 페이지는
  2017 년 목록으로 리다이렉트되고, CCS 2026 은 accepted 목록이 아직 공개 전이며,
  USENIX Security 26 technical sessions 는 403 입니다. arXiv API 는 레이트 제한에
  걸려 검색 UI(`/search/`)로 대체했습니다. `arxiv:2010.10387`(UWB distance bounding
  복조 기법)은 **저자가 철회한 논문**이라 후보에서 제외했습니다.

## 2026-08-26 (17차: 신규 4건, 보강 2건 — 협대역 PBR 계보를 통째로 편입, 인용 오탐 12건 제거)

이번 실행에서 두 가지가 열렸습니다. 첫째, **IEEE Xplore 의 OA 논문**은
`stampPDF/getPDF.jsp?arnumber=<번호>` 에 브라우저 UA 를 붙이면 그대로 받아집니다 —
IEEE Access 는 CC BY 이므로 이 경로가 통하고, 유료 논문(WCNC·VNC·ICASSP·Sensors
Letters·VCC)은 여전히 0바이트입니다. 이걸로 `gunia-2026` 전문을 확보했습니다.
둘째, ACM DL 은 **UA 만으로는 부족하고 `sec-ch-ua`·`Sec-Fetch-*` 를 포함한 전체
브라우저 헤더 세트**가 있어야 Cloudflare 챌린지를 넘습니다(14차의 쿠키 예열만으로는
오늘 막혔습니다). 이 경로로 TU Braunschweig 의 InPhase 논문을 받았고, 거기서
**협대역 2.4 GHz PBR 계보** 세 편이 한꺼번에 들어왔습니다.

- 신규: **InPhase: Phase-based Ranging and Localization** (Schröder·Wolf, ACM TOSN
  18(2) Art.24, 2022, 관련도 **높음**, `verified`). CS 의 PBR 과 같은 물리를 쓰면서
  획득 절차·거리계산 알고리즘·품질지표까지 전부 공개된 시스템입니다. 칩(AT86RF233)과
  코드(GitHub 2개)가 공개돼 있어 **CS 칩 없이 시작할 수 있는 대조군**이 됩니다.
  보안 관점에서 두 대목이 바로 쓰입니다 — (1) 측정마다 **DQI** 를 내고 Youden 지수로
  임계값(CDE 0.289)을 정해 이상치를 버리는 구체적 판정 규칙이 있고, (2) 다중경로에서
  **거리가 과대추정 쪽으로 치우친다**고 반복 보고합니다(RDE·ESSR 은 양의 오차 편향).
  자연 오차가 + 방향이면 거리축소 공격은 분포의 반대편 꼬리를 만드는 셈입니다.
  정확도는 Park 0.149 m(σ 0.104) / Apartment 0.376 / Office corridor 0.550 /
  Basement 0.414 m, 3D 라이브 트래킹 0.95 m(IPSN 2018 경진대회).
  회랑의 특정 지점에서 **네 알고리즘 모두가 높은 DQI 를 붙인 채 틀린 거리**를 반복
  보고한 기록이 특히 중요합니다 — 품질지표가 다중경로를 못 걸러낸 사례입니다.
- 신규: **Investigation of Multipath Effects on Phase-based Ranging** (Schröder 외,
  IPIN 2019, 관련도 **높음**, `partial`). 같은 연구진의 선행 논문으로, PBR 이
  **직접경로 대신 반사경로의 길이를 보고할 수 있다**고 실측으로 말합니다. 공격자 없이
  식별가능성 문제를 먼저 보여주는 자료라, riaz-2022 의 "다중경로에서도 임의 거리축소가
  된다"와 짝을 이룹니다. IEEE 유료라 전문은 못 열었고 초록 기준으로만 기록했습니다
  (세 가지 측정 결과 유형의 정의, 51% 개선의 조건은 미확인).
- 신규: **The Unambiguous Distance in a Phase-based Ranging System with Hopping
  Frequencies** (Zhang 외, arXiv 2014, 관련도 보통, `verified`). PBR 의 비모호거리가
  **사용한 주파수 인덱스들의 최대공약수 k** 로 결정된다(UD = c/(k·f_min))는 것과,
  주파수를 무작위로 고르면 그 확률이 1/ζ(M) 로 근사되어 M > 10 이면 P > 0.999 라는
  결과입니다. CS 로 옮기면 검증 가능한 가설이 하나 나옵니다 — **간섭·채널맵·재밍으로
  실제 사용 채널 집합이 특정 간격으로 치우치면 k 가 1 이 아니게 되고 비모호거리가
  접힌다.** 즉 "공격자가 채널 선택에 영향을 주어 모호거리를 축소시킬 수 있는가"의
  판정식이 여기 있습니다.
- 신규: **Robust Localization of Key Fob Using Channel Impulse Response of UWB Sensors
  for Keyless Entry Systems** (Kolli 외, arXiv 2024, 관련도 보통, `verified`).
  코퍼스의 방어 논문 여럿이 채널 특징에 신경망을 얹는데, **그 신경망 자체가 공격면**
  임을 같은 도메인에서 보여줍니다(FGSM·BIM·PGD, ε=0.1 에서 37~38% 열화, 구조 변경만으로
  특정 구간 67% 복구). 다만 위협모델은 정직하게 봐야 합니다 — 섭동을 48차원 특징
  벡터에 화이트박스로 직접 가하며, 저자들도 UWB 펄스 반복률 때문에 실시간 무선 생성은
  실현 가능하지 않다고 적습니다. 무선계층 공격의 실증이 아니라 판정기 강건성 평가입니다.
- 보강: **gunia-2026-cs-metrological** `partial` → `verified` (IEEE Access OA 경로).
  가장 쓸모 있는 것은 Table 2 의 **평균오차와 최대오차의 간극**입니다 — PBR(AC-FFT-PD)
  실외 평균 0.40 m 에 **최대 69.97 m**, 실내 1.36 m 에 최대 11.98 m. 정상 채널에서도
  두 자릿수 미터 이상치가 자연 발생한다는 뜻이고, 조작된 측정을 그 꼬리에 숨길 여지가
  그만큼 큽니다. 그리고 저자들은 실내 집계로 **최단거리 채택**을 권하는데, 이는
  거리축소 공격에 최악의 집계 규칙입니다(공격자가 만든 짧은 값이 항상 선택됨).
  다중경로 때문에 짧은 쪽을 고른다는 논리가 공격자가 있으면 그대로 뒤집힙니다.
  장비도 확정했습니다 — Atmel AT86RF233(K=152, 2.403–2.479 GHz, 500 kHz 스텝),
  자체 UWB 3.774–4.243 GHz, RN42·WRT54G·Galaxy S5(RSS), 기준값은 Leica TS15
  토탈스테이션(오차 <0.001 m). **CS 칩으로는 측정하지 않았다**는 점을 한계에 명시했습니다.
- 보강: **wacsa-2025-nn-ranging-fusion** `unverified` → `partial` (Springer 출판사 페이지).
  저자명을 출판사 기록으로 교정했고(Fang Yang → Fanwei Yang, Y. B. Zhao → Yubin Zhao,
  소속 Sun Yat-Sen/Jinan), 초록에서 **1–30 m 구간 평균 절대오차 0.22 m**, 구조가
  attention 기반 다중방식 융합 BPNN(AMF-BPNN)임을 확인했습니다. 이로써 **코퍼스에
  `unverified` 항목이 하나도 남지 않았습니다**(verified 67 / partial 7).
- 정정: **인용 관계 12건이 오탐이었습니다.** `scripts/extract-cites.mjs` 가 제목의
  콜론 앞부분으로도 프로브를 만드는데, `gunia-2026` 의 머리제목이 하필
  "Channel Sounding" 이라 **본문에 그 흔한 어구가 있기만 하면 인용으로 잡혔습니다**
  (10건). 같은 이유로 `suresh-2025`("BLE Channel Sounding"), `kravets-2025`
  ("BLE phase-based ranging") 도 각각 오탐을 만들었습니다. 인용한다고 기록된 논문의
  전문에 대상의 전체 제목도, 제1저자의 성도 없는 것을 확인하고 12건을 제거했습니다
  (242 → 240건). **이것은 데이터만 고친 임시 조치입니다** — 다음 실행에서
  `extract-cites.mjs` 를 다시 돌리면 같은 오탐이 되살아납니다. 서베이 실행은
  `data/` 밖을 고치지 않으므로 스크립트 수정은 사람의 판단으로 남깁니다.
- 표준: 변경 없음. Core Spec 6.3 이 최신, Ranging Profile/Service 1.0 채택 유지,
  Channel Sounding Inline Phase Correction Term Transfer 는 여전히 `VSr01_PR` 초안입니다.
- 실패: **zand-2019-ble-pbr 4회 연속 실패** — IEEE 유료이고 Unpaywall·OpenAlex 어디에도
  OA 사본이 없으며, TU/e 연구포털(research.tue.nl)에는 메타데이터만 있고 파일이 없습니다.
  santra-2024·eriksson-2024·pnn-2025·sheikh-2025 도 같은 이유로 IEEE stampPDF 경로가
  0바이트를 돌려줬습니다(유료 논문에는 안 통함). Semantic Scholar 는 이번에도 429.
- 보류: **A Novel Demodulation Scheme for Secure and Reliable UWB Distance Bounding**
  (Rezaee·Singelee·Preneel, arXiv 2010.10387)은 **저자가 철회한 논문**이라 편입하지
  않았습니다. **Kluge & Eggert, "Ranging with IEEE 802.15.4 Narrow-Band PHY"**
  (IEEE 802.15-09-0613-01-004f, 2009)는 InPhase 와 Gunia 가 **둘 다 협대역 PBR 의 출발점으로
  인용**하는 문서라 `standards.json` 후보로 올려둡니다(.ppt 라 이번엔 못 읽었습니다).
  Zhang 외의 RIPS 다중경로 보정(arXiv 1702.07624)도 후보로 남깁니다.

## 2026-08-24 (16차: 신규 4건, 보강 3건 — 참고문헌 캐기로 CS 실측·설계 두 편 발굴)

이번 실행의 수확은 전부 **참고문헌 캐기**에서 나왔습니다. 지난 회차에 편입한
schex-2026 의 참고문헌 목록을 훑다가 코퍼스에 없던 CS 문헌 두 편 — Gunia·Ellinger 의
IEEE Access 설계공간 탐색과 Sheikh 의 2.4 GHz 간섭 실측 — 을 찾았습니다. 둘 다
키워드 검색으로는 안 걸렸습니다. 목차 훑기(WiSec 2026 / NDSS 2026 / S&P 2026 /
arXiv)는 이번에도 신규를 거의 내놓지 않았고, 남은 미확인 후보 두 편(Pair-Fi,
BSFuzzer)은 CS 와의 접점이 없어 보류했습니다. 반대로 **원문을 이미 캐시에 갖고
있으면서 `unverified` 로 방치돼 있던 항목 두 건**을 이번에 정리했습니다 — 받아만
놓고 안 읽은 것이 남아 있었다는 뜻이라, 다음 회차부터는 캐시 대조를 먼저 합니다.

- 신규: **Channel Sounding: Metrological Exploration of the Design Options Using
  Related Positioning Systems** (Gunia·Ellinger, IEEE Access 14:18913–18928, 2026-02,
  관련도 **높음**, `partial`). CS 의 설계 선택지 — 랑잉 알고리즘, **집계(aggregation)**,
  측위 방식 — 를 계측학 관점에서 훑고 제약별 권고를 내놓습니다. 집계 단계가 중요한
  이유는 조작된 한 스텝이 평균에 섞여 들어가는지 걸러지는지가 거기서 정해지기
  때문입니다. 다만 저자가 **CS 하드웨어의 연결 설정 지연 때문에 대규모 측정이
  불가능해 '매우 유사한 시스템'으로 대신 탐색했다**고 초록에 명시하므로, 수치를
  CS 실측으로 인용하면 안 됩니다. Gold OA(CC BY)인데도 IEEE Xplore 가 403 을
  돌려주고 Unpaywall 에 직접 PDF 링크가 없어 초록까지만 확인했습니다.
- 신규: **Impact of 2.4 GHz Interference on Bluetooth® 6.0 Channel Sounding Ranging
  Measurements** (Sheikh, IEEE VCC 2025, 관련도 **높음**, `partial`). evaluation kit
  으로 Wi-Fi 및 2.4 GHz 간섭 아래 LOS/NLOS CS 를 실측한 문헌입니다. 탐지의 오탐
  여유는 정상 상태의 오차 분포로 정해지므로 이 축이 곧 임계값의 바닥입니다.
  kravets-2025, sheikh-2023 과 나란히 놓을 자리입니다. IEEE Xplore 유료,
  Semantic Scholar 가 openAccess 를 CLOSED 로 명시해 초록까지만 확인했습니다.
- 신규: **Channel Reciprocity Based Attack Detection for Securing UWB Ranging by
  Autoencoder** (Gou 외, IEEE/CIC ICCC 2024, 관련도 보통, `verified`). 탐지 근거를
  신호 하나가 아니라 **양쪽이 본 채널이 같은가**에 두는 방식입니다. CS 로 옮길
  여지가 실재합니다 — CS 는 initiator 와 reflector 가 같은 스텝에서 각자 I/Q 를 얻고
  RAS 가 reflector 측 결과를 넘기도록 규격에 정해져 있어, 양측 측정을 한자리에
  모으는 것이 이미 가능합니다. 실용적으로 값진 대목은 **CIR 을 오토인코더로
  700→32 차원, 4 bit 로 압축**해 전송량을 줄인 점으로, RAS 대역폭 제약 아래 무엇을
  넘겨야 하는가에 그대로 대응됩니다. 수치: 실기기(DW3110, 실내 10 m, SDC 모드)에서
  Ghost Peak 성공확률 **60.067% → 0.045%**, 오경보 2.4%, 미탐 0.075%. 시뮬레이션은
  4 bit 에서 탐지 99% 초과. 한계도 분명합니다 — 상호성 가정이 UWB 의 넓은 대역과
  CIR 해상도에 기대고 있어, **협대역 톤 교환인 CS 에서 같은 판별력이 남는지**가
  곧 검증해야 할 질문입니다. 같은 그룹의 gou-2025 가 이 논문을 인용해 관계를 채웠습니다.
- 신규: **Association-based Privacy Attacks in Wireless Protocols** (Jangid 외,
  arXiv 2608.11337, 2026-08-11, 관련도 보통, `verified`). 근접성 검증을 **쓰는 쪽**의
  문헌입니다. BLE 재연결의 allowlist 조건 검사가 응답 유무로 소속을 흘리고, 대책으로
  condition-oblivious response 와 **거리한정 검사**를 넣습니다. 여기서 얻는 것은
  비용의 실측치입니다: BLE 재연결 왕복 중앙값이 원 규격 **31.1 ms**, 제안 설계
  11.0 ms, 거리한정 **8 라운드 64.8 ms / 16 라운드 123.3 ms**. CS 를 재연결·페어링
  경로에 넣자고 주장할 때 반드시 나오는 "얼마나 느려지나"에 인용할 숫자입니다.
  저자들도 **거리한정 요구가 충분조건이라는 증명은 없다**고 명시하므로 그 빈틈이
  후속 연구의 자리입니다.
- 보강: **One Tap to Hijack Them All** (Duttagupta 외, IEEE S&P 2026) —
  `unverified` → `verified`. 저자 페이지에 전문(whisperpair.pdf)이 올라와 있었습니다.
  장비(Raspberry Pi 4 + BlueZ, 상용 액세서리 25 종 / 벤더 16 곳 / 칩셋 17 종),
  수치(**25 개 중 17 개(68%)가 pairing state predicate 미강제**, 탈취 6~35 초
  중앙값 10 초, 거리 14 m, 탈취 성공 시 마이크 접근 100%, nonce 검증 실패 68%,
  Find Hub 지원 4 종 전부 은밀 결속, CVE-2025-36911), 한계, 아티팩트(GitHub +
  KU Leuven RDR 데이터셋)를 채웠습니다. CS 관점의 쓸모는 **규격이 정한 상태 술어를
  응용계층 검사에 맡기면 벤더별로 무너지고 인증도 그걸 못 잡는다**는 논증이
  그대로 CS 의 보안 수준 주장에 옮겨온다는 것입니다. 인용 2 건 확인.
- 보강: **Stealtooth** (Kimura 외, arXiv 2507.00847) — `unverified` → `verified`.
  전문이 이미 캐시에 있었는데 읽지 않은 채였습니다. 저자 4 명, 장비(Raspberry Pi 4
  Model B ×2, Surface Laptop 4, 상용 헤드셋 10 종), 소프트웨어(BlueZ 5.55,
  PulseAudio 기반 A2DP Sender/Receiver, Breaktooth 공개 도구), 수치(**10 대 중 8 대
  에서 무음 link key 덮어쓰기**, 그 중 4 대에서 MitM, 도청 4/4 성공, 변조 2 종,
  중계는 코덱 재인코딩 실패로 부분 성공)를 채웠습니다. **같은 MediaTek 계열
  MT2822 / MT2822S 가 서로 다르게 거동**한다는 관찰이 핵심입니다 — 규격이 아니라
  구현의 결함이라는 뜻이고, CS 도 벤더 격차가 크므로 같은 논증이 성립합니다.
- 보강: **Securing Bluetooth Low Energy: A Literature Review** (Wang, arXiv
  2404.16846) — `unverified` → `verified`, 그리고 **평가를 내렸습니다**. 전문을
  읽어 보니 번호 매긴 참고문헌 목록이 아예 없고 선정 기준·검색 범위·분류 방법론이
  기술되지 않은 서술식 개괄이며, 조판 템플릿 잔여물(`Proposta recebida em Outubro
  2017`, 키워드가 `article sample, notes for the authors`)이 그대로 남아 있습니다.
  related work 인용 풀로 쓸 수 없다는 뜻이라 `relevance_note` 를 그렇게 고쳤습니다.
  이 저장소에서의 정직한 용도는 **BLE 보안 서베이가 CS 이전에 멈춰 있다**는 공백의
  근거입니다.
- 표준: 변경 없음. Bluetooth SIG 규격 목록에 6.3 이후 신규 없음, Channel Sounding
  Inline Phase Correction Term Transfer 는 여전히 `VSr01_PR` 초안(2026-08-24 확인).
  IEEE 802.15.4ab 은 WG 재회람 letter ballot #227 이 **D04 로 2025-12-18 개시,
  2026-01-08 마감**이었음을 확인했고 이후 새 정보가 없어 기존 상태를 유지합니다.
- 실패: Gunia·Ellinger(IEEE Access, Gold OA 인데 Xplore 403·Unpaywall 직접 링크 없음),
  Sheikh(IEEE VCC, 유료·CLOSED), 그리고 기존 미확인 항목 중 zand-2019, santra-2024,
  pnn-2025, eriksson-2024 는 이번에도 경로가 열리지 않아 손대지 않았습니다.
  arXiv API(`export.arxiv.org`)는 연속 질의에서 `Rate exceeded` 와 타임아웃이 반복돼
  6 개 질의 중 1 개만 성공했고, 나머지는 arXiv 검색 UI 를 WebFetch 로 열어 대체했습니다.
- 주의(사람 판단 필요): 새로 넣은 Gunia 논문의 제목이 `Channel Sounding:` 으로
  시작해서 `scripts/extract-cites.mjs` 의 부제 분리 규칙이 **`channel sounding`
  이라는 일반 어구를 프로브로 만듭니다.** `--dry` 로 확인해 보니 2026 년 논문
  두 편(vehicular-positioning-survey-2026, varughese-2026)이 오탐으로 잡힙니다.
  이번에는 스크립트를 돌리지 않고 원문 참고문헌에서 확인한 schex-2026 한 건만
  손으로 넣었습니다. 스크립트를 그대로 두면 다음 실행에서 유령 인용이 들어갑니다.

## 2026-08-21 (15차: 신규 3건, 보강 3건 — 규격 준수 CS 물리계층 시뮬레이터 편입)

이번 실행의 수확은 **arXiv API 를 목차 훑기 도구로 쓴 것**입니다. WebFetch 로 arXiv
목록 페이지를 열면 앞쪽 50 건만 보이고 나머지를 놓치는데, `export.arxiv.org/api/query`
에 `sortBy=submittedDate` 를 걸면 주제별 최신순 전체가 나옵니다. 이 경로로 사흘 전
공개된 CS 물리계층 시뮬레이터를 잡았습니다. 또 하나, **CEUR-WS 가 IPIN 워크숍
전문의 무료 경로**라는 것을 확인했습니다 — ResearchGate 링크만 있던 항목이 실은
CEUR Vol-4047 에 CC BY 로 통째로 올라와 있었고, 그 덕에 `unverified` 하나를
수치까지 갖춘 `verified` 로 올렸습니다.

- 신규: **Channel Modeling for Phase-Based Ranging** (Droemmer·Gardill, arXiv
  2608.17497, 2026-08-18 공개, 관련도 **높음**, `verified`). **Core Spec v6.2 기준
  Mode 3 PBR 의 72 톤을 규격대로 만드는 Python 물리계층 시뮬레이터**입니다.
  코퍼스에 계속 비어 있던 '통제된 CS 실험대' 자리를 정확히 채웁니다. 값진 것은
  손상 항이 식 하나에 분리돼 있다는 점입니다 — 위상잡음(σ_φ 1° 실험실 / 5~8°
  소비자 SoC), CFO 위상램프(0.05~0.7°/step), IQ 불균형(0.5~1.0 dB, 1.5~2.0°),
  ADC 양자화(12~16 bit), Wi-Fi OFDM 협대역 간섭(부반송파 64 개, duty 0.8)을
  **하나씩 켜고 끌 수 있습니다.** 여기에 공격 항을 하나 더 얹으면 '조작이 만드는
  위상 왜곡'과 '다중경로·하드웨어가 만드는 왜곡'을 같은 축에서 비교할 수 있습니다.
  탐지 지표의 오탐 여유를 장비 없이 정량화하는 첫 실험이 이 위에서 됩니다.
  다만 **시간영역 파형과 수신기 샘플클럭을 모델링하지 않는다**고 저자가 못박았으므로
  ED/LC 같은 타이밍 계열 공격은 이 위에서 못 돕니다. PBR 축 전용입니다.
  검증은 wieme-2025 의 공개 nRF54L15-DK 데이터셋과의 **정성 대조**에 그칩니다.
- 신규: **Hold the Door! Fingerprinting Your Car Key to Prevent Keyless Entry
  Car Theft** (Joo 외, NDSS 2020, 관련도 보통, `verified`). CS 가 푸는 문제를
  **거리를 아예 재지 않고** 푸는 경쟁 노선입니다. 서론에서 거리한정을 검토한 뒤
  버리는 논거가 그대로 내 반대편 주장이 됩니다 — "타이밍 오차에 극도로 민감하고,
  UWB-IR 을 쓰려면 통신 시스템을 통째로 새로 넣어야 한다." CS 는 두 번째 반론을
  무력화하는 기술이므로, 'CS 가 왜 판을 바꾸는가'의 직전 세대 대안으로 인용됩니다.
  동시에 보완재입니다: 판별 특징(peak frequency, SNR, spectral brightness,
  kurtosis)이 전부 송신기 하드웨어 지문이라 거리와 직교하고, **재생 공격은
  peak frequency 는 흉내내도 ADC/DAC 를 새로 거치므로 spectral brightness 와
  kurtosis 에서 걸린다**는 분석이 CS 릴레이 공격자에게 그대로 적용됩니다.
  수치: PKES 디지털 릴레이 SVM **FPR 0.27% / FNR 0%**, 단일밴드 릴레이는 5·10·15 m
  전부 FPR 0%. 그러나 **지하주차장에서 FPR 5%, 0°C 이하에서 정상 신호가 임계를
  넘습니다** — 물리 지문 단독으로는 못 버틴다는 근거입니다. staat-2022 가 이 논문을
  인용하고 있어 인용 관계도 채웠습니다.
- 신규: **BLE Theft Auto** (Yu 외, USENIX Security 2026, 관련도 낮음, `verified`).
  거리 논문이 아니지만 **위협 모델의 순서**를 못박는 자료라 넣었습니다. 애프터마켓
  BLE 차량 원격제어 6 종 중 3 종이 공유 키·페어링 부재 같은 응용계층 결함을 갖고
  있고 취약 차량이 **140 만 대**(순차 MAC 추정으로 KARR 1,473,136 대) 규모입니다.
  이런 시스템에 CS 를 얹어도 공격자가 정당한 사용자로 인증되므로 거리 검증이 그냥
  통과합니다. 게다가 **공격 사거리가 KARR 3~10 m, CarLink 150 m 미만**이라 애초에
  거리를 속일 이유가 없습니다. WiGLE 공개 워드라이빙 DB 로 표본 50 개 중 **31 개
  (62%)를 표적화 가능**하다고 실증한 대목은 CS 기기의 광고 패킷 설계에도 걸립니다.
- 보강: **Study of BLE6 Ranging Performance in a Utility Basement** (Ulsamer 외,
  IPIN-WCAL 2025) — `unverified` → `verified`. **CEUR-WS Vol-4047 에 무료 전문**이
  있었습니다. 같은 nRF54L15 DK 로 실외/지하를 대조한 값이 그대로 탐지 임계의
  정상 상태 분포가 됩니다: 실외 23 지점(1~40 m) 평균오차 **IFFT2 0.13 m(SD 0.01)**,
  IFFT 0.21, Slope 0.98, RTT 0.35. 지하 설비실에서는 평균 표준편차가 **1.21~2.05 m**
  로 두 자릿수 악화하고 80% 오차가 5 m 근처입니다. 가장 중요한 발견은
  **조작 없이도 거리 축소 방향 오차가 자연 발생한다**는 것입니다 — 실내 1→4 구간
  (참값 23.0 m)에서 IFFT 가 8.797 m 를 내 **오차 -14.2 m**, 1→5 구간에서 -14.4 m.
  축소 공격의 탐지 임계를 정할 때 정면으로 걸립니다. 방식별 상수 오프셋
  (RTT 3.78 m, Slope 1.91 m)을 사후 보정해야 했다는 기록, 초기화 펌웨어를 고쳐
  75 채널 원시 IQ 를 시리얼로 뽑은 레시피도 그대로 씁니다. 인용 3 건(santra-2024,
  suresh-2025, pnn-2025)도 전문 대조로 채웠습니다.
- 보강: **Tsemko 외 2025** (파라메트릭 신경망 CS 거리추정, ICASSP) — `unverified`
  → `partial`. 초록을 확인해 **초해상도 알고리즘 대비 RMSE 최대 0.4 m 감소**라는
  수치를 넣었습니다. 전문은 여전히 미확보.
- 보강: **Eriksson 외 2024** (CS 다중경로 식별 포스터, IEEE VNC) — `unverified`
  → `partial`. DOI(10.1109/VNC61989.2024.10575979)와 페이지(271–272)를 확정하고
  초록 기반 요약으로 "확인 필요"를 걷어냈습니다. IQ 샘플 + 기계학습으로 다중경로를
  검출하며 차량 내부 측정 정확도 개선과 IQ 데이터 라벨링이 목적입니다.
- 표준: 변경 없음. Bluetooth SIG 규격 목록을 직접 확인한 결과 Core Specification 은
  **6.3 이 여전히 최신 adopted**, RAS/RAP 는 1.0, Channel Sounding Inline Phase
  Correction Term Transfer 는 **아직 VSr01_PR 공개검토 초안** 상태 그대로입니다.
  IEEE 802.15.4ab 도 "2026 년 내 출판 예정"에서 확정된 변화를 확인하지 못해
  기존 상태(초안 D04, SA 투표 단계)를 유지했습니다.
- 실패: **Zand 2019**(WCNC, PBR 계보의 뿌리)와 **Santra 2024**(IEEE Sensors
  Letters)는 이번에도 전문을 못 구했습니다. Semantic Scholar 의 `openAccessPdf`
  가 둘 다 비어 있고(Santra 는 `CLOSED` 명시), TU/e 연구 포털 검색도 빈손이었습니다.
  두 항목의 `verification` 은 올리지 않고 `last_checked` 만 갱신했습니다.
  WASA 2025 논문(Springer LNCS)도 ACM DL 색인만 있고 PDF 호스팅이 없어 그대로 둡니다.

## 2026-08-18 (14차: 신규 3건, 보강 7건 — 쿠키 예열로 ACM DL 이 완전히 뚫림)

지난 실행에서 "브라우저 UA 를 붙이면 연차가 오래된 ACM 논문만 열린다"고 적었는데,
**그 진단이 틀렸습니다.** 문제는 UA 가 아니라 세션이었습니다. `dl.acm.org/doi/<DOI>`
랜딩 페이지를 **쿠키 항아리(`curl -c`)로 먼저 한 번 받아 두고**, 몇 초 뒤 같은 쿠키로
`doi/pdf/<DOI>` 를 요청하면 최근 논문도 그대로 열립니다. 요청을 연달아 쏘면 다시
막히므로 건당 6초 + 사이 15초를 둡니다. 이 경로로 **코퍼스에 남아 있던 ACM 차단
항목 6건을 한 번에 전부** 확보했고, 그 전문의 참고문헌에서 계보의 가장 큰 구멍
두 개(Francillon 2011, Cremers 2012)를 찾았습니다.

- 신규: **Relay Attacks on Passive Keyless Entry and Start Systems in Modern Cars**
  (Francillon 외, NDSS 2011, 관련도 **높음**, `verified`). **CS 가 왜 존재하는지를
  설명하는 원점 문헌**인데 코퍼스에 없었습니다. 캐시에 전문이 있는 코퍼스 논문
  **16 편이 이 논문을 인용**합니다 — 계보에서 가장 크게 비어 있던 노드입니다.
  8 개 제조사 **10 개 차종 전부**에서 문 열기와 시동까지 성공했고, 물리계층 아날로그
  릴레이가 더하는 지연은 **케이블 30 m 에서 160 ± 20 ns, 무선 30 m 에서 120 ± 20 ns**
  입니다. 차종별 **최대 허용 지연이 35 µs ~ 수십 ms** 라서 이론적 릴레이 거리가
  10~3000 km 가 됩니다. 내 연구에 바로 쓰이는 대목은 대응책 절입니다 — 저자들이
  "릴레이 지연이 250 ns 인데 거리한정 구현의 왕복시간 분산이 그보다 크면 탐지 불가"
  라고 못박고, rasmussen-2010 의 **62 ps 분산**을 근거로 충족 가능하다고 판정합니다.
  CS 의 RTT 분산을 같은 틀에 넣는 것이 그대로 한 절이 됩니다. USRP1 은 최소 처리지연이
  10~20 ms 라 한 대를 빼고는 모두 너무 느렸다는 기록도 남겼습니다.
- 신규: **Distance Hijacking Attacks on Distance Bounding Protocols** (Cremers 외,
  IEEE S&P 2012, 관련도 보통, `verified`). CS 보안 논의가 전부 "릴레이를 막는가"에
  쏠려 있는데, 이 논문은 **공모자가 필요 없는 네 번째 공격 유형**을 정의합니다 —
  부정직한 프로버가 근처 **정직한** 프로버의 fast phase 를 가로챕니다. 프로토콜
  **19 종 중 10 종이 취약**하고 그 대부분이 신규 발견입니다. 구조적 진단이 CS 에
  직접 걸립니다 — Brands-Chaum 계열은 fast phase 응답에 신원이 안 묶여 취약하고,
  fast phase 에서 공유키를 직접 쓰는 Hancke-Kuhn 계열은 안전합니다. CS 는 CS_SYNC 와
  PBR 톤이 세션키에서 유도되므로 형식상 후자지만, **같은 환경에서 여러 프로토콜이
  동시에 도는 다중 프로토콜 환경에서는 저자들도 "쉬운 해결책이 없다"** 고 못박습니다.
  RAS/RAP 다중 리플렉터 구성이 정확히 그 환경입니다. 읽은 전문은 IEEE 게재본이 아니라
  ETH D-INFK Technical Report 판본이며 그 사실을 항목에 명시했습니다.
- 신규: **Security evaluation of quantum distance-bounding protocols via semidefinite
  programming** (Bogner 외, arXiv 2607.13464, 관련도 낮음, `verified`). 양자 채널이라
  CS 에 직접 적용되지 않지만 **방법론 하나가 넘어옵니다** — fast phase 한 라운드를 떼어
  distance/mafia fraud 게임으로 정식화하고 최적 공격 성공확률을 **근사가 아니라 정확히**
  SDP 로 계산합니다. CS 논의는 "이 공격이 몇 % 성공했다"는 실측 위주라 "이 구조에서
  최적 공격자의 상한이 얼마인가"를 묻지 않습니다. DF 값은 모든 DV-QDB 에서 0.5000 으로
  프로토콜을 구별하지 못하지만 MF 값은 0.7500~0.9332 로 잘 구별되고, 전부 선행 보고치를
  넘습니다. 저자가 abidin-2021 과 같은 KU Leuven COSIC 그룹이라 협대역 랑잉과 형식
  거리한정을 함께 다루는 계보가 보입니다. 재현 코드가 Zenodo 에 아카이브돼 있습니다.
- 보강: **Riaz 2022** (PBR 다중경로 보안, ACM JETC) — `partial` → `verified`, 관련도
  높음 유지. 지난 실행에서 초록만 보고 올린 항목인데, 전문이 초록보다 훨씬 CS 에
  가깝습니다. 실험 장비가 **AD9361 SDR 2 대로 2.4 GHz ISM 80 MHz 를 1 MHz 스텝**으로
  훑는 구성이라 CS 의 PBR 파라미터와 사실상 같고, 공격자는 **USRP-N300 + 지연 소자를
  FPGA 커스텀 IP 로 구현**(호스트 우회)했습니다. 가장 쓸모 있는 것은 대응책 분석입니다 —
  **주파수 호핑은 공격자가 FFT 로 1 MHz 해상도로 톤을 찾고 톤 유지시간 100 µs 안에
  대응하면 무력화**되고, **ToF 이중인증은 2 Mbps 링크에서 해상도가 150 m 라 태그가 그
  안에 있으면 아무것도 못 잡습니다.** 지연 기반 통계 탐지(Z-검정, α=1%)는 Δf 를
  100 kHz 로 낮추면 통하지만 **실시간 위상 곱셈 공격자에게는 통하지 않습니다.**
  NLOS 성립(직선경로에서 수직 0~100 m)도 실측으로 확인했습니다.
- 보강: **Singh 2021** (802.15.4z/HRP 보안분석, WiSec) — `partial` → `verified`.
  핵심은 **트레이드오프의 수치화**입니다: 수신기 (백서치, PAPR) = (20, 4) 에서 오검출률
  0.96% 미만일 때 **Cicada++ 성공률 88.4%**, 오검출률 1.5% 미만인 **모든** 설정에서
  성공률 최소 50% — 이 수신기 설계로는 둘을 동시에 만족하는 설정이 없습니다.
  반직관적 결론도 얻었습니다: **Industrial LoS 처럼 "깨끗한" 채널이 오히려 더 취약**
  합니다(리딩엣지가 가장 강해 백서치 윈도우를 길게 잡을 수 있으므로). **하드웨어를
  전혀 쓰지 않은 MATLAB 전용 논문**이라는 것도 확정했습니다.
- 보강: **UWB-SV** (Joo 외, CCS 2023) — `partial` → `verified`. 탐지율 **96.24%**,
  오탐률 **0.32%**, 그리고 CS 에 옮길 때 가장 중요한 수치인 **연산 오버헤드 +125.9 µs**
  (DWM3000 + NUCLEO-Z429 실측, 기본 처리지연 125.9 µs 대비 약 +100%)를 채웠습니다.
  운용 제약도 저자가 명시했습니다 — 링크버짓이 낮으면 오탐이 나므로 **측정 거리가
  수 m 이내일 때만** 적용해야 합니다. 코드 공개(github.com/kyunghojoo/uwb-sv).
- 보강: **Nagaraj 2025** (FBR, IoT '25) — `partial` → `verified`. **하드웨어 없는
  시뮬레이션 전용**이며 저자가 "Bluetooth 하드웨어 검증은 향후 과제"라고 명시한 것을
  확인했습니다. 20 m 에서 10 cm 정확도에 **ATS 약 4 ms** 필요(Bluetooth 슬롯 0.3125 ms
  기준 긴 패킷 필요). PBR 대비 논증이 명확합니다 — 주파수는 지연에 단조 증가해 모호성이
  없고 T_IFS 호핑 대기도 발진기 드리프트도 안 겪습니다. 대신 **PBR 보다 훨씬 높은 수신
  전력이 필요**한 것이 한계입니다. **보안 분석이 전혀 없다는 점을 한계에 명시**했습니다 —
  지연-주파수 단조 대응은 정확도에는 유리하나 공격자에게도 조작 경로가 단순해진다는
  뜻일 수 있어 그 지점이 빈틈입니다.
- 보강: **Timestamps Unchained** (von Tschirschnitz 외, WiSec '26) — `unverified` →
  `verified`. 발견의 핵심은 **ESP32-C3 하드웨어가 FTM 프레임뿐 아니라 일반 OFDM
  프레임에, 그것도 프로미스큐어스 모드로 관측한 남의 프레임에까지 피코초 해상도
  타임스탬프를 만든다**는 것입니다(TRM 에 "Reserved" 로만 적힌 영역). `pp_wdev_funcs`
  전역 배열의 함수 포인터를 덮어써 훅을 겁니다. 실측은 5~15 m 에서 **표준편차
  0.076~0.271 m**, 임계 10 m 판정에서 **10.5 m 초과 수락률 0 / 9.5 m 미만 수락률 1**
  (폭 1 m 모호구간). 저자들이 **"물리계층 거리축소 공격에 대한 내성은 제공하지 않는다"**
  고 명시한 것이 중요합니다 — 이 논문은 방어가 아니라 **개방 실험 플랫폼**입니다.
  Intel AX-200 으로는 나노초급 타임스탬프를 못 얻었다는 실패 기록도 남겼습니다.
- 보강: **BlueBrothers** / **HardaBLE** (Sacchetti 외, WiSec '26) — 둘 다 `unverified`
  → `verified`. BlueBrothers 는 nRF52840 2 대 + Mynewt v1.13.0 + 패치 NimBLE v1.8.0,
  ProVerif 모델 3 종, **BB-Pairing 지연 55.0% 감소 / 에너지 17.65% 감소**. HardaBLE 은
  nRF5340 + TrustZone-M + TF-M + Zephyr, TLA+/TLC 모델검사, **페어링 지연 오버헤드
  +0.99%(808 → 816 ms), 전하 -0.65%**. 둘 다 거리측정과 무관하다는 점을 `limitations`
  에 명시해 관련도 낮음을 유지했습니다.
- 인용 관계: 171 → **217 건**. Francillon 2011 은 코퍼스 논문 **16 편**이, Cremers 2012 는
  3 편이 인용하는 것으로 전문 대조 확인했습니다(전문 미확보 항목은 건드리지 않음).
- 표준: **변경 없음.** Bluetooth SIG 스펙 목록 재확인 — Core 6.3 이 최신이고 Ranging
  Service / Ranging Profile 은 1.0 adopted, Channel Sounding Inline PCT Transfer 는
  여전히 `VSr01_PR` 초안입니다. 다음 코어 릴리스는 11월경 예상.
- 실패: **WCNC 2019 (Zand)** 전문 — **4 회 연속 실패**. 이번에는 새 경로를 두 개 뚫었으나
  둘 다 막혔습니다. imec 의 DSpace(`imec-publications.be`)에서 항목과 비트스트림 UUID
  까지는 찾았지만 `/content` 가 **401 Unauthorized**(ORIGINAL 과 TEXT 번들 모두)이고,
  TU/e Pure 포털은 DOI 링크만 제공합니다. IEEE Xplore 유료, Unpaywall 기준 OA 사본 없음.
  ETH Research Collection 에 **Singh 2021 항목은 있으나 Scopus 메타데이터 XML 뿐**이라
  거기서도 전문이 안 나왔습니다(ACM 경로로 해결).
- 정정: 지난 실행의 "브라우저 UA 는 연차가 오래된 ACM 논문에만 통한다"는 진단은
  틀렸습니다. 필요한 것은 UA 가 아니라 랜딩 페이지 쿠키 예열이었고, WiSec '26 · IoT '25 ·
  JETC 2022 · CCS 2023 · WiSec 2021 전부 열렸습니다.

## 2026-08-17 (13차: 신규 3건, 보강 2건 — 브라우저 UA 로 ACM DL 이 부분적으로 뚫림)

이번 실행의 수확도 **접근 경로**에서 나왔습니다. `dl.acm.org/doi/pdf/` 요청에 브라우저
User-Agent 를 붙였더니 **2012 년 WiSec 논문이 그대로 열렸습니다**. 최근 논문(WiSec '26,
IoT '25, JETC 2022)은 여전히 Cloudflare 가 막으므로 **연차가 오래된 ACM 논문에만 통하는
경로**로 보입니다. 이 경로로 코퍼스에 마지막까지 남아 있던 `unverified` 고전인
Ranganathan 2012 를 열었고, 저자 개인 페이지(`francozappa.github.io`)에서 BLUFFS 전문도
확보했습니다.

- 신규: **Security Assessment of Phase-Based Ranging Systems in a Multipath Environment**
  (Riaz 외, ACM JETC 18(4), 2022, 관련도 **높음**, `partial`). 코퍼스에 없던 축을 채웁니다 —
  **다중경로 조건에서의 MCPR 거리축소**입니다. olafsdottir-2017 과 staat-2022 는 채널을
  대체로 우호적으로 두었는데, 이 논문은 "다중경로가 달라져도 임의의 거리 감소가
  성립하는가"를 묻고 **30 m 이격을 1 m 미만으로 스푸핑**했다고 보고합니다. 사실이라면
  "다중경로가 공격을 어렵게 한다"는 흔한 반론이 약해집니다. ACM DL 차단으로 전문은
  못 열었고, 서지정보는 Crossref 로 확정했습니다(저자 7인 전체 명단 확보).
- 신규: **Spectrum-Flexible Secure Broadcast Ranging** (Vo-Huu 외, ACM WiSec 2021,
  관련도 **높음**, `verified`). "2.4 GHz 에서 CS 급 좁은 대역으로 물리계층 공격에 견디는
  거리측정이 되는가"의 **직접 대조군**입니다. 25 MHz 에서 50 cm, 100 MHz 에서 15 cm 를
  실측으로 내는데 수단은 정확도 기법이 아니라 설계 원칙입니다 — **프리앰블을 없애고
  요청·응답 전체를 PRF 난수열로 만들어 잡음과 구별 불가능하게 하고, 응답 시각까지
  무작위화**합니다. CS 는 시퀀스는 감추지만 타이밍과 채널 스케줄은 규격으로 공개된다는
  대비가 여기서 선명해집니다. USRP X310 + 커스텀 FPGA, GNU Radio/UHD, 5 µs 버스트.
- 신규: **Resilient Random Time-hopping Reply against Distance Attacks in UWB Ranging**
  (Gou 외, arXiv 2406.06252v2, 관련도 보통, `verified`). 위와 같은 문제를 방어 쪽에서
  건드립니다. 답신 간격 T_reply 를 매 라운드 난수화해 **Qorvo DW3110 실측에서 Ghost Peak
  성공률을 SDC 모드 60.67% → 0% (각 10,000 회)** 로 낮춥니다. 부수 소득으로 **SDC 모드가
  Mode1(0.3%)보다 200 배 취약**하다는 실측치를 얻었습니다. CS 관점의 값은 "이 방어를
  CS 에 쓸 수 없다"는 데 있습니다 — CS 의 스텝 타이밍은 T_IFS 와 서브이벤트 스케줄로
  고정되어 있으므로, 왜 못 쓰는지를 논증하면 표준 수준 개선 제안으로 이어집니다.
- 보강: **Physical-Layer Attacks on Chirp-Based Ranging Systems** (Ranganathan 2012) —
  `unverified` → `verified`, 관련도 낮음 → 보통. 전문에서 **공격자 하드웨어 지연
  t_hw = 87 ns (Spartan 3A zero-crossing 검출 7 ns 포함)**, **chirp 1 µs 에서 150 m /
  4 µs 에서 600 m 축소**, **조기검출 정확도 100% 구간(t_ed = T_chirp 의 20~70%, 실채널)**,
  그리고 **(7,4) Hamming 오류정정이 공격 여유를 넓혀 chirp 의 10% 만 보고 90% 지점까지
  늦게 커밋해도 성립**한다는 관찰을 채웠습니다. 저자들이 "USRP 류는 처리 지연이 µs 라
  ED/LC 에 부적합"이라고 명시한 대목은 내 FPGA 경로 판단의 선행 근거입니다.
  hardware/software 모두 `verified`.
- 보강: **BLUFFS** (Antonioli, CCS 2023) — `partial` → `verified`. 장비(CYW20819 보드 +
  Linux 노트북), 도구(InternalBlue, Ghidra, ARM Thumb-2 패치 7종), 규모(**17 종 칩 / 18 개
  기기, 기기당 15 분 미만**), 대응책 비용(**LMP 명령 1 개 + 공중 48 바이트 + 함수 호출 3 회**),
  코드 링크를 채웠습니다. 동시에 **`relevance_note` 의 적용 범위를 좁혔습니다** — 이 공격은
  Bluetooth Classic 의 LSC 세션 확립 대상이고 CS 가 쓰는 LE Secure Connections 가 아닙니다.
  CS 로의 함의는 **"논스 없이 일방적·반복 가능한 키 유도라는 근본 원인이 CS Security
  Start 에도 있는가"**라는 질문 형태로만 남깁니다.
- 인용 관계: 152 → 171건 (자동 추출 + 참고문헌 육안 대조로 Vo-Huu→Flury, Gou→UWBAD 2건
  수동 보정 — 줄바꿈으로 제목이 깨져 자동 추출이 놓친 것들).
- 표준: 변경 없음. Bluetooth SIG 스펙 목록 재확인 — Core 6.3 이 최신이고 Inline PCT
  Transfer 는 여전히 `VSr01_PR` 공개검토 초안. 다음 코어 릴리스는 11월경 예상.
- 실패: JETC 2022(Riaz), IoT '25(Nagaraj FBR), WiSec '26(Timestamps Unchained) 전문 —
  ACM DL 이 브라우저 UA 를 붙여도 최근 논문은 차단. WCNC 2019(Zand) — IEEE Xplore 유료,
  Unpaywall 기준 OA 사본 없음(3회 연속 실패, 다른 경로 필요).

## 2026-08-15 (12차: 신규 3건, 보강 6건 — ED/LC 계보의 빠진 두 칸을 메움)

이번 실행의 수확은 **접근 경로**에서 나왔습니다. ACM DL 이 막혀 있어 `partial` 로
방치돼 있던 항목들을 뚫으려고 `dl.acm.org/doi/fullHtml/` 을 시도했더니 Leu 2021 이
통째로 열렸습니다(다른 ACM 논문은 여전히 Cloudflare 차단). 그 전문의 참고문헌을 캐다가
코퍼스의 ED/LC 계보에 **두 칸이 비어 있었다는 것**을 발견했고, EPFL infoscience 의
DSpace REST API(`/server/api/discover/search/objects` → `/bundles` → `/bitstreams`)로
둘 다 전문을 확보했습니다. 이 경로는 앞으로도 EPFL·ETH 계열 논문에 재사용할 수 있습니다.

- 신규: **Effectiveness of Distance-Decreasing Attacks Against Impulse Radio Ranging**
  (Flury 외, ACM WiSec 2010, 관련도 보통, `verified`). Clulow 2006 이 개념으로 지적한
  '긴 심볼' 문제를 **실제 표준 PHY 위에서 처음 수치로 환산**한 논문입니다. 802.15.4a
  필수 모드에서 거리 축소 **140 m 를 성공률 99% 이상**으로 달성하고, 그 대가가 정상
  동작 대비 **LPRF 에서 ED +4 dB / LC +6 dB**, HPRF 에서 양쪽 +7 dB 임을 보입니다.
  20 MHz 부반송파별 축소량 표(8→15 m, 64→225 m)와 함께, **페이로드만 공격해서는
  부족하고 프리앰블(SYNC/SFD)까지 밀어야 한다**는 지적이 CS 의 CS_SYNC + PBR 2단
  구조에 그대로 걸립니다. 하드웨어 없이 MATLAB 시뮬레이션(물리계층 100 ps 정밀도)만
  사용했다는 점도 전문에서 확인했습니다.
- 신규: **Distance Bounding with IEEE 802.15.4a: Attacks and Countermeasures**
  (Poturalski 외, IEEE TWC 2011, 관련도 보통, `verified`). 위 논문의 확장판이자 이
  계보에서 **대응책을 처음 수치로 설계한** 논문입니다. rake 공격자 대 에너지검출
  수신기에서 2.8 dB 비용으로 **218 m** 축소, ED 단독은 65 m. 표준의 convolutional
  code 이상과 time-hopping 이 각각 공격 표면이 된다는 지적이 나옵니다. 가장 쓸모 있는
  것은 마지막 거래입니다 — 조기 검출 대응책이 심볼 절반을 버려 생기는 성능 손실을
  **논스 길이를 42→108 비트로 늘려** 흡수하고, P_guess = 2^-32 와 PER 을 유지한 채
  거리 축소를 **약 12 m** 로 억제합니다. CS 의 sounding sequence 길이·스텝 수로 같은
  거래가 되는지가 바로 후속 질문입니다. 확보한 전문이 TWC 게재본이 아니라 EPFL
  기술보고서 확장판이라는 점은 `limitations` 에 적어 두었습니다.
- 신규: **Bridging the Indoor-Outdoor Gap: Cross-Technology Ranging** (Schwarzbach,
  arXiv 2026, 관련도 보통, `verified`). CS **이전 세대** BLE 위상 거리측정이 밀리미터급
  기준값(Leica TS16) 대비 실제로 얼마나 틀리는지를 UWB·Wi-Fi FTM·GNSS 와 같은
  실험장에서 나란히 잰 자료입니다. BLE PBR 은 전 구역에서 **5–12 m 양의 편향, 실외
  σ 약 12 m** 로 네 기술 중 최악인 반면 UWB 는 LOS 본체가 무편향(실내 중앙값 0.05 m).
  저자가 "이건 배치된 Metirionic DMK-215 의 특성이지 현재 BLE Channel Sounding 이
  아니다" 라고 못박은 문장이 중요합니다 — CS 가 무엇을 개선했는지 말할 때 규격 인용이
  아니라 실측 대비로 쓸 수 있는 기준선입니다. 데이터셋은 Zenodo 공개.
- 보강: **Security of Multicarrier Time-of-Flight Ranging** (Leu 2021) —
  `partial` → **`verified`**. ACM fullHtml 로 전문 확보. 하드웨어 없음(수학적 증명 +
  시뮬레이션만)을 확인해 `hardware_verified`/`software_verified` 를 채웠고, 지금까지
  "구체 수치 확인 필요" 로 비어 있던 `results` 를 정리 3.1~따름정리 3.4 와 거리 축소
  표(20 MHz / 64 부반송파 → **225 m**)로 대체했습니다. `cites` 4건 추출.
- 보강: **Protecting HRP UWB Ranging System** (uwb-sv-2023-ccs) — **DOI 가 틀려
  있었습니다.** `10.1145/3576915.3623111` 은 실제로는 range-revocable pseudonym 논문의
  DOI 이고, 이 논문은 `10.1145/3576915.3623145` (pp. 622–635) 입니다. Crossref 대조로
  확정했습니다. BibTeX 로 새어 나가고 있던 오류라 서지정보 신뢰도에 직결됩니다.
- 보강: **Physical-Layer Attacks on Chirp-Based Ranging Systems** (Ranganathan 2012) —
  같은 유형의 오류. `10.1145/2185448.2185452` (실제로는 jamming 논문) → 정정
  `10.1145/2185448.2185453`. Crossref 대조.
- 보강: WiSec 2026 3건(**Timestamps Unchained**, **BlueBrothers**, **HardaBLE**) —
  2026-06-29 프로시딩 발행이 확인되어 `doi: null` 이던 세 항목에 DOI·페이지·정식
  venue 를 채웠습니다. 본문은 여전히 못 열었으므로 `verification` 은 `unverified` 유지.
- 인용: 새 노드 두 개가 코퍼스 전반에 깊이 박혀 있었습니다. 정규화 대조로 **기존 14개
  항목의 `cites` 를 갱신**(Flury 2010 을 인용하는 논문 10건, Poturalski 2011 을 인용하는
  논문 8건). 인용 관계가 121건 → 152건으로 늘었습니다.
- 표준: 변경 없음. Core Specification 은 6.3 이 여전히 최신이고, Ranging Profile/Service
  는 v1.0, Channel Sounding Inline PCT Transfer 는 VSr01_PR 초안 그대로입니다.
  IEEE 802.15.4ab 도 공식 TG 페이지에 상태 변화가 게시되지 않았습니다.
- 실패: ACM DL 이 Cloudflare 로 자동 요청을 차단해 `uwb-sv-2023-ccs`(OpenAlex 기준
  **gold OA 인데도** 차단), `singh-2021-4z-security-analysis`, `ranganathan-2012-chirp-attacks`,
  `nagaraj-2025-fbr`(역시 gold OA), WiSec 2026 3건의 본문을 열지 못했습니다.
  curl(브라우저 UA 포함)과 WebFetch 모두 403. `zand-2019-ble-pbr` 은 TU/e 연구
  포털에서 저자 전체 명단과 초록 원문은 재확인했으나 전문 파일이 없어 `partial` 유지.

## 2026-08-12 (11차: 신규 3건, 보강 2건 — 보안수준을 '측정'하는 방법론 계보 편입)

목차 훑기(WiSec/NDSS/S&P/USENIX 2026, arXiv)에서는 신규가 나오지 않았습니다. 대신
**ETH syssec 발행목록을 훑다가 코퍼스에 없던 계보 하나를 통째로 발견**했습니다.
검색 축을 학회 목차에서 연구그룹 발행목록으로 한 번 바꾼 것이 이번 실행의 수확 전부입니다.

- 신규: **FAST: Fast and Accurate Security Testing of HRP UWB Chips** (Aad 외,
  TCHES 2026, 관련도 **높음**, `verified`). 이번 실행의 핵심입니다. 독점 구현이라
  폐형식 보안식을 쓸 수 없는 수신기의 랜덤추측 공격 성공률을, importance sampling 으로
  **수만 샘플만에 2^-10 ~ 2^-128 범위까지** 신뢰구간과 함께 추정합니다. 결정적으로
  저자들이 5.2절에서 적용 대상으로 **"sounding sequence randomization for narrowband
  secure ranging with Bluetooth"를 명시**하고 근거로 Abidin 2021 과 Bluetooth CS 규격을
  듭니다. 즉 CS_SYNC 검증과 NADM 판정의 보안 수준을 실칩에서 수치로 말하는 절차가
  이미 제시되어 있다는 뜻입니다. 장비는 R&S SMW200A 신호발생기 + Qorvo DWM3000EVB
  (nRF52DK 구동) + NXP SR040/SR150, 계측은 R&S RTP164b 40 GSa/s. 코드는 Zenodo 공개.
  수치: Qorvo STS_NTM 기본값 12 → 2^-12.1, 24 로 올리면 2^-37.2. NXP SR150 은 같은
  조건에서 2^-13.4 ~ 2^-17.3 으로 SR040(2^-40 ~ 2^-98)보다 훨씬 취약.
  **측정 1회당 1.5 초** — 내 CS 실험 계획에서 "성공률을 재려면 몇 번 돌려야 하나"가
  병목이었던 부분에 그대로 답이 됩니다.
- 신규: **PURE: Payments with UWB RElay-protection** (Coppola 외, USENIX Security 2024,
  관련도 보통, `verified`). FAST 의 참고문헌 캐기로 발견. 결제는 카드-단말 거리가 5 cm
  이하라 링크버짓이 좋고, 그래서 절대 문턱값을 크게 올려도 오탈락이 늘지 않습니다.
  **"유스케이스가 채널을 좁히면 수신기 정책을 공격적으로 조일 수 있다"** 는 논증의 모범
  사례이고, CS 의 디지털 키(수 m) 대 근접 결제(수 cm) 유스케이스별 NADM 문턱 차등화의
  근거가 됩니다. T = 702 로 Ghost Peak 성공률을 2^-49 로 상한, 거래시간 증가 41 ms.
  Tamarin 형식검증이 **레인징 단계를 모델에서 뺐다**는 점도 기록 — CS 를 형식적으로 다룰 때
  경계선을 어디에 그을지의 선례입니다.
- 신규: **Realization of RF Distance Bounding** (Rasmussen & Capkun, USENIX Security 2010,
  관련도 보통, `verified`). 역시 참고문헌 캐기. **처리시간 1 ns = 15 cm** 라는 환산 척도의
  출처이고, 실측은 μ = 912.92 ps (σ = 61.22 ps). 중요한 것은 저자들이 XOR·비교 함수는
  복조를 요구해 약 170 ns(≈ 25 m) 지연을 낳아 못 쓴다고 못박고, **복조 없이 아날로그
  믹서로 채널만 바꿔 되쏘는 CRCS** 를 쓴 점입니다. 이것은 `fhss-tracking` 인사이트에서
  도달한 결론(LO 재조정 불가 → 고정 LO + DSP)과 같은 구조의 문제이며, 공격자 쪽 아날로그
  중계기 설계와 방어자 쪽 고속 응답기 설계가 사실상 같은 회로 문제임을 보여줍니다.
  협대역 CS 조건에서 같은 계산을 다시 하는 것이 바로 이어지는 작업입니다.
- 보강: **A Relay a Day Keeps the AirTag Away** (Gegenhuber 외, arXiv 2026)
  `partial` → `verified`. arXiv 전문 확보(4쪽 단편). 장비는 ESP32/Linux BLE 송출기와
  **타 국가에 둔 Raspberry Pi 중계 노드**, 도구는 AirGuard·OpenHaystack. 새 수치:
  배터리를 빼 키 회전을 막으면 포착한 비컨을 **7일간** 재생 가능하고 8일째부터
  outdated 로 표시됩니다. 저자 명단 순서도 원문 byline 대로 정정.
- 보강: **The Zen of Bluetooth Security** (Antonioli, WiSec 2026) `unverified` →
  `verified`. ACM DL 이 이 건은 CC-BY 라 전문이 열렸습니다. **확인 결과 1쪽 기조 발표
  초록이고, 분야 체계화가 아니라 연사 본인 논문 8편을 묶은 것**이며 ZOBS 원칙의 내용도
  초록에 없습니다. 이전 실행에서 제목만 보고 "Bluetooth 보안 전체 지형을 인용할 단일
  출처"라고 적어둔 것은 과대평가였으므로 **관련도를 보통 → 낮음으로 내렸습니다.**
  (의도적 하향이라 근거를 여기 남깁니다.) Channel Sounding·거리측정은 전혀 다루지 않습니다.
- 인용: 신규 3건을 기존 논문에 역참조 반영 — Olafsdottir 2017 / Leu 2020 / Abidin 2021 /
  Anliker 2023 → Rasmussen 2010, Anliker 2026 → FAST, Coppola 2025(LEO-Range) → PURE.
  인용 관계 126건.
- 표준: 변경 없음. Core Spec 최신은 여전히 6.3, Inline Phase Correction Term Transfer 는
  아직 VSr01_PR 초안, RAS/RAP 1.0 그대로. 802.15.4ab 도 공개 최신 초안이 D03(2025-09) /
  D04 로 상태 변화 없음. (참고: STMicroelectronics 가 Embedded World 2026 에서 첫
  802.15.4ab 칩군 ST64UWB 를 발표했으나 표준 문서 자체의 상태는 그대로.)
- 실패: **Leu 2021 "Security of Multicarrier Time-of-Flight Ranging"**(ACSAC, 관련도 높음)
  전문 확보 재실패. ETH Research Collection 에 해당 항목은 있으나 ORIGINAL 번들이 없어
  OA PDF 가 없고, ACM DL 은 유료, Semantic Scholar 에도 OA 링크 없음. `last_checked` 만
  갱신하지 않고 항목 자체를 손대지 않았습니다. **Zand 2019 BLE PBR**(관련도 높음) 도
  TU/e 리포지터리에 OA 없음. WiSec 2026 유료 3건(Timestamps Unchained / HardaBLE /
  BlueBrothers)과 CCS 2023 / WiSec 2021 도 ACM DL 유료 벽에 막혔습니다.

## 2026-08-10 (10차 후속: 신규 1건, 보강 3건 — 미검증 상위 항목 정리)

10차 보고에서 "다음 실행에서 팔 것"으로 남긴 네 건을 바로 처리했습니다. 셋은 끝났고
하나는 다시 막혔습니다.

- 보강: **Formal Analysis of BLE Secure Connection Pairing and Revelation of the PE
  Confusion Attack** (Shi 외, NDSS 2026) `unverified` → `verified`. NDSS 전문 무료라
  바로 확보. 6,400개 조합을 84개 pairing case로 줄여 Tamarin으로 전수 검증(서버 6대·
  컨테이너 20개, 약 5일). **핵심은 공격이 아니라 각 case별 '최소 보안 가정' 표**입니다 —
  CS 위협모델에서 "페어링은 안전하다고 가정한다"를 쓸 때 어떤 IO capability 조합에서
  그 가정이 서고 어떤 조합에서 무너지는지를 그대로 인용할 수 있습니다. 가장 강한 가정
  아래에서도 case 6–16 전부에서 LTK 인증이 위반된다는 점, 단방향 OOB는 기밀성+무결성을
  함께 요구한다는 점이 특히 CS 배치에 걸립니다. 영향 범위는 12개 pairing case, v4.2–v6.0.
  Bluetooth SIG가 2025-02-07에 영향을 확인했습니다. Zenodo 아티팩트도 기록.
- 신규: **Method Confusion Attack on Bluetooth Pairing** (von Tschirschnitz 외,
  IEEE S&P 2021, 관련도 보통, `verified`). PE confusion의 원형인데 코퍼스에 없었습니다
  (참고문헌 캐기로 발견, TUM에서 무료 전문). **사용자 연구 40명 중 단 한 명도 공격을
  눈치채지 못했고 37명(92.5%)이 페어링을 완성**시켰습니다. 프로토콜 내부 완화가 불가능해
  규격 변경이 필요하다는 결론이, CS Security Start의 암호적 뿌리를 무비판적으로 신뢰하면
  안 되는 근거가 됩니다. BLERP와 Stealtooth도 이 논문을 인용해 인용 3건 추가.
- 보강: **Assessing Localization Technologies for Pedestrian Collision Avoidance**
  (Varughese 외, arXiv 2026) `partial` → `verified`. 전문 확인 결과 **BTCS 맞습니다**
  (Nordic nRF54L15-DK 2대). CS를 UWB·GNSS와 같은 로봇 플랫폼에서 나란히 잰 옥외
  벤치마크로, 숫자가 아픕니다 — 개활지 LOS에서 BTCS RMSE 0.718 m 대 UWB 0.226 m,
  지붕 아래에서 BTCS 2.012–2.46 m로 벌어지는 동안 UWB는 0.49–0.63 m 유지.
  **다중경로가 CS를 UWB보다 훨씬 빨리 무너뜨린다**는 외부 근거입니다.
  다만 저자들이 CS 측정을 "TDoA 기반"이라 서술한 것은 규격(RTT+PBR)과 어긋나므로
  limitations에 명시해 두었습니다. 인용할 때 각주 필요.
- 실패: **Zand 2019 (WCNC)** 재시도 실패 — IEEE Xplore 유료, TU/e 연구 포털에 전문 파일
  없음, Semantic Scholar `openAccessPdf` 비어 있음, ResearchGate 로그인 요구. `partial` 유지.
- 실패: **Leu 2021 (ACSAC)** 재시도 실패 — ETH Research Collection이 스크래핑 차단으로
  "Access Restricted"를 반환하고 syssec.ethz.ch 직접 PDF는 404. 저자의 ETH 박사논문
  *Secure Ranging: Physical-Layer Attacks and Countermeasures*(2023)에 챕터로 실렸을
  가능성이 높다는 단서만 확보해 limitations에 남겼습니다. `partial` 유지.

다음 실행 후보(이번 참고문헌 캐기에서 나온 미추가 항목): Shi 외 *Formal Analysis and
Patching of BLE-SC Pairing*(USENIX Security 2023), Claverie 외 *Tamarin-based Analysis
of Bluetooth*(ESORICS 2023), Jangid 외 *Extrapolating Formal Analysis to Uncover Attacks
in Bluetooth Passkey Entry Pairing*(NDSS 2023).

## 2026-08-10 (10차: 신규 5건, 보강 2건 — Wi-Fi 보안 레인징 계보를 통째로 들여옴)

이번 회차의 발견은 검색이 아니라 **참고문헌 캐기**에서 나왔습니다. arXiv `cs.CR`
목록에서 걸린 ARES 2026 논문의 전문을 열었더니, 그 참고문헌에 코퍼스가 통째로
비워두고 있던 축이 드러났습니다 — **Wi-Fi FTM/802.11az 보안 계보**. CS와 같은
2층 구조(상위 협상·설정 + 하위 사운딩 파형)를 가진 인접 표준이고, 그쪽에서 이미
찾아낸 실패 양식이 CS 질문으로 거의 1:1 번역됩니다.

- 신규: **Secure Wi-Fi Ranging Today: Security and Adoption of IEEE 802.11az/bk**
  (Antonijević 외, ARES 2026, 관련도 높음, `verified`). 논리계층에서 WPA2/WPA3-Personal과
  standalone PASN이 특정 AP에 레인징을 결속하지 못함을 보이고, EDCA 모드 강등과
  Secure HE-LTF Required 미강제로 인한 조용한 다운그레이드를 정리합니다. 물리계층에서는
  20 MHz secure HE-LTF(122 비영 부반송파 × 64-QAM)를 부분 관측 + message-passing으로
  예측해 MUSIC ToF에 거리 편향을 유도합니다. zero-power GI의 스펙트럼 마스크 영향까지
  정량화(비보안 최악 +10.9 dB·초과 빈 6.7% → 보안 최악 +6.2 dB·초과 빈 31.6%).
  **802.11az를 표방한 개발보드조차 secure HE-LTF 미구현**이었다는 관찰이 특히 큽니다.
- 신규: **Here, There, and Everywhere: Security Analysis of Wi-Fi FTM**
  (Schepers·Singh·Ranganathan, WiSec 2021, 관련도 보통, `verified`). 시판 Wi-Fi 동글만으로
  2–20 m 구간을 평균오차 75 cm 이내로 스푸핑하고, 최종 응답 프레임 리플레이로 RTT를
  3.99 µs / 8.02 µs 줄여 598.62 m / 1,201.58 m를 축소합니다(기기당 1,000 세션).
  '데이터 복조는 최강 피크로, ToA는 back-search 창의 이른 피크로'라는 수신기 비결속이
  근본 원인이라는 지적이 CS의 CIR first-path 탐색에도 걸리는지가 다음 질문입니다.
- 신규: **Security of Multicarrier Time-of-Flight Ranging** (Leu 외, ACSAC 2021,
  관련도 높음, `partial`). '부반송파를 늘리면 심볼이 길어지고 긴 심볼은 ED/LC에 취약하다'를
  OFDM에 대해 정면으로 논증한 논문. Anliker 2026과 Antonijević 2026이 모두 출발점으로
  인용하는데 코퍼스에 없었습니다. Clulow 2006과 Anliker 2026 사이의 빠진 고리입니다.
- 신규: **Assessing Localization Technologies for Pedestrian Collision Avoidance**
  (Varughese 외, arXiv 2026, 관련도 보통, `partial`) — Bluetooth 6.0을 UWB·GNSS와
  같은 실험에서 벤치마크. BLE 6.0 레인징이 CS 기반인지 초록에 없어 원문 대조 필요.
- 신규: **A Relay a Day Keeps the AirTag Away** (Gegenhuber 외, arXiv 2026,
  관련도 낮음, `partial`) — 거리 검증이 없는 BLE 근접 서비스의 대조군.
- 보강: **So Near and Yet So Far** (Clulow 외, ESAS 2006) `unverified` → `verified`.
  4개 원칙 전문, 조기 판정(1/5 적분 → 4/5 비트시간 선점, SNR 진폭비 1/5), deferred bit
  signalling, 그리고 MICA2 사례(38.4 kbit/s → 1비트 26,042 ns = 공간상 7.8 km, 통신반경
  300 m를 수 km 조작; 8 MHz 클록 → 왕복 거리분해능 최소 20 m)까지 채웠습니다.
  DOI와 무료 전문(Wellesley 미러)도 확보.
- 보강: **Bluetooth Channel Sounding Evaluations and Improvements** (Lund MSc)
  `partial` → `verified`. 저자 확인(Siwei Jiang, u-blox 협업). 플랫폼은 **u-blox NORA-B2
  (Cortex-M33) + NORA-B206 EVK**. 핵심 관측은 **IQ 샘플의 NaN이 거리에 따라 증가**한다는
  것 — 75채널 프레임당 평균 4.9233개(4.15 m) → 6.9568개(12.06 m). 근거리 phase-slope /
  중장거리 CIR 하이브리드 전환(0.2 m 미만 클리핑)과 MCU 이식 제약(CMSIS-DSP)도 기록.
- 인용 관계: 새 노드 3개를 넣고 기존 논문을 다시 훑어 **12건**을 이었습니다.
  Clulow 2006 ← 9건(Staat 2022, Anliker 2023/2026, Leu 2020, Olafsdóttir 2017,
  Singh 2019 UWB-PR, Singh 2022 V-Range, Abidin 2021, Coppola 2025),
  Leu 2021 ← 2건, Schepers 2021 ← 1건. 인용 96건.
- 표준: 변경 없음. Core 6.3(2026-05-06) 이후 신규 릴리스 없음. CS Inline PCT Transfer는
  여전히 draft(채택일 미공개), IEEE P802.15.4ab는 IEEE SA에서 "Active PAR"로만 표시됩니다.
- 실패: **Leu 2021 ACSAC 전문 미확보** — ACM DL 403, ETH Research Collection 직접 PDF 없음,
  Semantic Scholar `openAccessPdf` CLOSED. 초록 기준으로만 기록하고 `partial`로 남겼습니다.

## 2026-08-04 (9차: 신규 0건, 보강 2건 — 거리 확대 계보를 verified로)

신규 논문은 없었습니다(전날 8차가 훑은 구간과 겹침). 대신 미검증으로 남아 있던
`estimation`·`defense` 두 항목을 전문 확인으로 `verified`까지 올렸습니다.

- 보강: **UWB-ED** (Singh 외, USENIX Security 2019) — 거리 확대 탐지의 원형.
  hardware/software/results/limitations 전면 채움. 2단계(Commitment+Verification)와
  에너지 분포 이진 가설검정, 규제 제약(PSD -41.3 dBm/MHz), 보안 수치(α=100에서
  r=2일 때 27% → r=8일 때 5.85%)까지. `distance-enlargement-blind-spot` 인사이트의 근거.
- 보강: **VAA 기반 BLE ToA/DoA** (Xie 외, arXiv 2026) — BLE two-way CFR의 이진 위상
  모호성을 신경망 다수결로 풀고 MUSIC으로 결합 추정. 시뮬레이션(SNR 5 dB 이상 CRLB 근접).
  CS PBR 추정기 계열(`spec-vs-implementation-debate`)과 이어짐.
- 표준: 변경 없음. 실패: 없음(둘 다 arXiv 전문 확보).
- 진행: `exp-estimator-threshold` 실험 완료 반영(추정기 문턱), 관련 todo done 처리.

## 2026-08-03 (8차: 신규 5건, 보강 4건 — PBR의 톤 축이 열림)

이번 실행에서 새로 생긴 축은 **"톤이 비거나 오염되면 PBR은 어떻게 되는가"** 입니다.
지금까지 코퍼스는 CS를 시간 축(ED/LC, RTT 조작)에서만 보고 있었는데, PBR이 균일
주파수 격자를 전제로 한다는 사실과 실제로는 광고 채널·블록리스트·Wi-Fi 때문에 그
전제가 깨진다는 사실이 세 편으로 연결되었습니다. 톤 하나가 오염되면 Q90 오차가
20 cm에서 4 m로 무너진다는 실측이 나왔고, 이는 신호를 위조하지 않고 잡음만 넣는
거리 확대 공격의 가능성을 뜻합니다. 세 논문 모두 간섭을 자연 현상으로만 다루므로
적대적 톤 선택은 비어 있습니다.

### 신규 논문

- 신규: Phase-Based Ranging in Narrowband Systems With Missing/Interfered Tones
  (IEEE IoT-J 2023, vol. 10, no. 17, pp. 15171–15185, 관련도 높음) — 전문 확인 완료.
  imec 계보(zand-2019 → abidin-2021)의 최신 노드. NXP KW36 야외 실측에서 Q90 오차가
  ToF 6 m 대 PBR-MUSIC 7.5 cm, nRF52833 유선 셋업에서 톤 39 간섭 시 NN 채널 복원이
  Q90 오차를 4 m → 20 cm로 개선(플래시 60.5 KB). `wieme-2025-cs-commercial-hw`가
  이 논문을 인용하고 있어 기존 항목의 `cites` 도 함께 갱신했습니다.
- 신규: BLE phase-based ranging: accuracy and capability under strong Wi-Fi interference
  (IJET 2025, 관련도 보통) — 전문 확인 완료. NXP KW38 + TP-Link 공유기 실측.
  Wi-Fi 간섭만으로 랜덤 오차가 5.4 cm → 17.7~18.4 cm(약 4배). 간섭 채널을 빼면
  공간 평활화를 못 써 MUSIC이 DFT로 퇴화한다는 구조적 함정을 저자가 명시.
- 신규: Joint Classification and Regression Deep Learning Model for Universal
  Phase-based Ranging in Multiple Environments (arXiv 2511.19891, 관련도 보통) —
  전문 확인 완료. 2NN 평균 RMSE 49 mm. 환경 분류기가 틀리면 거리 추정이 함께
  무너진다는 점이 NN 기반 CS 거리추정(wacsa-2025, pnn-2025)에도 같은 논리로 걸립니다.
- 신규: Joint single-shot ToA and DoA estimation for VAA-based BLE ranging with
  phase ambiguity (arXiv 2602.02503, 관련도 보통) — 초록만 확인, `partial`.
- 신규: Poster: Identifying Multipath in Phase-Based Ranging Measurements Using
  Channel Sounding (IEEE VNC 2024, 관련도 보통) — 서지정보만 확인, `unverified`.

### 보강

- 보강: LEO-Range (USENIX Security 2025) — `partial` → `verified`.
  hardware(R&S SMW200A / RTP164B, Keysight Propsim FS16), software, results(고앙각 LoS
  78 m 상한에 FRR 3%, NLoS 117 m에 9%; 저앙각 117 m에 4%, 195 m에 6%), limitations,
  artifacts(Zenodo), cites 8건을 원문에서 채웠습니다. 이 논문이 Bluetooth의 정규화
  교차상관·최소자승오차 대응책을 "최적 공격자에 대한 보안 증명이 없는 방식"으로
  분류한 대목이 NADM 계열 지표의 학술적 위치를 확정해 줍니다.
- 보강: UWB-PR (NDSS 2019) — `partial` → `verified`. hardware(802.15.4f 시제품,
  3db Access 지원), software(MATLAB 공격 시뮬레이션), results(93 m / 10 cm,
  802.15.4a coherent 20 m 축소 대 UWB-PR 1 m 미만, non-coherent 최대 2461.6 m),
  limitations(distance fraud 미방어), cites에 ranganathan-2012 추가.
- 보강: Lightweight NLOS Channel Detection for ML-assisted BLE DF (arXiv 2026) —
  `unverified` → `verified`. 저자 6인, hardware(u-blox XPLR-AOA-3 / ANT-B10 /
  NINA-B411 / C209, 그래핀 차단막), software(Scikit-learn, NKA, RFF),
  results(NKA가 선형 SVC 대비 7~14%p 개선, MLP 0.908, RFF+SVC 추론 0.009 s,
  AWGN 20 dB 주입 시 저하 1~3%p)를 채웠습니다.
- 보강: Vehicular Wireless Positioning: A Survey (arXiv 2026) — `unverified` →
  `verified`. 저자 12인, CS 서술 내용(HADM은 80 MHz RTT, PBR은 2.4 GHz 반송파 위상)과
  한계를 확인. 측위 전문가 12인의 대형 서베이가 CS에 한 문단만 쓰고 보안 논의는
  전무하다는 사실 자체가 빈칸의 근거가 됩니다.

### 표준

- 변경 없음. Core 6.3(2026-05-06)이 최신 adopted, RAS/RAP 1.0 유지,
  Channel Sounding Inline PCT Transfer는 여전히 Draft(VSr01_PR) 상태입니다.

### 실패

- USENIX Security 2026 technical sessions 페이지가 HTTP 403 — 목차 훑기 실패.
- NDSS 2026 accepted papers 페이지의 M–Z 구간을 WebFetch로 받았더니 존재하지 않는
  제목("Portable Executable …" 계열)이 대량으로 생성되어 폐기했습니다. 키워드
  필터 질의로 다시 받아 BLE 관련 3건만 확인했습니다. 목차 전체 훑기는 미완입니다.
- `zand-2019-ble-pbr`(관련도 높음, `partial`)은 이번에도 무료 전문 경로를 찾지 못해
  보강하지 못했습니다.

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
