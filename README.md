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




<h1 align="center">MID TERM REPORT</h1>



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




<h1 align="center">END TERM REPORT</h1>


---



### 🕹️ Week 5-6: Applying DQN to Flappy Bird (Training & Fine-Tuning)

---

**What I Learned**

- How to **adapt DQN** from a classic control task (CartPole) to a complex environment (Flappy Bird)
- Importance of **state representation**: Image-based CNN vs. feature-based (position, pipe gap)
- Critical role of **reward shaping** and **hyperparameter tuning** in sparse-reward settings

---

**Resources Used**

- Previous **CartPole DQN** implementation
- **PyTorch** official documentation
- Online **RL course material** (Coursera, DeepMind research papers)
- **Flappy Bird PyGame** base code (YouTube: CodeEmporium, CodingBytes)

---

**What I Did**

- Reused the `DQNAgent` from CartPole, **modified for Flappy Bird's state inputs**
- Built two agent versions:
  - **Image-based CNN**
  - **Position-based features** (bird height, pipe gap, velocity)
- Trained the agent over **5000+ episodes** with **epsilon decay** strategy
- **Logged rewards** and **saved gameplay videos** to observe qualitative improvements

---

## Output & Results

| Episode Phase       | Observation                                                                 |
|---------------------|------------------------------------------------------------------------------|
| Initial Training     | No meaningful learning due to sparse rewards                                |
| Mid Training         | After tuning hyperparameters, agent began surviving longer                  |
| Final Episodes       | Agent consistently passed multiple pipes                                    |
| Evaluation Videos    | Demonstrated visible improvement in bird's flapping and obstacle avoidance  |

---

## 🚧 Challenges Faced

| Problem                             | Solution                                                   |
|-------------------------------------|-------------------------------------------------------------|
| Agent stuck in local minima         | Adjusted epsilon decay to encourage exploration             |
| Sparse rewards = poor learning      | Introduced **reward shaping** (e.g., +1 for good flap)      |
| Image-based model too slow          | Switched to position-based features for faster iteration    |

---

## 🧠 Key Learnings

- DQN **generalizes well** to custom environments with properly shaped rewards
- **Visual feedback** (videos) is crucial to validate agent’s learning
- **Patience is key** — RL agents learn slowly, but results compound

---

## 📈 Experimental Summary

| Environment        | Agent Behavior                          | Max Reward Achieved |
|--------------------|------------------------------------------|----------------------|
| `CartPole-v1`      | Balances pole reliably after training    | > 180                |
| `FlappyBird-PyGame`| Survives 3–5 pipes; learning is visible  | Improving steadily   |

---

## ✨ Final Reflections

### 🛠️ Technical Skills Gained
- In-depth understanding of **DQN internals**: Target networks, Replay Buffers, etc.
- Gained confidence in **PyTorch model design** and debugging training loops
- Hands-on experience with **OpenAI Gym** & **PyGame** for environment integration

### 👨‍💻 Personal Learning
- Balanced **theory and implementation** effectively
- Improved in **real-time debugging**, especially in game-like environments
- Learned the true value of **trial-and-error** in reinforcement learning

---

> 🏁 *This was a major milestone in my RL journey — applying core concepts to a real, dynamic game and observing my agent evolve from random flapping to consistent survival!*


##🙏 Acknowledgements

I would like to sincerely thank my mentor and the SoS’25 team for their constant guidance, timely feedback, and for structuring this opportunity in a way that allowed deep exploration without overwhelming deadlines. This has been one of the most enriching academic experiences I've had so far.

---

## 📚 **REFERENCES / RESOURCES**

- [OpenAI Gym Docs](https://www.gymlibrary.dev/)  
- [Deep Q-Network (DQN) Paper](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf)  
- [Coursera – RL Module](https://www.coursera.org/learn/unsupervised-learning-recommenders-reinforcement-learning)  
- [YouTube Playlist – RL Concept Clarity](https://www.youtube.com/playlist?list=PLKnIA16_RmvbMK0_fdp0DZHZKm4Q1slAB)  
- [CodeEmporium YouTube](https://www.youtube.com/@CodeEmporium)  
- [Flappy Bird RL – TensorFlow + PyGame](https://www.youtube.com/watch?v=cM2a7AQeh6w)

---
