### How to add CSS in react component

```
const styles = {
    dayPickerInput: {
        padding:'10px',
        borderWidth:'0 0 1px 0',
        borderBottomColor:'#e0e0e0',
        outline: 'none'
    },
    enddateLabel:{
        paddingRight:'7px'
    }
};

<label style={styles.enddateLabel}>End Date </label>

````
### Stateless Functional Component:
```

const Comments = props => {
    return (
        <div></div>
    );
}
```
### Component which just has a render method:

```
class Comments extends Component {
    render() {
        return (
            <div></div>
        );
    }
}
```

### componentDidMount()

componentDidMount() is invoked immediately after a component is mounted (inserted into the tree). Initialization that requires DOM nodes should go here. If you need to load data from a remote endpoint, this is a good place to instantiate the network request.
