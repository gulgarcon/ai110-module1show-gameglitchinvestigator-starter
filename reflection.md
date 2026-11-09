# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
|61     | (Hint stating to go lower)| Hint says to go higher | None |
|Click new game once won | New game to start (new secret number) | No game started | None/You already won. Start a new game to play again|
|Click new game once lost | New game to start (new secret number) | No game started | None/Game over. Start a new game to play again|
|53 with a secret number of 53| Score in debug info to match the message| Debug score says 0 while message at bottom if screen says Final Score: 70| You won! The secret was 53. Final score: 70
| Changing difficulty| Blue Message to user to guess between ranges to change | Message stays the same | Message changes in settings (e.g changing to easy -> guess a number between 1 to 20)

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
I used Claude on this project 
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
In test_game_logic.py, testing a guess that is too low is quite easy to spot. I manually verified this through the app and running pytest
- Give one example of an AI suggestion you did not accept as written (including what the AI suggested, why you rejected or changed it, and how you verified your version). It does not have to be a suggestion that was wrong: over-engineered, out of scope, harder to read, or a poor fit for this codebase all count.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
After implementing my code changes, I manually re-ran my streamlit app to confirm the app behaved as intended.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
With Claude's assistance, I wrote a suite of python test cases to test the game logic 
- Did AI help you design or understand any tests? How?
Yes, AI helped with the designing but because the tests were rather simple in scope it was quite easy to understand by checking (using assert) whether the result is what was intended.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

A Streamlit re-run is a python script that runs from top to bottom every time something happens (e.g. clicking a button, text-input change, etc). Session state is a dictionary object that persists for a session. If you close the tab or the server restarts, then it no longer persists. 
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
