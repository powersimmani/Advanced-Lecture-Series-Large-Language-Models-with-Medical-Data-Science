# Lecture 2: Medical Data Preprocessing and Curation

## 📋 Overview

**Instructor:** Ho-min Park  
**Email:** homin.park@ghent.ac.kr | powersimmani@gmail.com

데이터 품질이 모델 성능의 80%를 결정합니다. 이 강의에서는 의료 데이터 전처리와 큐레이션의 핵심 기술을 학습합니다.

---

## 🎯 Learning Objectives

1. **임상 텍스트 처리**: PHI 제거, 텍스트 정규화, 약어 확장, 부정 탐지
2. **의료 온톨로지**: UMLS, SNOMED CT, ICD, RxNorm, LOINC 활용
3. **멀티모달 통합**: DICOM, HL7 FHIR, 생체신호 처리
4. **데이터 품질**: 품질 평가, 편향 탐지, 결측값 처리
5. **실습**: MIMIC-III 데이터 전처리 파이프라인 구축

---

## 📚 Lecture Structure

### Part 1: Clinical Text Processing Pipeline (슬라이드 3-10)
- De-identification Techniques
- PHI Detection and Removal
- Clinical Text Normalization
- Abbreviation Expansion
- Negation Detection
- Temporal Expression Extraction
- Section Segmentation

### Part 2: Medical Ontologies and Coding Systems (슬라이드 11-17)
- UMLS Metathesaurus
- SNOMED CT Hierarchy
- ICD-10/11 Coding
- RxNorm Drug Normalization
- LOINC Lab Values
- Entity Linking Techniques

### Part 3: Multimodal Data Integration (슬라이드 18-27)
- DICOM Image Handling
- HL7 FHIR Integration
- Waveform Signal Processing
- Lab Value Normalization
- Data Quality Assessment
- Bias Detection & Mitigation
- Missing Data Strategies
- Data Augmentation Techniques
- Pipeline Orchestration

### Hands-on & Best Practices (슬라이드 28-30)
- MIMIC-III Preprocessing
- Best Practices Checklist
- Summary & Next Steps

---

## 🔧 Key Tools & Libraries

### Text Processing
- **spaCy**: NLP 파이프라인
- **MedCAT**: 의료 개념 추출
- **NLTK**: 텍스트 전처리
- **Presidio**: PHI 탐지 및 제거

### Medical Ontologies
- **UMLS API**: 의료 용어 매핑
- **SNOMED CT Browser**: 개념 탐색
- **pyRxNorm**: 약물 정규화

### Data Processing
- **pydicom**: DICOM 파일 처리
- **fhirclient**: FHIR 리소스 접근
- **wfdb**: 생체신호 처리
- **pandas**: 데이터 프레임 조작

### Pipeline Orchestration
- **Apache Airflow**: 워크플로우 관리
- **Kubeflow**: ML 파이프라인

---

## 💡 Key Concepts

### PHI (Protected Health Information)
18가지 HIPAA 식별자:
- 이름, 주소, 날짜, 전화번호, 이메일, SSN, 의료기록번호 등
- Safe Harbor vs Expert Determination 방법

### Medical Coding Systems
- **ICD**: 질병 분류 (70,000+ 코드)
- **SNOMED CT**: 임상 용어 (350,000+ 개념)
- **RxNorm**: 약물 정규화
- **LOINC**: 검사 결과 코드 (96,000+)

### Data Quality Metrics
- **Completeness**: 완전성
- **Accuracy**: 정확성
- **Consistency**: 일관성
- **Timeliness**: 적시성

### Bias Types
- 인구통계 편향 (demographic bias)
- 선택 편향 (selection bias)
- 측정 편향 (measurement bias)
- 라벨 편향 (label bias)

---

## 📊 Practical Applications

### 1. Clinical Note Processing
```python
from presidio_analyzer import AnalyzerEngine
from presidio_anonymizer import AnonymizerEngine

# PHI 제거
analyzer = AnalyzerEngine()
anonymizer = AnonymizerEngine()

text = "Patient John Doe, MRN 123456"
results = analyzer.analyze(text, language='en')
anonymized_text = anonymizer.anonymize(text, results)
```

### 2. Abbreviation Expansion
```python
abbrev_dict = {
    'BP': 'blood pressure',
    'HR': 'heart rate',
    'MI': 'myocardial infarction'
}

def expand_abbreviations(text, abbrev_dict):
    for abbrev, expansion in abbrev_dict.items():
        text = text.replace(abbrev, expansion)
    return text
```

### 3. LOINC Mapping
```python
# Glucose measurement
loinc_code = '2339-0'  # Glucose [Mass/volume] in Blood
```

---

## 🎓 Best Practices Checklist

✅ PHI 완전 제거 확인  
✅ 약어 일관성 검증  
✅ 날짜/단위 표준화  
✅ 부정 표현 처리  
✅ 온톨로지 매핑  
✅ 결측값 처리  
✅ 이상치 탐지  
✅ 편향 평가  
✅ 품질 메트릭 계산  
✅ 문서화 완료  

---

## 📖 Additional Resources

### Documentation
- UMLS: https://www.nlm.nih.gov/research/umls/
- SNOMED CT: https://www.snomed.org/
- HL7 FHIR: https://www.hl7.org/fhir/
- LOINC: https://loinc.org/

### Datasets
- MIMIC-III: https://mimic.physionet.org/
- MIMIC-IV: https://physionet.org/content/mimiciv/

### Tools
- spaCy: https://spacy.io/
- MedCAT: https://github.com/CogStack/MedCAT
- Presidio: https://microsoft.github.io/presidio/

---

## 📂 Slide Files

총 30개의 슬라이드가 제공됩니다:

1. `L02_01_Title_Medical_Data_Engineering.html` - 타이틀 슬라이드
2. `L02_02_Lecture_Overview.html` - 강의 개요
3-10. Part 1: Clinical Text Processing
11-17. Part 2: Medical Ontologies
18-27. Part 3: Multimodal Data Integration
28-30. Hands-on & Best Practices

**슬라이드쇼 실행**: `lecture02_slideshow.html` 파일을 브라우저에서 열어주세요.

---

## 🚀 Next Lecture Preview

**Lecture 3: Advanced LLM Training**
- Fine-tuning strategies
- PEFT methods (LoRA, QLoRA)
- Instruction tuning
- RLHF and DPO

---

## 📧 Contact

**Ho-min Park**  
- Email: homin.park@ghent.ac.kr
- Email: powersimmani@gmail.com

---

*Last updated: November 2025*
