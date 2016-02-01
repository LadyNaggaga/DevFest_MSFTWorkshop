# DevFest_MSFTWorkshop

DevFest 2016 Microsoft IoT Workshop. Requirements :  Hardware  Sparkfun Weather Shield + Particle Photon, [Visual Studio Code](https://code.visualstudio.com/Download) (free, opensource and available on Mac, Linux, and Windows),  Microsoft Azure account(ACTIVATE YOUR AZURE ACCOUNT USING [DREAMSPARK](https://www.dreamspark.com/Product/Product.aspx?productid=99)), [Node](https://nodejs.org/en/), and [Project Oxford API](https://www.projectoxford.ai/). 

## Project description 
### Emotional Hardware
We will be  using the  Particle Photon and Microsoft Project Oxford Emotion API to detect your emotions. Are you anger, contempt, disgust, fear, happiness, neutral, sadness, or surprise?  Before you come to the workshop please make sure to sign up for a free Azure account  using DreamSpark (instructions below), and  Microsoft account so you can access the Project Oxford API. 

##Get your Azure Account 

### Activate your FREE Azure Account with DreamSpark 
[![Alt text for your video](http://www.gmlpu.org.uk/wp-content/uploads/2014/10/freestuff.jpg)](https://channel9.msdn.com/Series/Free-Cloud-for-Students/Activating-a-Free-Azure-DreamSpark-Subscription)

Click image to  play video.In this two minute learn how to activate your free Azure account with DreamSpark. 

### Use a FREE Azure Pass 
1. Go to [Azure Passes](http://www.microsoftazurepass.com/)
2. Follow instructions in the video below. Click on image to play video
[![Alt text for your video](http://www.qssolutions.nl/wp-content/uploads/2015/07/Microsoft-Azure.jpg)](https://channel9.msdn.com/Blogs/joeraio/Activating-Microsoft-Azure-Subscription-Using-Azure-Pass)

###Project Oxford API 
Project Oxford is a suite of AI APIs from Microsoft and includes APIs around  Vision APIs, Speech APIs, and Language APIs.In this workshop we will be looking at the emotions APIs. 

Emotions APIs detect emotions based on facial expressions.The Emotion API takes an image as an input, and returns the confidence across a set of emotions for each face in the image, as well as bounding box for the face, using the Face API.The emotions detected are anger, contempt, disgust, fear, happiness, neutral, sadness, and surprise. 

####Signing up for Emotion API (Are you happy/ Sad or surprised)

![](http://marianaggaga.com/wp-content/uploads/2016/02/emotionapi.png)

1. Go to [Project Oxford site](https://www.projectoxford.ai/)
2. Click get free trial 
![](http://marianaggaga.com/wp-content/uploads/2016/02/start-trial-1.png)
3. Signing with your Microsoft account. 
![](http://marianaggaga.com/wp-content/uploads/2016/02/Microsoftaccount2.png)
4. Show your Emotion API key 
![](http://marianaggaga.com/wp-content/uploads/2016/02/getapikey.png)
5. Copy and paste your key into a notepad for now. 

####Getting started with Project Oxford API and Node.js 

Adding images from a URL 

`var oxfordEemotion = require("node-oxford-emotion")( api-key)`

 ` var emotion = oxfordEmotion.recognize("url", image-url, function(cb)`
 
  `{`
  
   ` console.log(cb);`
    
  `});`

Adding images from your machine 

`var oxfordEemotion = require("node-oxford-emotion")(api-key)`

 `var emotion = oxfordEmotion.recognize("image", imageData, function(cb) {`
  
   ` console.log(cb);`
    
  `}); `

### [Node.js](https://nodejs.org/en/),[Socket.IO](http://socket.io/) & [Azure](https://www.dreamspark.com/Product/Product.aspx?productid=99)
####Video Resources 
Watch [Stacey Mulcahy]( https://twitter.com/bitchwhocodes) and [Rami Sayar]( https://twitter.com/ramisayar) in this incredibly interesting and entertaining intro to Node.js. 
#####In this video you will learn:
1. [Intro to Node.js ]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=CePazYKz_5504984382)
2. [Intro to Express](https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=hPPfQZKz_4404984382)
3. [Building a Backend]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=cyMHmZKz_4304984382) 
    [What are web Socket?]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=cyMHmZKz_4304984382)
  [NoSQL Database with MongoDB]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=cyMHmZKz_4304984382)
4. [Creating UI]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=jJXdHaKz_5804984382)
5. [Connecting the UI to the Backend ]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=1nDCeaKz_504984382)
6. [Deploying your app to Azure ]( https://mva.microsoft.com/en-US/training-courses/building-apps-with-nodejs-jump-start-8422?l=xK3w2aKz_9304984382)

####Other Resources 
[Install the Azure CLI tools for Mac, Windows, and Linux](http://blogs.msdn.com/b/cdndevs/archive/2014/09/11/a-chatroom-for-all-part-2-welcome-to-express-with-node-js-and-azure.aspx)

[Create and Deploy a Node App in Azure](https://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-develop-deploy-mac/)

[Quick guide to building a Node.js Chat Application with Socket.IO on Azure ](https://azure.microsoft.com/en-us/documentation/articles/cloud-services-nodejs-chat-app-socketio/)

###[Github](https://github.com/sayar/NodeMVA) 

