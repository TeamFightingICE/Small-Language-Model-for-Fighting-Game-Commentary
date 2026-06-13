# Real-Time FTG AI Combat & Commentary System 🎮

An integrated platform for fighting game AI built on the `FightingICE` framework. This system combines a **Deep Reinforcement Learning agent (BlackMamba)** for ultra-low latency combat decision-making with a **Large Language Model (T5)** to generate real-time, e-sports style commentary based on live frame data.

## 📁 Project Structure

```text
Commentary/
├── real_ftg_launcher.py          # Main entry: Launcher, gateway connection & UI overlay
├── fixed_blackmamba_agent.py     # Combat core: RL agent with action masking & frame skip
├── realtime_commentary_system.py # Commentary core: Frame analyzer & async LLM generator
├── checkpoint/                   # Directory for T5 model weights (model.pt)
├── BlackMamba/ZEN/normal/        # Directory for BlackMamba network weights (.csv)
└── blackmambarecord/             # Auto-generated combat frame records
```

How to run?
Make sure you have a GPU(Nvidia) and linux enviroment.
