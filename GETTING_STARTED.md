Get started with Angular Material 2 using the Angular CLI.

## Install the CLI
 
 ```bash
 npm install -g angular-cli
 ```
 
## Create a new project
 
 ```bash
 ng new my-project
 ```

The new command creates a project with a build system for your Angular app.

## Install Angular Material components 

```bash
npm install --save @angular/material
```

## Import the Angular Material NgModule
  
**src/app/app.module.ts**
```ts
import { MaterialModule } from '@angular/material';
// other imports 
@NgModule({
  imports: [MaterialModule.forRoot()],
  ...
})
export class PizzaPartyAppModule { }
```

## Including core and theme styles:
This is required to apply all of the core and theme styles to your application.
See the [Theming Guide](docs/theming.md) for instructions.

**From the Theming Guide:**

> If you're using Angular CLI, this is as simple as including one line in your `style.css` file:

> `@import '~@angular/material/core/theming/prebuilt/deeppurple-amber.css';`

> Alternatively, you can just reference the file directly. This would look something like:

> `<link href="node_modules/@angular/material/core/theming/prebuilt/indigo-pink.css" rel="stylesheet">`


## Additional setup for `md-slide-toggle` and `md-slider`:
The slide-toggle and slider components have a dependency on [HammerJS](http://hammerjs.github.io/).

Add HammerJS to your application via [npm](https://www.npmjs.com/package/hammerjs), a CDN 
(such as the [Google CDN](https://developers.google.com/speed/libraries/#hammerjs)), or served 
directly from your app.

## [Optional] Using Material Design icons with `md-icon`:

- If you want to use Material Design icons in addition to Angular Material components, 
load the Material Design font in your `index.html`.  
`md-icon` supports any font icons or svg icons, so this is only one option for an icon source.
       
**src/index.html**
```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```

## Sample Angular Material 2 projects
- [Material 2 Sample App](https://github.com/jelbourn/material2-app)
- [Angular Connect 2016 Demo](https://github.com/kara/leashed-in)
