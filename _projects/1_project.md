---
layout: page
title: ReAL‑E (Remote Adult Language – Experiment)
description: A friendly, at‑home way to study adult speech, language, and reading—built for accessibility, scale, and modern research.
img: assets/img/real-e/cover.jpg
importance: 1
category: ongoing
related_publications: true
---

**ReAL‑E** is a set of simple, online tasks designed so adults (ages 19–64) can contribute to language science **from home**, using their own computer and a pair of headphones. The goal is to make data collection more **inclusive**, **efficient**, and **scalable**—so we can answer bigger questions about communication and learning  {% cite lancaster2025enhancing %}. 

{% include figure.liquid loading="eager" path="assets/img/real-e/fig-what-is.jpg" title="What is ReAL‑E? A short, at‑home battery for speech, language, and reading." class="img-fluid rounded z-depth-1" %}

---

## Why build ReAL‑E?
Traditional, in‑person testing takes time, space, travel, and staff—barriers that can shrink who gets to participate. By moving carefully selected tasks online, we can **reach more people**, collect data **faster**, and enable **large‑scale studies** (including genetics) that would be impractical otherwise. 

{% include figure.liquid loading="eager" path="assets/img/real-e/fig-why.jpg" title="Why online? Broader reach, lower cost, faster studies." class="img-fluid rounded z-depth-1" %}

---

## What participants do
ReAL‑E currently includes:
- **Syllable repetition (DDK)** — a quick speech‑motor task  
- **Real‑word repetition** and **Nonword repetition** — listening + speaking tasks  
- **Word definitions** and **Following directions** — language tasks  
- **Irregular word spelling** and **Timed nonword reading**  — quick reading tasks

Early pilot testing showed healthy variability and sensible ranges across tasks (e.g., Real‑word repetition mean ≈ 92.33% ± 6.97; Irregular word spelling mean ≈ 78.00% ± 16.07; Following directions mean ≈ 77.86% ± 9.59) {% cite lancaster2025enhancing %}. These insights guided wording, timing, and interface tweaks. 

<div class="row">
  <div class="col-lg-8">
    {% include figure.liquid path="assets/img/real-e/fig-tasks-grid.jpg" title="A peek at the task battery" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-lg-4">
    {% include figure.liquid path="assets/img/real-e/fig-ux-metrics.jpg" title="Early performance snapshots from pilot testing" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    *Note.* DDK timing was referenced to classic time‑by‑count norms (Fletcher, 1972), while reading/language tasks used percent accuracy. We revised instructions (e.g., “repeat steadily”) and item sets based on user feedback. 
</div>


---

## How we built it
We identified tasks from the literature, adapted them for web delivery, and asked experts to review **face validity** before running user experience sessions. Technically, tasks were coded in **jsPsych** and hosted on **cognition.run**, with screening surveys in **REDCap**. 

{% include figure.liquid path="assets/img/real-e/fig-pipeline.jpg" title="Pipeline: literature → expert review → UX testing → revisions" class="img-fluid rounded z-depth-1" %}

**Expert feedback.** On a 5‑point scale across multiple criteria, experts gave supportive scores for several tasks (e.g., syllable repetition, nonword repetition, spelling) and flagged “following directions” as an area to improve. Overall averages: ~**3.29** (Adaptation), **3.48** (Effectiveness), **3.76** (Face validity).

**User feedback.** People called the experience “interesting” and “kinda fun,” and asked for clearer navigation, a shorter “following directions” task, and more flexible typing (backspace in spelling). We also noted strong interest in mobile access. 

<div class="row">
  <div class="col-lg-4">
    {% include figure.liquid path="assets/img/real-e/fig-expert-scores.jpg" title="Expert rating highlights" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-lg-8">
    {% include figure.liquid path="assets/img/real-e/fig-user-feedback.jpg" title="What users told us" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

---

## What we’ve learned so far

### Headphone quality: a pleasant surprise
When we compared **home earbuds** to **lab‑quality headphones**, we didn’t find meaningful performance differences for **nonword** or **real‑word** repetition—great news for at‑home testing. (Example: Nonword *t*(18)=−0.24, *p*=.810; Real‑word *t*(18)=1.12, *p*=.279.) Next up: looking at **internet speeds** and **individual differences**.

{% include figure.liquid path="assets/img/real-e/fig-headphones.jpg" title="Headphones vs. earbuds: performance looks similar for repetition tasks" class="img-fluid rounded z-depth-1" %}

### Do speech and language always travel together?
In a community sample, **human scoring** showed **weak correlations** among syllable repetition (DDK), irregular‑word spelling, and word definitions; **automated scoring** (edit distance and semantic similarity) confirmed minimal association (e.g., IWS–WD *r*≈−0.03). Together, results suggest a relative **dissociation** between speech‑motor, grapheme‑phoneme, and lexical‑semantic skills in typical adults. 

{% include figure.liquid path="assets/img/real-e/fig-associations.jpg" title="Speech–language associations: small in typical adults" class="img-fluid rounded z-depth-1" %}

---

## What’s next
- **Phase 2:** Fully online, broader recruitment, reliability, and item selection.  
- **Phase 3:** Validity, scale‑up, and building/training **automatic scoring** pipelines. 

{% include figure.liquid path="assets/img/real-e/fig-roadmap.jpg" title="Roadmap: Phase 2 → Phase 3" class="img-fluid rounded z-depth-1" %}

---

## Team & support
ReAL‑E is a collaboration across research, clinical, and technical teams, with support from **COBRE 5 P20 GM109023‑08 (Project 13)**. 

---

## Posters & downloads

**Do Self-Reported Language and Reading Skills Predict Performance on Remote Behavioral Tasks in Adults?**
Strait, Buttner, & Lancaster - Research Assisstant Flash Talks December 2025.
[Download the slides (PDF)](/assets/pdf/ra_flash_talks_2025.pdf)

**Impact of Headphone Quality on Remotely Delivered Repetition Tasks**  
Parks, Buttner, Fitzgerald, Bashford, & Lancaster — Conference poster March 2024. 
[Download the poster (PDF)](/assets/pdf/lancaster_2024_postdoc_symp.pdf)

**Associations Between Speech and Language Performance in Adults**  
Lancaster, Farzana, Parks, Fitzpatrick, Buttner, Bashford, & Parde — Conference poster November 2023.
[Download the poster (PDF)](/assets/pdf/Lancaster2023_NSLHA.pdf)
