# Ultimate Tic-Tac-Toe Architecture

## Project Overview

This project implements Ultimate Tic-Tac-Toe in the Effekt programming language. The game is a complex variant of traditional Tic-Tac-Toe played on a 3x3 grid of smaller Tic-Tac-Toe boards.

## Core Components

### 1. Game Core (`src/lib.effekt`)
- Defines fundamental data types and structures
- Contains core type definitions:
  - `Cell`: Represents board cell states (Empty, Active, Nought, Cross, etc.)
  - `GameBoard`: Main game state container
  - `SmallBoard`: Individual 3x3 board
  - `BigBoard`: Collection of nine SmallBoards
- Implements utility functions and shared constants

### 2. Game Logic (`src/Game.effekt`)
- Contains the main game loop and control flow
- Handles:
  - Game mode selection (Local/Computer)
  - Player turn management
  - Game state transitions
  - User input processing
  - Win condition verification

### 3. Board Generation (`src/Generate.effekt`)
- Manages board state creation and modifications
- Key functionalities:
  - Initial board generation
  - Board state updates
  - Win condition checking
  - Computer move generation
  - Cell availability verification

### 4. Rendering System (`src/Render.effekt`)
- Handles all visual output
- Features:
  - Board visualization
  - Game state display
  - Welcome and exit screens
  - Rules display
  - Console-based UI components

### 5. Entry Point (`src/main.effekt`)
- Application entry point
- Initializes game components

## Data Flow

1. Game initialization starts from `main.effekt`
2. `Game.effekt` controls the game loop:
   - Player input → State validation → Board update → Render update
3. `Generate.effekt` handles state transformations
4. `Render.effekt` provides visual feedback
5. `lib.effekt` provides shared utilities and type definitions

## Key Design Patterns

### Effect System
- Uses Effekt's effect system for error handling
- Defined effects:
  - `WrongInput`
  - `ExitGame`
  - `PrintRules`

### State Management
- Immutable data structures
- Pure functions for state transformations
- Clear separation of rendering and game logic

### Board Representation
- Nested list structure for the game board
- Efficient state tracking with SmallBoard copies
- Type-safe cell state representation

## Testing

Test suite (`src/test.effekt`) includes comprehensive tests for:
- Board generation
- Game mechanics
- Win condition verification
- Computer player logic
- Cell availability checking

## Future Improvements

1. Network multiplayer support
2. Advanced AI strategies
3. Save/Load game state
4. Graphical user interface
5. Game statistics tracking

## Technical Requirements

- Effekt programming language
- Console-based display
- Standard input/output handling