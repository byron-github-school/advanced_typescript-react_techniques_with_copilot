# Advanced TypeScript & React Workshop

In this workshop, we will explore advanced TypeScript and React concepts using GitHub
Copilot. We will build a memory card game that will help us understand how to use
Copilot to generate code, write tests, and add documentation.

## Introduction

We will be using Copilot to help us extend our skeleton memory game project by adding new features such as basic game logic, score tracking and some cosmetic improvements.

Along the way, we will learn how to write an application using TypeScript and React.

<!-- include (../how_to_use_guide.md) -->

## How to Use This Guide

Each module builds on the previous one, so it is important to complete them in order.

<details>
<summary><strong>Show More</strong></summary>
<blockquote>

Each module contains a series of prompts that you can use to interact with Copilot. The
prompts are meant to guide you through the workshop and help you understand how Copilot
can assist you in building a REST API backend.

Please take a moment to familiarize yourself with the different conventions used in this
guide.

### Prompts

```markdown
This is a prompt
```

Prompts are meant to be typed into the Copilot prompt bar. They are used to guide Copilot
to generate code or provide information.

```markdown
This is a prompt with a #file:filename.py directive
```

The prompts with a **#** directive need to be typed directly into the Copilot prompt bar.
For all other prompts, you can copy and paste them into the prompt bar.

### Hints

> [!TIP]
>
> This is a hint or a tip

Throughout the guide, you will find hints and tips to provide more insights into getting
the most out of Copilot. Feel free to experiment with the hints and tips to see how they
can help you.

### Expected Output

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

Code suggestions or sample outputs from Copilot can be viewed here for reference\. You can
expand and collapse the content as needed by clicking the _View Response_ header\.

</blockquote>
</details>

Copilot will generate code based on the prompts you provide. Since there are many ways to
solving a coding challenge the suggested code may vary slightly based on the context
provided by the prompt, your previous interactions with Copilot, and the comments in the
codebase.

To help you along, we have provided some possible outputs for some of the prompts. This
will give you an idea of what to expect when you run the prompt. We encourage you to
experiment with the prompts and see how Copilot can help you.

### Checkpoints

Throughout the workshop, you will find checkpoints that summarize the code you have
generated so far. These checkpoints are meant to help you keep track of your progress and
ensure that you have completed the tasks correctly.

If your experimentations with Copilot lead you to a different solution, feel free to use
the code in the checkpoints as a reference to ensure you are on the right track.

### Skeleton Project

We've provided you with a skeleton project to help you get up and running.

Each file in the skeleton project contains comments which will guide you through the

</blockquote>
</details>
<!-- /include -->

Modules:
- module 1: Getting Started
  - Exploring TypeScript
    - Learning a new language
  - Creating a new React app
    - Setting up a new project
- module 2: Defining project requirements
  - using an instruction file
  - switching sessions
- module 3: Understanding the codebase
  - using /explain and @workspace
- module 4: Working with data
  - asking the user for input
  - data structures
- module 5: Game logic
  - card match logic
  - scoring logic
  - tracking number of moves
- module 6: Events
  - adding a game timer
  - updating the leaderboard
- module 7: Styles and animations
- module 8: Testing
  - writing tests
  - test coverage
- module 9: Writing documentation

## Module 1: Getting Started

### Exploring TypeScript

Copilot is great at helping us tackle new languages and frameworks. Let's start simple:

```markdown
help me learn TypeScript
```

```markdown
compare it to JavaScript
```

> [!TIP]
>
> We can tell copilot to include as much or as little context when generating code. For example, you can ask Copilot to always provide an explanation of the code it generates or compare it with a language you are familiar with.

### Creating a new React app

Using the `@workspace /new` command is a great way to get started with a new project. We can tell copilot to include as much or as little code as we need.

Let's start by creating a new React app:

```markdown
@workspace /new react app
```

Feel free to click on each file and see it's content. Pay particular attention to the `App.tsx` file which contains the main component of the application.

> [!TIP]
>
> Until you click the `Save Workspace...` button, Copilot will not save the changes you make to the workspace. This is useful when you want to experiment with different code snippets without affecting the original codebase.

Now let's try something a bit more interesting.

```markdown
@workspace /new react app. include a Start button which displays a start screen and a Close button which takes us back to the Start button.
```

Notice the additional files suggested by Copilot?

Take a look at `App.tsx` and the new files in the `components` directory.

Providing context and instructions to Copilot helps it generate more accurate code. The more context you provide, the better the suggestions will be.

> [!TIP]
>
> Did you know you can use the `#file` directive to tell Copilot to look at a specific file such as a project requirements or a README file while using the `/new` command?

Try experimenting with the `/new` command:

```markdown
@workspace /new react app for a beginner to learn React
```

```markdown
@workspace /new react app to showcase some advanced React features. include comments in the code to explain the React concepts used.
```

## Module 2: Defining project requirements

Providing clear instructions to Copilot is important when generating code. This can be in the form of comments in the codebase, a project requirements file, or a README file.

Let's start by creating a project requirements file.

Create a markdown file called `copilot-instructions.md` inside the `.github` directory; for the moment, you can leave it empty.

```markdown
how do I use variables in TypeScript
```

Note the variable name format suggested by Copilot.

Add the following text to the `copilot-instructions.md` file:

```markdown
## coding style
- always use the following format for variable and function names: Variable_Name, Function_Name
```

Now let's try the same prompt again:

```markdown
how do I use variables in TypeScript
```

Notice anything different? Copilot is now suggesting variable names in the format specified in the instructions file. We can use this to define coding standards and best practices for our project in addition to providing context for Copilot.

Let's add something a bit more useful in our instructions file. Replace the contents of `copilot-instructions.md` with the following:

```markdown
## coding standard
- always use camelCase for variable and function names
- always include comments for functions to explain their purpose and usage
```

Save the file.

> [!TIP]
>
> Instructions in the `copilot-instructions.md` file will be used by Copilot whenever we ask a question. Consider including coding standards, or basic high level project requirements in this file.

While working with Copilot, we can also use sessions to switch between different contexts. This is useful when working on multiple tasks or projects.

Use the `+` button in the Copilot prompt bar to create a new session. You can switch between sessions using the session dropdown.

Let's create a new session and switch to it.

Ask Copilot a question.

Now switch back to the previous session. Notice how your previous interactions with Copilot are saved in each session.

> [!TIP]
>
> Sessions are a great way to start a new conversation with Copilot without losing the context of your previous interactions.

## Module 3: Understanding the codebase

