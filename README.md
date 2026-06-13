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

### How to run?

1.Make sure you have a GPU(Nvidia) and linux enviroment. (Python 3.11)

2.run
pip install pyftg loguru numpy sentencepiece

pip install transformers==4.30.0

3.Install the PyTorch version that matches your CUDA environment.

4.Ensure the FightingICE Java server is running and listening on 127.0.0.1:31415

5.Start the combat and commentary system:  python real_ftg_launcher.py --games 3 --opponent RandomAI

Common Arguments:
--games: Number of matches to play (default: 5).

--opponent: Opponent AI name (e.g., RandomAI, MctsAi23i).

--character: Character to use (default: ZEN).

--device: Compute device to use (cuda or cpu).

--no-commentary: Disable real-time commentary and the UI overlay.

6.Subtitle Overlay Guide
Upon running the script, a black semi-transparent bar will appear on your screen.

Click and drag this bar to a suitable position over your FightingICE game window (e.g., just below the health bars).

The UI will automatically display the generated commentary in real-time and clear itself after 5 seconds of inactivity.
