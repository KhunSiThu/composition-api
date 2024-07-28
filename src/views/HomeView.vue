<template>
  <div class="home">
    <h1>Home Page</h1>
    <input type="text" v-model="search">
    <p>Search item - {{ search }}</p>
    <div v-for="name in filterNames" :key="name">
      {{ name }}
    </div>
  </div>
</template>

<script>
import { computed, ref } from 'vue';




export default {
  setup(){

    let names = ref(["aungaung","kyawkyaw","mgmg","susu"]);
    let search = ref("");
    let filterNames = computed(()=> {
      return names.value.filter((name) => {
        return name.includes(search.value);
      })
    })
    return {names,search,filterNames}
  }
}
</script>
