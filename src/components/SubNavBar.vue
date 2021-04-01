<template>
  <div id="subnav">
    <span class="d-inline-block h5 mx-5 dark active textstyle"  @click="changePage($event)">Personal</span>
    <span class="d-inline-block h5 mx-5 dark remained textstyle"  @click="changePage($event)">Educational</span>
    <span class="d-inline-block h5 mx-5 dark remained textstyle"  @click="changePage($event)">Technology</span>
    <span class="d-inline-block h5 mx-5 dark remained textstyle"  @click="changePage($event)">Experience</span>
    <span class="d-inline-block h5 mx-5 dark remained textstyle"  @click="changePage($event)">Project Details</span>
  </div>
  <!-- <router-view/> -->
</template>
<script lang="ts">
import { Vue } from "vue-class-component";
export default class SubNavBar extends Vue {
    currentPage = 'Personal'
  changePage(event: MouseEvent): void {
    const currentPage = event.target as HTMLSpanElement;
    for (let i = 0; i < 5; i++) {
      (event.target as HTMLSpanElement).parentElement?.children[i].classList.remove("active");
      (event.target as HTMLSpanElement).parentElement?.children[i].classList.add("remained");
      (event.target as HTMLSpanElement).parentElement?.children[i].classList.remove("completed");
    }
    currentPage.classList.remove("remained");
    currentPage.classList.add("active");
    for (let i=0;i<5;i++) {
        if((event.target as HTMLSpanElement).parentElement?.children[i] === currentPage) {
            break
        }
      (event.target as HTMLSpanElement).parentElement?.children[i].classList.add("completed");
    }
  }
}
</script>

<style scoped>
#subnav {
  text-align: center;
  padding-top: 30px;
}
.textstyle {
  color: rgb(134, 133, 133);
  font-weight: bold;
}
.remained {
  border-bottom: 2px solid rgb(134, 133, 133);
}
.active {
  border-bottom: 2px solid black;
  color: black;
}
.completed {
  border-bottom: 2px solid rgb(124, 194, 124);
  color: rgb(74, 145, 74);
}
/* .completed:after { 
  content:""; 
  float:left; 
  background:green; 
  width:fit-content; 
  height:6px; 
  border-radius: 3px;
} */
</style>