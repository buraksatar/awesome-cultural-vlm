# Awesome Cultural VLM [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Benchmarks, datasets and studies of cultural and geographic robustness in vision-language models: image, video, text-to-image and text-to-video.

A vision-language model can name a dish, a dance or a festival and still miss what the image means to the people in it. This list collects the resources that measure that gap and the work that tries to close it. Text-only cultural NLP is covered by [awesome-cultural-nlp](https://github.com/simran-khanuja/awesome-cultural-nlp); this list is its visual counterpart.

Every entry was checked one by one on 16 September 2026: the paper link, the venue, whether the data is public, and what it covers. Entries are newest first within each section. *No public data yet* means the paper exists but the artifact has not been released; *gated* means a Hugging Face agreement is required. The maintained version of this list, with commentary, lives at [buraksatar.github.io/resources](https://buraksatar.github.io/resources/); this repository is the place to contribute.

## Contents

- [Southeast Asia](#southeast-asia)
- [Multi-country VQA and cultural knowledge](#multi-country-vqa-and-cultural-knowledge)
- [Country and region VQA and cultural knowledge](#country-and-region-vqa-and-cultural-knowledge)
  - [South Asia](#south-asia)
  - [East Asia](#east-asia)
  - [Middle East and North Africa](#middle-east-and-north-africa)
  - [Africa](#africa)
- [Visual reasoning, grounding and retrieval](#visual-reasoning-grounding-and-retrieval)
- [Norms, values and safety](#norms-values-and-safety)
- [Memes, humor, art and heritage](#memes-humor-art-and-heritage)
- [Captioning, translation and transcreation](#captioning-translation-and-transcreation)
- [Video understanding](#video-understanding)
- [Text-to-image and text-to-video generation](#text-to-image-and-text-to-video-generation)
- [Geographic robustness of visual recognition](#geographic-robustness-of-visual-recognition)
- [Models, training data and adaptation methods](#models-training-data-and-adaptation-methods)
- [Analyses, position papers and surveys](#analyses-position-papers-and-surveys)
- [Foundational reading](#foundational-reading)
- [By region](#by-region)
- [Related lists](#related-lists)

## Southeast Asia

Everything on this list that is built from Southeast Asian images, videos or prompts, whatever the task. Neighboring traditions here share surface features (rice, water, gold, drums), so fine-grained discrimination is the test.

- [Cultural Moment Benchmark](https://arxiv.org/abs/2608.23065) - Three-stage video benchmark of 306 expert-curated cultural concepts from seven Southeast Asian countries: naming, recognizing among video moments, and temporal localization. EMNLP 2026 Main. Maintainer's own work. [Data](https://huggingface.co/datasets/Multimedia-SMU/culturalmoment-benchmark) [Code](https://github.com/culturalmoment-benchmark/culturalmoment-benchmark.github.io) [Project](https://culturalmoment-benchmark.github.io/)
- [GG-EZ](https://arxiv.org/abs/2604.11490) - Regional data filtering plus model merging to adapt LVLMs, SDXL and SigLIP-2 to Southeast Asia, gaining 5 to 15 percent in cultural relevance. arXiv, 2026. [Data](https://huggingface.co/collections/SEACrowd/sea-vl-phase-2-multimodal-vision-language-models-for-sea)
- [Rice-VL](https://arxiv.org/abs/2512.01419) - ASEAN cultural VQA benchmark: 7,000 images, over 28,000 expert-annotated questions and 1,000 grounding boxes across 11 countries and 14 categories. arXiv, 2025. No public data yet.
- [SEA-VL](https://arxiv.org/abs/2503.07920) - Compares crowdsourcing, crawling and synthetic generation to build 1.28M culturally relevant Southeast Asian images with captions across 11 countries. ACL 2025 Main. [Data](https://huggingface.co/collections/SEACrowd/sea-vl-multicultural-vl-dataset-for-southeast-asia-67cf223d0c341d4ba2b236e7) [Code](https://github.com/SEACrowd/sea-vl-experiments) [Project](https://seacrowd.github.io/seavl-launch/)
- [Seeing Culture](https://arxiv.org/abs/2509.16517) - Two-stage benchmark: multiple-choice VQA with image options then segmentation of the cultural artifact, 1,065 images, 138 artifacts, 3,178 questions, seven Southeast Asian countries. EMNLP 2025 Main. Maintainer's own work. [Data](https://huggingface.co/datasets/Multimedia-SMU/seeingculture-benchmark) [Code](https://github.com/buraksatar/seeingculture) [Project](https://seeingculture-benchmark.github.io)
- [VietMEAgent](https://arxiv.org/abs/2511.09058) - Vietnamese cultural VQA method pairing cultural object detection, program generation and a knowledge base for dual-modality explanations, with a 28,484-sample dataset over 12 categories. arXiv, 2025. [Data](https://huggingface.co/datasets/Dangindev/viet-cultural-vqa)
- [SEA-VQA](https://aclanthology.org/2024.alvr-1.15/) - 1,999 four-way questions on 515 UNESCO cultural heritage images from 8 Southeast Asian countries; GPT-4 and Gemini drop versus A-OKVQA. ACL 2024 Workshop (ALVR). [Data](https://huggingface.co/datasets/wit543/sea-vqa) [Project](https://wit543.github.io/sea-vqa)
- [SEACrowd](https://arxiv.org/abs/2406.10118) - Data hub of 498 datasheets and 399 dataloaders for Southeast Asian languages across text, image and audio, with a benchmark on 13 tasks. EMNLP 2024 Main. [Data](https://github.com/SEACrowd/seacrowd-datahub) [Code](https://github.com/SEACrowd/seacrowd-experiments) [Project](https://seacrowd.org/seacrowd-catalogue/)

## Multi-country VQA and cultural knowledge

Benchmarks that span many countries or regions. Use these to compare models across cultures at once.

- [CulturalMenuBench](https://arxiv.org/abs/2609.03526) - 4,870 culinary items in 10 languages and 18 regions pair dish and cooking-step images with text to test regional cuisine attribution beyond recognition. EMNLP 2026 Findings. No public data yet. [Code](https://github.com/BobTsang-NLP/CulturalMenuBench)
- [BLEnD-Vis](https://arxiv.org/abs/2510.11178) - Extends BLEnD to VQA with 4,916 generated images and over 21,000 multiple-choice questions across 16 regions, testing rephrasing and cross-modal robustness. EACL 2026 Main. [Data](https://huggingface.co/datasets/Incomple/BLEnD-Vis) [Code](https://github.com/Social-AI-Studio/BLEnD-Vis)
- [C3B](https://arxiv.org/abs/2510.00041) - Comic-image benchmark of 2,220 images and 18,789 QA pairs over 77 cultures with recognition, cultural-conflict detection and multilingual generation tasks. ICLR 2026. [Data](https://huggingface.co/datasets/Coder109/C3B) [Project](https://c3b-benchmark.github.io/)
- [Confused Tourists](https://arxiv.org/abs/2511.17004) - Adversarial robustness suite stacking or generating conflicting geographic cues into 5,451 images of cuisine, attire and instruments from 57 countries; accuracy drops sharply. CVPR 2026 Findings. [Data](https://huggingface.co/datasets/patrickamadeus/vlms-are-confused-tourists) [Code](https://github.com/patrickamadeus/vlms-are-confused-tourists)
- [CultureMix](https://arxiv.org/abs/2511.22787) - 23k generated food VQA images mixing dishes and backgrounds from 30 countries, testing whether VLMs keep each element's cultural identity. arXiv, 2025. [Data](https://huggingface.co/datasets/EunsuKim/CultureMix)
- [GIMMICK](https://arxiv.org/abs/2502.13766) - Six tasks on 728 cultural events and facets from 144 countries in six regions, with 6,887 images and 993 videos; 31 models evaluated. ACL 2025 Findings. Data gated. [Data](https://huggingface.co/datasets/floschne/gimmick-civqa) [Code](https://github.com/floschne/gimmick)
- [MMAC](https://arxiv.org/abs/2510.08608) - Human-curated multiple-choice benchmark of 27,000 questions aligned across text, image and speech, covering 8 Asian countries and 10 languages, with cross-modal consistency tests. ACL 2026 Main. [Data](https://huggingface.co/datasets/ZWHTXY/MMAC-Bench)
- [ALM-bench](https://arxiv.org/abs/2411.16508) - 22,763 human-annotated VQA pairs in 100 languages from 73 countries, 13 cultural plus 6 generic categories, four question formats. CVPR 2025. [Data](https://huggingface.co/datasets/MBZUAI/ALM-Bench) [Code](https://github.com/mbzuai-oryx/ALM-Bench) [Project](https://mbzuai-oryx.github.io/ALM-Bench/)
- [CROPE](https://arxiv.org/abs/2410.15453) - VQA benchmark of 1,060 binary questions on culture-specific versus common concepts, testing whether VLMs adapt from in-context text and image descriptions. NAACL 2025 Main. No public data yet.
- [CulturalVQA](https://arxiv.org/abs/2407.10920) - 2,378 questions on 2,328 images from 11 countries across five continents covering clothing, food, drinks, rituals and traditions, answered by local annotators. EMNLP 2024 Main. No public data yet. [Data](https://culturalvqa.org/)
- [CVQA](https://arxiv.org/abs/2406.05967) - Multilingual VQA benchmark of 10,374 four-way questions on culturally driven images from 30 countries in 31 languages, written by native speakers. NeurIPS 2024 Datasets and Benchmarks. [Data](https://huggingface.co/datasets/afaji/cvqa) [Project](https://cvqa-benchmark.org/)
- [WorldCuisines](https://arxiv.org/abs/2410.12705) - Multilingual food VQA benchmark with over 1 million instances in 30 languages, asking dish names and origins for 2,414 dishes from 189 countries. NAACL 2025 Main. [Data](https://huggingface.co/datasets/worldcuisines/vqa) [Code](https://github.com/worldcuisines/worldcuisines) [Project](https://worldcuisines.github.io/)

## Country and region VQA and cultural knowledge

Benchmarks built for one country or region, usually by people from it. Grouped by region.

### South Asia

- [BanglaProtha](https://openaccess.thecvf.com/content/WACV2026/html/Fahim_BanglaProtha_Evaluating_Vision_Language_Models_in_Underrepresented_Long-tail_Cultural_Contexts_WACV_2026_paper.html) - VQA dataset of Bengali cultural images with native Bengali questions and semantically similar distractors, evaluating VLMs across prompting, fine-tuning and cultural aspects. WACV 2026. [Data](https://www.kaggle.com/datasets/sourove/bangla-culturally-relevant-vqa) [Code](https://github.com/farhanishmam/BanglaProtha)
- [BanglaVerse](https://arxiv.org/abs/2603.21165) - 1,152 Bengali-culture images with captions and VQA in Bangla, English, Hindi, Urdu and 5 Bangla dialects, about 32.3K items across 9 domains. EMNLP 2026 Findings. [Data](https://huggingface.co/datasets/FaiyazAbdullah114708/BanglaVerse) [Code](https://github.com/faiyazabdullah/BanglaVerse) [Project](https://labib1610.github.io/BanglaVerse)
- [TAB-VLM](https://arxiv.org/abs/2605.15071) - 600 questions over 1,600 Indian artifacts from prehistoric to modern periods testing temporal reasoning; best of ten models (GPT-5.2) reaches 58.7%. ACL 2026 Findings. [Data](https://huggingface.co/datasets/mukul54/tab-vlm) [Code](https://github.com/KHUSHBOO0012/tab-vlm/) [Project](https://khushboo0012.github.io/tab-vlm-webpage/)
- [DRISHTIKON](https://arxiv.org/abs/2509.19274) - Indian-culture VQA benchmark of 64,288 text-image pairs in 15 languages covering all states and union territories across 16 cultural categories. EMNLP 2025 Main. [Data](https://huggingface.co/datasets/13ari/DRISHTIKON) [Code](https://github.com/13ari/DRISHTIKON)
- [IndicVisionBench](https://arxiv.org/abs/2511.04727) - India-centric benchmark: about 5K images and 37K+ QA pairs for VQA, OCR and multimodal translation in English and 10 Indian languages, 13 cultural topics. ICLR 2026. [Data](https://huggingface.co/datasets/krutrim-ai-labs/IndicVisionBench) [Code](https://github.com/ola-krutrim/IndicVisionBench)

### East Asia

- [Hanfu-Bench](https://arxiv.org/abs/2506.01565) - Expert-curated Hanfu benchmark: 1,192 images across five Chinese dynasties with VQA and image transcreation tasks; closed VLMs trail experts by about 10%. EMNLP 2025 Main. Data gated. [Data](https://huggingface.co/datasets/lizhou21/hanfu-bench) [Code](https://github.com/lizhou21/TemporalCulture)
- [TaiwanVQA](https://openreview.net/forum?id=atofIc3x1q) - Taiwan-specific VQA benchmark of 2,736 images and 5,472 questions on food, signs, festivals and landmarks, plus augmentation to improve cultural reasoning. NeurIPS 2025. [Data](https://huggingface.co/datasets/hhhuang/TaiwanVQA) [Code](https://github.com/hhhuang/TaiwanVQA) [Project](https://taide-taiwan.github.io/TaiwanVQA/)
- [CVLUE](https://arxiv.org/abs/2407.01081) - Chinese vision-language benchmark with native-speaker-selected images over 92 categories, covering image-text retrieval, VQA, visual grounding and visual dialogue. AAAI 2025. Data on request. [Data](https://github.com/WangYuxuan93/CVLUE)
- [FoodieQA](https://arxiv.org/abs/2406.11030) - Manually curated Chinese regional food benchmark: 389 unseen images, multi-image, single-image and text QA; open VLMs trail humans by 41% and 21%. EMNLP 2024 Main. Data gated. [Data](https://huggingface.co/datasets/lyan62/FoodieQA) [Code](https://github.com/lyan62/FoodieQA)
- [K-Viscuit](https://arxiv.org/abs/2406.16469) - Korean culture VQA benchmark of 657 questions on 237 images across ten categories, built with VLM-generated questions validated by native speakers. ACL 2025 Main. [Data](https://huggingface.co/datasets/ddehun/k-viscuit)

### Middle East and North Africa

- [M2CQA](https://arxiv.org/abs/2602.05437) - 9,990 images from 17 MENA countries with true and counterfactual statements in English, MSA, Egyptian and Levantine Arabic, measuring counterfactual hallucination rate. ACL 2026 Findings. [Data](https://huggingface.co/datasets/QCRI/M2CQA)
- [PEARL](https://arxiv.org/abs/2505.21979) - Over 309K Arabic multimodal instruction examples and a 6,867-question benchmark over 10 cultural domains across Arab countries, human annotated. EMNLP 2025 Findings. Data gated. [Data](https://huggingface.co/datasets/UBC-NLP/PEARL) [Code](https://github.com/UBC-NLP/pearl) [Project](https://pearl.dlnlp.ai/)

### Africa

- [Afri-MCQA](https://arxiv.org/abs/2601.05699) - Culturally grounded multiple-choice and open-ended VQA in 15 African languages from 12 countries, about 7.5k QA pairs with native-language and accented-English audio. ACL 2026 Main. [Data](https://huggingface.co/datasets/Atnafu/Afri-MCQA)

## Visual reasoning, grounding and retrieval

Beyond recognition: visually grounded reasoning, grounding and segmentation of cultural objects, and culture-aware retrieval.

- [M4-RAG](https://arxiv.org/abs/2512.05959) - Retrieval-augmented VQA benchmark over CVQA and WorldCuisines: over 80,000 image-question pairs in 42 languages and 189 countries with Wikipedia knowledge bases. CVPR 2026. [Data](https://huggingface.co/datasets/davidanugraha/M4-RAG) [Code](https://github.com/davidanugraha/M4-RAG)
- [RAVENEA](https://arxiv.org/abs/2505.14462) - 1,868 culture-grounded images with over 10,000 human-ranked Wikipedia documents for retrieval-augmented cultural VQA and captioning across 8 countries. ICLR 2026. [Data](https://huggingface.co/datasets/jaagli/ravenea) [Code](https://github.com/yfyuan01/RAVENEA) [Project](https://jiaangli.github.io/ravenea/)
- [GlobalRG](https://arxiv.org/abs/2407.00263) - Retrieving culturally diverse images for 20 universal concepts across 50 countries, and grounding culture-specific concepts in images from 15 countries. EMNLP 2024 Main. [Data](https://huggingface.co/datasets/UBCNLP/GlobalRG-Retrieval) [Code](https://github.com/meharbhatia/globalrg) [Project](https://globalrg.github.io/)
- [GD-VCR](https://arxiv.org/abs/2109.06860) - 328 movie and TV screenshots with 886 four-way QA pairs over West, East Asia, South Asia and Africa, exposing regional performance gaps. EMNLP 2021 Main. [Data](https://github.com/WadeYin9712/GD-VCR)
- [MaRVL](https://arxiv.org/abs/2109.13238) - 5,670 native-speaker true/false statements over image pairs in Indonesian, Chinese, Swahili, Tamil and Turkish, built from speaker-selected concepts. EMNLP 2021 Main. [Data](https://marvl-challenge.github.io/download) [Code](https://github.com/marvl-challenge/marvl-code) [Project](https://marvl-challenge.github.io)

## Norms, values and safety

Whether models read social norms, values and offensiveness the way people in a given place do.

- [NormViz](https://arxiv.org/abs/2609.06831) - Contrastive image pairs from 16 countries test whether VLMs judge behaviors against local social norms; includes a 64k image training set with explanations. COLM 2026. No public data yet. [Code](https://github.com/Akhila-Yerukola/NormViz)
- [CROSS](https://arxiv.org/abs/2505.14972) - 1,284 image-grounded queries from 16 countries in 14 languages testing cultural norm safety; best model scores 61.79% awareness, 37.73% compliance. TMLR 2025. [Data](https://github.com/haoyiq114/CROSS)
- [MC-SIGNS](https://arxiv.org/abs/2502.17710) - 288 gesture-country pairs (25 gestures, 85 countries) annotated for offensiveness, used to test T2I systems, LLMs and VLMs for US-centric bias. ACL 2025 Main. [Data](https://github.com/Akhila-Yerukola/culturally-offensive-gestures)

## Memes, humor, art and heritage

Memes and humor need shared context; art and heritage need domain knowledge. Both fail in culturally specific ways.

- [AVMeme Exam](https://arxiv.org/abs/2601.17645) - Human-curated benchmark of 1,032 iconic Internet audio-visual memes in 10+ languages, with multiple-choice questions on content, context, emotion, usage and world knowledge. arXiv, 2026. Data gated. [Data](https://huggingface.co/datasets/naplab/AVMeme-Exam) [Project](https://avmemeexam.github.io/public)
- [DuwatBench](https://arxiv.org/abs/2601.19898) - Arabic calligraphy benchmark of 1,272 images across 6 styles with transcriptions, word bounding boxes and style labels, evaluating 13 multimodal models on recognition and detection. EACL 2026 Main. [Data](https://huggingface.co/datasets/MBZUAI/DuwatBench) [Code](https://github.com/mbzuai-oryx/DuwatBench) [Project](https://mbzuai-oryx.github.io/DuwatBench/)
- [MemeCULT-1K](https://arxiv.org/abs/2609.01772) - 1,000 South Asian memes in Bengali, English and Hindi with context notes and human explanations; evaluates 13 VLMs with and without cultural context. EMNLP 2026 Main. No public data yet. [Code](https://github.com/TawsifDipto17/MemeCULT-1K)
- [VULCA-Bench](https://arxiv.org/abs/2601.07986) - Art-critique benchmark of 7,410 image-critique pairs across 8 cultural traditions with bilingual Chinese-English expert critiques over a five-layer framework from perception to aesthetics. arXiv, 2026. [Data](https://github.com/vulca-org/vulca-cultural-visual-benchmark) [Code](https://github.com/yha9806/VULCA-Bench)
- [TimeTravel](https://arxiv.org/abs/2502.14865) - 10,250 expert-verified images of historical artifacts from 266 cultures across 10 historical regions, for describing manuscripts, art, inscriptions and archaeology. ACL 2025 Findings. [Data](https://huggingface.co/datasets/MBZUAI/TimeTravel) [Code](https://github.com/mbzuai-oryx/TimeTravel) [Project](https://mbzuai-oryx.github.io/TimeTravel/)
- [Multi3Hate](https://arxiv.org/abs/2411.03888) - 300 parallel memes in five languages annotated by 445 annotators from five countries; VLMs align more with US labels than other cultures. NAACL 2025 Main. [Data](https://huggingface.co/datasets/MinhDucBui/Multi3Hate) [Code](https://github.com/MinhDucBui/Multi3Hate)

## Captioning, translation and transcreation

Describing, translating and adapting images across languages and cultures.

- [CaMMT](https://arxiv.org/abs/2505.24456) - Over 5,800 image plus parallel English and regional-language caption triples from 23 regions for testing whether images help culturally aware translation. EMNLP 2025 Findings. [Data](https://huggingface.co/datasets/villacu/cammt)
- [CIC](https://arxiv.org/abs/2402.05374) - Pipeline generating culture-category questions, extracting cultural elements via VQA, and prompting an LLM to write culturally descriptive captions, judged by 45 evaluators. IJCAI 2024. [Code](https://github.com/shane3606/CIC) [Project](https://shane3606.github.io/cic)
- [MosAIC](https://arxiv.org/abs/2411.11758) - Multi-agent framework with cultural personas that writes culture-enriched captions for 2,832 images from China, India and Romania, with a culture-adaptable metric. NAACL 2025 Main. [Data](https://github.com/MichiganNLP/MosAIC)
- [Crossmodal-3600](https://arxiv.org/abs/2205.12522) - Geographically diverse image captioning evaluation set: 3,600 images with 261,375 human captions in 36 languages, 100 images per language region. EMNLP 2022 Main. [Data](https://google.github.io/crossmodal-3600/)

## Video understanding

Cultural understanding over time: events, rituals, norms and moments in video.

- [MINERVA-Cultural](https://arxiv.org/abs/2601.10649) - Human-annotated long-video QA with reasoning traces in 18 native languages over 540 culturally specific videos from 18 locales; Video-LLMs fall well below human accuracy. CVPR 2026. [Data](https://github.com/google-deepmind/neptune)
- [VideoVista-CulturalLingo](https://arxiv.org/abs/2504.17821) - Bilingual (Chinese, English) video QA benchmark with 1,389 videos and 3,134 questions spanning Chinese, North American and European cultural content; 24 models evaluated. ACL 2025 Main. [Data](https://huggingface.co/datasets/Uni-MoE/VideoVista-CulturalLingo) [Code](https://github.com/HITsz-TMG/VideoVista) [Project](https://videovista-culturallingo.github.io/)
- [ViMUL-Bench](https://arxiv.org/abs/2506.07032) - Video QA in 14 languages: 879 videos and 8,025 questions over 8 cultural and 7 generic categories, plus the ViMUL model. EMNLP 2025 Main. [Data](https://huggingface.co/datasets/MBZUAI/ViMUL-Bench) [Code](https://github.com/mbzuai-oryx/ViMUL) [Project](https://mbzuai-oryx.github.io/ViMUL/)

## Text-to-image and text-to-video generation

How faithfully generative models depict cultures, and how to measure and fix the gaps.

- [CultureVidBench](https://arxiv.org/abs/2608.01942) - 1,000 prompts over 12 countries and 14 cultural aspects for judging cultural faithfulness of text-to-video models, with human and MLLM evaluation of seven models. EMNLP 2026 Main. [Data](https://huggingface.co/datasets/XianjingHan/CultureVidBench) [Project](https://hanxjing.github.io/CultureVidBench/)
- [When Cultures Move](https://arxiv.org/abs/2605.16716) - 243 prompts and 972 generated videos across Chinese, American and Romanian cultures, mono and cross-cultural, plus MAVEN multi-agent prompt refinement for cultural fidelity. EMNLP 2026 Workshop (NLP4PI). [Data](https://huggingface.co/datasets/AIM-SCU/MAVEN_Multicultura_Text-to-Video_Generation) [Code](https://github.com/AIM-SCU/MAVEN)
- [CAIRe](https://arxiv.org/abs/2506.09109) - Retrieval-augmented metric grounding image entities to a knowledge base to score cultural relevance per label, validated on rare-item and 10-country universal-concept sets. EACL 2026 Main. [Data](https://huggingface.co/datasets/cmu-lti/caire-universal) [Code](https://github.com/siddharthyayavaram/CAIRE)
- [CultDiff](https://arxiv.org/abs/2502.08914) - Tests whether text-to-image diffusion models generate the architecture, clothing and food of 10 countries, with a learned similarity metric, CultDiff-S. ACL 2025 Main. No public data yet.
- [CULTIVate](https://arxiv.org/abs/2511.05681) - 576 social-activity prompts from 16 countries and over 19,000 generated images, scored for alignment, hallucination, exaggeration and diversity. ICLR 2026. No public data yet. [Code](https://github.com/sinamalakouti/AHEaD) [Project](https://sinamalakouti.github.io/AHEaD/)
- [CulturalFrames](https://arxiv.org/abs/2506.08835) - Text-to-image benchmark of 983 prompts across 10 countries and 5 social domains, with 3,637 images and over 10,000 human annotations of cultural expectations. EMNLP 2025 Findings. [Data](https://huggingface.co/datasets/mair-lab/CulturalFrames) [Code](https://github.com/mair-lab/CulturalFrames) [Project](https://culturalframes.github.io)
- [Culture-TRIP](https://arxiv.org/abs/2502.16902) - Iterative prompt refinement that retrieves cultural context for culture nouns from 8 countries, improving Stable Diffusion alignment in a 66-participant study. NAACL 2025 Main. [Code](https://github.com/Kakaomacao/Culture-TRIP) [Project](https://shane3606.github.io/Culture-TRIP/)
- [CuRe](https://arxiv.org/abs/2506.08071) - 300 cultural artifacts from 64 countries in 32 subcategories across six axes, scoring text-to-image systems on long-tail cultural fidelity. ICCV 2025. [Data](https://huggingface.co/datasets/aniketr/cure) [Code](https://github.com/aniketrege/cure-bench) [Project](https://aniketrege.github.io/cure/)
- [Exposing Blindspots](https://arxiv.org/abs/2510.20042) - Audits text-to-image generation and image-to-image editing across six countries with an 8-category, 36-subcategory, era-aware prompt schema and native expert ratings. IASEAI 2026. [Data](https://huggingface.co/datasets/seochan99/ecb-datasets) [Code](https://github.com/cmubig/ECB) [Project](https://seochan99.github.io/ECB/)
- [When Cultures Meet](https://arxiv.org/abs/2502.15972) - Multicultural text-to-image benchmark of 9,000 generated images mixing people and landmarks from five countries in five languages, with the MosAIG multi-agent prompting framework. ACL 2026 Findings. [Data](https://huggingface.co/datasets/AIM-SCU/When-Cultures-Meet) [Code](https://github.com/AIM-SCU/MosAIG)
- [Where Culture Fades](https://arxiv.org/abs/2511.17282) - Shows multilingual T2I models give culturally neutral or English-biased images across 15 languages, localizes culture neurons, and proposes activation and layer-targeted fixes on CultureBench. CVPR 2026 (venue not confirmed).
- [CUBE](https://arxiv.org/abs/2407.06863) - 1,000 prompts and about 300,000 cultural artifacts across cuisine, landmarks and art in 8 countries, for text-to-image cultural awareness and diversity. NeurIPS 2024 Datasets and Benchmarks. [Data](https://github.com/google-deepmind/cube)
- [Image transcreation](https://arxiv.org/abs/2404.01247) - Three generative pipelines and 700 evaluation images across 7 countries for adapting images to a target culture; edits succeed on as few as 5% for some countries. EMNLP 2024 Main. [Data](https://huggingface.co/datasets/cmu-lti/machine-translation-for-vision) [Code](https://github.com/simran-khanuja/image-transcreation) [Project](https://machine-transcreation.github.io/image-transcreation)
- [SCoFT](https://arxiv.org/abs/2401.08053) - Self-contrastive fine-tuning of Stable Diffusion on the CCUB dataset, judged by 51 participants from 5 countries to reduce stereotypes and raise cultural relevance. CVPR 2024. [Data](https://github.com/cmubig/CCUB) [Code](https://github.com/cmubig/SCoFT) [Project](https://ariannaliu.github.io/SCoFT/)
- [ViSAGe](https://arxiv.org/abs/2401.06310) - Visual stereotype attributes for 135 nationalities with annotated T2I images; stereotypical attributes appear three times more often, most offensively for Global South identities. ACL 2024 Main. [Data](https://github.com/google-research-datasets/visage)
- [CCUB](https://arxiv.org/abs/2301.12073) - Expert-curated set of 1,095 image-text pairs across 8 countries, used to fine-tune Stable Diffusion and GPT-3 prompts for culturally relevant generation. arXiv, 2023. [Data](https://github.com/cmubig/CCUB)
- [CulText2I](https://arxiv.org/abs/2310.01929) - Images from six TTI models prompted in ten languages, evaluated with CLIP, VQA and humans to expose each model's cultural point of view. TACL 2025. Data on request. [Data](https://github.com/venturamor/CulText-2-I) [Project](https://venturamor.github.io/CulText2IWeb/)
- [DIG In](https://arxiv.org/abs/2308.06198) - Three automatic indicators of realism, diversity and prompt consistency for T2I generations across world regions, with GeoDE and DollarStreet based prompt sets. TMLR 2023. [Data](https://github.com/facebookresearch/DIG-In/) [Project](https://openreview.net/forum?id=FDt2UGM1Nz)
- [Geographical representativeness of T2I](https://arxiv.org/abs/2305.11080) - 540 participants from 27 countries rate whether DALL-E 2 and Stable Diffusion images of common nouns reflect their country; defaults skew to the US. ICCV 2023.

## Geographic robustness of visual recognition

The older and more basic question: does image recognition work everywhere, or only where the training data came from?

- [Multilingual diversity improves VL representations](https://arxiv.org/abs/2405.16915) - Shows that translating non-English web captions to English and re-filtering improves vision-language pretraining, with gains on GeoDE across regions, largest in Africa. NeurIPS 2024 Main. [Data](https://huggingface.co/datasets/thaottn/datacomp-medium-pool-translated) [Project](https://proceedings.neurips.cc/paper_files/paper/2024/hash/a6678e2be4ce7aef9d2192e03cd586b7-Abstract-Conference.html)
- [No Filter](https://arxiv.org/abs/2405.13777) - Shows English-only filtering of pre-training data lowers cultural and socioeconomic diversity of contrastive VLMs; global pre-training with English fine-tuning recovers both. NeurIPS 2024 Main.
- [Does progress on object recognition benchmarks improve generalization?](https://arxiv.org/abs/2307.13136) - Evaluates nearly 100 vision models on DollarStreet and GeoDE, finding 7 to 20 percent geographic accuracy gaps that ImageNet progress does not close. ICLR 2024. [Project](https://openreview.net/forum?id=rhaQbS3K3R)
- [GeoDE](https://arxiv.org/abs/2301.02560) - 61,940 crowdsourced images of 40 object classes from six world regions, without PII, for geographically diverse evaluation and training. NeurIPS 2023 Datasets and Benchmarks. [Data](https://geodiverse-data-collection.cs.princeton.edu/) [Code](https://github.com/princetonvisualai/geode_dataset)
- [GeoNet](https://arxiv.org/abs/2303.15443) - Domain adaptation benchmark with USA and Asia splits for scene recognition (205 classes) and object classification (600 classes), plus a universal adaptation split. CVPR 2023. [Data](https://tarun005.github.io/GeoNet) [Code](https://github.com/ViLab-UCSD/GeoNet)
- [Dollar Street](https://proceedings.neurips.cc/paper_files/paper/2022/hash/5474d9d43c0519aa176276ff2c1ca528-Abstract-Datasets_and_Benchmarks.html) - Supervised dataset of 38,479 household-item images from homes worldwide, labeled with object tags, region, country and monthly income, released under CC-BY. NeurIPS 2022 Datasets and Benchmarks. [Data](https://www.kaggle.com/datasets/mlcommons/the-dollar-street-dataset) [Project](https://mlcommons.org/datasets/dollar-street/)
- [Does Object Recognition Work for Everyone?](https://arxiv.org/abs/1906.02659) - Evaluates five commercial object-recognition APIs on Dollar Street household photos from 54 countries, finding lower accuracy for low-income homes. CVPR 2019 Workshops. [Data](https://www.gapminder.org/dollar-street)

## Models, training data and adaptation methods

Training data, pre-training objectives, adaptation and prompting methods that target cultural or geographic gaps.

- [CulturalGround](https://arxiv.org/abs/2508.07414) - 22M synthetic multilingual VQA pairs on 2.8M Wikimedia images of Wikidata cultural entities from 42 countries in 39 languages, used to train CulturalPangea-7B. arXiv, 2025. [Data](https://huggingface.co/datasets/neulab/CulturalGround) [Code](https://github.com/neulab/CulturalGround) [Project](https://neulab.github.io/CulturalGround/)
- [CultureCLIP](https://arxiv.org/abs/2507.06210) - Fine-tunes CLIP on CulTwin, a synthetic set of 73,823 retained concept-caption-image triplets spanning 229 countries, to sharpen fine-grained cultural concept recognition. COLM 2025. [Code](https://github.com/lukahhcm/CultureCLIP)
- [CultureMixup](https://aclanthology.org/2023.emnlp-main.18/) - Annotation-free cultural concept mapping plus a mixup augmentation that improve four multilingual VLMs on MaRVL across five languages. EMNLP 2023 Main. [Data](https://huggingface.co/datasets/zhili312/multimodal-cultural-concepts) [Code](https://github.com/zhilizju/Culture-mixup)
- [GIVL](https://arxiv.org/abs/2301.01893) - Pre-trained VLM with Image-Knowledge Matching and Image Edit Checking objectives to reduce performance gaps on geo-diverse benchmarks such as GD-VCR and MaRVL. CVPR 2023. [Code](https://github.com/WadeYin9712/GIVL)

## Analyses, position papers and surveys

Where the failures come from, and how the field should evaluate.

- [Cultural representation disparities](https://arxiv.org/abs/2505.14729) - Probes VLMs on country identification over Country211 (211 countries) with open-ended, multiple-choice, multilingual and adversarial settings; prompts released on Hugging Face. IJCNLP-AACL 2025 Findings. [Data](https://huggingface.co/datasets/Biases/CulturalBiases-2025)
- [Cultural theory for VLM evaluation](https://arxiv.org/abs/2505.22793) - Position paper arguing VLM cultural evaluations should draw on cultural studies, semiotics and visual studies, proposing five frameworks after reviewing 35 recent papers. arXiv, 2025.
- [Culture-sensitive neurons](https://arxiv.org/abs/2510.24942) - Identifies culture-sensitive neurons in three VLMs on CVQA's 25 cultural groups, with a contrastive activation margin method validated by ablation. EACL 2026 Main. [Code](https://github.com/xiutian/vlm-culture-neuron)
- [See It from My Perspective](https://arxiv.org/abs/2406.11665) - Analysis showing VLMs favor Western over East Asian image subsets and that pre-training language mix and inference language shift the bias. ICLR 2025. [Code](https://github.com/amith-ananthram/see-it-from-my-perspective) [Project](https://openreview.net/forum?id=Xbl6t6zxZs)

## Foundational reading

Background that motivates the whole area.

- [The weirdest people in the world?](https://doi.org/10.1017/S0140525X0999152X) - Psychology review arguing that findings from Western, Educated, Industrialized, Rich and Democratic samples are outliers and do not generalize to humanity. Behavioral and Brain Sciences, 2010.

## By region

Where the region-specific resources draw their images, videos or prompts from. Multi-country resources are not repeated here.

| Region                       | Resources                                                                                         |
| ---------------------------- | ------------------------------------------------------------------------------------------------- |
| Southeast Asia               | Cultural Moment Benchmark, GG-EZ, Rice-VL, SEA-VL, SEA-VQA, SEACrowd, Seeing Culture, VietMEAgent |
| South Asia                   | BanglaProtha, BanglaVerse, DRISHTIKON, IndicVisionBench, MemeCULT-1K, TAB-VLM                     |
| East Asia                    | CVLUE, FoodieQA, Hanfu-Bench, K-Viscuit, TaiwanVQA, VideoVista-CulturalLingo                      |
| Middle East and North Africa | DuwatBench, M2CQA, PEARL                                                                          |
| Africa                       | Afri-MCQA                                                                                         |
| Asia, multi-country          | MMAC                                                                                              |

## Related lists

- [awesome-cultural-nlp](https://github.com/simran-khanuja/awesome-cultural-nlp#readme) - Cultural NLP resources, mostly text, with a growing multimodal section.
- [SEACrowd catalogue](https://seacrowd.github.io/seacrowd-catalogue/) - Datasheets for Southeast Asian language, speech and vision datasets.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first: an entry needs a public paper, a stated venue or preprint date, and an honest note on data access.
