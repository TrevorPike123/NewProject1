# Virtual Reality Project 1

Project 1 was an individual virtual reality assignment where we were tasked with creating an interactive environment which also displayed an aspect of how Covid-19 has affected us. 

## Project Links 

<a href="https://trevorpike123.github.io/NewProject1/">Enter my Virtual World</a>

<a href="https://youtu.be/OX1ovRHiuuE">Project 1 Demo Youtube</a>

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
There were a number of issues I ran into with this project. The first was being new to aframe and js as well as html. I had to do a lot of legwork on learning how to make a VR application with aframe before I began adding assets to my index.html file. The second complication came with my mp4 file I added to my television asset. I was able to change the src file by using a variable to check for if the tv was on or not and using an EventListener on the tv asset. This worked well with one exception, I was not able to actually stop the video once the source to the tv had changed, meaning the video would continue to loop after the tv turned black. I worked hard to fix this issue but in the end ran out of time unfortunately. I kept the mp4 file to keep the tv interactive because it was my favorite part of the project.

### Conclusion
In conclusion, I would say that I have learned a great bit about creating a VR environment from this project. The project was very challenging and required a lot of research as well as trial and error. I spent approximately 48 hours working to complete this project but feel like there was so much more functionality to add to it. I would have like to add multiple floors to my scene but ran out of time to try to implement that functionality. I think I will probably come back to this project and try to extend it and challenge myself further in the future.

### Objects and Interactions
26 Unique Models

Anvil - Blender Object Created by Trevor Pike
Mug - Blender Object Created by Trevor Pike
Dining Chairs - Blender Object Created by Trevor Pike
Dining Table - Blender Object Created by Trevor Pike
Front/Bedroom/ComputerRoom Door - https://sketchfab.com/models/720c98140848429c985fbd7c77eac70e
Couch - https://sketchfab.com/3d-models/leather-couch-b9c6af846a784919b7f2afcc023680ba
Desk - https://sketchfab.com/models/c66184828633438b94aabbbf9249e9ad
Computer - https://sketchfab.com/3d-models/personal-computer-aa398650fe6e4baa8771c71266d842f4
Mouse - https://sketchfab.com/3d-models/low-poly-steel-series-data-mouse-316a0da5fb1b49af92a51a6baf719098
Computer Chair - https://sketchfab.com/3d-models/gaming-chair-free-download-bcb13eb7ef9e4c3c9499aacff6c79757
Cabnets - https://sketchfab.com/3d-models/kitchen-cabinet-1-6ad39b0f52ad439ea12cbfdc1a1dd37f
Fridge - https://sketchfab.com/models/2fdaa56bbd85404cb4206dcaedc16658
Chandeller - https://sketchfab.com/3d-models/787102-montare-osgona-chandelier-9cb5d13365904384a835e438e6cfebfc
Entertainment Center - https://sketchfab.com/3d-models/70s-entertainment-center-9f66d53abae348a68956b6e11467600a
Bookshelf - https://sketchfab.com/models/efe2a35b92c443519fab5a5b515e92ab
Totoro - https://sketchfab.com/3d-models/totoros-cb8e95b3cbc041cf967360432512a986
Megumin - https://sketchfab.com/models/52a807d5f3184b0fa0a2c261258a495e
One Punch - https://sketchfab.com/3d-models/saitama-one-punch-man-revised-5933d345ad9441d499c93eb655a9b214
Guts - https://sketchfab.com/models/e4f0ed99c3e4486384b0f9abebd1699b
Bed - https://sketchfab.com/3d-models/bed-679c0f112f894623917b0599e9bb9d17
Dresser - https://sketchfab.com/3d-models/dresser-5fa40fc585f445c6b6fa028bd7c437a8
Crib - https://sketchfab.com/3d-models/wooden-baby-crib-c05d9d2c510d4ddfa98bd25f08358211
Bedroom Lamps - https://sketchfab.com/models/26f82e7ee59c444b9433a2458dc9451f
Hallway Light - https://sketchfab.com/3d-models/wall-light01-813a31583a2d47d7b7695338c457ab38
Outside Light - https://sketchfab.com/models/5ca3b4bdb3344824babb59ce9787573b





