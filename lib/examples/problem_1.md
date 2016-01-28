```javascript
function handleFieldChange(event) {
  const {dispatch} = this.props
  const value = event.target.value
  const componentName = this.constructor.name
  const fieldName = 'fieldName'

  dispatch(actions.saveField(componentName, fieldName, value))
  const validator = this.getValidator(componentName, fieldName)
  dispatch(actions.validateField(
    componentName, fieldName, validator(value)
  ))
}
```

Note: This code, needed to become...