# Virtual Reality Project 1

Project 1 was an individual virtual reality assignment where we were tasked with creating an interactive environment which also displayed an aspect of how Covid-19 has affected us. 

## Project Links 

<a href="https://trevorpike123.github.io/NewProject1/">Enter my Virtual World</a>

<a href="https://www.youtube.com/watch?v=fuZHbIO0vaQ&feature=youtu.be">Project 1 Demo Youtube</a>

### Instructions
Once you have entered the "Enter my Virtual World" link, you can freely move around using the wasd keys. You can turn camera with a mouse or by turning head with VR headset. My project utilizes clicking objects to interact with objects/lighting. 

All interactable objects are listed below: 

- Light switches in the livingroom and left bedroom may be turned on and off by clicking green and red button on the wall respectively.
- User may open and close all doors in the environment
- In the right bedroom, users may either select white lighting or multicolored lighting by clicking white and red button on the wall respectively.
- When user clicks on the monitor in the right bedroom, the user will hear a sound file played.
- User may turn the television on and off by clicking the tv and will see a video played (unfortunately I was not able to mute the sound of the video when the tv is turned off).
- Lastly, the user may click the "Covid Button" (yellow button) in the right bedroom to reveal a baby crib which is how Covid-19 effected me personally.


### Code    
The project uses aframe to run the code. I utilized an addon called aframe event-set-component which allowed to me tie multiple click event actions to one object. This is how I was able to use one button to turn all lights off and another button to turn all lights on in their specific rooms. Below is an example of how I utilized this feature:

```
<a-box id="rgbfunction_bedroom" material="color: red;"
        position="60.15 2.5 -4" height="0.5" depth="0.5" width="0.2"
        event-set__1="_event: click; _target: #Computerroom_Light1; color: #f52c2c;"
        event-set__2="_event: click; _target: #Computerroom_Light2; color: #2c47f5;"
        event-set__3="_event: click; _target: #Computerroom_Light3; color: #f52c2c;"
        event-set__4="_event: click; _target: #Computerroom_Light4; color: #2c47f5;"
        event-set__5="_event: click; _target: #Computerroom_Light5; color: #34db2e;"
        event-set__6="_event: click; _target: #Computerroom_Light6; color: #34db2e;"></a-box>
```
![ScreenShot](/demo_images/whiteLight.png)
![ScreenShot](/demo_images/multiLight.png)

### Covid Mode
I was able to use a box item in order to toggle the visibility of my covid object (baby crib). The baby crib was initially set as visible = false, and once the box item (I called this my covid button) was pressed it was make the baby crib appear. Below is screenshots of this feature:
![ScreenShot](/demo_images/covidOff.png)
![ScreenShot](/demo_images/covidOn.png)

### Issues
While doing my project I ran into many issues on the way, but there were two issues that gave me the most problem. My first issue was trying to find a way to have one object affect other objects. I spent countless hours trying to learn complicated JavaScript code to do a task that I thought was fairly simple. I came across a website after searching google which gave me a simple solution to my problem. 

<a href="https://www.npmjs.com/package/aframe-event-set-component">aframe-event-set-component</a>

This simple a-frame component addon fixed all the issues that I was having.

The second issue I had was trying to optimize my house to run better. My first implementation of my code had about 30 assets, multiple rooms, multiple lights, and high resolution textures. I quickly found out that this made my code sluggish and laggy. I ended up removing about 12 assets that were high resolution and pointless, and stick to two rooms. I found a very interesting article about aframe optimization that really helped me improve my performance while still meeting all the requirements.

<a href=https://hacks.mozilla.org/2017/07/optimizing-performance-of-a-frame-scenes-for-mobile-devices/>Optimizing Performance of A_Frame Scenes for Mobile Devices</a>

This article had very many interesting facts about aframe optimization, for example, using textures that are powers of two helps ensure optimal memory use. 

### Conclusion
In conclusion, I think that this project was a good stepping stone into learing how to code in virtual reality. A learned the basics of aframe and I now feel confident in my ability to code using it. I plan on coming back to this project in the future and improving it even more. Some improvements I would like to make is making an outside area, and making multiple levels(upstairs and downstairs). 

### Contribution
- Created by Jordan Coe.

### Objects and Interactions
19 Unique Models

<a href="https://github.com/JuJoCoe/JuJoCoe.github.io/blob/master/assets/Assetsworkcited.txt">Assets Used</a>

4 Interactions
- The user may interact with the light switches in the living room. The on switch is on the left, while the off switch is on the right.
- The dynamic object is the door. The user may open and close the door.
- The choose your color boxes in the bedroom. The user can choose 1 of 4 colors, and all the lights inside the bedroom will match the color. 
- When the user goes up to the laptop sitting on the desk, the laptop will make a startup sound. 
