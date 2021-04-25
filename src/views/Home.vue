<template>
  <div class="home">
    <span class="num"> {{ number }} </span>
    <br />
    <button @click="number++">Arttır</button>
    <button @click="number--">Eksilt</button>
    <button @click="increase">2 Arttır</button>
    <button @click="decrease">2 Eksilt</button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Home extends Vue {
  private number = 0;

  increase(): void {
    this.number += 2;
  }
  decrease(): void {
    this.number -= 2;
  }
}
</script>
<style scoped>
.num {
  font-size: 30px;
}
</style>
