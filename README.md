# Flappy Bird AI with NEAT

This project uses the NEAT (NeuroEvolution of Augmenting Topologies) algorithm to evolve an AI that learns to play the Flappy Bird game. The game is implemented using Pygame, and the AI is trained to navigate through the pipes using a neural network.

## Features

- **AI-Controlled Birds**: Birds are controlled by a neural network evolved using the NEAT algorithm.
- **Real-time Training Visualization**: Watch the birds learn and improve their performance over generations.
- **Logging**: Logs key events like bird jumps, collisions, and score updates.
- **Checkpointing**: Saves the best-performing neural network for future use.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/heysouravroy/AI_Flappy_Bird.git
    cd AI_Flappy_Bird
    ```

2. **Install dependencies**:
    Make sure you have Python 3.7 or later installed. You can install the required packages using pip:
    ```bash
    pip install pygame neat-python
    ```

## Usage

1. **Configure NEAT**:
    - The configuration for the NEAT algorithm is specified in the `config.txt` file. You can modify this file to tune the parameters for the genetic algorithm.

2. **Run the game**:
    ```bash
    python main.py
    ```

    This will start the training process. The AI will begin learning to play Flappy Bird. You can observe the progress in real-time.

3. **Load a previous winner**:
    - The program will automatically load a saved winner if available (`winner.pkl`). If not, it will start fresh.

## File Structure

- `main.py`: The main script to run the game and train the AI, containing the Bird, Pipe, and Base classes.
- `config.txt`: Configuration file for the NEAT algorithm.
- `imgs/`: Directory containing image assets for the game.
- `winner.pkl`: Serialized file to save the best-performing neural network.
- `neat-log.log`: Log file that stores information about the birds, including where they crash and how many birds are in the game.

## How It Works

1. **Initialization**: Pygame initializes the game window, loads images, and sets up logging.
2. **Bird Movement**: Birds move according to physics rules, jumping when activated by the neural network.
3. **Pipe Generation**: Pipes are generated at intervals and move across the screen.
4. **Collision Detection**: The game checks for collisions between birds and pipes or the ground.
5. **Fitness Calculation**: The fitness of each bird is calculated based on its survival time and distance traveled.
6. **Neural Network Training**: The NEAT algorithm evolves the neural networks over generations to improve their performance.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

- [NEAT-Python](https://github.com/CodeReclaimers/neat-python): NEAT implementation in Python.
- [Pygame](https://www.pygame.org/): Library for creating games in Python.
