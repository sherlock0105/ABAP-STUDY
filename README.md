# ZC505 ABAP 교육 프로그램 모음

> SAP ABAP 교육과정 실습 코드 전체 모음입니다.  
> ALV 기초부터 CDS View / AMDP / ADBC까지 단계별로 구성되어 있습니다.

---

## 폴더 구조 한눈에 보기

```
zc50501/
├── ZC505_SUB_01/   ALV 기초 (구석기 → 철기 → 기본형 → Color/Icon/Sort)
├── ZC505_SUB_02/   강의 노트 및 이전 기록 (SQL, 내부테이블, 구조체)
├── ZC505_SUB_03/   Function Group / FM 호출 / ALV Event + Popup
├── ZC505_SUB_04/   Edit ALV / DML / Toolbar Event
├── ZC505_SUB_05/   Tab Strip / Module Pool / BDC / CDS View (MP)
├── ZC505_SUB_06/   ALV Splitter Container
├── ZC505_SUB_07/   FOR ALL ENTRIES / Range / SUBMIT / Hotspot+Splitter
├── ZC505_SUB_08/   Field Symbol / Dynamic ALV / BDC
├── ZC505_SUB_09/   CDS View / AMDP / ADBC
└── ZC505_SUB_10/   개인 프로젝트 / 시험 / 복합 실습
```

---

## 파일 접미사 규칙

각 프로그램 폴더 안에는 Include 단위로 파일이 분리되어 있습니다.

| 접미사 | 역할 |
|--------|------|
| `_top` | 전역 데이터 선언부 (DATA, TYPE, CLASS DEFINITION) |
| `_s01` | Selection Screen 정의 |
| `_c01` | Local Class 구현부 (이벤트 핸들러 등) |
| `_o01` | PBO Module (화면 출력 전 처리) |
| `_i01` | PAI Module (사용자 입력 후 처리) |
| `_f01` | FORM 서브루틴 모음 (실제 로직의 핵심) |
| `screens/` | Screen Painter 화면 정의 (Module Pool 전용) |

---

## ZC505_SUB_01 — ALV 기초

