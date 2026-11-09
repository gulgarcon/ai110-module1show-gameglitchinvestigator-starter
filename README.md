# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
- [ ] Detail which bugs you found.
- [ ] Explain what fixes you applied.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:
In this example, the correct number is 27.

1. Guess a number from 1 to 100 (default for normal difficulty) within 7 attempts. User guesses 10
2. App returns "Go Higher"
3. User guesses 30
4. App returns "Go Lower"
5. User guesses 27
6. App returns "You Won! The secret was 27. Final score 35"


## 🧪 Test Results

```
(codepathai) ahmad@Ahmads-MacBook-Pro-2 ai110-module1show-gameglitchinvestigator-starter % python -m pytest
========================================================================= test session starts =========================================================================
platform darwin -- Python 3.14.8, pytest-9.1.1, pluggy-1.6.0
rootdir: /Users/ahmad/Documents/workspace/ai110-module1show-gameglitchinvestigator-starter
plugins: anyio-4.15.1
collected 4 items                                                                                                                                                     

tests/test_game_logic.py .... 
```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
