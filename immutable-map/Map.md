**Map()**

```
const data = {
  'todo 1': {
    title: 'todo 1',
    value: 'first todo'
  },
  'todo 2': {
    title: 'todo 2',
    value: 'second todo'
  },
  'todo 3': {
    title: 'todo 3',
    value: 'third todo'
  }
};

var todo = {
  title: 'todo 4',
  value: 'four todo'
};

var map = Immutable.Map(data);
// new data to Map
map = map.set('todo 4', todo);
// update data in map
map = map.update('todo 4', function(todo) {
  return {
    title: 'todo 5',
    value: 'four todo'
  }
});
// delete data in map
map = map.delete('todo 3');

// isMap()
console.log(Immutable.Map.isMap(map));

console.log(map.toJS());
```
