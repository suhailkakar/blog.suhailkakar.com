## Include HTML Inside of HTML - Just Like React Components

Yes, you can include HTML inside of HTML, just like a react / angular component. In this short article, I am going to walk you through, how to include HTML inside of HTML. 

### Creating files 
Go ahead and create a new HTML file and add the following simple code inside of it

```
<!-- index.html -->

<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Include HTML inside of HTML</title>
</head>
<body>
	
</body>
</html>
```
now create a new file and name it `nav.html` ( You can name it anything since this will be the component that we will include in `index.html`). Once created you can either write your component or paste this simple navbar code

```
<!-- nav.html -->

<!DOCTYPE html>
<html>
<body>

<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="#news">News</a></li>
  <li><a href="#contact">Contact</a></li>
  <li><a href="#about">About</a></li>
</ul>

</body>
</html>
```
### Adding package

Now we need to add an external NPM package to your index.html, to do that simply paste the following code in your `index.html` file. 

```html
<script src="https://unpkg.com/htmlincludejs"></script>
```

### Adding HTML inside of HTML

Once you added the script, paste the following `include` tag in your `index.html` file. 

```
<include src="./nav.html"></include>
```

Finally, this is how your `index.html` file should look like

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<script src="https://unpkg.com/htmlincludejs"></script>
	<title>Include HTML inside of HTML</title>
</head>
<body>
	<include src="./nav.html"></include>
</body>
 </html> 
```

Now open this index.html in your browser and BOOM 💥 you have a navbar in your webpage. Though we didn't add a navbar in your `index.html`,  we just include it from another `html` file but we still got navbar. Here is the full code in Codesandbox 

%[https://codesandbox.io/embed/floral-glitter-pdxvp?fontsize=14&hidenavigation=1&theme=dark]


### Conclusion

I hope you found this article helpful. If you need any help please let me know in the comment section. 

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time