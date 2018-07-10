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
