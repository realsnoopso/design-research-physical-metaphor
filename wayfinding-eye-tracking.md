# 🧭 Wayfinding & Eye Tracking in Spatial UI

**Wayfinding = 시각적 주의의 흐름**

공간 디자인에서 사람들이 어떻게 길을 찾고, 무엇을 보는지에 대한 연구.

---

## 📚 핵심 논문

### ⭐ iTrace: Click-Based Gaze Visualization on Apple Vision Pro (Aug 2025)

**arXiv:** https://arxiv.org/html/2508.12268v1  
**저자:** Technical University of Munich  
**날짜:** August 2025

#### 핵심 문제

**Apple Vision Pro의 딜레마:**
- ✅ 매우 정확한 eye tracking (VR 기기들보다 더 정확)
- ❌ Privacy 정책으로 raw gaze data 접근 불가
- → 연구자들이 시선 추적 연구를 못 함

#### iTrace 솔루션

**Click-based Gaze Extraction** (클릭 기반 시선 추출)

3가지 방법:
1. **Pinch Gesture** (손가락 집기) - 0.45 clicks/s
2. **Dwell Control** (응시 제어) - 자동이지만 느림
3. **Gaming Controller** (8BitDo) ⭐ - 14.22 clicks/s (가장 빠름!)

#### 두 가지 핵심 기능

**1. Video Eye Tracking**
```
[사용자] → [비디오 시청]
    ↓
 [시선 추적]
    ↓
 [Heatmap on video]
```

**응용:**
- 강의 영상: 학생들이 어디에 집중하는가?
- 광고: 어떤 요소가 눈길을 끄는가?

**발견:**
- 강의 영상: 집중된 focus (특정 영역)
- 문제 풀이: 넓은 scanning (전체 화면)

**2. Spatial Eye Tracking** ⭐ (Wayfinding 핵심!)
```
[사용자] → [실제 환경 돌아다님]
    ↓
 [환경 녹화 + 시선 추적]
    ↓
 [3D heatmap on real space]
```

**응용:**
- **건축 디자인**: 공간 배치 최적화
- **전시 디자인**: 사람들이 어디를 보는가?
- **소매점**: 어떤 진열대가 시선을 끄는가?
- **공항/역**: Wayfinding 표지판 배치

---

## 🏗️ Wayfinding의 시각적 메타포

### 현실 세계 메타포

**1. 자연스러운 시각적 계층**
```
멀리 보임 (지평선, 랜드마크)
    ↓
중간 (표지판, 안내판)
    ↓
가까이 (바닥, 문)
```

**2. Visual Landmarks (시각적 랜드마크)**
- 높은 것 = 멀리서도 보임
- 대비되는 색 = 눈에 띔
- 움직임 = 주목

**3. Depth Cues for Distance**
- 크기 (가까운 것 = 크게)
- 선명도 (가까운 것 = 선명)
- 겹침 (앞에 있는 것이 뒤를 가림)

---

## 🎯 Wayfinding 연구 응용

### Bianconi et al. (2019) - VR 건축 연구

**실험 설정:**
- 실제 캠퍼스 건물을 VR로 재구성
- HTC Vive + eye tracking
- 사용자들이 VR 속 건물을 탐험

**목표:**
> "사람들이 복잡한 건축 환경을 어떻게 인지하고 navigate하는가?"

**방법:**
1. 사용자가 VR 건물 속을 돌아다님
2. 시선 추적 (어디를 보는가?)
3. **3D heatmap을 VR 환경에 직접 임베딩**

**발견할 수 있는 것:**

**건축가/디자이너 관점:**
- 사람들이 **어디를 주로 보는가?**
  - 표지판? 문? 창문? 복도 끝?
- **Spatial layout이 최적화되었는가?**
  - 길 찾기가 쉬운가?
  - 시각적으로 복잡한가?
