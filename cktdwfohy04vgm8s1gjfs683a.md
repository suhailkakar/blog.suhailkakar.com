## Add An Advanced File Uploader To Your React.js App - Upload Care

### Overview 
In this article, we are going to integrate Upload Care ( An Advanced File Uploader ) which includes drag-and-drop image uploader, direct link image uploader and etc.. in our react.js app. 


 ### Creating a react app
The first step is to create a simple react app which you can do just by running the command below in your terminal. 

```sh
npx create-react-app upload-care
```
This might take a while and it depends on your computer specs but once it is done go to the new directory which is created ( In our case `upload-care` ) and run `npm start` or `yarn start`. This command will start the development server for your react app. Now open this directory (In our case `upload-care`) in any code editor


### Cleaning up the project
Once you opened the directory in your code editor, You can see that there are many files and folders, but for this project, we don't need most of them. Let's go ahead and delete the files which we don't need. In the `src` folder delete all files except `App.js`, `Index.js`, and `App.css`. 

Once you removed them, delete everything which is inside of `App.js` and paste the below code instead. 

```jsx
import React from 'react'

export default function App() {
  return (
    <div>
      <h1>React x UploadCare</h1>
    </div>
  )
}

```
also delete everything which is inside of `Index.js` and paste the below code instead. 
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);
```
and also delete everything inside of `App.css`. Now in the `public` folder delete everything except `index.html`. Delete everything which is inside of the `index.html` and instead paste the below code 
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>React x UploadCare</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>
```
Finally, this is how your folder structure should look like 👇
```
📦
├── package.json
├── public
│   └── index.html
├── README.md
├── src
│   ├── App.css
│   ├── App.js
│   └── index.js
└── yarn.lock
```
### Getting an API key
Signup for an account in   [Upload Care's website](https://app.uploadcare.com/accounts/signup/) and click on API Keys from the sidebar

![screely-1631249553895.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1631249565100/h3_4zD8Ex.png)
Copy your public key as we need it in further steps.  

### Installing and Adding Upload Care
Now It is time to install Upload Care in the react application, to do that simply run

```
npm install @uploadcare/react-widget
```
Once it is installed, you need to import the package into your app.js, to do that simply add this code to the top of your app.js code 
```
import { Widget } from "@uploadcare/react-widget";
```
To use the File Uploader component, you can add the below code to your app.js or another template of your choice:

```
<p>
  <label htmlFor='file'>Your file:</label>{' '}
  <Widget publicKey='YOUR_PUBLIC_KEY' id='file' />
</p>
```
finally, this is how your `app.js` should look like.

```
import React from "react";
import { Widget } from "@uploadcare/react-widget";

export default function App() {
  return (
    <div>
      <p>
        <label htmlFor="file">Your file:</label>{" "}
        <Widget publicKey="YOUR_PUBLIC_KEY" id="file" />
      </p>
    </div>
  );
}
```

Now, paste your public key in place of `YOUR_PUBILC_KEY` in the above code. Open your browser and go to `localhost:300`. and 💥 now you have upload care integrated into your app. 
If anyone uploads a file using the upload care widget, You can view those files in your dashboard. 


![screely-1631249899662.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1631249909192/E3C-rn7kCp.png)



## Conclusion 

I hope you found this article useful, if you need any help please let me know in the comment section. 

Would you like to buy me a coffee, You can do it [here](https://www.buymeacoffee.com/suhailkakar).

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/). 

👋 Thanks for reading, See you next time