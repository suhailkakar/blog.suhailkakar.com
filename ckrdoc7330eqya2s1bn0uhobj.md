## Turning Your Website Into A Mobile App using React Native

Every day more and more people spend their time on mobile platforms, especially when it comes to shopping and entertainment. Successful companies such as Amazon that initially launched only a website, but now they have also established their mobile presence.

There are 7,950,000,000+ mobile users around to world, and If you want to make your business successful, you should have mobile app beside your website.

React Native is a JavaScript framework for writing real, natively rendering mobile applications for iOS and Android. It’s based on React, Facebook’s JavaScript library for building user interfaces, but instead of targeting the browser, it targets mobile platforms. But in this article we are going to convert our website's web view into app 😉

![Turning Your Website Into A Mobile App using React Native](https://cdn.hashnode.com/res/hashnode/image/upload/v1626883339923/AP7SH_knP.gif)


### Step 1 : Installing Node JS

Node.js is a platform built on Chrome's JavaScript runtime for easily building fast and scalable network applications. Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient, perfect for data-intensive real-time applications that run across distributed devices.

Go to nodejs.org and download and install the the latest stable version (LTS) in your computer. "nodejs package includes both node and npm"

### Step 2 : Installing Expo

Expo is a framework and a platform for universal React applications. It is a set of tools and services built around React Native and native platforms that help you develop, build, deploy, and quickly iterate on iOS, Android, and web apps from the same JavaScript/TypeScript codebase.

The quickest way to install expo is using NPM, just open your terminal and write
```bash
npm install --global expo-cli
```

### Step 3 : Initialising our app

Open your terminal and write 
```bash 
expo init
``` 
This will generate a simple one screen app using React Native.

Once your app is create, navigate to your app folder using 
```bash
cd your-app-name
```
and run  
```bash
expo start
```
> When you run expo start (or npm start), Expo CLI starts Metro Bundler, which is an HTTP server that compiles the JavaScript code of our app using Babel and serves it to the Expo app. It also pops up Expo Dev Tools, a graphical interface for Expo CLI.

On your phone, download and install Expo Go app, after installing open it and press "Scan QR Code" on the "Projects" tab of the Expo Go app and scan the QR code you see in the terminal or in Expo Dev Tools.

### Step 3 : Converting our website to App

Open your terminal and install react-native-webview by running the command 
```bash
expo install react-native-webview
```

Once it is done, open your app's folder in any code editor such as VS code and in app.js paste the following code and save it

```javascript
import * as React from "react";
import { WebView } from "react-native-webview";

export default class App extends React.Component {
  render() {
    return (
      <WebView 
      source={{ uri: {your-website-link} }} 
      style={{ marginTop: 20 }} 
      />
    );
  }
}
```

### Step 4 : Building Android and IOS App

To build Android and IOS app your just need to write below command in your terminal

For Android : expo build:android
For IOS : expo build:ios

You can view your app in your expo dashboard at expo.io

That is it, We are done :)

I know, it is a bit confusing but, Hope you understand it. If you have any issues please let me know :)



