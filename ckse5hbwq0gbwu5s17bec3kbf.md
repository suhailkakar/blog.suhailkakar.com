## Stop Using ../../../ While Importing Components, Instead Use This Method

### Introduction 📚

When you go to GitHub and see some other developers code, most of them are importing their components like this👇
```jsx
import Button from "../../../components/Buttons/Button"
```
This is called relative import. Relative import will start with either `./`,`/` or `../`.

I am not telling that this is the wrong way and even there is no issue if you import like that, but if you have a very big and complex project, relative imports will look a lot messy similar to this. 
```jsx
import Button from "../../../../../../components/Buttons/Button"
```
However, there is a very better and cleaner way to import these components. This method is called absolute import. An absolute import will look this like 👇
```jsx
import Button from "components/Buttons/Button"
```
### Adding absolute imports to React Apps (CRA) 💡
Open your project in any code editor and create a new file in your project's root directory named `jsconfig.json`. Once you created the file paste the below JSON inside of it. 
```json
{
  "compilerOptions": {
    "baseUrl": "src"
  }
}
```
This will instruct Webpack to use the `src` directory as a base one.

### Conclusion ⌛

I hope you found this short article helpful. If you need any help please let me know in the comment section. 

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time

