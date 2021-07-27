## Find Social Media Accounts in 5 Minutes with Sherlock

### Disclaimer
Don't do this to anyone with ill intent, this is a legit hacking tool part of the hacking process called osens, where we gather information about our hacking targets. What we're doing is not technically illegal we're just gathering publicly available information on the internet but the lines can blur based on your intentions so just be careful use this as a learning tool.

### Introduction 

Sherlock is a powerful command line tool supplied by the Sherlock Project that may be used to locate usernames across a variety of social media platforms. It is a python open-source project available at GitHub. You just need to input the username and Sherlock will return all the social media account url of that username

### Requirement

This best thing about this project is that you don't need any extra thing, You just need a web browser

### How To Use ?


- Open this  [link](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/sherlock-project/sherlock&tutorial=README.md)  in your browser. This will open Google Cloud Console which we can use its shell to install Sherlock

- Make sure to check the Trust checkbox and click on Confirm and wait for 10 seconds 

![screely-1627356052231.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627356069411/sx6yI9aqt.png)

- Once everything is done, go a head and paste the below code in the Cloud Shell 
```bash
python3 -m pip install -r requirements.txt
```
- If all the packages are installed successfully, you should see something similar to below picture


![image (1).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627356959209/be5HQdOdb.png)

- Now we can start using Sherlock, you just need to a username to get the social media account. In the Cloud Shell paste the below code and click enter ( change username with the account you want to get information, In my case suhailkakar) and will get all the social media profile of the username
```bash
python3 sherlock --timeout 1 username
```
![Sherlock](https://cdn.hashnode.com/res/hashnode/image/upload/v1627357833292/qgItNii3M.gif)

### Conclusion

I hope you found this articles helpful. If you need any help please let me know at comment section

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time