Understanding the codebase is important when working on a project. Copilot can help us understand the structure of the codebase, the purpose of each file, and how the files are related to each other. This is useful when you are working on a new project or joining an existing team.

Let's start by asking Copilot to explain the codebase to us.

Open the `App.tsx` file and use the following prompt:

```markdown
/explain the codebase
```

If we need more information we can ask Copilot to explain the codebase in more detail:

```markdown
explain the codebase in more detail
```

Slash commands are a great way to interact with Copilot. You can use the `/help` command to see a list of all the available commands for your particular IDE.

Let's try this again:

```markdown
/explain the codebase
```

Sometimes we may not know where to start when looking at a new codebase. Copilot can help us generate a file tree specific to our project.

```markdown
@workspace Show me the ascii file tree with explanations for each major component
```

> [!TIP]
>
> We can use the `@workspace` command to tell Copilot to look at the entire workspace instead of just the currently open file or selected code. This is a great way to get an overview of the entire project.

Copilot uses comments, README files, variable names and instructions we provide in the `copilot-instructions.md` file to understand the codebase. The more context we provide, the better the suggestions will be.

The sample project alredy has some comments to help you get started but let's provide Copilot with more context.

Open the `copilot-instructions.md` file and add the following to the previous text we added earlier:

```markdown
## project defintion
- this is a memory card game project
- the project is written in TypeScript and React
- the goal of the player is to match pairs of cards
```

Save the file. We will be adding more defintion and game rules to this file as we progress through the workshop.

Try asking Copilot to explain the codebase again using the new context provided in the instructions file.

```markdown
@workspace what is the purpose of this project
```

Even with the limited context provided, Copilot is able to generate recommnedations on how enhace the codebase.

```markdown
@workspace suggest some way we can enhance the codebase
```

Not sure how to install or run your project? Ask Copilot for help.

```markdown
@workspace how do I install and run this project
```

In the following moduiles we will be adding more functionality to the project. Copilot will help us generate code based on the context provided by comments and variable names.

## Module 4: Working with data

### Asking the user for input

We need to add logic to ask for the player's name and store it in our application to refer to it later.

We can approach this in different ways. Let's start by asking Copilot for suggestions.

Close all the files in the IDE and enter the following prompt:

```markdown
how can I ask the user for their name
```

Copilot will reply with a general approach. From our previous discovery of the codebase, we know that the `App.tsx` file contains the main component of the application. Let's use this file to generate the code.

Open the `App.tsx` file and use the following prompt:

```markdown
how can I ask the user for their name
```

Notice how Copilot generates code based on the existing logic in the file.

But we can do better.

```markdown
@workspace how can I ask the user for their name
```

By using the `@workspace` command, Copilot will look at the entire workspace instead of just the currently open file or selected code. Notice the additional suggestions regarding the `SplashScreen` file.

> [!TIP]
>
> You can use the up arrow to recall previous prompts you've run. This is useful when you want to re-run a prompt or make changes to a previous prompt such as adding `@workspace`.

Open each of the suggested files and use the apply button to add the code to the file.

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

`SplashScreen.tsx`:

```tsx
import { useState } from 'react';

function SplashScreen({ onStartGame, setUserName }) {
  const [name, setName] = useState('');

  const handleStartGame = () => {
    setUserName(name);
    onStartGame();
  };

  return (
    <div>
      <h1>Welcome to the Game!</h1>
      <input
        type="text"
        placeholder="Enter your name"
        value={name}
        onChange={(e) => setName(e.target.value)}
      />
      <button onClick={handleStartGame}>Start Game</button>
    </div>
  );
}

export default SplashScreen;
```

`App.tsx`:

```tsx
import { useState } from 'react';
import SplashScreen from './components/SplashScreen';
import GameScreen from './components/GameScreen';
import EndScreen from './components/EndScreen';

function App() {
  const [gameState, setGameState] = useState('splash');
  // @ts-ignore
  const [userName, setUserName] = useState(''); // state to manage the user's name

  const startGame = () => {
    setGameState('play');
  };

  const endGame = () => {
    setGameState('end');
  };

  const restartGame = () => {
    setGameState('splash');
  };

  return (
    <div className="App">
      {gameState === 'splash' && (
        <SplashScreen onStartGame={startGame} setUserName={setUserName} />
      )}
      {gameState === 'play' && <GameScreen x={4} y={4} onEndGame={endGame} userName={userName} />}
      {gameState === 'end' && <EndScreen onRestartGame={restartGame} />}
    </div>
  );
}

export default App;
```

</blockquote>
</details>

Since we are capturing the player's name, let's display it on the game screen.

With the `app.tsx` file open, use the following prompt:

```markdown
how can I display the player's name on the game screen
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

`GameScreen.tsx`:

```tsx
import React from 'react';

interface GameScreenProps {
  x: number;
  y: number;
  onEndGame: () => void;
  userName: string; // add userName prop
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  return (
    <div>
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      {/* Game logic and UI here */}
      <button onClick={onEndGame}>End Game</button>
    </div>
  );
};

export default GameScreen;
```

`App.tsx`:

```tsx
import { useState } from 'react';
import SplashScreen from './components/SplashScreen';
import GameScreen from './components/GameScreen'; // import the GameScreen component
import EndScreen from './components/EndScreen'; // import the EndScreen component

function App() {
  const [gameState, setGameState] = useState('splash'); // state to manage the game state
  // @ts-ignore
  const [userName, setUserName] = useState(''); // state to manage the user's name

  const startGame = () => {
    setGameState('play'); // set gameState to 'play' when game starts
  };

  const endGame = () => {
    setGameState('end'); // set gameState to 'end' when game ends
  };

  const restartGame = () => {
    setGameState('splash'); // set gameState to 'splash' when game restarts
  };

  return (
    <div className="App">
      {gameState === 'splash' && (
        <SplashScreen onStartGame={startGame} setUserName={setUserName} />
      )}
      {gameState === 'play' && <GameScreen x={4} y={4} onEndGame={endGame} userName={userName} />}
      {gameState === 'end' && <EndScreen onRestartGame={restartGame} />}
    </div>
  );
}

export default App;
```

</blockquote>
</details>

Try out the new app and enter your name then click the `Start Game` button.

Does the game screen display your name?

If the game screen doesn't quite look right, ask Copilot for suggestions on how to improve it.


```markdown
@workspace how can I improve the look of the gamescreen
```

Apply the suggestions to the files.

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

`GameScreen.tsx`:

```tsx
import React from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

