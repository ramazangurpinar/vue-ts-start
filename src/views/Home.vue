<template>
  <div class="home">
    <span class="num"> {{ number }} </span>
    <br />
    <br />
    <button @click="number++">Arttır</button>
    <button @click="number--">Eksilt</button>
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {
  private number = 0;
}
</script>
<style scoped>
.num {
  font-size: 30px;
}
</style>
