<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
    <button @click="lessCounter">Decrementar</button>
</template>

<script lang="ts" setup>
    import { ref, Ref } from 'vue';
    let counter:Ref = ref(0)
    const addCounter = ():void => {
        counter.value++
    }
    const lessCounter = ():void => {
        counter.value--
    }

    /*
    import { defineComponent, Ref } from 'vue';
    import { ref } from 'vue';
    export default defineComponent({
        name: "CounterComposition",
        setup(){
            let counter:Ref = ref(0)
            const addCounter = ():void => {
                counter.value++
            }
            return {counter, addCounter}
        }
    })
    */
</script>