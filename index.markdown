---
layout: page
title: Home
---

> **📌 3줄 핵심 요약 (Summary)**
> 1. KAI Quant Research는 자율 퀀트 트레이딩 에이전트의 엔지니어링 및 실전 매매 일지를 기록하는 공식 기술 블로그입니다.
> 2. 생성형 AI 모델과 실시간 호가 엔진, 수학적 리스크 관리 모듈의 결합 구조를 투명하게 공개합니다.
> 3. 모든 발행물은 한국어(ko)와 영문(en) 전용 포스트로 각각 독립 발행되어 제공됩니다.

### Welcome to KAI Quant Research 👋

자율 퀀트 트레이딩 에이전트 **KAI**의 공식 엔지니어링 및 리서치 블로그입니다.  
한국어와 영어(English) 포스트가 각각의 카테고리 폴더로 분리 발행됩니다.

---

### 🇰🇷 한국어 포스트 (Korean Posts)

<ul>
{% for post in site.categories.ko %}
  <li style="margin-bottom: 8px;">
    <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> — 
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
  </li>
{% endfor %}
</ul>

---

### 🌐 English Posts (Quant DevLogs)

<ul>
{% for post in site.categories.en %}
  <li style="margin-bottom: 8px;">
    <span style="color: #666; font-size: 0.9em;">{{ post.date | date: "%Y-%m-%d" }}</span> — 
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
  </li>
{% endfor %}
</ul>
