## How To Install Node.js and NPM on Ubuntu


### Introduction
Node.js is an open-source, JavaScript runtime environment on Chrome’s V8 that lets you effortlessly develop fast and scalable web applications. It utilises an event-driven, non-blocking I/O model that makes it lightweight, efficient and excellent for data-intensive real-time applications that run across shared devices.

### Installation

The easiest way to install Node.js and npm on Ubuntu is using Ubuntu repository, To install the Node.js and npm from the Ubuntu repository open terminal (Ctrl + Alt + T) and run the following commands 

```sh
$ sudo apt update
```
```sh
$ sudo apt install nodejs npm
```

The above command will install a number of packages in order to compile and install native addons from npm.

Once it is done verify the installation by running :
```sh
$ nodejs --version && npm --version
```
```sh
v12.21.0
7.5.2
```

In output you should see the Node.js and NPM version respectively. 

> At the time of writing, the Node.js version and NPM version included in the Ubuntu repositories is 12.21.0 and 7.5.2 respectively 

### Uninstall Node.js

Sometimes, you may want uninstall Node.js. You can do that simply by running the below commands on your terminal. 
```sh
$ sudo apt-get remove nodejs npm
```
```sh
$ sudo apt update
```

### Conclusion
That is it, In this article we learned,

* What is Node.js
* How to install Node.js using Ubuntu repository
* How to install NPM using Ubuntu repository
* How to uninstall Node.js.

I hope you found this articles helpful. If you need any help please let me know at comment section

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time

