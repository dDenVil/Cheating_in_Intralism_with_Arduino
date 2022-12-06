## How to cheat in the game "Intralism" with Arduino Pro Micro

Hey there, I want to show you my first arduino project that I've made 4 years ago.
Have you ever played "Intralism" . The rules are quite simple. Press WASD or arrows in the right moments to keep the rhythm. Kinda like a tiles piano on the phone, beat saber or geometry dash.

![Game Interface](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/intro.jpg?raw=true)

## Problem
__I wanted to be the first__ in the leaderboard. So I came up with idea to cheat , but not with help software, but with hardware.

The first idea  that came up to my head, was to use servos and photoresistors, however it is not the most efficient way, but spectacular. So I decided to use __Arduino Pro Micro!__ and photoresistors. The feature of this board is microcontroller 32U4 that can emulate keyboard or mouse on PC.

## Device board
Round mdf board with [photoresistor modules](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/module.jpg?raw=true) and socket for MK.
Lately I changed photoresistor modules on photoresistor devider and added 3 LEDs, button.

![device](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/board.jpg?raw=true)

To make it work we have to put it on the screen and correspond photoresistors with sides and center it.
### Schematics
![schematics](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/scheme.jpg?raw=true)    
The way it is works based on [resistor divider](https://en.wikipedia.org/wiki/Voltage_divider). When red arc passes through photoresistor, photoresistor changes voltage in the middle point between this 2 resistors. This changes we can count as moment to press the button. To detect changes much more easy colors of  background and arcs should be opposite.
### Code
Code is really simple, the hardest was to callibrate timings. It is really shitty, but if you need it, it is [here](Readme_assets/code.txt).
- including <Keyboard.h> library
- setting A0-A3 as analogRead inputs
- checking condition if value of resistor devider changed
- pressing correspond button.

## In-game results
They are shocking.  __I achieved everything I wanted ;D__

![Top](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/top.jpg?raw=true)
![Top](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/top2.jpg?raw=true)
![Top](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/top3.jpg?raw=true)

Unfortunately, few weeks later __I was banned__ _(lately unbanned)_.

![Ban](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/ban.jpg?raw=true)

Found some old videos, here you can see how it worked.

![Gif](https://github.com/dDenVil/Cheating_in_Intralism_with_Arduino/blob/main/Readme_assets/VID_20190922_221437.gif?raw=true)
