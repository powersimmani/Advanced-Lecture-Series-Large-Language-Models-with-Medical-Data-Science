# Lecture 6: Chain-of-Thought for Clinical Reasoning

**Introduction to Biomedical Data Science**  
**Instructor:** Ho-min Park  
**Email:** homin.park@ghent.ac.kr | powersimmani@gmail.com

---

## 📋 Overview

This lecture covers Chain-of-Thought (CoT) prompting techniques for clinical reasoning with Large Language Models. Learn how to enable step-by-step medical reasoning, improve diagnostic accuracy, and apply advanced CoT methods to real clinical scenarios.

---

## 🎯 Learning Objectives

1. **Understanding CoT Prompting** - Learn the principles of chain-of-thought reasoning for medical applications
2. **Clinical Reasoning Process** - Master the systematic approach to diagnosis and treatment planning
3. **Advanced CoT Techniques** - Explore Tree of Thoughts, Graph of Thoughts, and Bayesian reasoning
4. **Real-World Applications** - Apply CoT to emergency triage, treatment planning, and clinical documentation
5. **Implementation Skills** - Build and evaluate CoT prompts for medical tasks

---

## 📚 Lecture Structure

### Part 1: Clinical Reasoning Fundamentals (Slides 3-10)
- Clinical Reasoning Process
- Diagnostic Reasoning Chains
- Zero-Shot and Few-Shot CoT
- Self-Consistency & Voting
- Reasoning Path Selection
- Medical Knowledge Integration

### Part 2: Advanced CoT Methods (Slides 11-17)
- Tree of Thoughts for Medical Reasoning
- Graph of Thoughts
- Differential Diagnosis Trees
- Bayesian Reasoning Integration
- Uncertainty Propagation
- Counterfactual Reasoning

### Part 3: Real Clinical Applications (Slides 18-30)
- Emergency Triage with CoT
- Treatment Planning Chains
- Drug Interaction Reasoning
- Lab Result Interpretation
- Clinical Note Generation
- Error Analysis & Verification
- Performance Comparison
- Case Studies
- Hands-on Implementation
- Best Practices Guidelines

---

## 🎓 How to Use

### Option 1: Full Slideshow (Recommended)
Open `lecture06_slideshow.html` in your browser for the complete interactive presentation.

**Navigation:**
- Arrow keys (← →) or Space bar to navigate
- Progress bar shows current position
- Keyboard hints appear on first load

### Option 2: Individual Slides
Open any `L06_XX_*.html` file directly in your browser to view specific topics.

---

## 🔑 Key Concepts

### Chain-of-Thought Prompting
- **Definition:** Prompting technique that elicits step-by-step reasoning from LLMs
- **Magic Phrase:** "Let's think step by step"
- **Benefits:** 15-80% accuracy improvement on complex medical reasoning tasks

### Clinical Applications
- **Diagnosis:** Generate systematic differential diagnoses with supporting evidence
- **Treatment Planning:** Evaluate options with risk-benefit analysis
- **Safety:** Identify drug interactions and contraindications
- **Documentation:** Create structured clinical notes with reasoning

### Advanced Techniques
- **Tree of Thoughts (ToT):** Explore multiple reasoning paths simultaneously
- **Self-Consistency:** Sample multiple solutions and vote for best answer
- **Bayesian Integration:** Combine prior probabilities with evidence
- **Uncertainty Quantification:** Manage and propagate diagnostic uncertainty

---

## 📊 Performance Metrics

**CoT vs Standard Prompting:**
- MedQA: 56% → 72% (+16%)
- PubMedQA: 68% → 81% (+13%)
- Clinical Diagnosis: 62% → 78% (+16%)
- Treatment Planning: 70% → 84% (+14%)

**Trade-offs:**
- 2-3x slower inference time
- Significantly higher accuracy
- More transparent and auditable
- Better error identification

---

## 💡 Best Practices

### DO:
✓ Use clear, explicit step labels  
✓ Reference clinical guidelines  
✓ Verify reasoning logic  
✓ Include safety checks  
✓ Test on diverse cases  

### AVOID:
✗ Vague instructions  
✗ Too many steps (>7-8)  
✗ Ignoring contradictions  
✗ Blind trust in output  
✗ Skipping validation  

---

## 🛠️ Implementation Example

```python
prompt = f"""
Patient: {patient_info}
Task: Provide differential diagnosis.
Let's think step by step:
1. Key symptoms and signs
2. Possible diagnoses
3. Tests to discriminate
4. Most likely diagnosis
"""

response = model.generate(prompt)
```

---

## 📖 Additional Resources

- **Research Paper:** "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models" (Wei et al., 2022)
- **Medical Benchmarks:** MedQA, PubMedQA, MMLU-Medical
- **Clinical Guidelines:** Evidence-based protocols from AHA, WHO, CDC
- **Implementation Tools:** LangChain, Guidance, DSPy for structured prompting

---

## ⚠️ Important Notes

1. **Clinical Validation Required:** All CoT outputs should be reviewed by qualified clinicians
2. **Not a Replacement:** CoT augments, does not replace, clinical judgment
3. **Safety Critical:** Always include safety verification steps
4. **Continuous Improvement:** Monitor errors and refine prompts iteratively

---

## 📝 Slide Index

1. Title Slide
2. CoT Medical Overview
3. **Part 1 Start:** Clinical Reasoning Fundamentals
4-10. Part 1 Content (7 slides)
11. **Part 2 Start:** Advanced CoT Methods
12-17. Part 2 Content (6 slides)
18. **Part 3 Start:** Real Clinical Applications
19-29. Part 3 Content (11 slides)
30. Thank You

**Total: 30 Slides**

---

## 🔗 Quick Links

- [Full Slideshow](./lecture06_slideshow.html)
- [Title Slide](./L06_01_Title_Clinical_Chain_of_Thought.html)
- [Contents Overview](./L06_02_Lecture_Contents.html)
- [Part 1 Start](./L06_03_Part1_Reasoning_Fundamentals.html)
- [Part 2 Start](./L06_11_Part2_Advanced_CoT_Techniques.html)
- [Part 3 Start](./L06_18_Part3_Clinical_Applications.html)
- [Thank You](./L06_30_Thank_You.html)

---

**Created:** November 2025  
**Design:** Consistent with Lecture 1 style (Aptos font, #1E64C8 blue theme, 960x540px slides)
