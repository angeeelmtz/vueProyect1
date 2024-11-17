<template>
    <p v-bind:style="{
        color : c,
        padding: '10px',
        fontSize: '20px',
        textAlign: 'center',
        fontFamily: 'Arial',
        backgroundColor: '#000'
    }">El mensaje se ha enviado correctamente</p>
    <button @click="handleClick">Cambiar color</button>
</template>

<script lang="ts">
    //Setup CompositionAPI
    /* import { ref } from 'vue';
    let c = ref('#fff')
    const handleClick = () => c.value = '#0f0' */

    /* CompositionAPI */
    import { defineComponent, ref } from 'vue';
    export default defineComponent({
        name: 'StyleBind',
        setup() {
            let c = ref('#f00')
            const handleClick = () => c.value = "#0f0"
            return {c, handleClick}
        }
    })

   /* OptionAPI
   import { defineComponent} from 'vue';
   export default defineComponent({
    name: 'StyleBind',
    data(){
        let c = "#00f"; return {c}
        return {
            c: '#0f0'
        }
    },
    methods: {
        handleClick(){
            this.c = '#f00'
        }
    }
   })*/

</script>

<style>

</style>