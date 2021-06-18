# Angular Notes

### References

1. [Express JS Website](https://expressjs.com/)

---

### Topics Covered

1. Important Commands
2. How Angular Gets Loaded
3. Understanding Data Binding

### Important Commands

```
ng new [app name] -- no strict
```

```
ng serve
```

### How Angular Gets Loaded

1. index.html served by the server
2. `<app-root>Loading...<app-root>`
3. app.component.ts has `selector: 'app-root'`
4. app.component.html
5. NG will create scripts that are inject by the CLI automatically
6. NG will build and inject those script files to index.html

### Creating a new Component

Components: You build your whole applicaiton by building components

Module: Gives information to angular about components and features the app has

1. Create a folder for the component
2. Name the folder after the name of the component
3. Create `[component name here].component.ts` ts file
4. `export class [component name here]Component{}`
5. Add `@Component()` decorator (needs to be imported)
6. Add `selector: 'app-server'`
7. Create the component HTML file
8. Example: `[component name here].component.html`
9. Add `templateURL: './server.component.html'`
10. Add `[component name]` to app.module.ts declarations array
11. Add `import { [component name] } from './[cn]/[cn].component';`
12. Add the component to app.component.html
13. `<app-[component name]></app-server>`

### Understanding Data Binding

_Databinding = Communication_

**Output Data - >**

String Interpolation { `{{data}}` }

Property Binding ( `[property] = "data"` )

**< - React to (User) Events**

Event Binding ( `(event) = "expression"` )

**Two-Way-Binding**

Combination of Both: Two-Way-Binding ( `[(ngModel)]="data"`)
