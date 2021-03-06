# Check Box List
Angular 2 checkbox list component with theming, no dependencys and customizable styles
## Getting Started
```bash
npm install ng2-checkboxlist --save
```
## Checking before using
this component assume that run under Angular2 application, so has this implicit dependency:
```javascript
    "@angular/common": "^4.4.0-RC.0",
    "@angular/core": "4.4.0-RC.0",
    "rxjs": "5.4.3"
```
## Simple Use
import
```javascript
//app.module.ts file
....
import { CheckBoxList } from 'ng2-checkboxlist/checkboxlist.js';
@NgModule({
  declarations: [
    AppComponent,
    CheckBoxList
  ],
  ....

//app.component.ts file
 export class AppComponent {
  title = 'app';
  listItemToPass:any[] = [
    {id:1, text:"one"}, 
    {id:2, text:"two"}, 
    {id:3, text:"three"},
    {id:4, text:"four"}
  ];
  checkboxStyles:string[] = ["container:greenClass, shadow", "title:whiteClass"];
  itemSelectedManager(event){
    console.log("selected items list -> ", event);
  }
}

```
insert selector
```html
<!-- app.component.html file -->
<checkbox-list 
               [title]="'choose a number'"
               [list]="listItemToPass" 
               [id] ="'id'"
               [value] = "'text'"
               [styles] = "checkboxStyles"
               (listSelected) = "itemSelectedManager($event)"
               ></checkbox-list>
```
## Styling
you can style by applying class to container, title, input and label passing a string or an array of string to [styles] input property.
String format is: "<container|title|input|label>:<classname1>, <classname2>, ..., <classnameN>"
Array format simply is an array of these strings.
in code sample 'checkboxStyles' is so declared:
```javascript
    checkboxStyles:string[] = ["container:greenClass, shadow", "title:whiteClass"];
```

## Screenshots
### example of how it is rendered
![Executing](http://LuigiSenzamici.com/Content/Images/Common/checkboxlist/checkboxlist-scr.PNG)

### example of reading listSelected property
![data reading](http://LuigiSenzamici.com/Content/Images/Common/checkboxlist/checkboxlist-result.PNG)

## Theming
it's also possible set a theme [dark or light] using input property theme:
```html
<!-- app.component.html file -->
<checkbox-list 
               [title]="'choose a number'"
               [list]="listItemToPass" 
               [id] ="'id'"
               [value] = "'text'"
               [theme] = "'dark'" 
               (listSelected) = "itemSelectedManager($event)"
               ></checkbox-list>
```
For using css file theme you have to set styles property in .angular-cli.json like so:
```javascript
      "styles": [
        "styles.css",
        "../node_modules/ng2-checkboxlist/theme/checkboxlist.dark.css",
        "../node_modules/ng2-checkboxlist/theme/checkboxlist.light.css"
      ],
```
[IMPORTANT] if you are under ng serve command you have to stop and repeat command (.angular-cli.json isn't watch by angular compiler)

### Dark Theme screeshoot
![Dark Theme screeshoot](http://LuigiSenzamici.com/Content/Images/Common/checkboxlist/checkboxlist-dark-theme.PNG)

### Light Theme screenshoot
![Light Theme screenshoot](http://LuigiSenzamici.com/Content/Images/Common/checkboxlist/checkboxlist-light-theme.PNG)

## Built With
Typescript

Stylus
## Author

[Luigi Senzamici](http://luigisenzamici.com)
### luigisenzamici@gmail.com

## License

This project is licensed under the MIT License 



