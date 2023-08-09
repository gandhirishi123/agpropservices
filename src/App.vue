<template>
  <div class="div" style="background-color: rgba(255, 255, 255, 0.5);">
    <NavBar/>
  <router-view></router-view>

  </div>
  
</template>

<script>
import NavBar from './components/NavBar.vue';
export default {
  name: 'App',

  data: () => ({
    //
  }),
  components:{ NavBar }
};
</script>
