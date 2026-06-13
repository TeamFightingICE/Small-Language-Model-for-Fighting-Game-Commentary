# Real-Time FTG AI Combat & Commentary System 🎮

An integrated platform for fighting game AI built on the `FightingICE` framework. This system combines a **Deep Reinforcement Learning agent (BlackMamba)** for ultra-low latency combat decision-making with a **Large Language Model (T5)** to generate real-time, e-sports style commentary based on live frame data.

## ✨ Key Features

- **Dual AI Engine:** Integrates BlackMamba (RL) for ~2ms combat inference and T5 for dynamic, context-aware commentary generation.
- **Asynchronous Architecture:** Non-blocking commentary generation using `asyncio.to_thread` ensures smooth 60 FPS gameplay without freezing the game engine.
- **Immersive Subtitle UI:** Features a draggable, borderless, and transparent Tkinter overlay to display real-time commentary directly over the game window.
- **Safe Action Routing:** Built-in action masking prevents the AI from executing invalid or passive states, ensuring continuous offensive/defensive flow.
- **GPU Accelerated:** Optimized tensor routing for high-performance inference on NVIDIA GPUs.

## 📁 Project Structure

```text
Commentary/
├── real_ftg_launcher.py          # Main entry: Launcher, gateway connection & UI overlay
├── fixed_blackmamba_agent.py     # Combat core: RL agent with action masking & frame skip
├── realtime_commentary_system.py # Commentary core: Frame analyzer & async LLM generator
├── checkpoint/                   # Directory for T5 model weights (model.pt)
├── BlackMamba/ZEN/normal/        # Directory for BlackMamba network weights (.csv)
└── blackmambarecord/             # Auto-generated combat frame records