interface GameScreenProps {
  x: number;
  y: number;
  onEndGame: () => void;
  userName: string;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const cards = Array.from({ length: x * y }, (_, i) => i + 1);

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      {cards.map((card) => (
        <Card key={card} cardNumber={card} />
      ))}
      <button onClick={onEndGame}>End Game</button>
    </div>
  );
};

export default GameScreen;
```

`GameScreen.css`:

```css
.gamescreen {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  gap: 10px;
  padding: 20px;
  background-color: #f0f0f0;
  border-radius: 10px;
}

.gamescreen h1 {
  grid-column: span 4;
  text-align: center;
  color: #333;
}

.gamescreen p {
  grid-column: span 4;
  text-align: center;
  font-size: 1.2em;
  color: #555;
}

.gamescreen button {
  grid-column: span 4;
  padding: 10px 20px;
  font-size: 1em;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.gamescreen button:hover {
  background-color: #0056b3;
}
```

</blockquote>
</details>

For development purposes, let's reduce the number of playing cards to just 4.

With `App.tsx` open, use the following prompt:

```markdown
how can I reduce the number of playing cards to 4
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
return (
  <div className="App">
    {gameState === 'splash' && (
      <SplashScreen onStartGame={startGame} setUserName={setUserName} />
    )}
    {gameState === 'play' && <GameScreen x={2} y={2} onEndGame={endGame} userName={userName} />}
    {gameState === 'end' && <EndScreen onRestartGame={restartGame} />}
  </div>
);
```

</blockquote>
</details>

As a bonus, see if you can use Copilot to ask the user for the number of playing cards. Don't forget that we need even number of cards to play the game.

### Data structures

Copilot is great at generating code for data structures. It's also really good at helping us create sample or test data.

We will be adding a leaderboard to our game. To get us started, open the sample `leaderboard.yml` file in the `public` directory.

Let's add a couple of additional entries to the leaderboard.

```markdown
add two more players named Diane and John to the leaderboard
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```yaml
leaderboard:
  - playerName: Alice
    numberOfMoves: 30
    numberOfCards: 16
  - playerName: Bob
    numberOfMoves: 35
    numberOfCards: 16
  - playerName: Charlie
    numberOfMoves: 25
    numberOfCards: 16
  - playerName: Diane
    numberOfMoves: 28
    numberOfCards: 16
  - playerName: John
    numberOfMoves: 32
    numberOfCards: 16
```

</blockquote>
</details>

Try adding a new player info manually. Enter a new line in the `leaderboard.yml` file and start tying the info for the new player. Notice how Copilot will recognize the structure and suggest the next line. This is a quick way to add random data to a file.

For a complete leaderboard, we also need o track the score for each user. Let's add a score field to the leaderboard.

```markdown
add a total score field to the leaderboard with a range of 6000-1000
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```yaml
leaderboard:
  - playerName: Alice
    numberOfMoves: 30
    numberOfCards: 16
    totalScore: 5000
  - playerName: Bob
    numberOfMoves: 35
    numberOfCards: 16
    totalScore: 4500
  - playerName: Charlie
    numberOfMoves: 25
    numberOfCards: 16
    totalScore: 5500
  - playerName: Diane
    numberOfMoves: 28
    numberOfCards: 16
    totalScore: 4800
  - playerName: John
    numberOfMoves: 32
    numberOfCards: 16
    totalScore: 4700
```

</blockquote>
</details>

Since TypeScript/JavaScript has built-in support for JSON, let's convert the leaderboard data to JSON format.

```markdown
convert the leaderboard data to JSON format
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```json
{
  "leaderboard": [
    {
      "playerName": "Alice",
      "numberOfMoves": 30,
      "numberOfCards": 16,
      "totalScore": 5000
    },
    {
      "playerName": "Bob",
      "numberOfMoves": 35,
      "numberOfCards": 16,
      "totalScore": 4500
    },
    {
      "playerName": "Charlie",
      "numberOfMoves": 25,
      "numberOfCards": 16,
      "totalScore": 5500
    },
    {
      "playerName": "Diane",
      "numberOfMoves": 28,
      "numberOfCards": 16,
      "totalScore": 4800
    },
    {
      "playerName": "John",
      "numberOfMoves": 32,
      "numberOfCards": 16,
      "totalScore": 4700
    }
  ]
}
```

</blockquote>
</details>

Save the JSON in a new file called `leaderboard.json` in the `public` directory.

> [!TIP]
>
> We can use Copilot to quickly generate random data or to adjust data structures by adding or removing fields.

Now let's display the leaderboard on the end game screen.

Open the `App.tsx` file and use the following prompt:

```markdown
@workspace load and display the leaderboard data stored in #file:leaderboard.json
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

`App.tsx`:

```tsx
import { useState, useEffect } from 'react';
import SplashScreen from './components/SplashScreen';
import GameScreen from './components/GameScreen';
import EndScreen from './components/EndScreen';

function App() {
  const [gameState, setGameState] = useState('splash');
  const [userName, setUserName] = useState('');
  const [leaderboard, setLeaderboard] = useState([]);

  useEffect(() => {
    fetch('/leaderboard.json')
      .then(response => response.json())
      .then(data => setLeaderboard(data.leaderboard))
      .catch(error => console.error('Error fetching leaderboard data:', error));
  }, []);

  const startGame = () => {
    setGameState('play');
  };

  const endGame = () => {
    setGameState('end');
  };

  const restartGame = () => {
    setGameState('splash');
  };

  return (
    <div className="App">
      {gameState === 'splash' && (
        <SplashScreen onStartGame={startGame} setUserName={setUserName} />
      )}
      {gameState === 'play' && <GameScreen x={4} y={4} onEndGame={endGame} userName={userName} />}
      {gameState === 'end' && <EndScreen onRestartGame={restartGame} leaderboard={leaderboard} />}
    </div>
  );
}

export default App;
```

`EndScreen.tsx`:

```tsx
import React from 'react';

const EndScreen = ({ onRestartGame, leaderboard }) => {
  return (
    <div>
      <h1>Game Over</h1>
      <button onClick={onRestartGame}>Restart Game</button>
      <h2>Leaderboard</h2>
      <ul>
        {leaderboard.map((player, index) => (
          <li key={index}>
            {player.playerName}: {player.totalScore} points, {player.numberOfMoves} moves, {player.numberOfCards} cards
          </li>
        ))}
      </ul>
    </div>
  );
};

export default EndScreen;
```

</blockquote>
</details>

Refresh the game and click the `End Game` button to see the leaderboard.

> [!TIP]
>
> Placing files in the `public` directory makes them accessible to the client-side code. This is useful when you need to load data from a file or serve static assets.

## Module 5: Game logic

Let's add some basic game logic to our memory card game.

### Card match logic

Open the `copilot-instructions.md` file and add the following text to the end of the file:

```markdown
## rules of the game
- the game can only contain an even number of cards
- each pair of cards must have the same value
- only one pair of cards can have the same value
```

Save the file.

Open the `GameScreen.tsx` file and use the following prompt:

```markdown
@workspace update the card logic
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React, { useState } from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

interface GameScreenProps {
  // keep track of the number of cards in the x and y grid
  x: number;
  y: number;
  onEndGame: () => void; // Prop function to end the game
  userName: string; // add userName prop
}

interface CardState {
  id: number;
  value: number;
  isFlipped: boolean;
  isMatched: boolean;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const [cards, setCards] = useState<CardState[]>(() => {
    const totalCards = x * y;
    const cardValues = Array.from({ length: totalCards / 2 }, (_, i) => i + 1);
    const allCardValues = [...cardValues, ...cardValues].sort(() => Math.random() - 0.5);
    return allCardValues.map((value, index) => ({
      id: index,
      value,
      isFlipped: false,
      isMatched: false,
    }));
  });

  const [flippedCards, setFlippedCards] = useState<number[]>([]);

  const handleCardClick = (id: number) => {
    setCards((prevCards) =>
      prevCards.map((card) =>
        card.id === id ? { ...card, isFlipped: !card.isFlipped } : card
      )
    );

    setFlippedCards((prevFlipped) => {
      const newFlipped = [...prevFlipped, id];
      if (newFlipped.length === 2) {
        const [firstCard, secondCard] = newFlipped.map((cardId) =>
          cards.find((card) => card.id === cardId)
        );
        if (firstCard && secondCard && firstCard.value === secondCard.value) {
          setCards((prevCards) =>
            prevCards.map((card) =>
              card.id === firstCard.id || card.id === secondCard.id
                ? { ...card, isMatched: true }
                : card
            )
          );
        } else {
          setTimeout(() => {
            setCards((prevCards) =>
              prevCards.map((card) =>
                card.id === firstCard?.id || card.id === secondCard?.id
                  ? { ...card, isFlipped: false }
                  : card
              )
            );
          }, 1000);
        }
        return [];
      }
      return newFlipped;
    });
  };

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      <div className="card-grid">
        {cards.map((card) => (
          <Card
            key={card.id}
            cardNumber={card.value}
            isFlipped={card.isFlipped}
            isMatched={card.isMatched}
            onClick={() => handleCardClick(card.id)}
          />
        ))}
      </div>
      <div>
        <button onClick={onEndGame}>End Game</button>
      </div>
    </div>
  );
};

