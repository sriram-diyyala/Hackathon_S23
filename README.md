# CalHacksLLM  - https://www.youtube.com/watch?v=SkapYN90mng

##Inspiration

AI is only truly intelligent when it solves your problems before you ask them. Our idea for SPECTRE (Sentient Personalized Emotionally Cognitive Task and Response Engine) came while we were building an adjacent product that was targeted to help people with neurodegenerative diseases that made it difficult to interact with their hands.

We realized that using Hume's API, we could actively assess when a user felt a certain emotion, like confusion, and we could automate the detection of what the user was interacting with to enable the LLM to help the user. We drew similarities to Iron Man's JARVIS and saw a vision that went beyond it, as even JARVIS didn't factor in human emotion to visibly alter its ability to interact and engage the user.

**What it does
**
In our demo, SPECTRE uses the Hume API to detect the emotion “confusion”. Once the confusion confidence crosses a certain threshold, a graphical user interface pops up that allows the user to enter a question promptly, except there's no need to give it context. SPECTRE automatically assesses what's on your screen, be it an image, a LeetCode problem, or a college textbook. Using the context on screen and any small 1-5 word prompts, it can solve any use case we have run it through. When the GUI is then closed, it will stay hidden until that confusion threshold is crossed again, when the process repeats. There is no interaction with the device unless you need help, and it runs in the background with negligible RAM usage.

**How we built it
**
We used a Python script to manage the API calls and the GUI. We used the Pytesseract library for the screen OCR, the Hume API for emotion detection through the webcam, and the OpenAI LLM to answer questions given a prompt and the current browser tab.

We had to meticulously prompt the engineer the LLM to provide an answer in a manner that is appropriate to the user.

**Challenges we ran into
**
One challenge was satisfying a competent human-computer interface. At first, we had to keep relaunching the script, then using the command line interface. We eventually narrowed it down to a flowchart of user interaction and prompting with a GUI.

We initially ran into many challenges such as the OCR taking too long to complete to be useful. after trying many libraries we found pytesseract that worked well enough as an input to the LLM.

**Accomplishments that we're proud of
**
After a small improvement, such as replacing keyboard use with speech, (refer "What's Next"), this bot may finally be able to work like JARVIS from Iron Man. It's primary immediate use case is in education, where on an education app, it can be integrated to assess how a human is behaving with the subject matter, what they get confused by, and contactless education tools.

What's next for SPECTRE
Our first integration would be the ability to provide context to the LLM without even the 1-5 word guiding prompt. This can be accomplished through recording audio of what the user is saying. Other interactions include incorporating responses to a wide ranges of Hume's 48 emotional indexes.
