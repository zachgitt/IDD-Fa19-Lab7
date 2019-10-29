# Video Doorbell, Lab 7

*A lab report by Zachary Gittelman*

### In This Report

1. Upload a video of your version of the camera lab to your lab Github repository
1. As usual, update your class Hub repository to add your [forked IDD-Fa18-Lab7](/FAR-Lab/IDD-Fa18-Lab7) repository.
1. Answer the questions in-line below on your README.md.

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**
[![Thumb](https://github.com/zachgitt/IDD-Fa19-Lab7/blob/master/thumb.png)](https://youtu.be/kX_qeujrImk)


## Part B. Web Camera
**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)** <br>
After using diff and comparing the two files, I found that to enable the webcam, a data structure of options are defined and used to create a Webcam object. Additionally, when the socket hears the 'takePicture' event it creates an image and saves it and sends it to the browser.

**b. Include a video of your working video doorbell**
The only code edited was in public/client.js where the following line was added in the case 'light'. <br>
`socket.emit('takePicture')`
[![Thumb](https://github.com/zachgitt/IDD-Fa19-Lab7/blob/master/web_thumb.png)](https://youtu.be/59-ZnLk0sHs)


## Part C. Make it your own

**a. Find, install, and try out a node-based library and try to incorporate into your lab. Document your successes and failures (totally okay!) for your writeup. This will help others in class figure out cool new tools and capabilities.**

**b. Upload a video of your working modified project**