export default GameScreen;
```

</blockquote>
</details>

Since we are moving the logic of the game to the `GameScreen` component, we can remove the placeholder logic from the `Card` component.

Open the `Card.tsx` file and use the following prompt:

```markdown
update the code
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React from 'react';
import '../styles/Card.css';

interface CardProps {
  cardNumber: number;
  isFlipped: boolean;
  isMatched: boolean;
  onClick: () => void;
}

/**
 * Card component represents a single card in the memory game.
 * It displays the card number if the card is flipped or matched.
 * @param {CardProps} props - The properties of the card.
 * @returns {JSX.Element} The rendered card component.
 */
const Card: React.FC<CardProps> = ({ cardNumber, isFlipped, isMatched, onClick }) => {
  return (
    <div className={`card ${isFlipped || isMatched ? 'flipped' : ''}`} onClick={onClick}>
      {isFlipped || isMatched ? `Card ${cardNumber}` : 'Card'}
    </div>
  );
};

export default Card;
```

</blockquote>
</details>

> [!TIP]
>
> Copilot remembers the context of our previous interactions. This is useful when we need to update or modify code that we have previously generated.

Refresh the game and click on the cards. Notice how we now have pairs of cards that match. Also notice how we use the setTimeout function to flip the cards back over if they don't match after a short delay.

Let's make sure we end the game. Open `copilot-instructions.md` and add the following text to the end of the game rules:

```markdown
- the game ends when all the cards are matched
```

Save the file and enter the following prompt after opening the `GameScreen.tsx` file:

```markdown
add code to end the game
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React, { useState, useEffect } from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

interface GameScreenProps {
  // keep track of the number of cards in the x and y grid
  x: number;
  y: number;
  onEndGame: () => void; // Prop function to end the game
  userName: string; // add userName prop
}

interface CardState {
  id: number;
  value: number;
  isFlipped: boolean;
  isMatched: boolean;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const [cards, setCards] = useState<CardState[]>(() => {
    const totalCards = x * y;
    const cardValues = Array.from({ length: totalCards / 2 }, (_, i) => i + 1);
    const allCardValues = [...cardValues, ...cardValues].sort(() => Math.random() - 0.5);
    return allCardValues.map((value, index) => ({
      id: index,
      value,
      isFlipped: false,
      isMatched: false,
    }));
  });

  const [flippedCards, setFlippedCards] = useState<number[]>([]);

  /**
   * Handles the card click event.
   * Flips the card and checks if two cards are flipped to determine if they match.
   * @param {number} id - The id of the clicked card.
   */
  const handleCardClick = (id: number) => {
    setCards((prevCards) =>
      prevCards.map((card) =>
        card.id === id ? { ...card, isFlipped: !card.isFlipped } : card
      )
    );

    setFlippedCards((prevFlipped) => {
      const newFlipped = [...prevFlipped, id];
      if (newFlipped.length === 2) {
        const [firstCard, secondCard] = newFlipped.map((cardId) =>
          cards.find((card) => card.id === cardId)
        );
        if (firstCard && secondCard && firstCard.value === secondCard.value) {
          setCards((prevCards) =>
            prevCards.map((card) =>
              card.id === firstCard.id || card.id === secondCard.id
                ? { ...card, isMatched: true }
                : card
            )
          );
        } else {
          setTimeout(() => {
            setCards((prevCards) =>
              prevCards.map((card) =>
                card.id === firstCard?.id || card.id === secondCard?.id
                  ? { ...card, isFlipped: false }
                  : card
              )
            );
          }, 1000);
        }
        return [];
      }
      return newFlipped;
    });
  };

  /**
   * Checks if all cards are matched and ends the game if they are.
   */
  useEffect(() => {
    if (cards.every((card) => card.isMatched)) {
      onEndGame();
    }
  }, [cards, onEndGame]);

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      <div className="card-grid">
        {cards.map((card) => (
          <Card
            key={card.id}
            cardNumber={card.value}
            isFlipped={card.isFlipped}
            isMatched={card.isMatched}
            onClick={() => handleCardClick(card.id)}
          />
        ))}
      </div>
      <div>
        <button onClick={onEndGame}>End Game</button>
      </div>
    </div>
  );
};

