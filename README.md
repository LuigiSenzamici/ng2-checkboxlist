# Check Box List
Angular 2 checkbox list component
## Getting Started
```bash
npm install ng2-checkboxlist --save
```
##checking before using
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
![Executing](http://LuigiSenzamici.com/Content/Image/Common/checkboxlist-scr.PNG)
![data reading](http://LuigiSenzamici.com/Content/Image/Common/checkboxlist-result.PNG)

## Built With
Typescript

Stylus
## Author

[Luigi Senzamici](http://luigisenzamici.com)


## License

This project is licensed under the MIT License 



