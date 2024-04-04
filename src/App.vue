<template>
  <div>
       <h3>App组件</h3>
       <p>count:{{count}}</p>
       <p>double:{{double}}</p>
       <button @click="add">+1</button>
  </div>
</template>

<script>
import {ref,computed} from 'vue'
export default {
  setup () {
    let count=ref(0);
    let double=computed(()=>count.value*2);
    let add=()=>{
      count.value++;
    }
    return {
      count,
      double,
      add
    }
  }
}
</script>

<style lang="scss" scoped>

</style>