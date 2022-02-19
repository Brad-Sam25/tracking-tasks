<template>
  <div class="input-container">
    <label for="task"> Task </label>
    <input type="text" v-model.trim="newTodo" placeholder="Enter task here..." />
    <button class="saveBtn" @click="addUserTask">Save</button>
  </div>

   <div>
    <ul>
      <li v-for="todo in toDoTasks" :key="todo.todos">
        <div class="form-check">
          <label class="form-check-label">
            <input class="checkbox" type="checkbox" /> {{todo.todos}}.</label
          >
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import TaskListVue from './TaskList.vue';

export default {
  components: TaskListVue,

  data() {
    return {
      visible: false,
      newTodo:"",
      toDoTasks: [
        {todos:'Buy skincare products'},
        {todos:'Buy milk'},
      ]
    }
  },

  methods: {
    addUserTask() {
      this.toDoTasks.push({todos: this.newTodo});

      if(!this.newTodo) {
        return
      }

      this.newTodo = "";
    }

  }
};
</script>

<style scoped>
.input-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 40px;
}

input {
  margin: 15px 0px;
  padding: 10px;
  border-radius: 10px;
  width: 75%;
} 

label {
    margin-right: 20px;
}

.saveBtn {
  background-color: blue;
  border: none;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 18px;
  cursor: pointer;
  margin-left: 10px;
}

.saveBtn:hover {
    box-shadow: 0 12px 16px 0 rgba(0, 0, 0, 0.24),
    0 17px 50px 0 rgba(0, 0, 0, 0.19);
}
.form-check {
  margin: 10px 0px;
  background: #f7f7f7;
  padding: 15px;
}

.form-check-label {
  margin-left: -400px;
}

</style>