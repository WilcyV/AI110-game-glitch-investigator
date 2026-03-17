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

### Game Purpose

This project is a simple number guessing game built with Streamlit. The goal is for the player to guess a secret number using Higher and Lower hints from the app.

### Bugs Found

When I first ran the game, the attempts counter was broken and could start at 0. I also noticed that the hints were inconsistent, and the secret number did not stay stable between guesses. The score could also become negative, which made the game feel unfair.

### Fixes Applied

I fixed the state bug by using `st.session_state` so the secret number, score, attempts, and history would not reset on every interaction. I corrected the Higher/Lower logic and moved the main game logic into `logic_utils.py`. I also ran pytest and fixed the code until all tests passed.

## 📸 Demo

- [ ] [Insert a screenshot of your fixed, winning game here]
![Winning game screenshot](Winnning_game_glitch.png)


## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, insert a screenshot of your Enhanced Game UI here]
