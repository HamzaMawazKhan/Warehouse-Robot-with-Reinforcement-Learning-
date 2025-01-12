# Optimizing Autonomous Warehouse Robot Navigation Using Deep Reinforcement Learning

## Project Overview
This project explores the application of Deep Reinforcement Learning (DRL) to optimize robot navigation in a warehouse environment. Using Deep Q-Networks (DQN) and Double DQN (DDQN), the robot agent learns to navigate a grid, avoid obstacles, and complete tasks like picking up and delivering items to specified drop-off points. The project compares DQN and DDQN approaches, analyzing their performance in deterministic and stochastic settings.

---

## Objectives
- Implement reinforcement learning algorithms to optimize autonomous robot navigation.
- Compare and analyze the effectiveness of DQN and DDQN in learning optimal policies.
- Ensure robust and stable training through advanced techniques such as experience replay and target networks.

---

## Key Features
- **Algorithms:** Implemented DQN and DDQN algorithms for policy learning.
- **Environment:** A warehouse grid with:
  - Obstacles represented as impassable grid cells.
  - Specific pick-up and drop-off points for items.
  - Rewards for task completion and penalties for collisions or inefficient actions.
- **Performance Metrics:** Cumulative rewards, epsilon decay trends, and convergence rates.

---

## Methods and Techniques
1. **Reward System**
   - Step penalty: -1
   - Collision penalty: -20
   - Task completion reward: +20
   - Goal: Maximize cumulative rewards per episode.

2. **Algorithms**
   - **Deep Q-Network (DQN):**
     - Leveraged a single Q-network with experience replay and target networks to reduce temporal correlations and improve stability.
   - **Double DQN (DDQN):**
     - Separated action selection and evaluation using two networks (online and target) to mitigate overestimation bias.

3. **Hyperparameter Tuning**
   - Learning Rate: 0.6
   - Gamma: 0.6
   - Epsilon Decay: Smooth decay from 1.0 to 0.4 over 1,000 episodes.

4. **Optimization Techniques**
   - Replay buffer to reuse experiences for efficient training.
   - Target network for stable Q-value updates.
   - Safety constraints to prevent invalid moves at grid edges.

---

## Results
### DQN and DDQN Performance
- **Deterministic Environment:**
  - Both algorithms converged to the maximum cumulative reward of 13 per episode.
  - DQN demonstrated faster convergence, while DDQN provided more stable learning.
- **Stochastic Environment:**
  - DQN achieved quicker stabilization.
  - DDQN exhibited reduced overestimation bias but faced more variability in early training episodes.

### Comparative Analysis
| Metric                | DQN                        | DDQN                     |
|-----------------------|----------------------------|--------------------------|
| Convergence Speed     | Faster                     | Slower                   |
| Stability             | Moderate                  | Higher                   |
| Overestimation Bias   | Present                   | Mitigated                |


## Author
**Hamza Mawaz Khan**  
Master's in Data Science, University at Buffalo  

