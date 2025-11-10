# Lecture 12: Knowledge Distillation and Model Compression

## 강의 개요

**주제**: Efficient Medical AI: Compression for Clinical Deployment  
**슬라이드 수**: 30개  
**구성**: 3개 파트로 구성된 포괄적인 모델 압축 강의

---

## 📂 파일 구조

```
lecture12_slides/
├── index.html                                          # 슬라이드 목차 (여기서 시작하세요!)
├── L12_01_Title_Medical_Model_Compression.html         # 타이틀 슬라이드
├── L12_02_Compression_Overview.html                    # 압축 개요
│
├── Part 1: Knowledge Distillation (슬라이드 03-10)
│   ├── L12_03_Part1_Knowledge_Distillation.html
│   ├── L12_04_Teacher_Student_Framework.html
│   ├── L12_05_Soft_Target_Training.html
│   ├── L12_06_Temperature_Scaling.html
│   ├── L12_07_Feature_Distillation.html
│   ├── L12_08_Attention_Transfer.html
│   ├── L12_09_Progressive_Distillation.html
│   └── L12_10_Multi_Teacher_Distillation.html
│
├── Part 2: Quantization and Pruning (슬라이드 11-17)
│   ├── L12_11_Part2_Quantization_Pruning.html
│   ├── L12_12_INT8_INT4_Quantization.html
│   ├── L12_13_Mixed_Precision_Strategies.html
│   ├── L12_14_Structured_Pruning.html
│   ├── L12_15_Magnitude_Pruning.html
│   ├── L12_16_Lottery_Ticket_Hypothesis.html
│   └── L12_17_Dynamic_Sparsity.html
│
└── Part 3: Edge Deployment (슬라이드 18-30)
    ├── L12_18_Part3_Edge_Deployment.html
    ├── L12_19_Mobile_Health_Apps.html
    ├── L12_20_Wearable_Device_Models.html
    ├── L12_21_Point_of_Care_Systems.html
    ├── L12_22_Latency_Optimization.html
    ├── L12_23_Battery_Efficiency.html
    ├── L12_24_Model_Serving_Edge.html
    ├── L12_25_Performance_vs_Size_Tradeoffs.html
    ├── L12_26_Accuracy_Preservation.html
    ├── L12_27_Case_Study_Mobile_Diagnostics.html
    ├── L12_28_Hands_On_Compression.html
    ├── L12_29_Deployment_Strategies.html
    └── L12_30_Thank_You.html
```

---

## 🚀 사용 방법

1. **index.html 파일을 열어주세요** - 모든 슬라이드의 목차를 볼 수 있습니다
2. 원하는 슬라이드를 클릭하면 새 탭에서 열립니다
3. 각 슬라이드는 독립적으로 볼 수 있습니다

---

## 📋 강의 내용

### Part 1: Knowledge Distillation for Medical Models
- Teacher-Student 프레임워크의 이해
- Soft Targets와 Temperature Scaling
- Feature-level과 Attention-level 증류
- Progressive 및 Multi-Teacher 증류 기법

### Part 2: Quantization and Pruning
- INT8/INT4 정수 양자화
- Mixed Precision 전략
- Structured vs Unstructured Pruning
- Lottery Ticket Hypothesis
- Dynamic Sparsity 기법

### Part 3: Edge Deployment in Healthcare
- 모바일 헬스 앱 최적화
- 웨어러블 디바이스 제약사항
- Point-of-Care 시스템
- Latency 및 Battery 최적화
- 모델 서빙 전략
- 성능-크기 트레이드오프 분석
- 실제 사례 연구 및 실습

---

## 🎯 학습 목표

1. **모델 압축의 필요성 이해**: 의료 현장의 제약 조건과 압축의 중요성
2. **주요 압축 기법 습득**: Knowledge Distillation, Quantization, Pruning
3. **실전 배포 전략 학습**: 모바일, 웨어러블, POC 시스템 배포
4. **트레이드오프 분석**: 성능, 크기, 정확도의 균형점 찾기
5. **실무 적용 능력**: 실제 의료 AI 프로젝트에 적용 가능한 기술

---

## 💡 디자인 특징

- **일관된 디자인**: Lecture 1의 디자인 스타일을 완벽하게 재현
- **시각적 명확성**: 개념을 쉽게 이해할 수 있는 다이어그램과 비교 차트
- **의료 AI 특화**: 의료 분야에 특화된 예시와 사례 연구
- **반응형 레이아웃**: 다양한 화면 크기에서 최적화된 표시
- **인터랙티브**: 호버 효과로 사용자 경험 향상

---

## 🛠️ 기술 스택

- HTML5
- CSS3 (Flexbox, Grid)
- 반응형 디자인
- Aptos 폰트 (Segoe UI fallback)
- 브라우저 호환성: 모든 최신 브라우저 지원

---

## 📊 주요 시각 자료

각 슬라이드는 다음과 같은 시각 자료를 포함합니다:
- 📈 비교 차트 및 그래프
- 🎯 프로세스 다이어그램
- 💻 코드 예제
- 📱 디바이스 사양 비교
- ⚡ 성능 메트릭 시각화
- 🔄 워크플로우 다이어그램

---

## 🎓 대상 수강생

- 의료 AI/ML 엔지니어
- 모바일 헬스케어 개발자
- AI 모델 최적화에 관심 있는 연구자
- 엣지 AI 배포 담당자
- 의료 기기 소프트웨어 엔지니어

---

## 📝 추가 자료

강의와 함께 활용하면 좋은 자료:
- PyTorch Quantization Documentation
- TensorFlow Model Optimization Toolkit
- ONNX Runtime
- TensorFlow Lite
- Core ML Tools

---

## 📧 문의

강의 내용에 대한 질문이나 피드백은 강의 포럼이나 오피스 아워를 통해 문의해주세요.

---

## 📄 라이센스

이 강의 자료는 교육 목적으로 제작되었습니다.

---

**제작일**: 2025년 11월  
**버전**: 1.0  
**슬라이드 총 개수**: 30개
