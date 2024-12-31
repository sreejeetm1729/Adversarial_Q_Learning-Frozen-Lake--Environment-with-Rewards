# Robust-Frozen ❄️ -Lake-Environment-with-Adversarial-Rewards (🏗️)

FrozenLake is a popular grid-based environment used in reinforcement learning (RL) to test and develop decision-making algorithms. The environment consists of a frozen grid representing a lake with four types of tiles: Start (S), Frozen (F), Hole (H), and Goal (G). The objective for the agent is to navigate from the start tile to the goal tile, avoiding the holes, which cause the agent to fall and reset the episode. Frozen tiles are safe for traversal, while hole tiles represent failure states. The goal tile is the destination, and reaching it ends the episode successfully. It is often configured in two versions: "slippery" and "non-slippery." In the slippery version, the agent's actions may not always result in the intended movement due to the icy surface, introducing a stochastic element where the agent can slip in unintended directions. This adds complexity as the agent needs to factor in uncertainty while planning its moves. In contrast, the non-slippery version is deterministic, with actions leading to predictable outcomes. The environment typically uses a simple 4x4 or 8x8 grid, where the agent can choose from four possible actions: moving left, right, up, or down. Rewards in FrozenLake are sparse: the agent generally receives a reward of 0 for each step, with a reward of 1 upon reaching the goal. FrozenLake is used to study exploration versus exploitation trade-offs and test RL algorithms' ability to handle uncertainty and risk in sequential decision-making. The challenge lies in balancing exploration of the grid and exploitation of known safe paths to maximize long-term rewards. Its simplicity, coupled with stochastic elements, makes it a valuable testbed for Q-learning, deep reinforcement learning, and robust learning strategies under uncertainty.

What we did ? 🍬
Our ε-Robust Q-Learning algorithm enhances traditional Q-learning in the FrozenLake environment by integrating robust statistical methods to combat reward corruption. The algorithm navigates a grid of frozen tiles, aiming to reach a goal while avoiding holes, all while dealing with noise introduced by corrupted rewards. Instead of relying solely on raw rewards, it employs a univariate trimmed mean approach to estimate rewards, filtering out outliers and ensuring more stable learning. A threshold function limits the influence of extreme reward estimates, providing additional stability in Q-value updates. By using an ε-greedy strategy for action selection, the agent balances exploration and exploitation effectively, adapting over time to focus on learned strategies. This robust learning framework ensures the agent can reliably learn optimal policies even in the presence of adversarial conditions, making it particularly valuable for real-world applications where data integrity can be compromised.

This numerical simulation in the frozen world environment aligns with our proven result, accepted for presentation, and publication at the 63rd IEEE Conference on Decision and Control.
<table>

<tr>
  <td>
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github_3.png" style="width:320px">
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github.png" style="width:320px">
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github_1.png" style="width:320px">
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github_4.png" style="width:320px">
 </td>
</tr>

Now, we wish to test our algorithm in a slightly more challenging setting. We will turn the slippery conditions on. This means, the player will move in the intended direction with a probability of 1/3 else will move in either perpendicular direction with an equal probability of 1/3 in both directions. 

<table>

<tr>
  <td>
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github_3.png" style="width:320px">
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github.png" style="width:320px">
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github_1.png" style="width:320px">
    <img src="https://github.com/sreejeetm1729/Adversarial_Q_Learning-Frozen-Lake--Environment-with-Rewards/blob/main/github_4.png" style="width:320px">
 </td>
</tr>
