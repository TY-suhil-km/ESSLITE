<template>
  <div id="nav">
    <SubNavBar/>
    <Experience/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import SubNavBar from "@/components/SubNavBar.vue";
import Experience from '@/components/Experience.vue';

@Options({
  components: {
    SubNavBar,
    Experience,
  },
})
export default class App extends Vue {}
</script>

<style>



#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
