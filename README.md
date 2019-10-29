# Video Doorbell, Lab 7

*A lab report by Zachary Gittelman*

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**
[![Thumb](https://github.com/zachgitt/IDD-Fa19-Lab7/blob/master/thumb.png)](https://youtu.be/kX_qeujrImk)

## Part B. Web Camera
**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)** <br>
After using diff and comparing the two files, I found that to enable the webcam, a data structure of options are defined and used to create a Webcam object. Additionally, when the socket hears the 'takePicture' event it creates an image and saves it and sends it to the browser.

**b. Include a video of your working video doorbell** <br>
The only code edited was in public/client.js where the following line was added in the case 'light'. <br>
`socket.emit('takePicture')`
[![Thumb](https://github.com/zachgitt/IDD-Fa19-Lab7/blob/master/web_thumb.png)](https://youtu.be/59-ZnLk0sHs)


## Part C. Make it your own

**a.**
I wanted to test to see if there was a race condition between the Virtual Button on the webpage vs. the Physical Button on the breadboard. To test which was faster I created a notification depending on which button was responsible for taking the picture as shown in my video. If you zoom into the video you can see whether "Virtual Button Wins!" or "Physical Button Wins!". As seeen in the video, the physical button seems to win even when both are pressed almost simultaneously, most likely due to some latency between the client and the server.

**b. Upload a video of your working modified project** <br>
[![Thumb](https://github.com/zachgitt/IDD-Fa19-Lab7/blob/master/race.png)](https://youtu.be/ZkSpn88RAd4)

