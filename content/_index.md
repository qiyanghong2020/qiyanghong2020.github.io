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
    design:
      view: citation
      columns: 1
  - block: collection
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
    id: research
    content:
      title: 'Research & Projects'
      subtitle: ''
      text: |-
        PhD candidate in Medical AI at the Institute of Basic Medical Sciences, Peking Union Medical College & Tsinghua University School of Medicine. I work on foundation models, medical LLM evaluation, multimodal and temporal modeling, deep phenotyping, and clinical bioinformatics pipelines for precision medicine.

        Selected projects:
        - Temporal foundation models for COPD progression (National Science and Technology Major Project, Youth Scientist Program, 2025-2028).
        - Biomedical foundation model on UK Biobank deep phenotyping (>500,000 participants), now online in *npj Digital Medicine* (2026), for disease prediction, multimorbidity analysis, and patient stratification across 289 conditions.
        - Automated clinical WES analysis pipeline from FASTQ to SNP/Indel/CNV detection, annotation, ACMG classification, and reporting.
        - Neoantigen prediction and immunogenomics pipeline integrating WES and RNA-seq with NetMHC/MHCflurry.
        - WES clinical interpretation and visualization platform (Django) for variants, coverage, CNVs, and Sanger traces.
        - Consumer genomics analysis framework plus inherited disease and metabolic panel pipelines (thalassemia, SMA, mitochondrial disorders, mtDNA).
        - Custom WES probe design optimization for pathogenic ClinVar regions.
        - High-throughput transcriptomics analysis with differential expression and KEGG/GO enrichment.
    design:
      columns: '1'
  - block: resume-experience
    id: experience
    content:
      username: me
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
  - block: resume-skills
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
    content:
      title: Peer Review Service
      username: me
---
