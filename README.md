# DevFest_MSFTWorkshop

DevFest 2016 Microsoft IoT Workshop. Requirements :  Hardware  Sparkfun Weather Shield + Particle Photon, [Visual Studio Code](https://code.visualstudio.com/Download) (free, opensource and available on Mac, Linux, and Windows),  Microsoft Azure account(ACTIVATE YOUR AZURE ACCOUNT USING [DREAMSPARK](https://www.dreamspark.com/Product/Product.aspx?productid=99)), [Node](https://nodejs.org/en/), and [Project Oxford API](https://www.projectoxford.ai/). 

## Project description 

We will be  using the  Particle Photon and Microsoft Project Oxford Emotion API to detect your emotions.  Before you come to the workshop please make sure to sign up for a free Azure account  using DreamSpark (instructions below), and  Microsoft account so you can access the Project Oxford API. 

##Step 1 Get your Azure Account 

### Activate your FREE Azure Account with DreamSpark 
[![Alt text for your video](http://www.gmlpu.org.uk/wp-content/uploads/2014/10/freestuff.jpg)](https://channel9.msdn.com/Series/Free-Cloud-for-Students/Activating-a-Free-Azure-DreamSpark-Subscription)

Click image to  play video.In this two minute learn how to activate your free Azure account with DreamSpark. 

## Step 2 Sign up for  Project Oxford Emotion API
####What is Project Oxford API?
Project Oxford is a suite of AI APIs from Microsoft and includes APIs around  Vision APIs, Speech APIs, and Language APIs.In this workshop we will be looking at the emotions APIs. 

Emotions APIs detect emotions based on facial expressions.The Emotion API takes an image as an input, and returns the confidence across a set of emotions for each face in the image, as well as bounding box for the face, using the Face API.The emotions detected are anger, contempt, disgust, fear, happiness, neutral, sadness, and surprise. 

![](http://marianaggaga.com/wp-content/uploads/2016/02/emotionapi.png)

1. Go to [Project Oxford site](https://www.projectoxford.ai/)
2. Click get free trial 
![](http://marianaggaga.com/wp-content/uploads/2016/02/start-trial-1.png)
3. Signing with your Microsoft account. 
![](http://marianaggaga.com/wp-content/uploads/2016/02/Microsoftaccount2.png)
4. Show your Emotion API key 
![](http://marianaggaga.com/wp-content/uploads/2016/02/getapikey.png)
5. Copy and paste your key into a notepad for now. 

## Step 3  Fork this repo
![](http://marianaggaga.com/wp-content/uploads/2016/02/githubrepofork.png)


## Step 4 [Create a  web app with Azure App Service](https://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-develop-deploy-mac/)
Before we build our first Node.js app fork this repo.

###Create a web app in Azure App Service using the Azure Portal

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
11. In the Continuous Deployment -> Click Configure Settings-> click Github
12. Click Github, and then click OK. GitHub will  ask if you want to authorize Azure to have access to your accounts. It's safe to click Authorize application.
13. Select DevFest_MSFTWorkshop GitHub repository from the list and make sure you are deploying the master branch. Click OK 
 ![](https://cloud.githubusercontent.com/assets/3477155/9880464/bea7f6e4-5b99-11e5-9601-f7a6767e32ba.gif)


## Step 5 [Setting up Particle Photon board](https://docs.particle.io/guide/getting-started/connect/photon/)

[How to get started with the Particle Photon board](https://docs.particle.io/guide/getting-started/start/photon/). 

### Prerequisites for Setup
Software Particle Mobile App - [iPhone](https://itunes.apple.com/us/app/particle-build-photon-electron/id991459054?ls=1&mt=8) | [Android](https://play.google.com/store/apps/details?id=io.particle.android.app)

1. Your Particle device, brand new and out of the box!

2. USB to micro USB cable (included with Photon Kit and Maker Kit)

3. Power source for USB cable (such as your computer, USB battery, or power brick)

4. Your [iPhone](https://itunes.apple.com/us/app/particle-build-photon-electron/id991459054?mt=8) or [Android](https://play.google.com/store/apps/details?id=io.particle.android.app)download the particle app.

### Setting up your Particle Photon
1. Go to [spark.io/start](https://docs.particle.io/guide/getting-started)
2. Select Photon 
3. Get a [particle account](https://build.particle.io/login) if you don't have one 
4. Connect your Photon to your acccount.You will do this with your iOS or android app.
5. On the packaging that your Photon Kit came in you'll see a barcode like the one below. Take note of the four digits in the thrid alphanumeric sequence. ![image here]
6.  Go to phone wifi setup and select your Photon-C***
7.  Continue to the Particle app and follow the instructions to get your Photon online.
#### Programming the particle Photon
8.  Go to [online IDE](https://build.particle.io)  and sign in with your particle username and password

[screen shots coming soon]

Get your Device ID  and Access token from your will need for the next section 
- Copy your device ID from the web IDE by clicking on Devices.
![](https://www.twilio.com/blog/wp-content/uploads/2015/10/mSbV1J9hj_Di2zw_hTQn0aJohHbHABoinC8MIS4FFC2K7BINRGIJJdBT_8V3yrnUW08Cr7QxoxiqEtfR1m0w4IYlXoE6W9_2elTdqoxz4Xpn0qXael0DGdro4sFoy1eXzDm4nnt4.png)

place holder gif from Twilio

- Copy the access token by clicking Settings.

![](http://marianaggaga.com/wp-content/uploads/2016/02/settings-e1454640147971.png)
## Step 6  Configure web apps in Azure App Service
Before we jump into the next portion, make sure you have your [Project Oxford Emotion API](https://github.com/LadyNaggaga/DevFest_MSFTWorkshop#step-2-sign-up-for--project-oxford-emotion-api), and your [particle device ID and access token](https://github.com/LadyNaggaga/DevFest_MSFTWorkshop#step-5-setting-up-particle-photon-board).

#### Referencing the Project Oxford API and  Photon in your  the code 
Open [routes/image.js](https://github.com/LadyNaggaga/DevFest_MSFTWorkshop/blob/master/routes/image.js) file

The code snippet below is referencing your Project Oxford API key. It is great practice to never leave your key in your code. We use the [process.env](https://nodejs.org/api/process.html#process_process_env) to c onfig variables inside a Node.js application and PO_KEY is our Project Oxford API key.




### Sign into your azure account 

Let's use our API keys. Open up your routes/image.js file 
COMING SOON 
## Deploy to Azure
[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

## Additional Resources 
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

###[Github Getting started with Node.js on Azure ](https://github.com/sayar/NodeMVA)
###[Github Project Oxford Web Cam  ](https://github.com/bitchwhocodes/project-oxford-webcam)   





