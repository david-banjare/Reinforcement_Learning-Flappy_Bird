# **REINFORCEMENT LEARNING – FLAPPY BIRD**
A Reinforcement Learning project that implements a Deep Q-Network (DQN) agent to play Flappy Bird, including environment setup, training logic, and visual gameplay using Pygame.


## 🗂️ **Overview**

This project is part of my **Summer of Code (SoC)** learning journey, where I am building a custom Reinforcement Learning (RL) agent to play the classic game **Flappy Bird**.
The goal is to train an agent using **Deep Q-Learning (DQN)** to learn how to flap between pipes and survive — all without any pre-programmed strategy. Inspired by the real-world decision-making process, this project helped me understand how agents learn through rewards, actions, and exploration.

The project started with a refresher in core Python programming concepts, followed by a structured introduction to the foundational theory behind Reinforcement Learning. I implemented my first RL agent using DQN on the classic CartPole environment from OpenAI Gym, and then progressed to developing a fully custom RL-compatible Flappy Bird environment using Pygame.

All my work is organized and uploaded to a public GitHub repository, which includes the Python refresher notebook, CartPole DQN implementation, and the custom Flappy Bird environment.


## ⚙️ **TECH STACK USED**

- **Python 3.x** – Core programming language  
- **PyGame** – To build and render the Flappy Bird environment  
- **NumPy** – Array operations and math  
- **TensorFlow** – Neural network backend for DQN  
- **OpenAI Gym** – API structure reference for creating environments  
- **Matplotlib** – For training plots and reward curves  

---

## 📆 **WEEK-WISE PROGRESS**

All modules from this course are structured to have units in a week-by-week format where I can record what requires to be done, achieved milestones, learned as well as self-reflected upon my progress within each module:

---

### **Week 0: Python Revision**

 **What I Learned:**
- Refreshed Python syntax, classes, functions, data structures  
- Practiced NumPy and Matplotlib basics

**What I Did:**
- Completed one of the 3 mentor-recommended videos (~3 hours)  
- Finished assignment: `python_assignment.ipynb` with examples

---

### **Week 1–2: RL Fundamentals + Gym Exploration**

**What I Learned:**
- Key concepts: Agent, Environment, State, Action, Reward  
- Q-learning, Exploration vs. Exploitation  
- Understanding of Markov Decision Processes (MDPs)

🛠 **Resources Used:**
- Coursera RL module  
- OpenAI Gym documentation  
- CodeEmporium’s RL intro video  
- Concept clarity playlist (YouTube)

**What I Did:**
- Explored built-in environments like `CartPole-v1`, `MountainCar-v0`  
- Understood how Gym defines observation/action spaces

---

### **Week 3: Deep Q-Learning on CartPole**

**What I Learned:**
- Deep Q-Network (DQN) architecture  
- Replay Buffer, Target Networks, Epsilon-Greedy strategy  
- Backpropagation and Q-value updates

**Resources Used:**
- DQN research paper (DeepMind)  
- CodeEmporium tutorial (CartPole setup + DQN explanation)

**What I Did:**
- Implemented DQN from scratch for `CartPole-v1`  
- File: `CartPole_DQN_Submission_24B0359.ipynb`  
- Used TensorFlow to define the Q-Network  
- Integrated Gym environment with model training loop

**Output:**
- Agent initially failed but started balancing the pole within 200 episodes  
- Training rewards gradually increased  
- Epsilon decayed correctly → more exploitation over time

 **Challenges Faced:**
- Understanding `tf.GradientTape()` and weight updates  
- Figuring out how to tune hyperparameters like gamma, epsilon

---

### **Week 4: Custom Flappy Bird Environment (PyGame)**

 **What I Learned:**
- Designing RL environments from scratch  
- Creating observation & action spaces manually  
- Integrating PyGame loops with Gym-like APIs

 **Resources Used:**
- CodeEmporium + CodingBytes videos  
- Flappy Bird + TensorFlow tutorial (YouTube)

 **What I Did:**
- Built a full Flappy Bird game using PyGame  
- Added `step()` and `reset()` functions (like OpenAI Gym)  
- Defined collision logic, scoring, and reward system  
- File: `flappy_custom_env.ipynb`

**Output:**
- Environment runs frame-by-frame  
- Game resets on collision  
- Rewards: +1 for passing pipes, -10 on collision  
- Successfully trained a basic agent loop for short-term learning

 **Challenges Faced:**
- Setting reward functions that promote learning  
- Debugging collisions and pipe generation logic  
- Integrating PyGame visuals with agent training loop

---

## 🧠 **KEY LEARNINGS**

- Learned how **agents learn via trial, error, and rewards**  
- Understood the **DQN architecture** and why it's effective for games  
- Built confidence in using **Gym-style APIs and PyGame rendering**  
- Developed a deeper appreciation for **reward tuning and exploration trade-offs**

---

## 🚧 **CHALLENGES FACED**

| Problem | Solution |
|--------|----------|
| Agent not learning on CartPole | Tuned epsilon decay and learning rate |
| Custom environment crashing | Isolated step/reset bugs in PyGame |
| Unstable training rewards | Used fixed target network updates |
| Reward shaping issues in Flappy Bird | Tweaked positive and negative reward balance |

---

## 📈 **EXPERIMENTAL RESULTS**

| Environment        | Agent Behavior                          | Max Reward Achieved |
|--------------------|------------------------------------------|----------------------|
| `CartPole-v1`      | Balances pole successfully after training | > 180               |
| `FlappyBird-PyGame`| Avoids 3–5 pipes with basic training      | Improving gradually |

Agent is learning basic survival — future episodes will improve flapping timing and score.

---

## 🚀 **FUTURE PLANS**

- Train the Flappy Bird agent using full DQN pipeline  
- Add model save/load functionality  
- Try Double DQN and Dueling DQN variants  
- Add real-time reward graphs and training logs  
- Record gameplay video of the learned agent  
- Finalize all notebooks with comments + cleanup  

---

## 📚 **REFERENCES / RESOURCES**

- [OpenAI Gym Docs](https://www.gymlibrary.dev/)  
- [Deep Q-Network (DQN) Paper](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf)  
- [Coursera – RL Module](https://www.coursera.org/learn/unsupervised-learning-recommenders-reinforcement-learning)  
- [YouTube Playlist – RL Concept Clarity](https://www.youtube.com/playlist?list=PLKnIA16_RmvbMK0_fdp0DZHZKm4Q1slAB)  
- [CodeEmporium YouTube](https://www.youtube.com/@CodeEmporium)  
- [Flappy Bird RL – TensorFlow + PyGame](https://www.youtube.com/watch?v=cM2a7AQeh6w)

---
