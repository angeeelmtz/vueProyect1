<template>
    <form>
        <input type="text" v-model="inputText">
        <input type="checkbox" v-model="agree"> Acepto los terminos y condiciones
        <select v-model="country">
            <option v-for="(countrie, index) in countries" :key="index">{{ countrie }}</option>
        </select>
    </form>
    <h3>{{ inputText }}</h3>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    let inputText = ref('')
    let agree = ref(true)
    let countries = ref(['Spain', 'Italy', 'Portugal'])
    let country = ref('Italy')

    /* import { defineComponent } from 'vue';
    export default defineComponent({
        name: "ModelForm",
        data(){
            return {
                inputText: '',
                agree: true
            }
        }
    }) */

   /* import { defineComponent, ref } from 'vue';
   export default defineComponent({
    name: 'ModelForm',
    setup(){
        let inputText = ref('')
        return {inputText}
    }
   }) */
</script>

<style scoped>

</style>