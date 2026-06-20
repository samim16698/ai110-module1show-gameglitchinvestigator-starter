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
| | | | |
| | | | |
| | | | |

---

## 2. How did you use AI as a teammate?

- I used Chatgpt as an assistant for this project. AI was very helpgul in learning how to use AI and Github (as I don't have much experience with these tools)
- One of the bugs I observed while looking at the game was that it was giving wrong hints. It kept on saying "go higher" even though the answer was low. 
- When I ashowed the code to AI, AI pointed out that the bug was due to the code saying when guess > score, the player should "GO HIGHER" but the code should "GO LOWER." I rade the chaange that was suggested by AI and then went back to the site to check the result. When I saw that the hints were now correct, I knew that AI had made the correct suggestion. 
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result)

--- THE AI suggested moving check_guess() to logic_utlis.py
It created confusion for me because at first I didn't know whether to keep the old function or delete it from app.py 
I verified the result by running the test and Streamlit again to make sure the game was still working. 

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

- I knew that the bug (the one that was giving wrong hints) was fixed when I ran the new code and went back to the game to see if it was working properly. When the game started giving correct hints when number was too high, I knew the bug was fixed. 

- I ran pytest and all three tests passed. i also ran the Streamlit app and tested the game manually and the game was running better and wiith proper hints this time. This showe me that the updated code was working properly. 

- Yes AI helped me create the pytest case for check_guess() and explained what the tests were checking. This helpeme me understand how to verigy that the bug was fixed. 

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
