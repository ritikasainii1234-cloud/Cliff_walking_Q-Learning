🤖 Q-Learning Implementation using Cliff Walking Environment

This project demonstrates the implementation of the Q-Learning algorithm, a popular Model-Free Reinforcement Learning algorithm, using the CliffWalking-v1 environment from Gymnasium.

The agent learns an optimal policy by interacting with the environment and updating a Q-table based on the rewards it receives.

📌 Project Overview
Algorithm: Q-Learning
Environment: CliffWalking-v1
Library: Gymnasium
Programming Language: Python
Learning Type: Model-Free Reinforcement Learning

The objective is to train an agent to reach the goal while avoiding the cliff, maximizing the cumulative reward.

🛠️ Technologies Used
Python
NumPy
Gymnasium
Random
📂 Project Structure
Q_Learning/
│
├── Q_Learning.ipynb
└── README.md
📖 Algorithm Steps
Initialize the Q-table with zeros.
Set hyperparameters:
Learning Rate (α)
Discount Factor (γ)
Exploration Rate (ε)
Start each episode.
Select an action using the ε-Greedy Policy.
Perform the selected action.
Observe:
Next State
Reward
Update the Q-value using the Q-Learning update equation.
Repeat until the episode ends.
Continue training for multiple episodes.
🔄 Q-Learning Update Formula
Q(s,a)=Q(s,a)+α[R+γ
a
′
max
	​

Q(s
′
,a
′
)−Q(s,a)]

Where:

Q(s,a) → Current Q-value
α (Alpha) → Learning Rate
γ (Gamma) → Discount Factor
R → Reward
s' → Next State
max Q(s',a') → Maximum future reward
⚙️ Hyperparameters
Parameter	Value
Episodes	500
Learning Rate (α)	0.5
Discount Factor (γ)	0.99
Epsilon (ε)	0.1
🎯 Environment

The project uses the CliffWalking-v1 environment.

Grid World Environment
Start Position
Goal Position
Cliff Region
Stepping into the cliff gives a large negative reward and resets the agent.

The agent learns the safest and shortest path to the goal.

🧠 Exploration Strategy

This implementation uses the Epsilon-Greedy Policy.

10% of the time → Explore random actions.
90% of the time → Exploit the best known action from the Q-table.

This balances Exploration and Exploitation.

📊 Training Process

During training:

The environment is reset for every episode.
The agent interacts with the environment.
Q-values are updated after every action.
Episode reward and episode length are displayed.
Every 50 episodes, the environment is rendered for visualization.
📈 Results

After training:

The learned policy is tested.
The agent follows the action with the highest Q-value.
Total reward is displayed.
Episode length is displayed.
Learned Q-values for selected states can be inspected.
