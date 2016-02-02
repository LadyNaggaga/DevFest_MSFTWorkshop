# DevFest_MSFTWorkshop

DevFest 2016 Microsoft IoT Workshop. Requirements :  Hardware  Sparkfun Weather Shield + Particle Photon, [Visual Studio Code](https://code.visualstudio.com/Download) (free, opensource and available on Mac, Linux, and Windows),  Microsoft Azure account(ACTIVATE YOUR AZURE ACCOUNT USING [DREAMSPARK](https://www.dreamspark.com/Product/Product.aspx?productid=99)), [Node](https://nodejs.org/en/), and [Project Oxford API](https://www.projectoxford.ai/). 

## Project description 

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

##[Create a Node.js web app in Azure App Service](https://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-develop-deploy-mac/)
###Create a web app in Azure App Service by using the Azure Portal
In this section you will learn how to create a web app and enable git publishing 

1. Sign in to the Azure Portal.
2. Click the + NEW icon on the top left of the Azure Portal.
3. Click Web + Mobile, and then click Web app.
  ![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp1.png)
4. Enter a name for the web app in the Web app box.This name must be unique in the azurewebsites.net domain 
5. Select a Subscription (this will be DreamSpark).
6. Select a Resource Group or create a new one.
7. Select an App Service plan/Location or create a new one.

8. Click create

 ![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp2.png)
9. Click Web apps > {your new web app}.
10. In the Web app blade, click the Deployment part.
 ![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp10.png)
11. In the Continuous Deployment blade, click Choose Source
12. Click Local Git Repository, and then click OK.
![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp11.png)
13. Set up deployment credentials if you haven't already done so.In the Web app blade, click Settings > Deployment credential 
![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp13a.png)
Then  add a password 
![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp13b.png)
14. In the Web app blade, click Settings, and then click Properties.To publish, you'll push to a remote Git repository. The URL for the repository is listed under GIT URL. You'll use this URL later in the tutorial.
 ![](http://marianaggaga.com/wp-content/uploads/2016/02/webapp14.png)

### Build a Node.js app
This will be covered in the workshop. 

###Deploy a Node.js application using Git repository.
Now that we have learned to build a Node.js applicaiton that takes 
1. Takes a image from your webcam 
2. Uses the Project Oxford Emotion API to sense your emotion
3. Uses the Particle Photon to blink according to the emotion idenfied 
Let's go a head an deploy your app to Azure 

1. Install Git / if you have go to step 2 
2. Initialize a local Git repository

   `git init`
 
3. Add files to your repo

   `git add .`
   
   `git commit -m "initial commit"`

4. Add a Git remote for pushing updates to the web app that you created in the Create a web app in Azure App Service by using the Azure Portal section

   `git remote add azure [URL for remote repository]`
 
5. Push your changes to 

   `git push azure master`

6. You will be promoted for the user name an password you created earlier Create a web app in Azure App Service by using the Azure Portal section in step 13.
7. To view your app, click the Browse button on the Web App part in the Azure portal.
![](http://marianaggaga.com/wp-content/uploads/2016/02/browse.png)

## [Getting Started with Particle Photon board](https://docs.particle.io/guide/getting-started/connect/photon/)

[How to get started with the Particle Photon board](https://docs.particle.io/guide/getting-started/start/photon/). 

 
##Additional Resources 
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