- **Wayfinding에 도움이 되는 요소?**
  - 어떤 시각적 단서가 효과적인가?
  - 어디에 표지판을 두어야 하는가?
- **Visual comfort**
  - 어디가 불편한가?
  - 어디가 혼란스러운가?

---

## 💡 iTrace로 검증 가능한 가설

**가설 예시:**
> "높은 위치의 표지판이 wayfinding에 더 효과적이다"

**검증 과정:**
1. VR 건물에 다양한 높이의 표지판 배치
2. iTrace로 사용자 시선 추적
3. Heatmap 분석
4. 결과: 실제로 높은 표지판을 더 자주/빨리 보는가?

---

## 🎨 실제 응용 시나리오

### 시나리오 1: 박물관 디자인
```
1. 새 전시관 디자인
2. Vision Pro로 프리뷰
3. 사람들이 어디를 보는지 추적
4. 작품 배치 최적화
5. 실제 건설 전에 검증!
```

### 시나리오 2: 공항 표지판
```
1. 승객이 Vision Pro 착용
2. 공항 돌아다님
3. 어디서 길을 잃는가?
4. 어떤 표지판을 놓치는가?
5. 표지판 재배치/재디자인
```

### 시나리오 3: 소매점 레이아웃
```
1. 고객 동선 파악
2. 어떤 진열대를 주목하는가?
3. 시선이 머무는 위치
4. 주요 상품 배치 최적화
```

---

## 🔑 핵심 인사이트

**Wayfinding = 시각적 주의의 흐름**

좋은 wayfinding:
1. **자연스러운 시선 흐름** 유도
2. **중요한 순간에 시각적 단서** 제공
3. **인지 부하 최소화** (찾기 쉽게)

iTrace가 보여주는 것:
- 사람들의 **실제** 시선 흐름
- **디자이너의 의도 vs. 사용자의 실제 행동**
- 어디서 **혼란**이 발생하는가

---

## 📊 정확도

**iTrace 성능:**
- Gaze precision: 91%
- Data collection rate (controller): 14.22 clicks/s
- Apple Vision Pro eye tracking: VR 기기 중 최고 수준

---

## 🌐 관련 연구

### 기존 Eye Tracking 방법

**1. Webcam-based (Kaduk et al., 2024)**
- 장점: 접근성 높음
- 단점: 정확도 낮음, 움직임 제한

**2. Eye-tracking Glasses (MacInnes et al., 2018)**
- Pupil Labs, SMI ETG, Tobii
- 장점: 실세계 환경, 자유로운 움직임
- 단점: 3D 매핑 복잡

**3. HMD (Huang et al., 2024)**
- HTC Vive Pro Eye, Apple Vision Pro
- 장점: 높은 정확도, 가상+실세계
- Vision Pro: SMI ETG2, Tobii Pro 2보다 정확

---

## 🎯 시각적 메타포 관점

**기존:**
- iOS gesture: 2D 터치
- Dynamic Island: 2D 화면에 물리 법칙

**iTrace:**
- **3D 공간에서의 시각적 주의**
- 실제 세계 공간 디자인에 **데이터 기반 검증** 가능

---

## 📚 참고 문헌

1. **iTrace: Click-Based Gaze Visualization on Apple Vision Pro**
   - Berrezueta-Guzman, S., & Wagner, S. (2025)
   - https://arxiv.org/html/2508.12268v1

2. **Wayfinding and spatial legibility in VR**
   - Bianconi, F., et al. (2019)
   - HTC Vive eye tracking in campus building VR

3. **Eye-tracking accuracy on Apple Vision Pro**
   - Huang, H., et al. (2024)
   - Vision Pro vs. SMI ETG2, Tobii Pro 2

4. **Eye tracking for architects and designers**
   - Chrześcijańska (2024)
   - Tobii glasses for floor plan analysis

---

**작성일:** 2026-03-02  
**주제:** Wayfinding, Eye Tracking, Spatial UI, Apple Vision Pro
