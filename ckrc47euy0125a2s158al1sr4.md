## How to Deploy React JS Applications for Free on Firebase 2021

In this article , I’ll show you how to deploy react js applications for free on Firebase, First let’s understand what is Firebase

### What is Firebase

Firebase is a Backend as a Service that started as a YC11 startup and grew up into a next-generation app-development platform on Google Cloud Platform. Firebase frees developers to focus crafting fantastic user experiences. You don’t need to manage servers. You don’t need to write APIs. Firebase is your server, your API and your datastore, all written so generically that you can modify it to suit most needs. Yeah, you’ll occasionally need to use other bits of the Google Cloud for your advanced applications. Firebase can’t be everything to everybody. But it gets pretty close.

### Getting Started
Before deploying your app on Firebase, you need to have Firebase project and a React project (create-react-app)

### Build Your App for Production
Open your project folder cd your-project and build your app for production using command below 
```
npm run build / yarn build
```
The JavaScript and CSS files will be inside the build/static directory.

### Install Firebase Tools
Once you built your app then you can install Firebase tools that will allow you to deploy your React app. You can install the tools by running

```bash
npm install firebase-tools -g or yarn global add firebase-tools
```

### Login to Firebase
Make sure you’re in the root directory of your React app and run the following command to login to firebase in your terminal 
```
firebase login
```

*If you’re not logged in, you’ll be asked to enter the credentials for your google account.

### Initialise Firebase
Now that you’re logged in, you will need to initialise Firebase in your React app. You can do it by running the following command 
```
firebase init
```
You will then be prompted with a series of questions and configuration options.

Choose Hosting: Configure and deploy Firebase Hosting sites
Choose Use an existing project
Select the firebase project that you created
What do you want to use as your public directory? (public) build
Configure as a single-page app (rewrite all urls to /index.html)? No

Now it is time to deploy our app

### Deploying Our React JS App on Firebase
Run the following command to deploy your app: 

```
firebase deploy
```

*Firebase will then give you a unique URL where your deployed app is located (e.g. react-app.web.app).That’s all there is to it!



