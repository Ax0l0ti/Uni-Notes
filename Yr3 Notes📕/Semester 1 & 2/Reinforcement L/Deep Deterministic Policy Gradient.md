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
> [[#]]


--- 
> [!tip]+ 🕰️* Speed run*
> Break down of topic 
> - DDPG is an off-policy algorithm.
> - DDPG can only be used for environments with continuous action spaces.
> - DDPG can be thought of as being deep Q-learning for continuous action spaces.
> - The Spinning Up implementation of DDPG does not support parallelization.
> HOWEVER
> TD3 optimal
> TD3 Twin Delayed DDPG gets rid of DDPG issues

---
[Proximal Policy Optimization — Spinning Up documentation](https://spinningup.openai.com/en/latest/algorithms/ppo.html)
[Deep Deterministic Policy Gradient — Spinning Up documentation](https://spinningup.openai.com/en/latest/algorithms/ddpg.html)
[Soft Actor-Critic — Spinning Up documentation](https://spinningup.openai.com/en/latest/algorithms/sac.html)

$L(\phi, {\mathcal D}) = \underset{(s,a,r,s',d) \sim {\mathcal D}}{{\mathrm E}}\left[\Bigg( Q_{\phi}(s,a) - \left(r + \gamma (1 - d) \max_{a'} Q_{\phi}(s',a') \right) \Bigg)^2\right]$



Pseudo code 
![[DDPG pseudo code.png]]
#TODO 


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