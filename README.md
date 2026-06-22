# 🎮 Vision-Language-Action & World Models for Game Agents

> A curated collection of cutting-edge research on **Vision-Language-Action (VLA)** models, **World Models (WM)**, and **World-Action Models (WAM)** applied to gaming and embodied AI.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Papers](https://img.shields.io/badge/Papers-50+-blue.svg)]()
[![Last Update](https://img.shields.io/badge/Last%20Update-June%202026-green.svg)]()

---

## 📋 Table of Contents

- [Overview](#overview)
- [VLA for Game Agents](#-vla-for-game-agents)
- [World Models & World-Action Models](#-world-models--world-action-models)
- [Surveys & Benchmarks](#-surveys--benchmarks)
- [Related Resources](#-related-resources)
- [Contributing](#contributing)

---

## Overview

This repository systematically organizes frontier research at the intersection of:
- **Vision-Language-Action (VLA) Models**: Multimodal agents that directly output keyboard/mouse/gamepad actions
- **World Models (WM)**: Predictive models that simulate future game states
- **World-Action Models (WAM)**: Joint models that couple world prediction with action generation

**Key Research Directions:**
- Closed-loop perception-reasoning-execution in 3D games
- Real-time action generation with low latency (<50ms)
- Cross-game generalization and transfer learning
- Bridging the "Latency-Intelligence Dilemma"

---

## 🎯 VLA for Game Agents

### Core Paradigm
**VLA models** enable agents to go from pixels to actions in an end-to-end manner, achieving closed-loop "See → Think → Act" gameplay.

---

### 🔥 Featured Papers

#### **CombatVLA: An Efficient VLA Model for 3D Action RPGs**
> 🎮 *Black Myth: Wukong* | ⚡ 50× inference speedup

**Key Contributions:**
- **Truncated Action-of-Thought (AoT)**: Reduces reasoning overhead by 98%
- Achieves <20ms per-action latency on complex boss fights
- Handles dynamic camera & fast-paced combat mechanics

**Links:** [Paper](#) | [Code](#)

---

#### **JARVIS-VLA: Post-Training for Keyboard & Mouse Control**
> 🖱️ Visual-rich games | 🔧 Post-training LVLMs

**Key Contributions:**
- Post-trains large vision-language models to play games via keyboard/mouse
- No need for game-specific APIs or simulators
- Evaluated on strategy, puzzle, and action games

**Links:** [Paper](#) | [Project](#)

---

#### **MAIN-VLA: Modeling Abstraction of Intention and Environment**
> 🏢 Tencent/NetEase | 🎯 FPS games (Delta Force, Valorant)

**Key Contributions:**
- **2nd-gen VLA architecture** with streaming memory reasoning
- Intention & scene abstraction reduces redundant information by 70%
- Cross-game generalization without retraining

**Links:** [Paper](#) | [Demo](#)

---

#### **SIMA & SIMA 2: Generalist Embodied Agents**
> 🤖 Google DeepMind | 🌍 Multi-game (No Man's Sky, Goat Simulator, etc.)

**Key Contributions:**
- **SIMA 2**: Gemini Flash-Lite + self-evolution mechanism
- Instruction following in 3D virtual worlds
- Open-ended task completion without hardcoded behaviors

**Links:** [Paper (SIMA)](https://deepmind.google/discover/blog/sima-generalist-ai-agent-for-3d-virtual-environments/) | [SIMA 2](#)

---

#### **NitroGen: Open Foundation Model for Gaming**
> 🎮 1000+ games | ⏱️ 40K hours training data

**Key Contributions:**
- Based on **SigLIP + DiT** architecture
- Direct continuous gamepad output
- Pre-trained on massive multi-game dataset

**Links:** [Paper](#) | [Weights](#)

---

#### **OpenHA: Hierarchical Agents in Minecraft**
> ⛏️ Minecraft | 🧠 Fast-slow thinking framework

**Key Contributions:**
- Open-source hierarchical agent models
- High-level abstract actions + low-level VLA coordination
- Bridging symbolic planning and reactive control

**Links:** [Paper](#) | [Code](#)

---

#### **Lumine: Generalist Agents in 3D Open Worlds**
> 🌐 Genshin Impact | 🚀 30Hz real-time control

**Key Contributions:**
- Unified language reasoning + action generation
- Predicts millisecond-level **action chunks**
- Handles open-world navigation and combat

**Links:** [Paper](#) | [Project](#)

---

#### **OmniJarvis: Unified Vision-Language-Action Tokenization**
> ⛏️ Minecraft | 🔤 Unified tokenization

**Key Contributions:**
- Single tokenizer for vision, language, and actions
- Enables open-world instruction following
- Simplifies multimodal training pipeline

**Links:** [Paper](#) | [Code](#)

---

#### **UI-TARS / Game-TARS Series**
> 🖥️ GUI control | 🎮 Game automation

**Key Contributions:**
- General-purpose VLMs for GUI and game control
- Reinforcement learning for multi-round trial-and-error
- Evolution through self-play

**Links:** [UI-TARS Paper](#) | [Game-TARS](#)

---

#### **Cultivating Gaming Sense: Making VLMs Gaming Experts**
> 🧠 Human-like intuition | 📊 Data & RL training

**Key Contributions:**
- Explores how to instill "gaming sense" in VLMs
- Combines behavioral cloning and reward modeling
- Mimics human expert strategies

**Links:** [Paper](#)

---

## 🌍 World Models & World-Action Models

### Core Paradigm
**WAM/WM** models move beyond "see and react" to **"predict future states and then act"**, jointly modeling game dynamics and action consequences.

---

### 🔥 Featured Papers

#### **DreamZero: World Action Models are Zero-shot Policies**
> 🎥 Video diffusion → WAM | ⚡ 7Hz closed-loop control

**Key Contributions:**
- Converts pre-trained video diffusion models into closed-loop WAM
- **DreamZero-Flash**: Decoupled video/action denoising + feature caching
- Achieves <150ms latency for physics-based prediction

**Links:** [Paper](#) | [Project](#)

---

#### **WAIM: The DAWN of World-Action Interactive Models**
> 🔄 Bidirectional coupling | 🧠 Latent space rollout

**Key Contributions:**
- **Short-horizon latent rollout** avoids full pixel rendering
- Future world predictions guide action generation
- Action feedback refines world models iteratively

**Links:** [Paper](#) | [Code](#)

---

#### **Enhancing Policy Learning with World-Action Model**
> 🎮 DreamerV2++ | 🎯 Inverse dynamics

**Key Contributions:**
- Adds **inverse dynamics objective** to world models
- 10× sample efficiency improvement in RL
- Simultaneously predicts future frames and actions

**Links:** [Paper](#) | [Code](#)

---

#### **Genie Series (Genie, Genie 2, Genie 3)**
> 🤖 Google DeepMind | 🎬 Generative interactive environments

**Key Contributions:**
- **Genie 3**: 24fps 3D long-horizon consistent world generation
- Learns from **unlabeled videos** without action annotations
- Controllable world simulation for embodied AI

**Links:** [Genie 1](https://sites.google.com/view/genie-2024) | [Genie 2](#) | [Genie 3](#)

---

#### **GameNGen: Real-Time Neural Game Engine**
> 🎮 DOOM | 🖼️ Diffusion-driven rendering

**Key Contributions:**
- First **fully neural game engine** (no code, only model)
- Real-time interactive DOOM at >20fps
- Stable long-horizon rollouts (minutes)

**Links:** [Paper](https://gamengen.github.io/) | [Demo](#)

---

#### **Oasis: Interactive World Model for Minecraft**
> ⛏️ Minecraft | 🤖 Transformer-based

**Key Contributions:**
- Real-time interactive Minecraft world model
- Direct frame prediction from actions
- Supports multi-agent scenarios

**Links:** [Paper](#) | [Demo](#)

---

#### **Matrix-Game Series (1.0, 2.0, 3.0)**
> 🚀 Kunlun WanWei | 📈 40FPS real-time processing

**Key Contributions:**
- **Matrix-Game 3.0**: Error buffering + long-term memory
- Streaming inference for low latency
- Open-source large-scale interactive world models

**Links:** [Paper](#) | [Code](#)

---

#### **JOWA: Jointly-Optimized World-Action Model Pretraining**
> 🎮 Atari | 📦 Offline model-based RL

**Key Contributions:**
- Joint optimization of WAM + action prediction
- Enables offline RL policy transfer
- Scales to complex decision-making tasks

**Links:** [Paper](#) | [Code](#)

---

#### **Other Frontier WAM Architectures**
- **RynnVLA-002**: Unified VLA + WM vocabulary
- **WorldVLA**: Autoregressive action world model
- **DyWA**: Dynamic world-action coupling
- **Percept-WAM**: Perception-aware world models

---

## 📚 Surveys & Benchmarks

### Essential Reads

#### **Towards Generalist Game Players: An Investigation of Foundation Models in the Game Multiverse**
> 📖 Comprehensive survey | 🌐 Game multiverse

**Coverage:**
- Evolution of foundation models (LLM → VLM → VLA → WM → WAM)
- The **Latency-Intelligence Dilemma** in game AI
- Data ecosystem and future research directions
- Cross-game generalization challenges

**Links:** [Paper](#)

---

#### **World Action Models: The Next Frontier in Embodied AI**
> 📖 First systematic WAM survey | 🔬 Taxonomy

**Coverage:**
- Formal taxonomy: **Cascaded WAM** vs. **Joint WAM**
- Technical roadmap from VLA to WAM evolution
- Benchmarks and evaluation metrics
- Open challenges in long-horizon reasoning

**Links:** [Paper](#)

---

## 🔗 Related Resources

### Datasets
- **OpenGameData**: Multi-game behavioral dataset
- **NetHack Learning Environment**: Procedural generation + symbolic reasoning
- **MineDojo**: Minecraft foundation for open-ended agents
- **Atari 100K**: Sample-efficient RL benchmark

### Tools & Frameworks
- **LlamaFactory**: Efficient LLM/VLM fine-tuning
- **MineRL**: Minecraft RL research framework
- **Habitat**: Photorealistic 3D environments
- **Isaac Gym**: GPU-accelerated RL simulation

### Related Awesome Lists
- [Awesome Embodied AI](https://github.com/embodied-ai/awesome-embodied-ai)
- [Awesome World Models](https://github.com/awesome-wm/awesome-world-models)
- [Awesome Game AI](https://github.com/game-ai/awesome-game-ai)

---

## Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork** this repository
2. Add your paper to the appropriate section with:
   - Title, venue, and authors
   - Key contributions (3-5 bullet points)
   - Links to paper/code/demo
3. Submit a **Pull Request**

**Format:**
```markdown
#### **Paper Title**
> 🏢 Affiliation | 🎯 Key application

**Key Contributions:**
- Contribution 1
- Contribution 2
- Contribution 3

**Links:** [Paper](#) | [Code](#) | [Demo](#)
```

---

## Citation

If you find this resource helpful, please consider citing:

```bibtex
@misc{vla-wam-games-2026,
  title={Vision-Language-Action \& World Models for Game Agents},
  author={Community Contributors},
  year={2026},
  howpublished={\url{https://github.com/your-repo/vla-wam-games}}
}
```

---

## License

[![CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=your-repo/vla-wam-games&type=Date)](https://star-history.com/#your-repo/vla-wam-games&Date)

---

**Last Updated:** June 22, 2026  
**Maintainers:** [@your-github](#)  
**Contact:** your-email@example.com
