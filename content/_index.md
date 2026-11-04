---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '3rem'

sections:
  - block: resume-biography-3
    id: bio
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      subtitle: 'Machine Learning for Disease Risk & Progression'
      text: ''
      headings:
        about: 'About'
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
      title: Recent First-Author & Co-First-Author Publications
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
  - block: markdown
    id: copublications
    content:
      title: Recent Co-Authored Publications
      text: |-
        **Deep multi-omics profiling reveals three molecular subtypes of chronic obstructive pulmonary disease in a unique biomass-exposed Chinese population.** *Med* (2026). [Publication details](/publications/deep-multi-omics-copd-subtypes/)

        **Genetic determinants of gene expression noise and its role in complex trait variation.** *Cell Reports* (2025). [Publication details](/publications/cell-reports-gene-expression-noise/)

        [Selected publication details](/publications/) · [Google Scholar](https://scholar.google.com.hk/citations?user=1PCtyx8AAAAJ&hl=en)
    design:
      columns: 1
  - block: markdown
    id: research
    content:
      title: 'Recent Research Projects'
      subtitle: ''
      text: |-
        **ukbFound.** Independently developed, built, and evaluated a machine-learning model using deep phenotyping data from more than 500,000 UK Biobank participants. The study explored disease risk prediction and multimorbidity, and identified distinct patient subgroups in 289 diseases (npj Digital Medicine, 2026).

        **Medical language model evaluation.** Contributed to data acquisition, curation, and analysis for evaluating collaborative language models on medical questions and clinical reasoning tasks.

        **COPD and lung function decline.** Contributed to multi-omics studies integrating genetic, protein, metabolite, and clinical data to investigate molecular subtypes and longitudinal disease progression.

    design:
      columns: '1'
  - block: resume-experience
    id: experience
    content:
      username: me
    design:
      # Hugo date format
      date_format: 'January 2006'
  - block: markdown
    id: skills
    content:
      title: Technical Skills
      text: |-
        **Biomedical Data Science:** Analysis of clinical and cohort data, longitudinal health modeling, and evaluation and interpretation of models for disease risk prediction.

        **Bioinformatics & Statistical Analysis:** Multi-omics, genomic and transcriptomic data analysis; survival analysis, multiple-testing correction, and resampling methods.

        **Programming & analysis:** Python, PyTorch, statistical and survival analysis, and reproducible workflows.
    design:
      columns: '1'
  - block: markdown
    id: patents
    content:
      title: Patent Application
      text: |-
        **A method, device, medium and product for user phenotype identification based on hospital clinical data** (一种基于医院临床数据的用户表型识别方法、设备、介质及产品)

        Invention patent application · China (CNIPA) · Application No. 202610660571.0 · *Filed May 13, 2026; application accepted May 14, 2026* · Inventor 2 of 2
    design:
      columns: '1'
  - block: markdown
    id: service
    content:
      title: Peer Review Service
      text: |-
        **Independent peer reviewer (as of November 4, 2026):** Submitted 14 review reports on 13 manuscripts for seven journals, including the Journal of Medical Internet Research, JMIR AI, and JMIR Medical Informatics. Two further reviews are in progress.

        **Co-reviewer (with Prof. Erping Long):** Nature Medicine; Nature Biomedical Engineering; Frontiers in Aging Neuroscience.
    design:
      columns: '1'
---
