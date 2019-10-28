# StencilJS

## Commands

`npm run generate`
`npm run generate pages/page-home`


## Todo:
Read https://stenciljs.com/docs/faq
https://codethat.today/tutorial/creating-components-with-stenciljs/

## Notes

### Step 1: Metadata
`@Component()` - metadata about Component

### Step2 : JS class
`export class MyComponent` - functions and logic, standard JS class

`@Prop()` :
  - automatically watched for changes
  - tells the compiler that the property is public to the component (and the user should be setting it)

### Step 3: render fn that returns JSX

### Step 4: Include component in markup
Once compiled, can be used like an HTML tag

`<my-first-component name="Max"></my-first-component>`
```
import { Component, Prop, h } from '@stencil/core';

@Component({
  tag: 'my-first-component',
})
export class MyComponent {

  // Indicate that name should be a public property on the component
  @Prop() name: string;

  render() {
    return (
      <p>
        My name is {this.name}
      </p>
    );
  }
}
```
### Props
- add mutable property to allow property to be changed inside the component

### States
@State - used to manage internal data for a component
```
@State() isActive = false
updateStatement() {
 this.isActive = !this.isActive
}
```
State should only be used if the component needs to re-render when the data is changed. If that’s not the case it’s a good practice to avoid the @State declarator and use normal internal states instead.
```
internalState: boolean = true
```