export default GameScreen;
```

</blockquote>
</details>

Refresh the game and try to match all the cards. The game should end when all the cards are matched.

Try to use copilot to add a slight delay before showing the end game screen.

### Scoring logic

Let's add a scoring system to our game. The score will be based on the number of moves the player makes. Fewer moves will result in a higher score.

Open the `copilot-instructions.md` file and add the following text to the end of the file:

```markdown
## scoring system
- highest score is 10000
- the player's score is calculated based on the number of moves they make
- the player's score is reduced by 100 for each move
```

Save the file and enter the following prompt after opening the `GameScreen.tsx` file:

```markdown
@workspace add scoring logic
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React, { useState, useEffect } from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

interface GameScreenProps {
  // keep track of the number of cards in the x and y grid
  x: number;
  y: number;
  onEndGame: () => void; // Prop function to end the game
  userName: string; // add userName prop
}

interface CardState {
  id: number;
  value: number;
  isFlipped: boolean;
  isMatched: boolean;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const [cards, setCards] = useState<CardState[]>(() => {
    const totalCards = x * y;
    const cardValues = Array.from({ length: totalCards / 2 }, (_, i) => i + 1);
    const allCardValues = [...cardValues, ...cardValues].sort(() => Math.random() - 0.5);
    return allCardValues.map((value, index) => ({
      id: index,
      value,
      isFlipped: false,
      isMatched: false,
    }));
  });

  const [flippedCards, setFlippedCards] = useState<number[]>([]);
  const [score, setScore] = useState<number>(10000);

  /**
   * Handles the card click event.
   * Flips the card and checks if two cards are flipped to determine if they match.
   * @param {number} id - The id of the clicked card.
   */
  const handleCardClick = (id: number) => {
    setCards((prevCards) =>
      prevCards.map((card) =>
        card.id === id ? { ...card, isFlipped: !card.isFlipped } : card
      )
    );

    setFlippedCards((prevFlipped) => {
      const newFlipped = [...prevFlipped, id];
      if (newFlipped.length === 2) {
        const [firstCard, secondCard] = newFlipped.map((cardId) =>
          cards.find((card) => card.id === cardId)
        );
        if (firstCard && secondCard && firstCard.value === secondCard.value) {
          setCards((prevCards) =>
            prevCards.map((card) =>
              card.id === firstCard.id || card.id === secondCard.id
                ? { ...card, isMatched: true }
                : card
            )
          );
        } else {
          setTimeout(() => {
            setCards((prevCards) =>
              prevCards.map((card) =>
                card.id === firstCard?.id || card.id === secondCard?.id
                  ? { ...card, isFlipped: false }
                  : card
              )
            );
          }, 1000);
        }
        setScore((prevScore) => prevScore - 100); // Reduce score by 100 for each move
        return [];
      }
      return newFlipped;
    });
  };

  /**
   * Checks if all cards are matched and ends the game if they are.
   */
  useEffect(() => {
    if (cards.every((card) => card.isMatched)) {
      onEndGame();
    }
  }, [cards, onEndGame]);

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      <p>Score: {score}</p> {/* Display the score */}
      <div className="card-grid">
        {cards.map((card) => (
          <Card
            key={card.id}
            cardNumber={card.value}
            isFlipped={card.isFlipped}
            isMatched={card.isMatched}
            onClick={() => handleCardClick(card.id)}
          />
        ))}
      </div>
      <div>
        <button onClick={onEndGame}>End Game</button>
      </div>
    </div>
  );
};

export default GameScreen;
```

</blockquote>
</details>

Save the file and refresh the game. Try to match all the cards and notice how the score decreases with each move.

### tracking the number of moves

Since we are tracking the score based on the number of moves, let's also track the number of moves the player makes. This will also be part of the leaderboard data.

Open `GameScreen.tsx` and use the following prompt:

```markdown
@workspace add logic to track the number of moves
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React, { useState, useEffect } from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

interface GameScreenProps {
  // keep track of the number of cards in the x and y grid
  x: number;
  y: number;
  onEndGame: () => void; // Prop function to end the game
  userName: string; // add userName prop
}

interface CardState {
  id: number;
  value: number;
  isFlipped: boolean;
  isMatched: boolean;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const [cards, setCards] = useState<CardState[]>(() => {
    const totalCards = x * y;
    const cardValues = Array.from({ length: totalCards / 2 }, (_, i) => i + 1);
    const allCardValues = [...cardValues, ...cardValues].sort(() => Math.random() - 0.5);
    return allCardValues.map((value, index) => ({
      id: index,
      value,
      isFlipped: false,
      isMatched: false,
    }));
  });

  const [flippedCards, setFlippedCards] = useState<number[]>([]);
  const [score, setScore] = useState<number>(10000);
  const [moves, setMoves] = useState<number>(0); // Initialize moves state

  /**
   * Handles the card click event.
   * Flips the card and checks if two cards are flipped to determine if they match.
   * @param {number} id - The id of the clicked card.
   */
  const handleCardClick = (id: number) => {
    setCards((prevCards) =>
      prevCards.map((card) =>
        card.id === id ? { ...card, isFlipped: !card.isFlipped } : card
      )
    );

    setFlippedCards((prevFlipped) => {
      const newFlipped = [...prevFlipped, id];
      if (newFlipped.length === 2) {
        const [firstCard, secondCard] = newFlipped.map((cardId) =>
          cards.find((card) => card.id === cardId)
        );
        if (firstCard && secondCard && firstCard.value === secondCard.value) {
          setCards((prevCards) =>
            prevCards.map((card) =>
              card.id === firstCard.id || card.id === secondCard.id
                ? { ...card, isMatched: true }
                : card
            )
          );
        } else {
          setTimeout(() => {
            setCards((prevCards) =>
              prevCards.map((card) =>
                card.id === firstCard?.id || card.id === secondCard?.id
                  ? { ...card, isFlipped: false }
                  : card
              )
            );
          }, 1000);
        }
        setScore((prevScore) => prevScore - 100); // Reduce score by 100 for each move
        setMoves((prevMoves) => prevMoves + 1); // Increment moves by 1 for each move
        return [];
      }
      return newFlipped;
    });
  };

