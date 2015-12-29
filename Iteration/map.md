```
console.clear();

const data = {
  'todo 1': {
    title: 'todo 1',
    value: 'first todo',
    completed : true
  },
  'todo 2': {
    title: 'todo 2',
    value: 'second todo',
    completed : true
  },
  'todo 3': {
    title: 'todo 3',
    value: 'third todo',
    completed : false
  }
};

let todo = {
  'todo 1':{
    title : 'todo 1',
    value: 'first todo'
  }
};


let todos = Immutable.Map(data);

//has returns boolean value.
console.log(todos.has('todo 1'));

// get
console.log(todos.get('todo 1'));

// includes
console.log(todos.includes(todo));

let groupedTodos = todos.groupBy((todo) => todo.completed);
console.log(groupedTodos.toJS());
```
