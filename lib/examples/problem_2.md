```javascript
function handleFieldChange(event) {
  const {dispatch} = this.props
  const value = event.target.value
  const componentName = this.constructor.name
  const fieldName = 'fieldName'

  dispatch(
    actions.saveAndValidate(componentName, fieldName, value)
  )
}
```

Note: Find and replace would not work because of different implementations, a larger issue, but not going to discuss here. Correct pattern was designed out using the acceptance tests that were already there.