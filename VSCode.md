https://code.visualstudio.com/api/

### Workbench color customization

Change title bar to different colors to help visually differentiate projects. Read more documentation [here](https://code.visualstudio.com/docs/getstarted/settings).

1. On macOS - Code > Preferences > Settings
2. Go to Workbench > Appearance > Color Customization > Edit in settings.json
3. Add this code
```
{
  "workbench.colorCustomizations": {
    "titleBar.activeBackground": "#ffc907"
  }
}
```
4. Change the hex color
