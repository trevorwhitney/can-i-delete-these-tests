```javascript
describe('changing the field value', () => {
    beforeEach(() => {
        //...init component
        //...simulate change of foo-field to value 'foobar'
    })
    it('calls saveField with component and field name and current value', () => {
        expect(saveFieldSpy).toHaveBeenCalledWith(
            'FooComponent', 'foo-field', 'foobar'
        )
    })
    //...
```
