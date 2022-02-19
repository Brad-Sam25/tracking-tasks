<template>
  <header class="container">
    <div>
      <h1>
        {{ title }}
      </h1>
      <button class="btn" @click="addTask()">Add Task</button>
    </div>
  </header>

  <div v-if="display">
    <TaskInput />
  </div>
</template>

<script>
import TaskInput from "./TaskInput.vue";

export default {
  name: "Header",
  components: {
    TaskInput,
  },

  props: {
    title: String,
  },
  data() {
    return {
      display: false,
    };
  },

  methods: {
    addTask() {
      this.display = true;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: row;
  background-color: rgb(237, 179, 157);
  background-image: url(https://images.pexels.com/photos/7657599/pexels-photo-7657599.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940);
  background-position: center;
  background-size: cover;
  padding: 75px;
  margin-top: 0;
}

.btn {
  background-color: #4caf50;
  border: none;
  color: white;
  padding: 19px 40px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 18px;
  cursor: pointer;
  margin-top: 50px;
}

.btn:hover {
  box-shadow: 0 12px 16px 0 rgba(0, 0, 0, 0.24),
    0 17px 50px 0 rgba(0, 0, 0, 0.19);
}
</style>
