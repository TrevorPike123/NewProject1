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

### Complications
There were a number of issues I ran into with this project. The first was being new to aframe and js as well as html. I had to do a lot of legwork on learning how to make a VR application with aframe before I began adding assets to my index.html file. The second complication came with my mp4 file I added to my television asset. I was able to change the src file by using a variable to check for if the tv was on or not and using an EventListener on the tv asset. This worked well with one exception, I was not able to access the sound portion of the video file in order to stop the audio that was part of the mp4 file. Thus the sound file would continue to play even after the video had been changed to off. I worked hard to fix this issue but in the end ran out of time unfortunately. I kept the mp4 file to keep the tv interactive because it was my favorite part of the project.

### Conclusion
In conclusion, I think that this project was a good stepping stone into learing how to code in virtual reality. A learned the basics of aframe and I now feel confident in my ability to code using it. I plan on coming back to this project in the future and improving it even more. Some improvements I would like to make is making an outside area, and making multiple levels(upstairs and downstairs). 

### Objects and Interactions
19 Unique Models

<a href="https://github.com/JuJoCoe/JuJoCoe.github.io/blob/master/assets/Assetsworkcited.txt">Assets Used</a>
