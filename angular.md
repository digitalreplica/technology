# Angular
Angular is a front-end, web UI framework written in Javascript. It originally started as angular.js, but the current version is just called Angular.

Caveat: definately an angular newbie

[Docs](https://angular.io/docs)

## Reading local json file in Angular 12
This is far more complicated than it should be.

Add to tsconfig.json
```
{
  "compilerOptions": {
    "resolveJsonModule" : true,
    "esModuleInterop": true
  },
}
```

Create a service to hold your data. In the my.service.ts, add outside the class
```
import MyData from './mydata.json';
let my_list: string[] = MyData.somelist
```

Then create a function inside the class to retrieve the data
```
  getList() {
    return my_list;
  }
```

# Angular Material
UI components for Angular.
* [Angular Material UI component library](https://material.angular.io/)
* [Material Icons](https://fonts.google.com/icons?selected=Material+Icons)
