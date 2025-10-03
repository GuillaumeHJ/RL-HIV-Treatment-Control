# RL HIV Treatment Control

## Project Overview

This project was completed as part of the Reinforcement Learning course at ENS (MVA) in 2024–25. The assignment aimed to design and train a Reinforcement Learning (RL) agent to control the treatment of HIV patients through structured treatment interruption (STI), balancing drug administration to maintain patient health while avoiding side effects and resistance. 

The project is inspired by the works of Ernst et al. (2006) and Adams et al. (2004), simulating the patient's immune system through six state variables (CD4/CD8 cells, infected cells, virus particles).  

## Objectives

- Develop a reinforcement learning agent capable of optimizing HIV treatment strategies.
- Interact with a deterministic, Gym-like simulation environment (`HIVPatient`).
- Explore various RL algorithms and training strategies.
- Evaluate the agent on default and randomized patients via automated tests.

## Repository Structure

```text
RL-HIV-Treatment-Control/
├── README.md
├── requirements.txt
├── notebooks/
│   └── rl_mva_HIV.ipynb   # Colab notebook to launch training and evaluation
├── src/
│   ├── env_hiv.py          # Simulator (do not modify)
│   ├── interface.py        # Agent interface (do not modify)
│   ├── evaluate.py         # Evaluation script (do not modify)
│   ├── train.py            # Your RL agent implementation
│   └── main.py             # Entry point for automated evaluation
└── saved_models/           # Folder to store trained agent(s)
```

- `src/train.py`: Your RL agent implementation (DQN with epsilon-greedy and RMSProp optimization).  
- `saved_models/`: Store trained models here.  

## Your Contributions

- Implemented a **DQN agent** with customizable neural network architectures.
- Applied **epsilon-greedy exploration** for policy optimization.
- Used **RMSProp optimizer** to stabilize training.
- Experimented with **different layer architectures** to balance learning speed and stability.
- Successfully trained the agent to pass **8/9 automated evaluation tests** on the GitHub Classroom challenge.

## Colab Notebook

For convenience, you can launch training and evaluation in Google Colab using the provided notebook:

`notebooks/rl_mva_HIV.ipynb`

This notebook allows you to:

- Run the RL agent training interactively.
- Monitor training progress and performance metrics.
- Load saved models from `saved_models/` for evaluation or further experimentation.

Simply open the notebook in Colab, ensure the `src/` folder is mounted or copied, and run the cells sequentially.
