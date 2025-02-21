# Ultimate Tic-Tac-Toe Architecture

## Project Overview

This project implements Ultimate Tic-Tac-Toe in the Effekt programming language. The game is a complex variant of traditional Tic-Tac-Toe played on a 3x3 grid of smaller Tic-Tac-Toe boards, featuring both local multiplayer and AI opponent modes.

## Core Components

### 1. Game Core (`src/lib.effekt`)
- Defines fundamental data types and structures
- Core type definitions:
  - `Cell`: Board cell states (Empty, Active, Nought, Cross, Draw)
  - `GameMode`: Game mode types (Local, Computer)
  - `GameBoard`: Composite type containing BigBoard and SmallCopy
  - `SmallBoard`: Single 3x3 board representation
  - `BigBoard`: Collection of nine SmallBoards
  - `Finish`: Game state tracking (isFinished, state, player)
- Effect definitions:
  - `WrongInput`
  - `ExitGame`
  - `PrintHelp`
- Utility functions and constants

### 2. Game Logic (`src/game.effekt`)
- Implements main game loop and control flow
- Key functionalities:
  - Game mode selection (Local/Computer)
  - Difficulty level selection (Easy/Medium/Hard)
  - Player side selection (X/O)
  - Turn management
  - Input validation
  - Game state transitions
  - Win condition verification
  - User interaction handling

### 3. Board Generation (`src/generate.effekt`)
- Manages board state creation and modifications
- Core functionalities:
  - Initial board generation
  - Board state updates
  - Cell activation/deactivation
  - Win condition checking
  - Board state validation
  - Victory pattern detection

### 4. AI Opponent System (`src/opponent.effekt`)
- Implements computer player logic
- Features:
  - Multiple difficulty levels
  - Minimax algorithm implementation
  - Position evaluation
  - Strategic move selection
  - Win/block detection
- Optimization strategies:
  - Position scoring
  - Depth-limited search
  - Move prioritization

### 5. Rendering System (`src/render.effekt`)
- Handles all visual output
- Components:
  - Board visualization
  - Game state display
  - Welcome screen
  - Exit screen
  - Rules display
  - Color-coded UI elements
  - Console-based interface

### 6. Entry Point (`src/main.effekt`)
- Application entry point
- Game initialization

## Data Flow

1. Game initialization from `main.effekt`
2. Game mode and settings selection
3. Main game loop (`game.effekt`):
   - Input processing
   - State validation
   - Board updates
   - AI moves (if applicable)
   - Visual feedback
4. State management through `generate.effekt`
5. AI processing via `opponent.effekt`
6. Visual output through `render.effekt`

## Effect System Usage

### Core Effects
- `WrongInput`: Input validation errors
- `ExitGame`: Game termination
- `PrintHelp`: Help system access
- `OutOfBounds`: Array bounds checking

### Effect Handlers
- Input validation
- Error recovery
- Game state management
- Visual feedback

## Testing

Comprehensive test suite (`src/test.effekt`) covering:
- Cell representation
- Board initialization
- State management
- Move validation
- Win detection
- AI logic
- Difficulty levels
- Edge cases

## Technical Requirements

- Effekt programming language
- Console-based interface
- ANSI color support
- Standard input/output handling

## Future Enhancements

1. Enhanced AI strategies
2. Network multiplayer
3. Game state persistence
4. Statistics tracking
5. Advanced difficulty levels
6. Replay system
7. Tutorial mode
8. Configuration options

## Development Guidelines

1. Type safety first
2. Effect system for error handling
3. Pure functions where possible
4. Clear separation of concerns
5. Comprehensive testing
6. Modular design
7. Documentation maintenance