  /**
   * Checks if all cards are matched and ends the game if they are.
   */
  useEffect(() => {
    if (cards.every((card) => card.isMatched)) {
      onEndGame();
    }
  }, [cards, onEndGame]);

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      <p>Score: {score}</p> {/* Display the score */}
      <p>Moves: {moves}</p> {/* Display the number of moves */}
      <div className="card-grid">
        {cards.map((card) => (
          <Card
            key={card.id}
            cardNumber={card.value}
            isFlipped={card.isFlipped}
            isMatched={card.isMatched}
            onClick={() => handleCardClick(card.id)}
          />
        ))}
      </div>
      <div>
        <button onClick={onEndGame}>End Game</button>
      </div>
    </div>
  );
};

export default GameScreen;
```

</blockquote>
</details>

Save the file and refresh the game. Try to match all the cards and notice how the number of moves is tracked.

## Module 6: Events

### Adding a game timer

Let's add to our scoring system by introducing a game timer. The player will have a limited amount of time to complete the game. The game ends when the timer runs out.

Open the `copilot-instructions.md` file and add the following text to the scoring system section:

```markdown
- the player has 30 seconds to complete the game
- the game ends when the timer runs out
```

Save the file and enter the following prompt after opening the `GameScreen.tsx` file:

```markdown
add a game timer
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React, { useState, useEffect } from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

/*
    This is the GameScreen component that will be displayed when the game is in progress.
    It will display the grid of cards and a button to end the game.
    Optionally, we can add a timer, a score, and other game-related information here.
    We need to keep track of the state of each card, the number of cards, and the type of cards
    and implement the logic to check if two cards are a match. If they are a match, we can
    update the state of the cards to indicate that they are matched. If they are not a match,
    we can flip the cards back over.
*/

interface GameScreenProps {
  // keep track of the number of cards in the x and y grid
  x: number;
  y: number;
  onEndGame: () => void; // Prop function to end the game
  userName: string; // add userName prop
}

interface CardState {
  id: number;
  value: number;
  isFlipped: boolean;
  isMatched: boolean;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const [cards, setCards] = useState<CardState[]>(() => {
    const totalCards = x * y;
    const cardValues = Array.from({ length: totalCards / 2 }, (_, i) => i + 1);
    const allCardValues = [...cardValues, ...cardValues].sort(() => Math.random() - 0.5);
    return allCardValues.map((value, index) => ({
      id: index,
      value,
      isFlipped: false,
      isMatched: false,
    }));
  });

  const [flippedCards, setFlippedCards] = useState<number[]>([]);
  const [score, setScore] = useState<number>(10000);
  const [moves, setMoves] = useState<number>(0); // Initialize moves state
  const [timeLeft, setTimeLeft] = useState<number>(30); // Initialize timer state

  /**
   * Handles the card click event.
   * Flips the card and checks if two cards are flipped to determine if they match.
   * @param {number} id - The id of the clicked card.
   */
  const handleCardClick = (id: number) => {
    setCards((prevCards) =>
      prevCards.map((card) =>
        card.id === id ? { ...card, isFlipped: !card.isFlipped } : card
      )
    );

    setFlippedCards((prevFlipped) => {
      const newFlipped = [...prevFlipped, id];
      if (newFlipped.length === 2) {
        const [firstCard, secondCard] = newFlipped.map((cardId) =>
          cards.find((card) => card.id === cardId)
        );
        if (firstCard && secondCard && firstCard.value === secondCard.value) {
          setCards((prevCards) =>
            prevCards.map((card) =>
              card.id === firstCard.id || card.id === secondCard.id
                ? { ...card, isMatched: true }
                : card
            )
          );
        } else {
          setTimeout(() => {
            setCards((prevCards) =>
              prevCards.map((card) =>
                card.id === firstCard?.id || card.id === secondCard?.id
                  ? { ...card, isFlipped: false }
                  : card
              )
            );
          }, 1000);
        }
        setScore((prevScore) => prevScore - 100); // Reduce score by 100 for each move
        setMoves((prevMoves) => prevMoves + 1); // Increment moves by 1 for each move
        return [];
      }
      return newFlipped;
    });
  };

  /**
   * Checks if all cards are matched and ends the game if they are.
   */
  useEffect(() => {
    if (cards.every((card) => card.isMatched)) {
      onEndGame();
    }
  }, [cards, onEndGame]);

  /**
   * Handles the game timer.
   * Decrements the timer every second and ends the game when the timer runs out.
   */
  useEffect(() => {
    if (timeLeft > 0) {
      const timer = setInterval(() => {
        setTimeLeft((prevTime) => prevTime - 1);
      }, 1000);
      return () => clearInterval(timer);
    } else {
      onEndGame();
    }
  }, [timeLeft, onEndGame]);

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      <p>Score: {score}</p> {/* Display the score */}
      <p>Moves: {moves}</p> {/* Display the number of moves */}
      <p>Time Left: {timeLeft}s</p> {/* Display the time left */}
      <div className="card-grid">
        {cards.map((card) => (
          <Card
            key={card.id}
            cardNumber={card.value}
            isFlipped={card.isFlipped}
            isMatched={card.isMatched}
            onClick={() => handleCardClick(card.id)}
          />
        ))}
      </div>
      <div>
        <button onClick={onEndGame}>End Game</button>
      </div>
    </div>
  );
};

export default GameScreen;
```

</blockquote>
</details>

Save the file and refresh the game. Notice how the timer counts down from 30 seconds. The game should end when the timer runs out.

Our game is now beginning to feel like a game.

### Updating the leaderboard

We still have one last piece to complete our game. We need to update the leaderboard with the player's score, number of moves, and the number of cards they played with.

Open the `copilot-instructions.md` file and add the following text to the scoring system section:

```markdown
- if the player completes the game, add their name, score, number of moves, and number of cards to the leaderboard
- if the player does not complete the game, do not add them to the leaderboard
- players in the leaderboard should be sorted by score in descending order
```

Save the file and enter the following prompt after opening the `GameScreen.tsx` file:

```markdown
@workspace update the leaderboard
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

`App.tsx`:

