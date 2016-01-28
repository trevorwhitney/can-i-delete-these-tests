```
//...
it('calls the validator with the current value', () => {
  expect(validatorSpy) .toHaveBeenCalledWith('foobar')
})
it('calls validateField with component and field name and validation obj', () => {
  validatorSpy.and.returnValue({dummy: 'obj'})
  expect(validateFieldSpy).toHaveBeenCalledWith(
    'FooComponent', 'foo-field', {dummy: 'obj'}
  )
  })
})
```

Note: These are developer tests that are testing the boundaries of this React component, that it sends the proper messages in response to certain inputs. All of this plumbing is caught through acceptance tests.