> `cl_gui_alv_grid` 의 기본 사용법을 단계별로 익히는 시리즈.  
> "구석기 → 신석기 → 청동기 → 철기 → 기본형" 순서로 기능이 추가됩니다.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505rlect01` | Report Training 01 | 기본 SELECT + 리스트 출력 |
| `zc505rlect02~04` | 12월 강의 실습 시리즈 | Selection Screen, Radio Button |
| `zc505rlect05` | Selection Screen Training | PARAMETERS, SELECT-OPTIONS |
| `zc505rlect06` | Radio Button 실습 | RADIOBUTTON GROUP |
| `zc505rlect07` | 12월 12일 실습 | — |
| `zc505r0001` | ALV 구석기 01 | `WRITE` 리스트 출력 |
| `zc505r0002` | ALV 구석기 02 실습 | `WRITE` 기반 리스트 |
| `zc505r0003` | ALV 구석기 02 | `WRITE` 개선 |
| `zc505r0004` | ALV 신석기 01 | `REUSE_ALV_GRID_DISPLAY` FM 방식 |
| `zc505r0005` | ALV 신석기 실습 | `REUSE_ALV_GRID_DISPLAY` |
| `zc505r0006` | Group Idol | `REUSE_ALV_GRID_DISPLAY` 그룹핑 |
| `zc505r0007` | ALV 청동기 01 | `cl_gui_alv_grid` + Docking Container |
| `zc505r0008` | ALV 청동기 02 | FieldCatalog 수동 생성 |
| `zc505r0009` | ALV 청동기 03 실습 | FieldCatalog 실습 |
| `zc505r0010` | ALV 철기 | `LVC_FIELDCATALOG_MERGE` 자동생성 |
| `zc505r0012` | ALV 기본형 | Layout (`gs_layout`) 설정 |
| `zc505r0013` | ALV 기본형 실습 | Layout 실습 |
| `zc505r0014` | ALV 기본형 실습 02 | Module Pool 화면 연동 |
| `zc505r0015` | 12월 19일 실습 | ALV 종합 실습 |
| `zc505r0016` | 12월 19일 실습 2 | ALV 종합 실습 |
| `zc505r0017` | 12월 19일 실습 3 | ALV 종합 실습 |
| `zc505r0018` | 12월 19일 실습 4 | ALV 종합 실습 |
| `zc505r0019` | ALV Color / Icon / Sort / Total / Subtotal | `lvc_t_scol` 셀 색상, 아이콘 |
| `zc505r0020` | ALV Color 실습 | 행/셀 색상 설정 |
| `zc505r0021` | ALV Color 실습 2 | 색상 조건 분기 |
| `zc505r0022` | 12월 22일 ALV 실습 3 | 재고 관리 ALV |
| `zc505r0023` | Subtotal / Color / Cell Color | `gs_layout-grp_fld` 소계 그룹핑 |

---

## ZC505_SUB_02 — 강의 노트 / 이전 기록

> 강의 중 작성된 노트 프로그램입니다.  
> SQL 문법, 내부 테이블 개념, 구조체 등 ABAP 기초를 다룹니다.

| 프로그램 | 날짜/주제 | 핵심 내용 |
|----------|-----------|-----------|
| `zc505r_note_01` | 11월 21일 | ABAP 기초 첫 노트 |
| `zc505r_note_02~03` | 초기 실습 | 기본 DATA 선언, 테이블 구조 |
| `zc505r_note_04~05` | 11월 27일 | SELECT 기초 |
| `zc505r_note_06~08` | 11월 28일 | SELECT, JOIN |
| `zc505r_note_09~11` | 11월 29일 ~ 12월 1일 | SQL 심화, FOR ALL ENTRIES 개념 |
| `zc505r_note_12~15` | 12월 2일 ~ 4일 | LEFT OUTER JOIN, SQL 실습 |
| `zc505r_note_16~18` | 12월 4일 ~ | 실습 및 과제 |
| `zc505r_note_19~23` | 12월 8일 ~ 9일 | 내부 테이블 / 구조체 |
| `zc505r_note_24~28` | 12월 9일 ~ 10일 | 다양한 SELECT 패턴 |
| `zc505r_note_29~35` | 12월 10일 ~ 12일 | 종합 실습 |
| `zc505r_tomato1~4` | 개인 실습 | 토마토 시리즈 (커스텀 테이블 포함) |

---

## ZC505_SUB_03 — Function Group / FM / ALV Event + Popup

> Function Group 생성, FM 호출, ALV 이벤트(더블클릭/핫스팟/팝업)를 다룹니다.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505r0024` | Call Function | `CALL FUNCTION` 기본 사용 |
| `zc505r0025` | ALV with Get Function | FM으로 데이터 조회 후 ALV 표시 |
| `zc505r0027` | ALV Function Training | FM 활용 ALV |
| `zc505r0028` | Function Class Training | FM + Class 혼용 |
| `zc505r0029` | Function Class Training | **Function vs Method 비교** (`rb_func` / `rb_meth` 라디오버튼 분기) |
| `zc505r0030` | ALV with Custom Container | `cl_gui_custom_container` (Screen Painter 커스텀 컨트롤) |
| `zc505r0031` | ALV Event Training | **이벤트 핸들러 첫 등장** (`lcl_event_handler`, `SET HANDLER`) |
| `zc505r0032` | ALV Event Training | 이벤트 핸들러 실습 |
| `zc505r0033` | ALV Event Training | `DOUBLE_CLICK`, `HOTSPOT_CLICK` 이벤트 |
| `zc505r0034` | ALV Event Training 02 | 이벤트 심화 |
| `zc505r0035` | Production Order List | 생산오더 목록 ALV |
| `zc505r0036` | ALV Event Training 02 | 이벤트 실습 2 |
| `zc505r0037` | ALV Event Training 02 | **EKKO (구매발주) 조회 + FM** |
| `zc505r0038` | Bill of Material List | BOM 리스트 (Module Pool) |
| `zc505r0039` | ALV Event with Popup | **팝업 창 연동** (`POPUP_TO_CONFIRM` 등) |
| `zc505r0040` | ALV Event Popup Training | 팝업 실습 |
| `zc505r0041` | ALV Event with Popup Training | 멀티 스크린 팝업 (`CALL SCREEN`) |
| `zc505r0042` | ALV Event with Popup Training | 팝업 종합 실습 |
| `zc505r0043` | ALV Event Popup Training 03 | 팝업 고급 |
| `zc505r_pnote_01` | Program Function Group | **Function Group 생성 실습** |
| `zc505r_pnote_02` | Call Function | FM 호출 실습 |

---

## ZC505_SUB_04 — Edit ALV / DML / Toolbar Event

