<template>
  <div class="experience">
      <SubNavBar/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import SubNavBar from '@/components/SubNavBar.vue'
@Options({
  components: {
    SubNavBar,
  },
})
export default class Experience extends Vue {}
</script>
