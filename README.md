# Check Box List
Angular 2 checkbox list component
## Getting Started
```bash
npm install ng2-checkboxlist --save
```
## Simple Use
import
```javascript
import { CheckBoxList } from 'ng2-checkboxlist/checkboxlist.js';
@NgModule({
  declarations: [
    CheckBoxList
  ],
```
insert selector
```html
<checkbox-list 
               [title]="'title of checkbox'"
               [list]="itemlist" 
               [id] ="'id selector'"
               [value] = "'text selector'"
               (listSelected) = "method to manage checkd items($event)"
               ></checkbox-list>
```
## Styling

## Documentation

## Built With
Typescript

Stylus
## Author

[Luigi Senzamici](http://luigisenzamici.com)


## License

This project is licensed under the MIT License 



