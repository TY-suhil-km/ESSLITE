<template>
  <div class="education">
    <select  class="form-select empty" aria-label="Default select example">  
        <option value="" selected disabled >{{placeHolder}}</option>
        <option :key="arrayData.name" v-for="arrayData of data" :value="arrayData.value"> {{arrayData.name}} </option>
    </select>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
@Options({
  components: {
    CustomSelect,
  },
  props: {
    data: Array,
    placeHolder: String
  }
})
export default class CustomSelect extends Vue {
    mounted (): void {
        console.log('&&&&&&&&', this.data)
    }
}
</script>

<style scoped>
.education {
  margin: 10px;
}
select option {
	color: black;
}
select option[disabled]:first-child {
	color: #80808082;
}
select.empty {
	color: #80808082;
}
/* Hidden placeholder */
select option[disabled]:first-child {
	display: none;
}
.placeHolderStyle {
  color: gray
}
</style>
