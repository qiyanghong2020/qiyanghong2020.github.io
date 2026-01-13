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
  - block: markdown
    content:
      title: 'Research & Projects'
      subtitle: ''
      text: |-
        PhD candidate in Medical AI at the Institute of Basic Medical Sciences, Peking Union Medical College & Tsinghua University School of Medicine. I work on foundation models, LLMs, multimodal and temporal modeling for clinical AI, deep phenotyping, and model interpretability.

        Selected projects:
        - Temporal foundation models for COPD progression (National Science and Technology Major Project, Youth Scientist Program, 2025-2028).
        - Biomedical foundation model on UK Biobank (>500,000 participants) for disease prediction, multimorbidity analysis, and patient stratification across 289 conditions.
        - Automated clinical WES analysis pipeline from FASTQ to SNP/Indel/CNV detection, annotation, ACMG classification, and reporting.
        - Neoantigen prediction and immunogenomics pipeline integrating WES and RNA-seq with NetMHC/MHCflurry.
        - WES clinical interpretation and visualization platform (Django) for variants, coverage, CNVs, and Sanger traces.
        - Consumer genomics analysis framework plus inherited disease and metabolic panel pipelines (thalassemia, SMA, mitochondrial disorders, mtDNA).
        - Custom WES probe design optimization for pathogenic ClinVar regions.
        - High-throughput transcriptomics analysis with differential expression and KEGG/GO enrichment.
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: citation
      columns: 1
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
      columns: 1
---
