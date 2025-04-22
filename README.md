# Hex RL Bot: MATH499 Extra Credit Project

## What's All This Then?
I built this bot to compete in our MATH499 Game Theory class competition where we're all creating bots to play Hex against each other. The top 3 performers get extra credit. Rather than writing a traditional rule-based bot, I decided to use reinforcement learning to teach my bot how to play since I didn't really want to read through a bunch of articles and journals about the various strategies involved. Also YouTube as shown me a lot of cool reinforcement learning visualization videos so I was interested in this anyway.

## Stuff Inside

### hex_env.ipynb
Just a testing environment to make sure everything works before porting to Collab. It's built on the OpenAI Gym framework and handles all the basic stuff like:
- Tracking the game board
- Checking if moves are legal
- Figuring out when somebody wins (using a depth-first search)

### Hex_RL_Bot.ipynb
The main notebook where all the reinforcement learning stuff happens:
- Uses a neural network to learn strategies
- Implements the PPO (Proximal Policy Optimization) algorithm
- Has a way to play against the bot to test it (you can change which model to use, dimension of board, etc...)
- You can manually train for different dimensions and different amounts of steps

### selfplay_hex_6x6/hex_bot_300000.zip
Just a pre-trained model that's gone through 300,000 training steps, so it's actually quite dumb (it SHOULD start playing better around 500k to 1M). 

## How Hex Works
It's a simple but high-ceiling strategy game where:
- Players take turns placing pieces on a hexagonal board
- One player tries to connect top-to-bottom
- The other tries to connect left-to-right
- First player to make a complete path wins
- There are no draws in Hex!
- Note that the board being made of hexes is important as a 2D matrix with straights won't capture all winning states

Curious to see how RL approach stacks up against the other strategies from class. I feel like it's gonna crash and burn but only one way to find out.