```tsx
import { useState, useEffect } from 'react';
import SplashScreen from './components/SplashScreen';
import GameScreen from './components/GameScreen'; // import the GameScreen component
import EndScreen from './components/EndScreen'; // import the EndScreen component

/*
    This is the main App component that will manage the game state and render the appropriate
    GameScreen and EndScreen components. The App component will keep track of the game state and
    update it based on user interactions such as starting the game, ending the game, or restarting
    the game.
    Optionally, we can add more features such as a timer, a score, and a leaderboard to the game.
*/

function App() {
  const [gameState, setGameState] = useState('splash'); // state to manage the game state
  // @ts-ignore
  const [userName, setUserName] = useState(''); // state to manage the user's name
  interface LeaderboardEntry {
    playerName: string;
    numberOfMoves: number;
    numberOfCards: number;
    totalScore: number;
  }

  const [leaderboard, setLeaderboard] = useState<LeaderboardEntry[]>([]); // state to manage the leaderboard

  useEffect(() => {
    fetch('/leaderboard.json')
      .then(response => response.json())
      .then(data => setLeaderboard(data.leaderboard))
      .catch(error => console.error('Error fetching leaderboard data:', error));
  }, []);

  const startGame = () => {
    setGameState('play'); // set gameState to 'play' when game starts
  };

  const endGame = (score: number, moves: number, numberOfCards: number) => {
    if (score > 0) {
      const newEntry = {
        playerName: userName,
        numberOfMoves: moves,
        numberOfCards: numberOfCards,
        totalScore: score,
      };
      const updatedLeaderboard = [...leaderboard, newEntry].sort((a, b) => b.totalScore - a.totalScore);
      setLeaderboard(updatedLeaderboard);
      // Optionally, save the updated leaderboard to the server or local storage
    }
    setGameState('end');
  };

  const restartGame = () => {
    setGameState('splash'); // set gameState to 'splash' when game restarts
  };

  return (
    <div className="App">
      {gameState === 'splash' && (
        <SplashScreen onStartGame={startGame} setUserName={setUserName} />
      )}
      {gameState === 'play' && <GameScreen x={2} y={2} onEndGame={endGame} userName={userName} />}
      {gameState === 'end' && <EndScreen onRestartGame={restartGame} leaderboard={leaderboard} />}
    </div>
  );
}

export default App;
```

`GameScreen.tsx`:

```tsx
import React, { useState, useEffect } from 'react';
import '../styles/GameScreen.css';
import Card from './Card'; // import the Card component

interface GameScreenProps {
  x: number;
  y: number;
  onEndGame: (score: number, moves: number, numberOfCards: number) => void; // Update the onEndGame prop
  userName: string;
}

interface CardState {
  id: number;
  value: number;
  isFlipped: boolean;
  isMatched: boolean;
}

const GameScreen: React.FC<GameScreenProps> = ({ x, y, onEndGame, userName }) => {
  const [cards, setCards] = useState<CardState[]>(() => {
    const totalCards = x * y;
    const cardValues = Array.from({ length: totalCards / 2 }, (_, i) => i + 1);
    const allCardValues = [...cardValues, ...cardValues].sort(() => Math.random() - 0.5);
    return allCardValues.map((value, index) => ({
      id: index,
      value,
      isFlipped: false,
      isMatched: false,
    }));
  });

  const [flippedCards, setFlippedCards] = useState<number[]>([]);
  const [score, setScore] = useState<number>(10000);
  const [moves, setMoves] = useState<number>(0); // Initialize moves state
  const [timeLeft, setTimeLeft] = useState<number>(60); // Initialize timer state

  const handleCardClick = (id: number) => {
    setCards((prevCards) =>
      prevCards.map((card) =>
        card.id === id ? { ...card, isFlipped: !card.isFlipped } : card
      )
    );

    setFlippedCards((prevFlipped) => {
      const newFlipped = [...prevFlipped, id];
      if (newFlipped.length === 2) {
        const [firstCard, secondCard] = newFlipped.map((cardId) =>
          cards.find((card) => card.id === cardId)
        );
        if (firstCard && secondCard && firstCard.value === secondCard.value) {
          setCards((prevCards) =>
            prevCards.map((card) =>
              card.id === firstCard.id || card.id === secondCard.id
                ? { ...card, isMatched: true }
                : card
            )
          );
        } else {
          setTimeout(() => {
            setCards((prevCards) =>
              prevCards.map((card) =>
                card.id === firstCard?.id || card.id === secondCard?.id
                  ? { ...card, isFlipped: false }
                  : card
              )
            );
          }, 1000);
        }
        setScore((prevScore) => prevScore - 100); // Reduce score by 100 for each move
        setMoves((prevMoves) => prevMoves + 1); // Increment moves by 1 for each move
        return [];
      }
      return newFlipped;
    });
  };

  useEffect(() => {
    if (cards.every((card) => card.isMatched)) {
      onEndGame(score, moves, cards.length); // Pass score, moves, and number of cards to onEndGame
    }
  }, [cards, onEndGame, score, moves]);

  useEffect(() => {
    if (timeLeft > 0) {
      const timer = setInterval(() => {
        setTimeLeft((prevTime) => prevTime - 1);
      }, 1000);
      return () => clearInterval(timer);
    } else {
      onEndGame(score, moves, cards.length); // Pass score, moves, and number of cards to onEndGame
    }
  }, [timeLeft, onEndGame, score, moves, cards.length]);

  return (
    <div className="gamescreen">
      <h1>Game Screen</h1>
      <p>Welcome, {userName}!</p> {/* Display the username */}
      <p>Score: {score}</p> {/* Display the score */}
      <p>Moves: {moves}</p> {/* Display the number of moves */}
      <p>Time Left: {timeLeft}s</p> {/* Display the time left */}
      <div className="card-grid">
        {cards.map((card) => (
          <Card
            key={card.id}
            cardNumber={card.value}
            isFlipped={card.isFlipped}
            isMatched={card.isMatched}
            onClick={() => handleCardClick(card.id)}
          />
        ))}
      </div>
      <div>
        <button onClick={() => onEndGame(score, moves, cards.length)}>End Game</button> {/* Pass score, moves, and number of cards to onEndGame */}
      </div>
    </div>
  );
};

export default GameScreen;
```

</blockquote>
</details>

Save the file and refresh the game. Try to complete the game and notice how the leaderboard is updated with the player's information.

## Module 7: Styles and Animations

Let's add some styles and animations to our game to make it more visually appealing.

Enter the following prompt:

```markdown
@workspace #file:Card.css #file:Card.tsx flip a card on the horizontal axis when it is clicked to reveal the value
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

`Card.css`:

```css
.card {
  border: 1px solid #000;
  border-radius: 10px; /* Rounded corners */
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2); /* Shadow effect */
  padding: 1rem;
  text-align: center;
  background-color: #fff; /* White background */
  color: #000; /* Black text */
  width: 100px; /* Fixed width */
  height: 150px; /* Fixed height */
  display: flex; /* Use flexbox for centering */
  justify-content: center; /* Center horizontally */
  align-items: center; /* Center vertically */
  font-size: 1.2rem; /* Larger text */
  margin: 1rem; /* Space around each card */
  transition: transform 0.6s;
  transform-style: preserve-3d;
  position: relative;
}

