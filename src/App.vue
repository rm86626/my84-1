<template>
  <div>
       <h3>App组件</h3>
       <p>count:{{count}}</p>
       <p>double:{{double}}</p>
       <button @click="add">+1</button>
       <MyNews></MyNews>
  </div>
</template>

<script>
import {ref,computed} from 'vue'
import MyNews from './components/MyNews.vue';
export default {
    setup() {
        let count = ref(0);
        let double = computed(() => count.value * 2);
        let add = () => {
            count.value++;
        };
        return {
            count,
            double,
            add
        };
    },
    components: { MyNews }
}
</script>

<style lang="scss" scoped>

</style>