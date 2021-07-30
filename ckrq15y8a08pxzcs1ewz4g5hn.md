## Introducing Tomorrow - A New Look for Your Code Editor


### Introduction 
Visual Studio Code is by far one of the most popular code editors for web, mobile, and hardware developers. More than 2,600,000 people use VS Code every month, up by over 160% in the last year. 

A week ago I have created my own theme ( [ **Tomorrow**](https://marketplace.visualstudio.com/items?itemName=suhailkakar.tomorrow)  ), This theme was inspired by One Dark Pro and Material Theme. 

![Screenshot_2021-07-20_16-01-11.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1627628589779/0kjhAU7RI.png)


### Installation 

1.  Open  **Extensions** sidebar panel in VS Code.  `View → Extensions`
2.  Search for  `Tomorrow`  - find the one by  **Suhail Kakar**
3.  Click  **Install**  to install it.
4.  Code > Preferences > Color Theme >  **Tomorrow**

### Recommended Settings

If you want to give the same look as the above picture for your Code Editor you need to paste the below code into your VS Code Settings JSON


```json
{
  "editor.fontSize": 17,
  "editor.fontWeight": "500",
  "editor.fontLigatures": true,
  "editor.lineHeight": 35,
  "editor.tabSize": 2,
  "editor.lineNumbers": "off",
  "editor.renderIndentGuides": false,
  "editor.renderWhitespace": "none",
  "editor.renderControlCharacters": false,
  "editor.minimap.enabled": false,
  "workbench.colorTheme": "Tomorrow Theme",
  "tabnine.experimentalAutoImports": true,

  "editor.smoothScrolling": true,
  "editor.mouseWheelScrollSensitivity": 2,
  "editor.scrollBeyondLastLine": true,
  "editor.cursorStyle": "block",
  "editor.cursorBlinking": "phase",
  "editor.cursorSmoothCaretAnimation": true,
  "editor.cursorWidth": 2,

  "explorer.openEditors.visible": 0,
  "explorer.confirmDelete": false,
  "explorer.decorations.badges": false,
  "problems.decorations.enabled": false,
  "workbench.sideBar.location": "left",

  "window.zoomLevel": 1,
  "window.menuBarVisibility": "toggle",
  "workbench.statusBar.visible": true,
  "workbench.activityBar.visible": true,

  "terminal.integrated.cursorStyle": "block",
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.fontWeight": "500",
  "code-runner.runInTerminal": true,

  "editor.formatOnSave": true,
  "workbench.startupEditor": "none",
  "editor.detectIndentation": true,
  "editor.insertSpaces": false,
  "terminal.integrated.rendererType": "dom",
  "window.compositionAttribute": "acrylic",
  "editor.fontFamily": "'Cascadia Code', 'monospace', monospace, 'Droid Sans Fallback'",
  
}
```

### Font

**Cascadia Code** font is recommended, This font was created by Microsoft and available publicly on GitHub. You can download the font  [here](https://github.com/microsoft/cascadia-code/releases) 

### Conclusion 

If you like this theme, be sure to give it a start ⭐ on  [Github](https://github.com/suhailkakar/Tomorrow-Theme). I hope you found this article helpful. If you need any help please let me know in the comment section

Let's connect on  [Twitter](https://twitter.com/suhailkakar)  and  [LinkedIn](https://www.linkedin.com/in/suhailkakar/)  

👋 Thanks for reading, See you next time


