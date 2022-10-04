<template>
    <div id="todo">
  <input v-model="newTodo" placeholder="new todo">
  <button @click="add()">add</button>
  <button @click="undo()" :disabled="!canUndo">undo</button>
  <button @click="redo()" :disabled="!canRedo">redo</button>
  <ul>
    <li v-for="(todo,i) in todos">
      <div>
        <input v-if="edited" @blur="edited = false"  v-model="todos[i].name" @change="updateData()"  />
        <p v-else  @click="edited = true">{{ todo.name }}</p>
        <button @click="del(i)">delete</button>
      </div>
    </li>
  </ul>
</div>
</template>
<script>
    const todoData = [{
        name: 'nitesh',
        phone: '01747102896',
        email: ''
    }];
    const history = [Object.assign([], todoData)]
    const historyIndex = history.length - 1
    export default {
        data () {
            return {
                newTodo: undefined,
                todos: todoData,
                history: history,
                historyIndex: historyIndex,
                edited: false,
            }
        },
        computed: {
            canUndo: function() {
            return this.historyIndex > 0
            },
            canRedo: function() {
            return this.history.length - 1 - this.historyIndex > 0
            }
        },
  methods: {
    add: function() {
      if (this.newTodo) {
        this.todos.push({name: this.newTodo})
        this.newTodo = undefined
        this.log(this.todos)
      }
    },
    updateData: function() {
      this.log(this.todos)
    },
    del: function (i) {
      this.todos.splice(i,1)
      this.log(this.todos)
    },
    log: function(todos) {
    console.log(history, 'pending')
      this.historyIndex += 1
      this.history.splice(this.historyIndex)
      this.history.push(Object.assign([], todos));
      console.log(this.history)
    },
    undo: function() {
      if (this.canUndo) {
        this.historyIndex -= 1
        this.todos = this.history[this.historyIndex]
      }
    },
    redo: function() {
      if (this.canRedo) {
        this.historyIndex += 1
        this.todos = this.history[this.historyIndex]
      }
    }
  }
    }
</script>