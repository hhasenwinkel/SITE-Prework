# SITE-Prework
# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Hannah Hasenwinkel

Time spent: 4 hours spent in total

Link to project: (insert your link here, should start with https://glitch.com...)

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [ ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ ] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](your-link-here)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
https://developers.google.com/web/updates/2017/09/autoplay-policy-changes#webaudio

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
The main challenge I encountered in this submission involved the use of AudioContext. First, when I copy-pasted the code for the Sound Synthesis Functions, my browser would not play back the sound at all. Then by using console logging, I located the lines where the error was occuring and followed the link that Chrome recommended for a possible solution. I discovered that the sounds were not playing because Chrome blocks autoplaying audio for their users convenience because it is good practice to wait for user interaction before playing audio. Since the suggested prework code has AudioContext created upon page load, I realized that I would have to use resume() or start() on the context variable in order allow the sound to play or I would have to move the creation of AudioContext (and o and g) inside of a function. I decided that it was probably a lot easier just to add context.resume() into a function. Originally, I put context.resume() only in the startTone function. This was almost a complete solution, but the first tone in the computer sequence still would not play. Then I went back through the code and realized that the first call on the context variable is in the playTone() function. I moved context.resume() to this function and the problem was solved.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
I was pleasantly surprised to learn about the Web API library and look forward to further investigating its functionality. This leads me to probably my biggest question not only about web development, but about programming in general: How do you keep finding the "next thing" to learn? Not only is this question important as I continue to build up my skills for a future career, but when I actually have a career, I assume that lifelong learning is necessary for enduring success in the tech industry. 

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
One feature I think could be interesting would be letting users "learn" certain songs. For example, more patterns could be created that mimic the tune of popular songs and the user could select which song to learn before the game begins. This would almost certainly require the creation of more buttons with distinct pitches. If I knew more about machine learning and AI, it would be really cool to implement a feature that allowed a user to select a song from Spotify then would transcribe the pitches of the melody and "teach" it to the user. I know that transcription AI like this exists, but I'm not quite sure how to actually implement it.
Another interesting (and probably more feasible) feature would be to incorporate rhythm into winning the game by using all of the time related variables. The computer would play back each pattern with its specific pitches in a specific rhythm and the user's response would have to be not only the correct pitches, but the correct pitches within the correct time interval.



## License

    Copyright Hannah Hasenwinkel

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
