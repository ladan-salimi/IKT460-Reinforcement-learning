# 20 Questions Game with Reinforcement Learning

This project implements a reinforcement learning agent that plays a 20 Questions-style game to guess an animal based on binary features. The agent interacts by asking yes/no questions derived from the feature set and attempts to identify the correct animal using strategic reasoning and reward-based learning.

This is the final project for the course IKT460 Reinforcement Learning at the University of Agder.

This project was made by Ladan Salimi and Dominika I. Kowalska.

---

### 1. Version 1 - Baseline REINFORCE
**File:** `Version 1_Baseline_Reinforce.ipynb`  
- Implements the REINFORCE algorithm with a custom elimination-based reward function.
- Rewards are based on the number of animals eliminated after each question.
- Repeated questions are penalized.
- Final reward is given for correct or incorrect guesses.
- Achieves **~40% win rate** after **20,000 episodes**.

---

### 2. Version 2 - Improved REINFORCE with T5 and Guesser
**File:** `Version2_Improved_Reinforce_T5small.ipynb`  
- Builds on Version 1 with two key enhancements:
  - A **T5-small language model** generates natural language yes/no questions from features.
  - A **guesser network** replaces dot-product similarity, enabling better prediction of the target animal.
- Retains elimination-based reward strategy for informative question selection.
- Achieves **~62% win rate** after only **15,000 episodes**, showing improved learning efficiency.

---

### 3. Version 3 - PPO-Based Agent
**File:** `Version 3_PPO.ipynb`  
- Implements the **Proximal Policy Optimization (PPO)** algorithm.
- Uses the same reward structure and environment setup as previous versions.
- Offers algorithmic comparison with REINFORCE.
- Achieves **~35% win rate**, showing moderate improvement over baseline but lower than the improved REINFORCE version.

---

### 4. Dataset
**File:** `knowledge_base1.xlsx`  
- Contains the animal knowledge base used across all versions.
- 100 animals × 28 binary features (e.g., Hair, Feathers, Milk, Tail, etc.).

---

## Evaluation
- Each version includes an evaluation routine to measure agent accuracy.
- Metrics include win rate (%) and training episode count.

---

## Requirements
- Python ≥ 3.8  
- PyTorch  
- Transformers (`pip install transformers`)  
- pandas, numpy, matplotlib, openpyxl 

