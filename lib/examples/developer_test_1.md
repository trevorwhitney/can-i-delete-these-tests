A common pattern in Flux apps

```javascript
class TodoItem extends Component {
  componentDidMount() {
    TodoStore.addChangeListener(this._onChange);
  }

  componentWillUnmount() {
    TodoStore.removeChangeListener(this._onChange);
  }
}
```

Note: good for design, but you need to do this everywhere or your app won't work