# Yixuan Zhang

I build machine-learning systems that hold up outside the notebook: private split inference,
edge vision and LLM serving. I'm an MS CS student at the University of Illinois
Urbana-Champaign ('28), after a First-Class B.Sc. in Computer Science at the University of
Nottingham.

[Website](https://asher0913.github.io) · [Résumé](https://asher0913.github.io/Yixuan_Zhang_Resume.pdf) · [LinkedIn](https://www.linkedin.com/in/yixuan-zhang-b656392b5)

## Research

| | |
|---|---|
| [**DualPathCEM**](https://github.com/asher0913/DualPathCEM) | Split inference for private face recognition. Two client paths: a noise-protected spatial tensor carries the privacy burden and a compact semantic token carries utility. **81.96%** top-1 on FaceScrub, +1.63 points over Noise_ARL+CEM, with **75.8%** higher reconstruction error for a decoder attacker. Manuscript in preparation. |
| [**SlotCEM**](https://github.com/asher0913/SlotCEM) | B.Sc. dissertation (First Class). Slot-attention conditional-entropy regularisation against model inversion in split learning: +29.8% attack MSE for a 0.84-point accuracy cost. |

## Selected work

| | |
|---|---|
| [**multi-material-slicer**](https://github.com/asher0913/multi-material-slicer) | Internship project. Qt/C++17 and OpenGL desktop slicer for multi-material resin printing: STEP/STL assemblies to per-material masks and G-code, with a headless end-to-end self-test in CI. |
| [**skill-router**](https://github.com/asher0913/skill-router) | Progressive tool disclosure for large skill catalogues: **−85.5%** context tokens per query. Measured on held-out paraphrases, where lexical routing drops to 0.21 top-1 and an embedding stage brings it back to 0.56. |
| [**inference-lab**](https://github.com/asher0913/inference-lab) | LLM serving front end for vLLM, SGLang and Ollama. Request coalescing cuts backend generations **16 → 3**. A labelled study shows semantic caches serving wrong answers, and a simulation shows continuous batching sustaining **10×** the load of static batching. |
| [**secure-rag**](https://github.com/asher0913/secure-rag) | Permission-aware multi-tenant RAG. After ACL changes, a stale-index pre-filter leaks on **54%** of queries; a live re-check against the directory of record brings that to **0%**. |
| [**code-task-forge**](https://github.com/asher0913/code-task-forge) | SWE-bench-style harness for judging coding-agent patches. Exit codes accept 25 of 78 wrong patches; restored tests plus held-out tests accept none. |
| [**plant-leaf-recognition**](https://github.com/asher0913/plant-leaf-recognition) | ResNet-101 and ViT-B/16 feature fusion: **98.46%** top-1 on 100 leaf species over 20 splits. |
| [**oxford-pet-classification**](https://github.com/asher0913/oxford-pet-classification) | 37 breeds: fine-tuned ResNet-18 at **89.8%** against a from-scratch SE-ResNet at 49.7%, with a one-change-per-row ablation and Grad-CAM. |
| [**IAMABOT**](https://github.com/asher0913/IAMABOT) | MechMania 32 bot, built from the game engine's Rust source; climbed from 7th to **3rd** on the live leaderboard. |

## Labs

Laptop-scale reference implementations of production problems, each with seeded, reproducible
results checked in CI. Synthetic benchmarks are labelled as such in each README.

**Serving and systems**
- [tiered-kv-cache-lab](https://github.com/asher0913/tiered-kv-cache-lab): KV prefix caching across HBM, DRAM and NVMe, with capacity planning up to 14.5 req/s within the TTFT SLO.
- [ai-gateway-control-plane](https://github.com/asher0913/ai-gateway-control-plane): budgets, circuit breakers and latency-aware routing; p99 latency 14.3 s → 5.8 s under fault injection.
- [edge-quantization-lab](https://github.com/asher0913/edge-quantization-lab): INT8/INT4 post-training quantization, mixed-precision search at 6.4× compression, and a bit-exact integer kernel.
- [vision-pipeline-orchestrator](https://github.com/asher0913/vision-pipeline-orchestrator): CPU/GPU pipeline simulator with batching, backpressure, a dead-letter queue and autoscaling.

**Agents and evaluation**
- [agentops](https://github.com/asher0913/agentops): incident investigation under flaky telemetry: wrong on 0.4% of incidents against 33.5% for retry-and-answer, with replayable traces.
- [agent-trace-lab](https://github.com/asher0913/agent-trace-lab): trace model, process anti-pattern detectors and root-cause attribution, stress-tested on 1,000 generated traces.
- [reflective-agent-lab](https://github.com/asher0913/reflective-agent-lab): reflect-and-repair against sandbox verification; irreversible side effects fall from 12.0 to 0.2 per 100 tasks.
- [graph-sop-agent](https://github.com/asher0913/graph-sop-agent): service graph plus runbooks, against document-only RAG, with review-gated knowledge ingestion.
- [risk-agent-workbench](https://github.com/asher0913/risk-agent-workbench): span-cited evidence extraction that abstains when evidence is missing.
- [agent-guard](https://github.com/asher0913/agent-guard): policy gateway between an agent and its tools.

**Retrieval, data and safety**
- [recsys-ranking-lab](https://github.com/asher0913/recsys-ranking-lab): two-stage recommender on MovieLens-100K; GBDT re-ranking gives +40% HR@10 over ALS.
- [document-vlm-data-engine](https://github.com/asher0913/document-vlm-data-engine): quality stages for document-VLM training data.
- [multimodal-safety-lab](https://github.com/asher0913/multimodal-safety-lab): red-team benchmark for text+image input guards, with a held-out phrasing suite.

**Machine learning and algorithms**
- [music-emotion-regression](https://github.com/asher0913/music-emotion-regression): DEAM valence and arousal across eight model families (R² 0.60 / 0.43), with an annotator-noise floor. Data: [deam-song-level-features](https://github.com/asher0913/deam-song-level-features).
- [cifar10-ml-benchmark](https://github.com/asher0913/cifar10-ml-benchmark): PCA, MLP and Random Forest under matched cross-validation.
- [classical-ai-search](https://github.com/asher0913/classical-ai-search): six search algorithms on 300 seeded mazes, turn-aware routing and MDPs.
- [bin-packing-metaheuristics](https://github.com/asher0913/bin-packing-metaheuristics): best-fit decreasing, Minimum Bin Slack and annealing on Falkenauer's instances.
- [treasure-hunt-pathfinding](https://github.com/asher0913/treasure-hunt-pathfinding): A\* and BFS hints in a Swing game; A\* expands 7× fewer cells.

**Apps**
- [contactless-breathing-monitor](https://github.com/asher0913/contactless-breathing-monitor): on-device iOS breathing curve and respiratory rate from TrueDepth.
- [javafx-platformer](https://github.com/asher0913/javafx-platformer): Java 21 / JavaFX game built on MVC and GoF patterns (with Yueming Qu).
- [flask-music-library](https://github.com/asher0913/flask-music-library): Flask and SQLite catalogue with CSRF-protected, transactional writes.

---

Python · C++ · Java · Swift · SQL · PyTorch · scikit-learn · FastAPI · Qt/OpenGL · Docker · GitHub Actions
