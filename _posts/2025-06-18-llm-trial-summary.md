---
title: "Gemma 1B로 한국어 파인튜닝 실험"
categories: 
  - 실험기록
  - Gemma
tags:
  - LLM
  - Gemma
  - 한국어 파인튜닝
layout: categories
---

## 실험 요약

- 모델: `google/gemma-1.1-1b-it`
- 데이터: 2만 건, 한국어
- 방식: LoRA + QLoRA (4bit)
- 결과: OOM 발생 → FP32 전환 후 해결

코드:
```python
model = AutoModelForCausalLM.from_pretrained(...)




