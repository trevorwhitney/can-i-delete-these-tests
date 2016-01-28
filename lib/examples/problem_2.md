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

Note: We came to this through unit tests and acceptance tests. Then changed it everywhere else, and used acceptance tests to confirm it worked.