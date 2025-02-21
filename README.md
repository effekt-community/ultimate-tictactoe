# Ultimate Tic-Tac-Toe Game

An advanced version of the classic Tic-Tac-Toe game with a twist. The game consists of a 3x3 grid of Tic-Tac-Toe boards, where each move determines the board on which the opponent must play next. This implementation features an advanced AI opponent and a polished terminal interface.

## Must-have

- [x] A 3x3 grid of Tic-Tac-Toe boards.
- [x] Standard Tic-Tac-Toe rules apply to each individual board.
- [x] A move in one of the small boards determines the next board to play in.
- [x] Win conditions for both individual boards and the overall game.
- [x] A user-friendly terminal graphical interface.
- [x] Basic game Logic for a single-player mode.

## Can-have

- [x] Computer opponent logic with different difficulty levels:
  - Easy: Basic strategy
  - Medium: 3-move lookahead
  - Hard: 5-move lookahead with advanced evaluation
- [ ] Customizable themes and board designs.
- [ ] Replay functionality to review past games.

## Will-not-have

- Integration with social media platforms.
- In-game hints and move suggestions.
- Complex animations or 3D graphics.

## Effects and handlers

- Event handlers for user interactions (e.g., making a move, restarting the game).
- Effects for updating the UI based on game state changes.

## FFI and libraries

- Terminal output library for rendering the game interface with ANSI colors
- Current implementation uses:
  - Official List library for board representation
  - Official String library for text processing
  - Official Console library for user input
  - TTY library for terminal manipulation

## Project Structure

```
src/
├── main.effekt    # Entry point and game initialization
├── game.effekt    # Core game logic and flow control
├── lib.effekt     # Common utilities, types, and effects
├── opponent.effekt # AI implementation with minimax algorithm
├── render.effekt  # Terminal UI rendering
├── generate.effekt # Board generation and management
└── test.effekt    # Comprehensive test suite
```

## Running The Project

To run the project, you need to have Effekt installed on your machine. You can find instructions on how to install Effekt [here](https://effekt-lang.org/docs)

### For Development
```bash
effekt src/main.effekt --backend js --includes .
```

### Running Tests
```bash
effekt src/test.effekt --backend js --includes .
```

## Game Controls

- Numbers 1-9: Select board/cell position
- 'h': Display help and game rules
- 'b': Show board position guide
- 'q': Quit game

## Features

### AI Implementation
- Minimax algorithm with alpha-beta pruning
- Position evaluation heuristics
- Three difficulty levels
- Strategic decision making prioritizing:
  1. Winning moves
  2. Blocking opponent wins
  3. Strategic side moves

### User Interface
- Color-coded game elements
- Clear game state visualization
- Interactive help system
- Board position guide
- Game mode selection menu

## Resources

- [Ultimate Tic-Tac-Toe reference](https://en.wikipedia.org/wiki/Ultimate-tic-tac-toe)
- [Effekt Documentation](https://effekt-lang.org/docs)
- [Project Repository](https://github.com/dzianis-sudkou/effekt_ultimate_tictac)