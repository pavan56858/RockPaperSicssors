# Rock Paper Scissors Game

A classic Rock Paper Scissors game built with vanilla JavaScript, HTML, and CSS. Features an interactive web interface with real-time score tracking and visual feedback.

## Game Overview

This is a web-based implementation of the timeless Rock Paper Scissors game where players compete against a computer opponent. The game features a clean, responsive design with immediate visual feedback and persistent score tracking.

## Features

- **Interactive Gameplay**: Click-based choice selection with instant results
- **Real-time Score Tracking**: Live updates of player vs computer scores
- **Visual Feedback**: Color-coded messages indicating win/lose/tie results
- **Responsive Design**: Works seamlessly across desktop and mobile devices
- **Clean UI**: Modern interface with image-based choice selection
- **Instant Results**: Immediate game outcome display with detailed messaging

## Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Images**: PNG assets for rock, paper, and scissors choices
- **Styling**: Custom CSS with responsive design principles
- **Logic**: Pure JavaScript for game mechanics and DOM manipulation

## Getting Started

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional installations required

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/pavan56858/RockPaperSicssors.git
   ```

2. **Navigate to project directory**:
   ```bash
   cd RockPaperSicssors
   ```

3. **Open the game**:
   ```bash
   open index.html
   ```
   Or simply double-click the `index.html` file to launch in your browser.

## How to Play

1. **Make Your Choice**: Click on Rock, Paper, or Scissors image
2. **Computer Responds**: The computer automatically makes its choice
3. **View Results**: The outcome is displayed with color-coded messaging:
   - **Green**: You win
   - **Red**: You lose  
   - **Blue**: It's a tie
4. **Track Score**: Your score and computer score update automatically
5. **Continue Playing**: Make another choice to continue the game

### Game Rules
- **Rock** beats **Scissors**
- **Scissors** beats **Paper**
- **Paper** beats **Rock**
- **Same choice** = Tie

## Project Structure

```
RockPaperSicssors/
│
├── index.html              # Main HTML structure
├── app.js                  # Game logic and functionality  
├── style.css              # Styling and layout
├── images/                # Game choice images
│   ├── rock.png           # Rock choice image
│   ├── paper.png          # Paper choice image
│   └── scissors.png       # Scissors choice image
└── README.md              # Project documentation
```

## Code Structure

### JavaScript Implementation (`app.js`)

**Core Variables:**
```javascript
let userScore = 0;           // Player score tracking
let compScore = 0;           // Computer score tracking
const choices = document.querySelectorAll(".choice");  // Choice elements
const msg = document.querySelector("#msg");            // Message display
```

**Key Functions:**
- `genCompChoice()`: Generates random computer choice using Math.random()
- `drawGame()`: Handles tie game scenarios with blue background
- `showWinner()`: Updates scores and displays win/lose messages with color coding
- `playGame()`: Main game logic comparing choices and determining outcomes

**Game Logic Flow:**
1. User clicks a choice (rock, paper, or scissors)
2. Computer generates random choice
3. Choices are compared using conditional logic
4. Winner is determined and scores updated
5. Visual feedback provided through message styling

### HTML Structure (`index.html`)

**Main Components:**
- **Header**: Game title
- **Choices Section**: Three clickable choice divs with images
- **Score Board**: Real-time score display for user and computer
- **Message Container**: Dynamic feedback messages

### Event Handling

The game uses event listeners on each choice element:
```javascript
choices.forEach((choice) => {
  choice.addEventListener("click", () => {
    const userChoice = choice.getAttribute("id");
    playGame(userChoice);
  });
});
```

## Game Logic Details

### Computer Choice Generation
```javascript
const genCompChoice = () => {
  const options = ["rock", "paper", "scissors"];
  const randIdx = Math.floor(Math.random() * 3);
  return options[randIdx];
};
```

### Win Condition Logic
- **Rock vs Paper**: Paper wins (Paper covers Rock)
- **Rock vs Scissors**: Rock wins (Rock crushes Scissors)
- **Paper vs Scissors**: Scissors wins (Scissors cut Paper)
- **Same choices**: Tie game

## Visual Design Features

- **Color-coded Results**: 
  - Green background for wins
  - Red background for losses
  - Blue background for ties
- **Image-based Choices**: PNG images for intuitive selection
- **Responsive Layout**: Adapts to different screen sizes
- **Clean Typography**: Clear, readable fonts and messaging

## Future Enhancements

### Potential Improvements
- [ ] Add reset/restart game functionality
- [ ] Implement best-of-X game modes
- [ ] Add sound effects for choices and results
- [ ] Create animated choice reveals
- [ ] Add game statistics and win percentages
- [ ] Implement difficulty levels with different AI strategies
- [ ] Add local storage for persistent high scores

### Technical Improvements
- [ ] Add CSS animations and transitions
- [ ] Implement proper error handling
- [ ] Add keyboard navigation support
- [ ] Create mobile-optimized touch interactions
- [ ] Add loading states and performance optimizations

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Mobile browsers (iOS Safari, Chrome Mobile)

## Learning Objectives

This project demonstrates:
- **DOM Manipulation**: Dynamic content updates and event handling
- **JavaScript Fundamentals**: Variables, functions, conditionals, and arrays
- **Random Number Generation**: Using Math.random() for computer choices
- **Event-Driven Programming**: Click event handling and user interaction
- **CSS Styling**: Visual feedback and responsive design principles
- **HTML Structure**: Semantic markup and accessibility considerations

## Contact

**Pavan Kumar**
- **Email**: pavankumar1292004@gmail.com
- **GitHub**: [@pavan56858](https://github.com/pavan56858)
- **LinkedIn**: [Pavan Kumar](https://www.linkedin.com/in/pavan-kumar-b9a4102b8)

## License

This project is open source and available under the MIT License.

---

**Built with vanilla JavaScript for simplicity and learning purposes.**
