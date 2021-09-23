<template>
  <div id="app">
    <AttendingSubmit />

    <hr />

    <UserList />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import AttendingSubmit from './components/AttendingSubmit.vue';
import UserList from './components/UserList.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    AttendingSubmit,
    UserList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
