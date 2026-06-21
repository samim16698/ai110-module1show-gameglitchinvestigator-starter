# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

I noticed many bugs when I started playing around with the game. The bugs/error included:
1. Hints are not accurate
      - I entered 10 and it said to go lower and then entered 9 and it said to go higher and in reality, the answer was 4.
2. The score giving is inconsistent
      - For example I got a wrong answer and was given a score of 5
      - Sometimes, they give you a score of -5 for wrong answers and sometimes -25
3. The "New Game" Button does not Work
      - When I click "new game" it does not work
      - I have to reload/refresh the page in order to start over
4. Numbers that are out of range are accepted
      - The game says the range is 1-100 but if I enter 1000, it still gives hints to go higher instead of rejecting this input

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

Input: 32
Expected Behavior: go higher
Actual Behavior: It said to go lower
Console Output/Error: The correct number was 87 but it kept on giving wrong hints

Input: Click New Game
Expected Behavior: A new game should start
Actual Behavior: Nothing happened and user has to reload page to start new game
Console Output/Error: The new game button does not work

Input: 1000
Expected Behavior: Input should be rejected because its not within range of (1-100)
Actual Behavior: Game accepts input and says to go higher
Console Output/Error: Game accepts input and still says to go higher 


## 2. How did you use AI as a teammate?

- I used Chatgpt as an assistant for this project. AI was very helpful in learning how to use AI and Github (as I don't have much experience with these tools)

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).

- One of the bugs I observed while looking at the game was that it was giving wrong hints. It kept on saying "go higher" even though the answer was low. 
- When I showed the code to AI, AI pointed out that the bug was due to the code saying when guess > score, the player should "GO HIGHER" but the code should say "GO LOWER." I made the change that was suggested by AI and then went back to the site to check the result. When I saw that the hints were now correct, I knew that AI had made the correct suggestion. 


- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result)

- THE AI suggested moving check_guess() to logic_utlis.py
It created confusion for me because at first I didn't know whether to keep the old function or delete it from app.py 
I verified the result by running the test and Streamlit again to make sure the game was still working. 

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

- I knew that the bug (the one that was giving wrong hints) was fixed when I ran the new code and went back to the game to see if it was working properly. When the game started giving correct hints when number was too high, I knew the bug was fixed. 

- I ran pytest and all three tests passed. i also ran the Streamlit app and tested the game manually and the game was running better and with proper hints this time. This showed me that the updated code was working properly.. 

- Yes AI helped me create the pytest case for check_guess() and explained what the tests were checking. This helped me me understand how to verify that the bug was fixed. 

## 4. What did you learn about Streamlit and state?

- Streamlit reruns the entire app whenever a user interacts with such as : clicking a button. 

The session state is session state is used to save information between reruns so the app remembers things like the score and attempts. 

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

- I plan to use AI to assist with code I do not understand and to break down codes I don't understand. 
- One thing I would do differently is try to refactor on the code on my own before using AI. 
- The way this project changed the way I think about AI id
    - I thought AI mostly generated the correct code but turns out it doesn't and that caught me by surprise. 
    - While AI is frowned upon, I think it can be a very helpful tool when used repsonsibly. Instead of having to spend hours writing a code, AI was able to generate code in a short amount of time. However, at the same time, one should also know how to read, write and understand code on their own without compeltely outsourcing thinking to AI. 