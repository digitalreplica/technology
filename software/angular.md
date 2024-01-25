---
is: "[[software]]"
---
# Notes
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

# Hosting Angular app on GitHub Pages
* https://www.npmjs.com/package/angular-cli-ghpages
* [GitHub - angular-schule/angular-cli-ghpages: 🚀 Deploy your 🅰️Angular app to GitHub pages directly from the Angular CLI! Available on NPM.](https://github.com/angular-schule/angular-cli-ghpages/#readme)
* https://medium.com/rupesh-tiwari/how-to-deploy-angular-apps-to-github-pages-gh-pages-setup-ci-cd-for-angular-app-with-github-714c1e555de5
* [Deploy to Github Pages like a pro with Github Actions - DEV Community](https://dev.to/rolanddoda/deploy-to-github-pages-like-a-pro-with-github-actions-4hdg) more elemental install that doesn't require 3rd party library
