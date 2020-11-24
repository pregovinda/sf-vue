<template>
  <div> 
    <Navbar />   
    <h2 class="center">My Application</h2>
    <div v-text="message"></div>
    {{ message }}
    <ul>
      <li :key="word.id" v-for="word in words">{{ word }}</li>
    </ul>
  </div>
</template>

<script>
import Navbar from '../components/Navbar';

export default {
  name: 'App',
  components: {
    Navbar
  },
  data() {
    return {
      message: "A list of words",
      words: []
    };
  },
  mounted() {

  }
};
</script>

<style>
.center {
  text-align: center;
}
</style>