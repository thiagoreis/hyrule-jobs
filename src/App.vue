<template>
 <div class="app">
   <p>{{ name }} - {{ age }}</p>
   <button @click="changeName('Zelda')">change name</button>
   <button @click="changeAge(30)">change age</button>
 </div>
</template>

<script lang="ts">

import { defineComponent, reactive } from 'vue';


export default defineComponent({
  name: 'App',
  components: {
    
  }, 
  setup() {
    const state = reactive({
      name: 'Link', 
      age: 25 as string | number
    })
  },
  data() {
    return {
      name: 'Link',
      age: 25 as number | string
    }
  },
  methods: {
    changeName(name: string) {
      this.name = name
      return name
    },
    changeAge(age: string | number) {
      this.age = age
      return age
    }
  }
});
</script>

<style>

</style>
