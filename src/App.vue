<script>

// options API version of Vue.js is used here, which is the traditional way of defining components.
// This is a simple Vue.js component that demonstrates data binding, conditional rendering, and event handling.
export default {
  data() {
    return {
      message: 'Hello Vue!',
      status:"pending",
      tasks:["task one", "task two", "task three"],
      link:"https://www.google.com/"
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') {
        this.status = 'pending';
      } else if (this.status === 'pending') {
        this.status = 'inactive';
      } else {
        this.status = 'active';
      }
    }
  }
};
</script>



<template>
 <h1>{{message}} </h1>
 <p v-if="status==='active'">User is active</p>
 <p v-else-if="status==='pending'">User is pending</p>
 <p v-else>User is inactive</p>

 <h3>tasks</h3>
 <ul>
  <li v-for="(task,index) in tasks" :key="task">
    <span>{{ task }}</span>

    </li>
 </ul>

 <a v-bind:href="link">Click for google</a>
<br/>
 <!-- <button v-on:click="toggleStatus">Change Status</button> -->
 <button @click="toggleStatus">Change Status</button>
</template>

<style scoped>


</style>