> ALV 편집 모드, 커스텀 테이블 CRUD(INSERT/UPDATE/DELETE), 툴바 커스터마이징.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505r0044` | Edit ALV Training (이벤트 없음) | ALV 편집 모드, Style 설정 (`lvc_t_styl`) |
| `zc505r0045` | Idol Member Management | 커스텀 테이블 CRUD 기초 |
| `zc505r0046` | DML no Event Training | `INSERT / UPDATE / DELETE` (이벤트 없음) |
| `zc505r0047` | DML Training no Event | DML 실습 |
| `zc505r0048` | DML Training no Event | DML 실습 |
| `zc505r0049` | DML Training no Event | DML 실습 |
| `zc505r0050` | CRUD Change 유효성 | 변경 유효성 검사 + `MODIFY` |
| `zc505r0051` | CRUD ALV with Change Event | **`DATA_CHANGED` 이벤트** |
| `zc505r0052` | DML Changed Event (코스트센터) | `DATA_CHANGED` 이벤트 실습 |
| `zc505r0053` | DML Training Event | DML + 이벤트 종합 |
| `zc505r0054` | ALV with Change Finished Event | **`DATA_CHANGED_FINISHED` 이벤트** |
| `zc505r0055` | DML Changed Event (코스트센터) | 코스트센터 정보 관리 |
| `zc505r0056` | ALV with Toolbar Event | **`TOOLBAR` 이벤트** (커스텀 버튼 추가) |
| `zc505r0057` | Toolbar Event Training | `TOOLBAR` + `USER_COMMAND` 이벤트 |
| `zc505r_dnote_01` | DML Training (강의노트) | DML 강의 노트 |
| `zc505r_dnote_02` | DML LOOP | LOOP 내 DML 패턴 |

---

## ZC505_SUB_05 — Tab Strip / Module Pool / BDC / CDS View(MP)

> Module Pool 프로그램 (Transaction Code 연동), Tab Strip, BDC, CDS View 연동.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505r0058` | **Tabstrip Training** | `CL_GUI_TABSTRIP` + Tab Strip 이벤트 |
| `zsapmzc505lect01` | Module Pool Training 01 | Module Pool 기초 (PBO/PAI) |
| `zsapmzc5050001` | Student Info Manager | Module Pool 실습 |
| `zsapmzc5050003` | Module Pool Training | Module Pool 실습 (커스텀 테이블) |
| `zsapmzc5050004` | Module Pool Training 02 | Module Pool 실습 2 |
| `zsapmzc5050005` | Text Edit Training | `CL_GUI_TEXTEDIT` 텍스트 편집기 |
| `zsapmzc5050006` | Module Pool Text Edit ALV | Text Edit + ALV 복합 |
| `zsapmzc5050007` | BDC Training | **Batch Data Communication** (`CALL TRANSACTION`) |
| `zsapmzc5050008` | BDC Training | BDC 실습 |
| `zsapmzc5050009` | CDS View Training (Module Pool) | **CDS View 데이터를 Module Pool에서 조회** |
| `zsapmzcexam01` | Production Order Info Mgmt | Module Pool 종합 시험 (생산오더 관리) |

---

## ZC505_SUB_06 — ALV Splitter Container

> 한 화면에 ALV를 2개 이상 배치하는 Splitter 레이아웃.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505r0059` | Splitter Container Training | **`cl_gui_splitter_container`** 기초 (2분할) |
| `zc505r0060` | Splitter Container with Event | Splitter + `HOTSPOT_CLICK` 이벤트 (헤더 클릭 → 하단 갱신) |

---

## ZC505_SUB_07 — FOR ALL ENTRIES / Range / SUBMIT / Hotspot+Splitter

> 고급 SELECT 패턴, 프로그램 간 데이터 전달, Splitter + Hotspot 복합 구성.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505rlect08` | FOR ALL ENTRIES Training | **`FOR ALL ENTRIES IN`** 원리 및 실습 |
| `zc505rlect09` | Range 응용 | `TYPE RANGE OF`, Range 테이블 동적 구성 |
| `zc505rlect10` | SUBMIT and ABAP Memory | **`SUBMIT ... AND RETURN`** + `EXPORT / IMPORT` |
| `zc505r0062` | Range + Splitter + Hotspot | **3분할 Splitter** + Range 조건 + Hotspot 클릭 하단 상세 조회 |
| `zc505r0063` | Submit 실습 | `SUBMIT` 프로그램 호출 실습 |

---

## ZC505_SUB_08 — Field Symbol / Dynamic ALV / BDC

