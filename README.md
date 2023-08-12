# Welcome to Atari Games
***

## Task
The objective of this project is to create a Machine Learning (ML) model employing Reinforcement Learning (RL) to achieve flawless performance in three Atari Games:
Cartpole Game
SpaceInvaders
and Pacman

## Description
To address this challenge, I utilized the following packages/modules:

1. stablebaselines3: This package was employed for policy definition, policy evaluation, and other advanced functions essential for the Reinforcement Learning model.
2. gymnasium: Used to access the game environment and other relevant functionalities.
3. PIL or pillow: Utilized for image processing tasks.
4. os module: Facilitated file handling operations.
5. numpy: Employed for numerical computations.
6. warnings: Used to manage and filter warnings during the execution of the program.

## Installation
To utilize this project in your environment, there is no need for any specific installations.
However, it is crucial to ensure that all the dependencies (such as stablebaselines3, gymnasium, etc.) are installed and properly imported into your local, virtual, or cloud machines.

## Usage
1. I have implemented the model using a class named `DQNAgent`. To initialize the environment, you can use the following code: `CartPole_agent = DQNAgent(name='CartPole', env_name='CartPole-v1')`. Please note that the keyword parameters `name` and `env_name` are specific to Cartpole, SpaceInvaders, Pacman, or other similar games. For more information, you can visit the official website of gymnasium at `https://gymnasium.farama.org/environments/atari/`.

2. To perform a random test of the game and ensure it is working correctly, use the following line of code: `CartPole.play_episodes(num_episodes=10)`. You can choose any value for `num_episodes`, but it's advisable to test with a number between 10 and 20, especially for complex games like `SpaceInvaders`.

3. To start training the model, use the following code: `CartPole.train(time_steps=100000, stop_value=1000)`. The `time_steps` parameter defines the number of iterations the model will take to learn how to play the game. It can be set to any non-negative value. Keep in mind that larger values for `time_steps` will increase the execution time.

   The `stop_value` parameter is used for `early stopping`. It halts the learning process when the desired point is achieved. If the value is reached before the specified `stop_value`, the learning will continue for the duration of the specified time.

4. Once the model has learned, you can evaluate its performance using the following line of code: `CartPole.evaluate_policy(episodes=10)`. The `episodes` parameter determines the number of episodes over which to evaluate the learned policy.

5. To predict how the agent will behave, you can use the following code: `CartPole.play_episodes(num_episodes=10, play_type="predict")`. This line of code is similar to the one in point 2, but it includes a second parameter called `play_type`. By observing the rewards printed to the standard output, you can determine if the agent is making the right decisions. This code also generates a video of the agent's gameplay, and the length of the video is determined by the number of episodes specified.

6. To save the trained model, use this line of code: `CartPole.save_model(path/to/save)`

7. To load a saved model, use this line of code: `CartPole.load_model(path/to/saved/model)`

8. To close the environment, use the following line of code: `CartPole.close_env()`.

### The Core Team
Samuel Adamu Joshua