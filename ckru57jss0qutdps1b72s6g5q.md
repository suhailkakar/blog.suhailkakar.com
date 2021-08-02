## Integrate Twilio With Node JS - A Beginner's Guide


## Introduction

Node.js is an open-source, JavaScript runtime environment on Chrome’s V8 that lets you effortlessly develop fast and scalable web applications. It utilizes an event-driven, non-blocking I/O model that makes it lightweight, efficient, and excellent for data-intensive real-time applications that run across shared devices.

Twilio Verify is a comprehensive solution for validating end-user phone numbers, which will be used to deliver a numeric code to the Android / iOS app through text message. Our server app will sit in between our app and Verify, allowing us to verify a user's phone number once they sign up for your mobile app.

In this article, we are going to integrate Twillio SMS Verify API in Node JS. 

### Initializing Our Node JS Server 

The first step is to create our Node JS server, to do that, open your terminal and write 
```
npm init -y && npm i express
```
Now you should see a `package.json` in your project's folder, now go ahead and create a new file named `server.js`. This is the main file for our server, To get our server up and running, you need to paste the below code. 


![Node Simple App](https://cdn.hashnode.com/res/hashnode/image/upload/v1627811003907/_hsfwCMBk.png)

The above code is a simple node and express app. Now in your terminal run 
```
node server.js
```
Open your web browser and go to localhost:5000, you should see a simple GET response, similar to the below image


![screely-1627811176034.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627811190033/_zQIy0JY7.png)

Now, we got our Node & Express server running, it is time to integrate Twilio 

### Twilio Keys

In order to make our APIs up and running with Twilio, we need 3 keys that we can get from Twilio Dashboard. Go to the Twilio console and you can find 2 keys (ACCOUNT SID, AUTH TOKEN) These keys are used as an Authentication between our app and Twilio. Copy both keys and save them in a variable. 

![screely-1627876944560.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627876950323/r7pTAGlCL.png)

The next key is your service ID, to get that go [here](https://www.twilio.com/console/verify/services) and copy your service ID, if you don't have any service you can create it by clicking on the big blue button

![screely-1627877256394.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627877265269/GQclwH1dr.png)

### Integrating Twilio with Node JS

Now we need to create two APIs

1. First we need to create an API that sends verify code to Phone Number
2. To verify the Phone number with the verification code we need to create the second API

Before starting the integration we need to install Twilio module in our Node JS app to do that simple paste the below code in your terminal
```
npm i twilio
```
and import the module in the `server.js` just like the below code.

```
const client = require("twilio")(YOUR_ACCOUNT_SID, YOUR_AUTH_TOKEN);
```

Now in your `server.js` paste the below code. This snippet is to send verification code to our phone number

![raycast-untitled (2).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627877969749/NzL90raYr.png)

The above API takes two params, phone number, and channel. In channel, you can either use SMS or call. It is simply the way which you will receive the verification code. 

Now it is time to create our second API which verifies the code. Below API take two params "phone number and code"


![raycast-untitled (3).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627878669599/Zzfvi3B-F.png)


Paste the above code too in your `server.js` and that is it. Finally, your `server.js` should look similar to the below image


![raycast-untitled (6).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627878615937/6GBUksi-R.png)

You can find the whole source code in my GitHub repo  [here](https://github.com/suhailkakar/Twilio-SMS-Verify-Node-JS) 

## Testing API in Postman
 
Open Postman desktop and test the APIs, for the first API pass phone number and channel as params and click on send you should see an output similar to the below image


![screely-1627880816580.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627880835982/0ri0cuYvd.png)

Now check the phone number which you have given in params, you should receive a code to verify your phone number. 

You can verify the code using the other API


## Conclusion

In this article, we have learned 

- What is Node JS
- What is Twilio
- How to initialize a Node JS app
- How to Integrate Twilio Verify API with Node JS

I hope you found this article helpful. If you need any help please let me know in comment section

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time
