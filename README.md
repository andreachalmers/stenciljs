# StencilJS

## Commands

`npm run generate`
`npm run generate pages/page-home`


## Todo:
Read https://stenciljs.com/docs/faq

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
