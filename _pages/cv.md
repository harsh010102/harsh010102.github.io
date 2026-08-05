---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Munich, Germany · harsh.parikh@tum.de · [LinkedIn](https://www.linkedin.com/in/harshparikh2002/) · English (C2) · German (B1-B2)

AI researcher and venture scout with hands-on experience building production GenAI systems and evaluating deep-tech startups. My academic research, from LLM work at TUM to a multimodal AI pipeline built with Continental AG, trained me to tell genuine technical differentiation from well-packaged storytelling. I've since applied that same instinct to deal sourcing at NXP. Now looking for roles at the intersection of AI engineering, deep-tech VC, and impact.

Experience
======
**Working Student, Startup Innovation (CTO Office)**, NXP Semiconductors N.V. — Munich, Germany | Jun 2025 – present
* Ran deal flow scouts across 14 deep-tech verticals (electric mobility, modular robotics, AI chips, etc.), screening 380+ startups and shortlisting 4–5 high-fit candidates per topic (~15% pass rate) for internal stakeholder review and potential venture-client partnerships.
* Built AI-powered automation to manage deal flow pipelines and sync the investment database, cutting manual tracking overhead.
* Collaborated cross-functionally with internal stakeholders to validate startup-technology fit and advance high-potential partnerships from assessment to proof-of-concept stage.
* Represented NXP at key European deep-tech events (DeepTech Momentum, Hello Tomorrow, StartUP AUTOBAHN EXPO), sourcing live deal flow and benchmarking emerging technologies against NXP's strategic roadmap.

**Working Student, App Success**, Apaleo GmbH — Munich, Germany | Jan 2025 – May 2025
* Increased onboarding efficiency by 40% through the development of an AI chatbot integrated with Apaleo's API, enabling users to effortlessly set up their profile and use technical functionalities.
* Improved chatbot accuracy by 35% by writing and refining logic with hands-on programming, ensuring seamless implementation, reliable performance, and higher user adoption rates.

**Research Fellow**, Max Planck Institute for Software Systems — Saarbrücken, Germany | Jan 2023 – Oct 2024
* Designed and executed a satellite-imagery ML system for land cover detection (95% accuracy), building a novel proof-of-concept tool for disaster management and climate risk assessment.
* Engineered high-performance data infrastructure that cut model training time by 40%, enabling faster iteration across large-scale ML research pipelines.

**Research Intern**, Canadian Centre for Climate Change & Adaptation — Charlottetown, Canada | Jun – Nov 2022
* Improved groundwater forecasting accuracy by 30% using fine-tuned time-series models (FBProphet, GluonTS), contributing to climate resilience policy for the Government of Prince Edward Island.
* Partnered on 2 field projects driving a data-driven approach to provincial climate adaptation policy.
* Supported the Canadian Society for Bioengineering annual conference on "Agricultural Sustainability & Food Security through Precision Agriculture".

Projects
======
**AI Explainability Pipeline for Autonomous Vehicles**, TUM × Continental AG — Munich | June 2025
Built a multimodal pipeline generating real-time, natural-language explanations of AV driving decisions for passengers, to study trust and comfort (N=22 user study).
* Benchmarked 6 vision-language models (BLIP, CLIP, LLaVA 1.5, LLaMA 4, Kimi-VL) for driving-scene captioning; selected and deployed Kimi-VL based on speed/accuracy trade-offs.
* Built an LLM refinement layer (evaluated GPT-4o, Gemini 2.0 Flash, Claude 3.7 Sonnet) converting verbose captions into concise in-cabin explanations, with subtitle and TTS output modes.

**Measuring Creativity in LLMs**, Research Internship, TUM Social Computing Group — Munich | April 2026 – present
* Building LLM-CreativeBench, a platform evaluating convergent/divergent thinking and story continuation via OpenAI models, benchmarked against Project Gutenberg, SimpleStories, and Grimms' Fairy Tales corpora.
* Building an LLM-as-judge evaluation pipeline (Qwen, Gemma, Ministral) scoring unseen human creative-writing tasks with deterministic, reproducible linguistic-structure metrics.

**Master's Thesis — Machine Unlearning**, Chair of Responsible Data Science, TUM — Munich | May 2026 – present
* Building a rigorous benchmark for evaluating machine unlearning methods, applying mechanistic interpretability techniques (logit lens, tuned lens) to trace layer-wise token representations and pinpoint where sensitive information leaks within unlearned models.
* Benchmarked unlearning effectiveness against established frameworks (TOFU, MUSE, RWKU), exposing gaps between models that appear to forget and models that genuinely no longer encode the targeted information.
* Constructed an evaluation pipeline using the YAGO dataset of PII-sensitive entities, surfacing how current unlearning methods fail to fully eliminate retrievable private information at the representation level.

Education
======
**Technical University of Munich** | Oct 2024 – Sept 2026
* M.Sc. Artificial Intelligence in Society, GPA: 1.8
* Certification: Foundations of Financial Engineering (WorldQuant University)

**Nirma University** | July 2019 – Nov 2023
* B.Tech Instrumentation & Control Engineering, Minor: Computer Science
* Best Undergraduate Thesis Award (Top 5 / 80) · MITACS Globalink Research Award · Global Governance Impact Fellowship

Skills & Languages
======
* **AI/ML**: LLMs, LangGraph, RAG, vision-language models, mechanistic interpretability, PyTorch, TensorFlow, LangChain
* **Investment**: Deal sourcing & screening, market mapping, due diligence, investment memo drafting
* **Engineering**: Python, SQL, React, TypeScript, Git, REST APIs
* **Languages**: English (C2), German (B1-B2)

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
