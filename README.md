# 🤖 3D Simulation for Training Robots

A Python-based project that trains a robot arm in a 3D virtual environment using **Reinforcement Learning** — before deploying it in the real world.

---

## 📌 Project Overview

This project focuses on creating a virtual environment where robots can be trained and tested before being used in real-world situations. The aim is to:

- ✅ Improve robot performance through simulation-based training
- ✅ Reduce testing costs by avoiding physical hardware during development
- ✅ Understand how robots learn and respond to different tasks and environments

---

## 🎯 What the Robot Does

The robot arm (Reacher-v4) learns to **reach a moving target point** using trial and error. It starts with zero knowledge and gradually improves through thousands of training steps — getting rewarded when it gets closer to the target and penalized when it misses.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** | Core programming language |
| **MuJoCo** | 3D physics simulation engine |
| **Gymnasium** | Robot training environment framework |
| **Stable-Baselines3** | Reinforcement Learning algorithms |
| **Matplotlib** | Graphs and visualizations |
| **NumPy** | Numerical computations |
| **Google Colab** | Cloud-based Python environment |

---

## 🧠 Algorithm Used

**PPO — Proximal Policy Optimization**

PPO is one of the most popular and stable Reinforcement Learning algorithms. It trains the robot by:
1. Trying different actions in the environment
2. Collecting rewards/penalties based on performance
3. Updating its strategy slowly and carefully to avoid forgetting what it learned

---

## 📊 Results

The project shows a clear **before vs after** comparison:

| Metric | Untrained Robot | Trained Robot |
|--------|----------------|---------------|
| Strategy | Random actions | Learned policy (PPO) |
| Performance | Very low rewards | Significantly higher rewards |
| Behavior | Chaotic movement | Directed movement toward target |

A reward graph is generated showing the robot's learning progress over time.

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com)
2. Create a new notebook
3. Run the following in the first cell:
```python
!pip install gymnasium stable-baselines3 mujoco matplotlib numpy --upgrade
```
4. Paste the code from `robot_training.py` and run it

### Option 2 — Local (Python 3.10 recommended)
```bash
pip install "gymnasium[mujoco]" stable-baselines3 matplotlib numpy
python robot_training.py
```

---

## 📁 Project Structure

```
robot-simulation-project/
│
├── robot_training.py      # Main training script
├── README.md              # Project documentation
```

---

## 📈 Output

Running the project generates:
- 📊 A **before vs after reward graph** (saved as `robot_training_results.png`)
- 📋 A **summary report** printed in the console showing improvement metrics
- 📉 Training logs showing learning progress step by step

---

## 💡 Key Concepts

**Reinforcement Learning** — The robot learns by interacting with the environment, receiving rewards for good actions and penalties for bad ones. Over thousands of steps, it figures out the best strategy.

**Simulation-to-Real (Sim2Real)** — Training in simulation first reduces cost, risk, and time before deploying on actual hardware. Used by companies like Boston Dynamics and Tesla.

**Reward Function** — The scoring system that guides the robot's learning. Higher reward = closer to target.

---

## 🔮 Future Improvements

- [ ] Train for more timesteps (100k, 200k) and compare results
- [ ] Try other algorithms (SAC, DDPG, TD3)
- [ ] Add more complex environments (walking robot, maze navigation)
- [ ] Reduce the sim-to-real gap with domain randomization
- [ ] Deploy trained model on a physical robot arm

---

## 👨‍💻 Author

**Utkarsh Rathod**
Summer Internship Project — 3D Simulation for Training Robots

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
