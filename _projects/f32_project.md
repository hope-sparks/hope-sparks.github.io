---
layout: page
title: Predictors of Reading (Dis)Ability
description: A set of studies aimed at developing an analytic pipeline for understanding the genetic and environmental contributions to reading ability and disablity.
img: assets/img/f32/f32.png
importance: 1
category: completed
related_publications: true
---

## Purpose

Reading ability is a complex neurocognitive skill that develops through interactions between **genetic, environmental, and behavioral factors**. Dyslexia, a common reading disorder, affects approximately 5–15% of children and has substantial heritability, yet its underlying mechanisms remain incompletely understood.

Traditional research approaches have several limitations:

1. Reading ability is often reduced to **single measures** (e.g., word reading)  
2. Genetic studies rely on **one-variant-at-a-time methods** (GWAS)  
3. Studies rarely integrate **genetic and non-genetic predictors**  

The goal of this project was to develop and apply a **comprehensive analytic pipeline** to identify predictors of reading (dis)ability by integrating:

- Multidimensional reading phenotypes  
- Genome-wide genetic data  
- Demographic, environmental, and behavioral factors  
- Machine learning methods  

---

## What is reading (dis)ability?

Reading is not a single skill—it reflects the integration of multiple component processes, including:

- Phonological processing  
- Word decoding  
- Language comprehension  
- Attention and cognitive control

Children with reading disorders may show different profiles:

- **Dyslexia** (decoding difficulties)  
- **Poor comprehension** (language-related deficits)  
- **Comorbid profiles** (both)

To better capture this complexity, we modeled reading ability as a **latent trait**, combining multiple reading measures into a single, theory-driven construct.

---

## What do we already know about predictors?

Reading (dis)ability arises from **interacting systems**, not isolated factors.

### Genetic influences
- Reading is **polygenic**, influenced by many small genetic effects  
- Known genes (e.g., *KIAA0319*, *DCDC2*) interact within biological pathways  
- Traditional GWAS often identifies **few significant SNPs** due to strict corrections

### Behavioral and demographic influences
- Language skills (vocabulary, receptive language)  
- Nonverbal IQ  
- Maternal education  
- Birth outcomes and environmental exposures

### Key gap
Most studies isolate these domains instead of modeling **their combined effects**—a limitation this project directly addresses.

---

## How we did it

### Data source: ALSPAC

We used the [Avon Longitudinal Study of Parents and Children (ALSPAC)](https://www.bristol.ac.uk/alspac/), a population-based birth cohort that includes genetic, behavioral, and environmental measures across development.

We used:

- Behavioral data from ages 7, 8, and 9  
- Genome-wide genetic data for thousands of participants 
- Survey data from birth and early life

Final analytic sample: **~3,232 children with complete genetic + behavioral data** 

---

### Integrated analytic pipeline

{% include figure.liquid loading="eager" path="assets/img/f32/fig-pipeline.jpg" title="" %}
*Note. Pipeline to identify predictors of reading ability.*

We developed a **four-step analytic pipeline**:

#### 1. Latent phenotype construction
- Used **confirmatory factor analysis (CFA)**  
- Combined multiple measures (word reading, spelling, comprehension)  
- Reduced measurement error and improved statistical power  

---

#### 2. SNP screening
- Combined:
  - Prior candidate gene findings  
  - Genome-wide association results  
- Identified a set of **informative SNPs for modeling**  

GWAS identified:
- **1 genome-wide significant SNP (rs181384543)** in *PTCHD1-AS* 

---

#### 3. Machine learning (Elastic Net)

We used **elastic net regression** to model many predictors simultaneously:

- Handles high-dimensional genomic data  
- Selects informative features  
- Captures correlated and interacting predictors 

Two models:
- SNP-only model  
- SNP + demographic/behavioral model  

---

#### 4. Pathway enrichment analysis

We mapped identified SNPs to genes and biological pathways:

- Identified overrepresented biological processes  
- Linked genetic findings to brain development mechanisms 

---

## What we learned

### 1. Reading ability is best modeled as a system

Using a latent phenotype:

- Improved detection of genetic signals  
- Reduced measurement error  
- Produced more stable and interpretable results 

---

### 2. Genetic effects are distributed and additive

- GWAS alone identified **1 significant SNP**  
- Elastic net identified:
  - **~62 SNPs (SNP-only model)**  
  - **~96 SNPs (combined model)** 

➡️ Insight: Reading ability reflects **many small genetic effects**, not monogenic origins {% cite lancaster_identifying_2020 %}.

---

### 3. Non-genetic factors dramatically improve prediction

- SNP-only model explained ~12% of variance  
- Full model explained ~32% of variance 

Important positive predictors included:
- Vocabulary (r ≈ .42)  
- Nonverbal IQ (r ≈ .31)  
- Receptive language (r ≈ .29)  
- Mother’s education (r ≈ .25) 

➡️ Insight: **Behavioral and environmental factors are essential**, not optional {% cite lancaster_identifying_2020 %}.

---

### 4. Biological pathways—not single genes—drive reading

We found enrichment in pathways related to:

- Neuron and dendrite development  
- Synaptic and postsynaptic structures  
- Learning and memory processes  

➡️ Reading ability emerges from **interconnected neural systems** {% cite lancaster_identifying_2020 %}.

---

### 5. Cognitive architecture differs by reading ability

From complementary analyses:

- Typical readers:
  - Attention influences reading **indirectly**  
- Children with reading disorders:
  - Attention directly influences reading comprehension 

➡️ Insight: The **structure of reading changes with impairment**, not just performance level {% cite lancaster_selective_2021 %}.

---

## Why this work matters

This project introduces a **new framework for studying complex developmental traits**:

✅ Moves beyond single-gene models  
✅ Integrates genetic + behavioral + environmental data  
✅ Uses machine learning to identify meaningful patterns  
✅ Improves phenotype definition using latent constructs  
✅ Links genetic findings to biological pathways  

### Broader implications

- Better early identification of children at risk  
- More precise, individualized intervention strategies  
- Improved theoretical models of reading development  
- Generalizable pipeline for other complex traits  

---

## Team & support

This work was supported by NIH F32 grant (1F32HD089674-01A1) to Dr. Hope Lancaster.

**Dr. Hope S. Lancaster**  
- Conceptualization, analyses, modeling, writing, funding  

**Mentorship team:**

- Dr. Jing Li — machine learning & AI  
- Dr. Shelley Gray — reading and language  
- Dr. Valentin Dinu — biostatistics  

---

## Posters & Downloads

**Comparison of two phenotypes to identify SNPs associated with poor reading**  
Lancaster, Dinu, & Li - ASHG 2018  
[Download the poster (PDF)](assets/pdf/ASHG_2018.pdf)  

**Predicting reading comprehension in children with different types of reading disorders**  
Lancaster, Li, & Gray - SSSR 2018  
[Download the poster (PDF)](assets/pdf/SSSR18.pdf)  

**Sparse machine learning model and pathway analysis suggest novel genetic associations with dyslexia**  
Lancaster, Liu, Dinu, & Li - BGA 2019  
[Download the poster (PDF)](assets/pdf/BGA_2019.pdf)
