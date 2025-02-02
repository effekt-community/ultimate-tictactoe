# Ultimate Tic-Tac-Toe Game

An advanced version of the classic Tic-Tac-Toe game with a twist. The game consists of a 3x3 grid of Tic-Tac-Toe boards, where each move determines the board on which the opponent must play next.

## Must-have

- [x] A 3x3 grid of Tic-Tac-Toe boards.
- [x] Standard Tic-Tac-Toe rules apply to each individual board.
- [x] A move in one of the small boards determines the next board to play in.
- [x] Win conditions for both individual boards and the overall game.
- [x] A user-friendly terminal graphical interface.
- [x] Basic game Logic for a single-player mode.

## Can-have

- [x] Computer opponent logic with different difficulty levels.
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

- Terminal output library for rendering the game interface.
- Current status: Researching suitable libraries and evaluating their integration complexity.
- Official List library
- Official String library.
- Official Console library.

## Running The Project

To run the project, you need to have Effekt installed on your machine. You can find instructions on how to install Effekt [here](https://effekt-lang.org/docs)

After installing Effekt, you can run the project by executing the following command in the project's root directory:

```bash
effekt src/main.effekt --backend js --includes .
```

## Resources

- [Ultimate Tic-Tac-Toe reference](https://www.youtube.com/watch?v=dQw4w9WgXcQ)