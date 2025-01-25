# TicTacToe
Tic Tac Toe Game
This project is a simple implementation of the classic Tic Tac Toe game. It is built using HTML, CSS, and JavaScript, providing an interactive and visually appealing user interface.

Features
1. Player Turns: Players take turns marking the cells as either O or X.
2. Winner Detection: The game automatically detects the winner based on predefined winning patterns.
3. Reset Game: Allows players to reset the game board.
4. New Game: Starts a new game while hiding the winner message.
5. Responsive Design: The layout adjusts to different screen sizes for better user experience.
6. Dynamic UI: Smooth animations and hover effects enhance the gameplay experience.
  
   How It Works
Game Rules:
The game starts with Player O making the first move.
Players alternate turns by clicking on the boxes on the game board.
The first player to align three of their symbols (O or X) horizontally, vertically, or diagonally wins.

Key Functionalities:
1. Player Turn Management:
The turnO variable tracks whose turn it is (true for Player O and false for Player X).
Once a cell is clicked, the symbol is added, and the turn switches.
2. Winner Detection:
Winning patterns are pre-defined in the winP array.
The checkWinner() function iterates through these patterns and checks if all three cells in any pattern contain the same symbol.
3. Game Reset:
The resetGame() function clears the game board and allows a new game to start.
Both the Reset Game and New Game buttons call this function.
4. UI Feedback:
Winner messages are displayed dynamically using the showWinner() function.

Files Overview
1. index.html
The main HTML file that defines the structure of the game, including the game board, buttons, and message container.
2. style.css
Contains all the styles for the game, including the animations, layout, and responsiveness. Key animations include:
Fade-in effect for the body.
3. Hover and click effects for buttons.
Gradient background animation for visual appeal.
4. app.js
The main JavaScript file that powers the game logic, including:

Player turn handling.
Winner detection.
Game reset functionality.
How to Run
1. Download or clone the repository to your local machine.
2. Open the index.html file in any modern web browser.
3. Enjoy playing Tic Tac Toe!
Code Highlights
Winning Patterns Array
const winP = [
    [0,1,2], [0,3,6], [0,4,8], [1,4,7],
    [2,4,6], [2,5,8], [3,4,5], [6,7,8],
];
This array defines all the possible winning combinations.
Winner Detection Logic
const checkWinner = () => {
    for (let pattern of winP) {
        let pos1 = boxes[pattern[0]].innerText;
        let pos2 = boxes[pattern[1]].innerText;
        let pos3 = boxes[pattern[2]].innerText;

        if (pos1 !== "" && pos2 !== "" && pos3 !== "" && pos1 === pos2 && pos2 === pos3) {
            showWinner(pos1);
        }
    }
};
This function iterates through each pattern and checks if all three cells in the pattern are the same.

Future Improvements
1. Tie Detection: Add logic to detect when the game ends in a tie.
2. AI Opponent: Implement an AI opponent for single-player mode.
3. Scoring System: Add a scoreboard to keep track of wins and ties.
4. Sound Effects: Include sound effects for clicks and winner announcements.
