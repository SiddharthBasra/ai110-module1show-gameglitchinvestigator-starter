# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

When I first ran the game, the UI looked functional, but opening the Developer Debug Info immediately showed that the game's internal state was out of sync.

Two concrete bugs I noticed right at the start were:

The attempt counter initializes at 1 instead of 0 before any guesses are made, which unfairly leaves the player with only 7 attempts instead of the promised 8.

When a guess is submitted (even the exact correct secret number), the guess history array [] does not update to record the guess, and the internal score remains at 0 while the UI displays a mathematically incorrect final score.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

Streamlit runs the entire Python script from top to bottom every single time a user interacts with a widget. I would explain session state to a friend as the short term memory of the app that stores variables like the secret number and guess history so they are not wiped out during these reruns.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

A habit I want to reuse is using Copilot Agent mode to handle complex refactoring tasks like moving functions between files. Next time I will be more careful about how AI handles session state variables because I learned that AI can fix the logic while forgetting to update the app memory. This project changed my thinking by proving that AI generated code is a draft that requires human verification and manual adjustments to function correctly in a real world environment.