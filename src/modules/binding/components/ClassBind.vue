<template>
    <p v-bind:class="{'danger': hasError}">El mensaje se ha enviado correctamente</p>
    <!-- 
        Al dejar los dos puntos ':' se hace referencia a v-bind:class => ShortCut
        <p :class="{'danger': hasError}">El mensaje se ha enviado correctamente</p> 
    -->
</template>

<script lang="ts" setup>
    let hasError = true

    /* CompositionAPI 
    import { defineComponent } from 'vue';
    export default defineComponent({
        name: "ClassBind",
        setup() {
            let hasError = true
            return {hasError}
        }
    }) */

   /* OptionAPI
   import { defineComponent } from 'vue';
   export default defineComponent({
        name: "ClassBind",
        data(){
            let hasError = true
            return {hasError}
        }
   }) */
</script>

<style>
    .danger{
        color: red;
        font-size: 20px;
        text-align: center;
        font-family: Arial, Helvetica, sans-serif;
    }
</style>