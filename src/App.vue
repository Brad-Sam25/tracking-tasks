<template>
  <Header title="Task Tracker"/>
</template>

<script>
import Header from './components/Header.vue';


export default {
  name: 'App',
  components: {
    Header
  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Indie+Flower&display=swap');
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  
  body {
    font-family:'Indie Flower', cursive;
  }

</style>