.card.flipped {
  transform: rotateY(180deg);
}

.card .front,
.card .back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.card .back {
  transform: rotateY(180deg);
}

.card .front,
.card .back {
  display: flex;
  justify-content: center;
  align-items: center;
}

.card .back {
  transform: rotateY(180deg);
}
```

`Card.tsx`:

```tsx
import React from 'react';
import '../styles/Card.css';

interface CardProps {
  cardNumber: number;
  isFlipped: boolean;
  isMatched: boolean;
  onClick: () => void;
}

/**
 * Card component represents a single card in the memory game.
 * It displays the card number if the card is flipped or matched.
 * @param {CardProps} props - The properties of the card.
 * @returns {JSX.Element} The rendered card component.
 */
const Card: React.FC<CardProps> = ({ cardNumber, isFlipped, isMatched, onClick }) => {
  return (
    <div className={`card ${isFlipped || isMatched ? 'flipped' : ''}`} onClick={onClick}>
      <div className="front">Card</div>
      <div className="back">{`Card ${cardNumber}`}</div>
    </div>
  );
};

export default Card;
```

</blockquote>
</details>

Note the suggestion to add a flipped animation to the `card.css` file. Update the suggested files and refresh the game to see the animation.

Try asking Copilot to add a fade-in animation to the cards when they are flipped.

## Module 8: Testing

We'll add some tests to our game to ensure that it works as expected.

Let's start by asking Copilot how to approach testing our game.

```markdown
@workspace how should we test our game?
```

### Writing tests

To get us started, we've included the setup necessary to add and run tests for our game.

In the terminal, run the following command:

```bash
npm test
```

> [!TIP]
>
> You can press the q key to exit the test.

Let's start by adding test cases for our game screen component.

Create a new file called `GameScreen.test.tsx` in the `src/tests` directory.

> [!TIP]
>
> Test files are usually named with the `.test.tsx` extension and can be placed inside `src`.

Enter the following prompt:

```markdown
@workspace #file GameScreen.tsx add a unit test to ensure we have an even number of cards in the grid
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React from 'react';
import { render } from '@testing-library/react';
import GameScreen from '../components/GameScreen';

test('ensures there is an even number of cards in the grid', () => {
  const { container } = render(<GameScreen x={4} y={4} onEndGame={() => {}} />);
  const cards = container.querySelectorAll('.card');
  expect(cards.length % 2).toBe(0);
});
```

</blockquote>
</details>

Save the file as `GameScreen.test.tsx` and run the tests again.

```bash
npm test
```

You should see the test pass.

Congratulations! You've added your first test to the game.

Let's add another test to ensure that the game ends when all the cards are matched.

Enter the following prompt:

```markdown
@workspace #file GameScreen.tsx add a unit test to ensure the game ends when all cards are matched
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React from 'react';
import { render, fireEvent } from '@testing-library/react';
import GameScreen from '../components/GameScreen';

test('ensures the game ends when all cards are matched', () => {
  const onEndGame = jest.fn();
  const { container } = render(<GameScreen x={2} y={2} onEndGame={onEndGame} />);
  const cards = container.querySelectorAll('.card');

  // Simulate clicking all cards to match them
  cards.forEach(card => {
    fireEvent.click(card);
  });

  // Check if onEndGame was called
  expect(onEndGame).toHaveBeenCalled();
});
```

</blockquote>
</details>

Save the file and run the tests again.

```bash
npm test
```

You should see the test pass.

Now let's try adding unit tests for the rest of the GameScreen component.

Enter the following prompt:

```markdown
@workspace #file GameScreen.tsx add more unit tests for the GameScreen component
```

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

```tsx
import React from 'react';
import { render, fireEvent } from '@testing-library/react';
import GameScreen from '../components/GameScreen';

test('ensures there is an even number of cards in the grid', () => {
  const { container } = render(<GameScreen x={4} y={4} onEndGame={() => {}} />);
  const cards = container.querySelectorAll('.card');
  expect(cards.length % 2).toBe(0);
});

test('ensures the game ends when all cards are matched', () => {
  const onEndGame = jest.fn();
  const { container } = render(<GameScreen x={2} y={2} onEndGame={onEndGame} />);
  const cards = container.querySelectorAll('.card');

  // Simulate clicking all cards to match them
  cards.forEach(card => {
    fireEvent.click(card);
  });

  // Check if onEndGame was called
  expect(onEndGame).toHaveBeenCalled();
});

test('ensures the score decreases with each move', () => {
  const { getByText } = render(<GameScreen x={2} y={2} onEndGame={() => {}} />);
  const card = getByText('Card 1');

  // Initial score
  expect(getByText(/Score: 10000/i)).toBeInTheDocument();

  // Simulate a move
  fireEvent.click(card);
  fireEvent.click(card);

  // Score should decrease
  expect(getByText(/Score: 9900/i)).toBeInTheDocument();
});

test('ensures the timer counts down', () => {
  jest.useFakeTimers();
  const { getByText } = render(<GameScreen x={2} y={2} onEndGame={() => {}} />);

  // Initial time
  expect(getByText(/Time Left: 30s/i)).toBeInTheDocument();

  // Fast-forward time
  jest.advanceTimersByTime(10000);

  // Time should decrease
  expect(getByText(/Time Left: 20s/i)).toBeInTheDocument();
});
```

</blockquote>
</details>

Save the file and run the tests again.

```bash
npm test
```

You should see all the tests pass.

Did any of the tests fail? If so, try asking Copilot for help to fix the failing tests.

### Code coverage

Test coverage is a measure used to describe the degree to which the source code of a program is executed when a particular test suite runs. A program with high test coverage, measured as a percentage, has had more of its source code executed during testing, which suggests it has a lower chance of containing undetected software bugs compared to a program with low test coverage.

Let's see what our current test coverage is.

Enter the following in the terminal:

```bash
npm test -- --coverage
```

You should see a summary of the test coverage.

Let's ask Copilot how we can improve our test coverage.

```markdown
@workspace how can we improve our test coverage?
```

## Module 9: Writing Documentation

Documentation is an essential part of software development. Let's ask Copilot to help us write some documentation for our game.

```markdown
@workspace write documentation for the game
```

> [!TIP]
>
> We can ask Copilot to include information about our application such as how to install and play the game, the rules of the game, and any other relevant information.

<details>
<summary><strong>View Response</strong></summary>
<blockquote>

</blockquote>
</details>

