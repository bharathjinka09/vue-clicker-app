<template>
<h1>{{title}}</h1>
<h1>{{count}}</h1>
<button class="btn btn-info m-2" @click="increment">Increment</button>
<button class="btn btn-info m-2" @click="decrement">Decrement</button>
</template>   

<script>
import {ref} from 'vue';

export default {
    setup(){
        let title = "Clicker App";

        const count = ref(0);

        function increment(){
            count.value++;
        }

        function decrement(){
           count.value > 0 ? count.value-- : '';
        }

        return {
            title,
            count,
            increment,
            decrement,
        }
    }
}
</script> 


<style scoped>

</style>