---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: resume-biography-3
    id: bio
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  # Publications first. "Featured" is curated to the first-author /
  # co-first-author papers; the second list is the remaining co-authored
  # work. exclude_featured on the second list prevents any duplication.
  - block: collection
    id: papers
    content:
      title: First-Author & Co-First-Author Publications
      # Show every first/co-first paper at once (no "See all" link)
      count: 0
      filters:
        folders:
          - publications
        featured_only: true
      # Order the curated first/co-first list manually so published or
      # accepted papers appear before manuscripts still in review.
      sort_by: Weight
      sort_ascending: true
    design:
      view: citation
      columns: 1
  - block: collection
    id: copublications
    content:
      title: Co-Authored Publications
      text: ''
      # Show all at once; exclude the first/co-first set above (no duplicates)
      count: 0
      filters:
        folders:
          - publications
        exclude_featured: true
    design:
      view: citation
      columns: 1
  - block: markdown
    id: patents
    content:
      title: Patents
      text: |-
        **A method, device, medium and product for user phenotype identification based on hospital clinical data** (一种基于医院临床数据的用户表型识别方法、设备、介质及产品)

        Invention patent · China (CNIPA) · Application No. 202610660571.0 · *Filed, under substantive examination* · Inventor 2 of 2
    design:
      columns: '1'
  - block: markdown
    id: research
    content:
      title: 'Research Focus & Selected Contributions'
      subtitle: ''
      text: |-
        My research connects patient-level phenotypes, molecular mechanisms, and clinically evaluated AI. I build models and workflows around real biomedical questions, then test them with leakage-controlled, held-out designs and clinically meaningful endpoints.

        Selected contributions:
        - **Population-scale foundation modeling.** Built ukbFound from 2,781 traits in 502,118 UK Biobank participants. The model supported disease prediction, multimorbidity analysis, and patient stratification across 289 conditions; 53 disease cohorts contained subgroups with robust prognostic differences (*npj Digital Medicine*, 2026; co-first author).
        - **COPD progression and causal multi-omics.** Integrated GWAS, eQTL/pQTL, longitudinal lung-function outcomes, and single-cell and spatial evidence to prioritize SERPING1 as a COPD modulator (*Signal Transduction and Targeted Therapy*, 2026; co-first author). Ongoing work develops temporal foundation models for longitudinal multi-omics in COPD.
        - **Clinical LLM evaluation.** Co-led a five-arm, 350-patient randomized trial of real-time LLM support for HSCT discharge education (under review) and co-developed a debate-intelligence framework evaluated with benchmarks, clinicians, laypeople, and diagnostic dialogues (*Cell Reports Medicine*, 2026; co-first author).
        - **Clinical genomics infrastructure.** Developed production workflows spanning FASTQ-to-report WES analysis, SNP/Indel/CNV detection, ACMG interpretation, immunogenomics, inherited-disease panels, and clinician-facing Django visualization.

    design:
      columns: '1'
  - block: resume-experience
    id: experience
    content:
      username: me
    design:
      # Hugo date format
      date_format: 'January 2006'
  - block: resume-skills
    id: skills
    content:
      title: Skills
      username: me
  - block: markdown
    id: certifications
    content:
      title: Certifications & Licenses
      text: |-
        - Health Professional Qualification (Clinical Laboratory / Medical Testing), National Health Authority of China (2012).
        - Clinical PCR Laboratory Technician Certification, Fujian Provincial Clinical Laboratory Center (Sept 2020).
        - Bioinformatics Engineer Certification, ICT Support / ICTTT (Jan 2015).
    design:
      columns: '1'
  - block: resume-awards
    id: service
    content:
      title: Peer Review Service
      username: me
---
