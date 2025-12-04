# Deep Deterministic Policy Gradient
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  17-11-2025
> > *Module :* [[Reinforcement Learning]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#About DDPG]]
> [[#About TD3]]
> [[#Notes on CW]]


--- 
> [!tip]+ 🕰️* Speed run*
> Break down of topic 
> - DDPG is an off-policy algorithm. OG Paper [[1509.02971] Continuous control with deep reinforcement learning](https://arxiv.org/abs/1509.02971)
> - DDPG can only be used for environments with continuous action spaces.
> - DDPG can be thought of as being deep Q-learning for continuous action spaces.
> - The Spinning Up implementation of DDPG does not support parallelization.
> HOWEVER
> TD3 optimal OG Paper [[1802.09477] Addressing Function Approximation Error in Actor-Critic Methods](https://arxiv.org/abs/1802.09477)
> TD3 Twin Delayed DDPG gets rid of DDPG issues
> Talk about OG DDPG 

---
[Proximal Policy Optimization — Spinning Up documentation](https://spinningup.openai.com/en/latest/algorithms/ppo.html)
[Deep Deterministic Policy Gradient — Spinning Up documentation](https://spinningup.openai.com/en/latest/algorithms/ddpg.html)
[Soft Actor-Critic — Spinning Up documentation](https://spinningup.openai.com/en/latest/algorithms/sac.html)

$L(\phi, {\mathcal D}) = \underset{(s,a,r,s',d) \sim {\mathcal D}}{{\mathrm E}}\left[\Bigg( Q_{\phi}(s,a) - \left(r + \gamma (1 - d) \max_{a'} Q_{\phi}(s',a') \right) \Bigg)^2\right]$

## About DDPG

Pseudo code 
![[DDPG pseudo code.png]]
#TODO 


## About TD3
## TD3 
BRUUUUUHHHHH 


The **Twin Delayed Deep Deterministic Policy Gradient (TD3)** algorithm is an advanced reinforcement learning method designed for environments with continuous action spaces. It builds upon the **Deep Deterministic Policy Gradient (DDPG)** algorithm, addressing its limitations, particularly the overestimation bias in value function estimation. TD3 achieves this through several key modifications, making it more robust and effective for continuous control tasks.

Key Features of TD3

1. **Clipped Double Q-Learning**: TD3 uses two Q-value functions (critics) and selects the minimum Q-value during policy updates. This reduces overestimation bias by providing a more conservative estimate of the value function.
    
2. **Delayed Policy Updates**: The policy (actor) and target networks are updated less frequently than the Q-value functions. This helps stabilize training and prevents premature convergence to suboptimal policies.
    
3. **Target Policy Smoothing**: Noise is added to the target action during updates, making the policy less sensitive to small perturbations and improving robustness.
    
4. **Experience Replay**: TD3 uses a replay buffer to store past experiences and samples mini-batches for training. This decorrelates data and improves learning efficiency.
    
5. **Target Networks**: TD3 maintains target networks for both the actor and critics, which are updated periodically or using a smoothing factor to stabilize training.
    

Algorithm Workflow

1. Initialize the actor and two critics with random parameters, along with their corresponding target networks.
    
2. Perform a warm-up phase by taking random actions and storing experiences in the replay buffer.
    
3. For each training step: Select an action by adding noise to the actor's output. Execute the action, observe the reward, and store the experience in the buffer. Sample a mini-batch of experiences from the buffer. Compute the target Q-value using the minimum of the two target critics and the smoothed target policy. Update the critics by minimizing the loss between the predicted and target Q-values. Update the actor periodically using the sampled policy gradient. Update the target networks using smoothing or periodic updates.

---


## Notes on CW

The shift from Ornstein-Uhlenbeck (OU) noise to Standard Gaussian (White) noise in TD3 is primarily due to **Occam's Razor**: Gaussian noise is simpler, easier to tune, and empirically performs just as well (or better) for most Deep Reinforcement Learning tasks. Reasons TD3 authors (Fujimoto et al.) made this change:
### 1. Complexity vs. Necessity

- **OU Noise:** Designed to model **Brownian motion** with friction. It is "temporally correlated," meaning if the noise is positive at step $t$, it is likely to be positive at step $t+1$. **The original DDPG authors believed this was necessary to simulate "inertia" in physical control tasks (like swinging a pendulum).**
    
- **The Reality:** Later research showed that this correlated noise wasn't actually driving the learning performance. The neural network policy naturally learns smooth trajectories over time.
    
- **The TD3 Fix:** Standard Gaussian noise is uncorrelated. It is much simpler to implement and requires tuning only one parameter (variance/sigma) rather than three (theta, sigma, mu).
    

### 2. Tuning Difficulty

OU noise is notoriously annoying to tune. You have to balance:

- **Theta ($\theta$):** How fast it reverts to the mean.
    
- **Sigma ($\sigma$):** The magnitude of the noise.
    
- **Mu ($\mu$):** The mean (usually 0).
    

If you set $\theta$ wrong, the agent might get stuck applying maximum force in one direction for too long, destabilizing training. Gaussian noise simply adds a random jitter to the action at every step, which is predictable and robust.

### 3. Target Policy Smoothing (Specific to TD3)

This is a critical distinction. TD3 uses noise in two different places:

1. **Exploration (Action Selection):** To explore the environment.
    
2. **Target Smoothing (Update Step):** To regularize the Value function.