> 런타임에 타입을 결정하는 동적 프로그래밍 기법.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505rlect11` | Dynamic Programming with Field-Symbol | **`FIELD-SYMBOLS <lft>`**, 동적 내부테이블 생성, 동적 ALV |
| `zc505rlect12` | BDC Training | BDC (`CALL TRANSACTION`) 실습 |

---

## ZC505_SUB_09 — CDS View / AMDP / ADBC

> ABAP 7.5 이상 신문법. CDS View 조회, HANA DB 직접 접근(AMDP/ADBC).

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505rlect14` | CDS View Report | **`@AccessControl.authorizationCheck`**, CDS SELECT |
| `zc505rlect15` | CDS Association Select | **CDS Association** (`$projection`, path expression) |
| `zc505rlect16` | ADBC Training | **`CL_SQL_CONNECTION`**, `CL_SQL_PREPARED_STATEMENT` |
| `zc505rlect18` | AMDP Training 01 | **`IF_AMDP_MARKER_HDB`** 인터페이스, SQLScript 기초 |
| `zc505r0064` | CDS View 실습 | CDS View 조회 (`FROM zc505cds0004`) |
| `zc505r0065` | CDS View 실습 2 | CDS View 심화 |
| `zc505r0066` | CDS View Training | CDS View + Module Pool 화면 연동 |
| `zc505r0067` | CDS View Training 02 | CDS View + ALV |
| `zc505r0068` | CDS ADBC Training 01 | **CDS View + ADBC 복합** |
| `zc505r0069` | CDS View Tab Training | CDS View + Tab Strip |
| `zc505r0070` | AMDP Training | **`zc505cl_amdp_02=>get_bkpf`** AMDP 메서드 호출 |
| `zc505r0071` | AMDP + ADBC + CDS | **3가지 복합** (AMDP 메서드 + ADBC 직접 쿼리 + CDS) |
| `zc505r0072` | ADBC + AMDP Training | ADBC + AMDP 비교 실습 |
| `zc505r0073` | Flight Info ALV | CDS View 기반 항공편 정보 ALV |
| `zc505r0074` | Edit ALV | CDS View 데이터 편집 ALV |

---

## ZC505_SUB_10 — 개인 프로젝트 / 시험 / 복합 실습

> 교육 과정의 최종 실습 및 개인 프로젝트.

| 프로그램 | 설명 | 핵심 기법 |
|----------|------|-----------|
| `zc505rlect13` | 신문법 (New Syntax) | **`@`inline data**, `LOOP AT ... INTO DATA(ls)`, `REDUCE` |
| `zc505rlect17` | ADBC 코드 샘플 | ADBC 레퍼런스 코드 |
| `zc505r0061` | Splitter Container Training | Splitter 종합 실습 |
| `zc505r0067_cds` | CDS View Training 02 | CDS View 추가 실습 |
| `zc505rexam01` | BOM Master 관리 | **시험 문제**: 자재명세서(BOM) 마스터 CRUD |
| `zc505rexam02` | New Syntax 실습 | **시험 문제**: 신문법 종합 실습 (FM `zc505fm_get_materials` 포함) |
| `zc505mango01` | CDS + AMDP (Fiori 연동) | CDS View + AMDP 복합 |
| `zc505ship` | Shipment Management | 출하 관리 (`zc505tship` 커스텀 테이블) |
| `zc505tomato01~03` | 개인 실습 시리즈 | 코스트센터 / 복합 ALV |
| `zc505tomanote01` | TEST | CDS View 테스트 |

---

## 기술 스택 분류 요약

| 기법 | 해당 프로그램 |
|------|--------------|
| **ALV (구식 FM)** | r0001~006 (구석기/신석기) |
| **ALV Grid (OOP)** | r0007~ (청동기 이후 전부) |
| **ALV Event Handler** | r0031~, r0051~, r0056~ |
| **ALV Splitter** | r0059, r0060, r0061, r0062 |
| **Module Pool** | zsapmzc505* 시리즈 |
| **Tab Strip** | r0058 |
| **Function Group** | r_pnote_01, r0024~029 |
| **FOR ALL ENTRIES** | rlect08, r0062 |
| **SUBMIT** | rlect10, r0063 |
| **Field Symbol (동적)** | rlect11 |
| **BDC** | rlect12, zsapmzc5050007~008 |
| **CDS View** | r0064~069, rlect14~15, SUB_10 |
| **AMDP** | r0070~072, rlect18, mango01 |
| **ADBC** | r0068, r0071~072, rlect16~17 |
| **DML (CRUD)** | r0044~057 |
