# 🎮 Memory Matching Game

A fun and interactive memory matching game built with **jQuery**, **JavaScript**, **HTML5**, and **CSS3**. Test your memory by flipping cards and finding matching pairs!

![Game Preview](https://img.shields.io/badge/Game-Active-green)
![License](https://img.shields.io/badge/License-Open%20Source-blue)
![jQuery](https://img.shields.io/badge/jQuery-3.6.0-blue)

---

## ✨ Features

- 🎨 **Beautiful UI** - Modern gradient design with smooth animations
- 🎮 **3 Difficulty Levels** - Easy (8 pairs), Medium (12 pairs), Hard (16 pairs)
- ⏱️ **Game Statistics** - Real-time move counter, timer, and pairs found
- 🔊 **Sound Effects** - Match, wrong, and win sounds (toggle on/off)
- 📱 **Fully Responsive** - Works perfectly on mobile, tablet, and desktop
- 🎯 **Win Condition** - Displays victory message with final stats
- ⚡ **Fast & Lightweight** - Single HTML file with all code included
- 🎭 **Emoji Cards** - Colorful emoji symbols for visual appeal

---

## 🚀 Quick Start

### Option 1: Play Online (If GitHub Pages Enabled)
```
https://YOUR_USERNAME.github.io/memory-matching-game/
```

### Option 2: Download & Open Locally
1. Download `memory_game_complete.html`
2. Open it in any web browser
3. Start playing! 🎉

---

## 📁 Project Structure

```
memory-matching-game/
├── memory_game_complete.html    # Complete game (HTML + CSS + JS)
├── index.html                   # Separate HTML file (optional)
├── style.css                    # Separate CSS file (optional)
├── script.js                    # Separate JavaScript file (optional)
└── README.md                    # This file
```

**Choose one:**
- Use `memory_game_complete.html` for simplicity
- Use `index.html` + `style.css` + `script.js` for organization

---

## 🎮 How to Play

1. **Open the Game** - Open `memory_game_complete.html` in your browser
2. **Select Difficulty** - Choose Easy, Medium, or Hard from the dropdown
3. **Flip Cards** - Click on face-down cards to reveal symbols
4. **Find Pairs** - Remember card positions and match pairs
5. **Game Rules:**
   - Only 2 cards can be flipped at a time
   - Timer starts on first flip
   - Move counter increases after each pair attempt
   - Matched pairs glow green and stay revealed
   - Unmatched pairs flip back after 1 second
6. **Win** - Match all pairs to see the victory message!

---

## 📊 Difficulty Levels

| Level | Pairs | Cards | Difficulty |
|-------|-------|-------|-----------|
| 🟢 Easy | 8 | 16 | Beginner |
| 🟡 Medium | 12 | 24 | Intermediate |
| 🔴 Hard | 16 | 32 | Advanced |

---

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Grid layout, Flexbox, animations, gradients
- **JavaScript (ES6+)** - Game logic and state management
- **jQuery 3.6.0** - DOM manipulation and events
- **HTML5 Audio API** - Sound effects

---

## 💻 Game Logic

### Key Components

```javascript
// Game State Management
gameState = {
    cards: [],           // Array of card objects
    flipped: [],         // Currently flipped card indices
    matched: [],         // Matched card indices
    moves: 0,            // Number of moves
    timer: 0,            // Time elapsed in seconds
    canFlip: true,       // Can player flip cards?
    soundEnabled: true   // Sound effects on/off
}
```

### Main Functions

- `initializeGame()` - Resets and creates new game
- `flipCard(index)` - Flips a card and checks conditions
- `checkMatch()` - Compares two flipped cards
- `winGame()` - Handles victory condition
- `startTimer()` - Starts the game timer
- `renderBoard()` - Renders all cards on the board
- `shuffleArray()` - Fisher-Yates shuffle algorithm
- `playSound()` - Plays sound effects

---

## 🎨 Customization Guide

### Change Card Symbols

Edit the `CARD_SYMBOLS` array in the JavaScript section:

```javascript
const CARD_SYMBOLS = ['🌟', '🎨', '🎭', '🎪', '🎯', '🎲', '🎸', '🎺', 
                      '🏀', '🎾', '⚽', '🏐', '🍕', '🍔', '🍰', '🍎'];
```

### Change Colors

Edit CSS variables:
```css
/* Primary color */
background-color: #667eea;

/* Secondary color */
background: #764ba2;

/* Success color (matched cards) */
background: linear-gradient(135deg, #84fab0 0%, #8fd3f4 100%);
```

### Change Grid Size

Edit the CSS grid:
```css
#gameBoard {
    grid-template-columns: repeat(4, 1fr);  /* 4 columns */
}
```

### Change Difficulty Settings

Edit the `DIFFICULTY_LEVELS` object:
```javascript
const DIFFICULTY_LEVELS = {
    easy: 8,      // 8 pairs = 16 cards
    medium: 12,   // 12 pairs = 24 cards
    hard: 16      // 16 pairs = 32 cards
};
```

---

## 📱 Responsive Design

The game is fully responsive and adapts to all screen sizes:

- **Desktop** - 4x4 grid for medium difficulty
- **Tablet** - 4 columns, adjusts for screen width
- **Mobile** - 3x3 grid, optimized for touch

```css
@media (max-width: 480px) {
    #gameBoard {
        grid-template-columns: repeat(3, 1fr);
    }
}
```

---

## 🔊 Sound Effects

The game includes three sound effects (built-in base64 encoded):

- 🟢 **Match Sound** - When cards match
- 🔴 **Wrong Sound** - When cards don't match
- 🎉 **Win Sound** - When game is won

Toggle sound with the **🔊 Sound Toggle** button.

---

## 📈 Game Statistics

The game tracks:

| Stat | Description |
|------|-------------|
| **Moves** | Number of pair attempts |
| **Time** | Seconds elapsed since first flip |
| **Pairs Found** | Number of successfully matched pairs |

All stats are displayed in the header and shown again at victory.

---

## ⌨️ Keyboard Features

- **Click Cards** - Flip cards
- **Click Difficulty Dropdown** - Change difficulty
- **Click Sound Toggle** - Turn sound on/off
- **Click Reset Button** - Start a new game

---

## 🎯 Game Flow

```
START GAME
    ↓
SHUFFLE CARDS
    ↓
WAIT FOR FIRST FLIP
    ↓
START TIMER
    ↓
FLIP TWO CARDS
    ↓
DO THEY MATCH?
    ├─ YES → Keep flipped, play sound, add to matched
    └─ NO → Flip back, play sound
    ↓
ALL PAIRS MATCHED?
    ├─ NO → Go back to "FLIP TWO CARDS"
    └─ YES → SHOW WIN MESSAGE → RESET
```

---

## 🐛 Browser Compatibility

✅ Works in all modern browsers:

- Chrome/Edge (Latest)
- Firefox (Latest)
- Safari (Latest)
- Opera (Latest)
- Mobile browsers

**Note:** Requires JavaScript and jQuery enabled.

---

## 📚 Learning Outcomes

This project teaches:

- ✅ jQuery selectors and event handling
- ✅ DOM manipulation and dynamic rendering
- ✅ Game state management
- ✅ CSS animations and transitions
- ✅ JavaScript ES6+ features
- ✅ HTML5 Audio API
- ✅ Array manipulation (shuffle algorithm)
- ✅ Conditional logic and loops
- ✅ Function organization and documentation

---

## 🚀 Performance

- **File Size** - ~15KB (HTML + CSS + JS combined)
- **Load Time** - < 1 second
- **Animations** - Smooth 60 FPS
- **Memory** - Minimal footprint

---

## 📝 Code Examples

### Flip a Card
```javascript
function flipCard(index) {
    gameState.flipped.push(index);
    const $card = $(`[data-index="${index}"]`);
    $card.addClass('flipped').text(gameState.cards[index].symbol);
    
    if (gameState.flipped.length === 2) {
        gameState.canFlip = false;
        gameState.moves++;
        setTimeout(() => checkMatch(), 600);
    }
}
```

### Check for Match
```javascript
function checkMatch() {
    const [index1, index2] = gameState.flipped;
    const card1 = gameState.cards[index1];
    const card2 = gameState.cards[index2];

    if (card1.symbol === card2.symbol) {
        // Match found
        gameState.matched.push(index1, index2);
        gameState.pairsFound++;
    } else {
        // No match - flip back
        $(`[data-index="${index1}"], [data-index="${index2}"]`)
            .removeClass('flipped').text('');
    }
}
```

### Shuffle Cards
```javascript
function shuffleArray(array) {
    const shuffled = [...array];
    for (let i = shuffled.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
    }
    return shuffled;
}
```

---

## 🤝 Contributing

Want to improve this project? 

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit (`git commit -m 'Add new feature'`)
5. Push to branch (`git push origin feature/improvement`)
6. Open a Pull Request

**Suggestions for improvements:**
- Add difficulty presets
- Implement leaderboard
- Add different card designs
- Create multiplayer mode
- Add power-ups
- Implement undo feature

---

## 📄 License

This project is **Open Source** and free to use for learning and educational purposes.

You are free to:
- ✅ Download and use
- ✅ Modify and customize
- ✅ Share and distribute
- ✅ Use in personal projects
- ✅ Use in educational settings

---

## 🙏 Acknowledgments

- Built with [jQuery](https://jquery.com/)
- Inspired by classic memory card games
- Created for learning jQuery and JavaScript

---

## 📞 Support & Feedback

Found a bug or have a suggestion?

1. Check the code and try to understand the issue
2. Open an Issue on GitHub
3. Describe the problem clearly
4. Provide steps to reproduce

---

## 🎓 Learning Resources

If you're learning from this project, check out:

- [jQuery Documentation](https://jquery.com/)
- [JavaScript Guide - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [CSS Grid Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Game Design Patterns](https://en.wikipedia.org/wiki/Game_design)

---

## 🎉 Have Fun!

This game is meant to be **fun, educational, and engaging**. 

**Challenge yourself:**
- Can you beat Easy in under 30 seconds?
- Can you complete Medium with less than 20 moves?
- Can you master Hard difficulty?

**Happy playing! 🎮✨**

---

## 📊 Project Stats

- **Lines of Code** - ~500
- **Functions** - 10+
- **CSS Rules** - 50+
- **Development Time** - Learning project
- **Status** - Fully Functional ✅

---

## 🔗 Quick Links

- **Repository** - [GitHub](https://github.com/YOUR_USERNAME/memory-matching-game)
- **Live Demo** - [Play Online](https://YOUR_USERNAME.github.io/memory-matching-game/)
- **Issues** - [Report Bugs](https://github.com/YOUR_USERNAME/memory-matching-game/issues)
- **Discussions** - [Community](https://github.com/YOUR_USERNAME/memory-matching-game/discussions)

---

**Made with ❤️ for learning and fun!**

Last Updated: 2024 | Version 1.0
