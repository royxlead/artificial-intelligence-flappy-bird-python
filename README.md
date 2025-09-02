# Flappy Bird AI with NEAT (Python)

A Python-based **Flappy Bird game** enhanced with **AI using the NEAT (NeuroEvolution of Augmenting Topologies)** algorithm. Watch a neural network evolve over generations to master navigating through obstacles with increasing finesse.

## Features

* **AI-Controlled Gameplay**: Birds learn to play using NEAT-driven neural networks.
* **Real-Time Visualization**: Observe the AI improve its skills frame by frame.
* **Configurable AI Behavior**: Tweak NEAT parameters via `config.txt` for different evolution strategies.
* **Checkpointing / Model Loading**: Save and reload high-performing neural networks across runs.

## Demo

Imagine watching this: a swarm of birds flapping through gaps—with each generation getting smarter. Each run showcases the evolution of smarter decision-making over time.

## Installation & Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/royxlead/artificial-intelligence-flappy-bird-python.git
   cd artificial-intelligence-flappy-bird-python
   ```

2. **Install dependencies**

   ```bash
   pip install pygame neat-python
   ```

3. **Customize AI behavior (optional)**

   Modify settings like `pop_size`, `mutation_rate`, or `fitness_threshold` in `config.txt` to influence how quickly and effectively the AI evolves.

4. **Run the game**

   ```bash
   python main.py
   ```

   Sit back and watch the neural birds learn to fly.

## Project Structure

```
artificial-intelligence-flappy-bird-python/
├── main.py        # Launches game and handles NEAT evolution loop
├── config.txt     # NEAT configuration parameters
├── imgs/          # Image assets (bird, pipes, background, etc.)
├── winner.pkl     # (Optional) Saved best-performing AI model
├── neat-log.log   # Log of each generation's progress
├── README.md      # This documentation
└── LICENSE        # MIT License
```

## How It Works

* **Initialization**: NEAT starts with a population of randomly initialized neural networks (birds).
* **Simulation**: Each bird attempts to navigate the Flappy Bird obstacles.
* **Fitness Evaluation**: Birds are scored based on how far they fly—passing more pipes = higher fitness.
* **Evolution**: Top performers are selected and mutated to form the next generation.
* **Iteration**: This evolutionary cycle repeats—generation after generation—until the AI consistently achieves high scores.

## Future Enhancements

* **Human Play Mode**: Allow players to switch between controlling the bird and watching AI play.
* **Performance Tracking**: Display fitness graphs or plots for each generation.
* **UI Improvements**: Add pause/restart buttons, real-time metrics, or speed adjustment.
