<template>
  <div>
    <SubNavBar/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import SubNavBar from '@/components/SubNavBar.vue';

@Options({
  components: {
    SubNavBar,
  },
})
export default class SubNav extends Vue {}
</script>
