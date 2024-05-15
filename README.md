# Guessing Game Using Sockets

## Description
This Guessing Game uses socket programming to enable multiple clients to connect to a server and play simultaneously. Players guess a random number based on chosen difficulty levels: easy (1-50), medium (1-100), or hard (1-500). The server tracks the number of tries, calculates scores, and maintains a persistent leaderboard stored in a JSON file. Players can replay the game without disconnecting, and the server administrator can clear the leaderboard.

## Features
- Multiplayer support with multiple clients connecting to the server
- Difficulty levels: easy, medium, hard
- Persistent leaderboard stored in `scores.json`
- Admin console to clear the leaderboard
- Replay without disconnecting

## Installation

### Prerequisites
- Python 3.x
- Git (optional, for cloning the repository)

### Steps

1. **Clone the Repository (optional)**
    ```sh
    git clone https://github.com/yourusername/guessing-game.git
    cd guessing-game
    ```

2. **Create a Virtual Environment**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies**
    No external dependencies are required for this project. The code uses Python's standard library modules.

4. **Run the Server**
    ```sh
    python server.py
    ```

5. **Run the Client**
    ```sh
    python client.py
    ```

### Files

- `server.py`: Contains the server code which manages game sessions, tracks scores, and handles multiple clients.
- `client.py`: Contains the client code which connects to the server and allows users to play the game.
- `scores.json`: JSON file where leaderboard data is stored. This file is created automatically when the server runs if it does not already exist.

## Usage

1. **Start the Server**
    ```sh
    python server.py
    ```

2. **Connect Clients**
    - Run `client.py` in separate terminal windows to connect multiple clients to the server.

3. **Play the Game**
    - Follow the prompts in the client terminal to enter your name, select difficulty, and start guessing.

4. **Admin Commands**
    - In the server terminal, type `clear` and press Enter to clear the leaderboard.

## Clearing the Leaderboard

To clear the leaderboard, type `clear` in the server console and press Enter. This will reset the leaderboard and save the empty state to `scores.json`.
