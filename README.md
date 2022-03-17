# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Sophie Gessler**

Time spent: **5** hours spent in total

Link to project: https://glitch.com/edit/#!/heavy-pacific-tennis

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

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [x] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] User can choose how many buttons to display
- [ ] User can choose how long the pattern is

## Video Walkthrough (GIF)
Testing the Buttons

![](https://i.imgur.com/OepPNyk.gif)

Winning the Game

![](https://i.imgur.com/VJ3N43y.gif)

Losing the Game

![](https://i.imgur.com/9rwk2jB.gif)

Start Button Begins the Game / Stop Button Ends the Game

![](https://i.imgur.com/c1VIpGA.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

www.freecodecamp.org

www.w3schools.com

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

A challenge I encountered in creating this submission was implementing the feature of speeding up the playback cue each turn. After testing the game multiple times in a row, it came to my attention that the speed of the pattern was increasing each game, even if the game was reset. After a couple of tries, it was nearly impossible to play the game because the buttons flashed too quickly. I realized that the issue was caused by only declaring and initializing the clueHoldTime variable as a global variable. Because the clueHoldTime variable was decremented each time the startGame() function was called, the variable continued to get smaller and smaller each game. In order to solve this problem, I assigned the variable clueHoldTime to 1000 before the playClueSequence() function is called, in the startGame() function. That way, each time the startGame() function is called, clueHoldTime is reset to 1000 and then decremented throughout the game. I overcame this challenge by testing my code multiple times. From there, I tried to understand the problem and figure out where that problem would be. I traced through the program as it would execute and it came to my attention that there was an issue within the startGame() function. Another issue I ran into while completing the project was in implementing the random secret pattern at the beginning of each game. At first, I didn't really know where to begin in writing this method. I started solving this issue by analyzing  how the program operated with the array pattern that was already assigned variables. It came to my attention that I needed to find a way to use JavaScript's Math.random() function to select numbers in between 1-6, and then add them to the pattern array. Ultimately, I decided to use a for loop to iterate through the indices of the pattern array and use Math.random() to assign numbers 1-6 to the elements. A minor problem I ran into was that the Math.random() function generates numbers in the range 0 to less than 1. A simple solution to that was to multiply Math.random() by 6 and add one, while also taking the floor of the number to get a whole number. Throughout creating this method, I overcame the challenges through trial and error and by really thinking about the logic of what needed to be done.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

After completing my project, a question I have about web development is how to create a website that has less of a formal structure of a title, header, paragraphs, etc. I would love to learn more about how to design more creative websites with different shaped buttons and the freedom to place items anywhere on the page. I enjoyed choosing the colors, fonts, and shapes of the buttons in my project, however, I am eager to learn more about what other design features I can implement into my work. Another question I have is what is the difference between front end and back end development. This project mostly consisted of front end development, and I would love to learn more about how back end development works when designing a website. I am curious how similar or different they are, and how they work together to create a functioning product. After completing my submission, I have questions about how larger, more complex websites operate with millions of users, due to the fact that this project was fairly simple. I also have questions in regards to how I can make my project more interactive with the user. I wonder what other features of HTML, CSS, and JavaScript exist, so that I can create functions to give the user a better experience. 

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

If I had a few more hours to work on this project, I would design more functions to add additional features. I would implement the other optional features that I did not create, and also design some of my own. I would create a feature to let the user choose the difficulty of the game before playing. I would create three buttons for easy, medium, and hard that the user could select before starting. These buttons would control how long each pattern would be, for example easy containing less numbers and hard containing more numbers that the user needs to repeat before winning the game. I would also implement a feature where the user could choose how many buttons are in the game. I would create an option for the user to choose between 3-6 buttons at the beginning of the game. These functions allow the user to personalize the game, which creates a better experience for the player. I would also add to the design of the game and research more fonts, color palettes, and images that I could include to make the project more appealing to the eye. If I could spend more time on this project, I would definitely add more unique features that reflect more personality.



## Interview Recording URL Link

[My 5-minute Interview Recording](https://SDSU.zoom.us/rec/share/7PAe4QoaqrKBuDYRKbTPv0U01VT5NOSqJv2LeyhNlfxJqTwQ6rzone3ioRL7hnDr.u-nPbNvV8yCDCrk_?startTime=1647547330000)


## License

    Copyright Sophie Gessler

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
