<template>
    <ul>
        <!-- <li v-for="country in countries" v-bind:key="country">{{ country }}</li> -->
        <li v-for="country in countries" v-bind:key="country.code">{{ country.name }}</li>
        
        <!-- 
        Este ejemplo es en caso de que el bucle tenga datos repetivos y necesite que cada dato
        tengo un identificador unico 
        <li v-for="(country, index) in countries" v-bind:key="index">{{ country }}</li> 
        -->
    </ul>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';

    /* interface ICountry{
        code: string,
        name: string
    }
    let countries:Ref<Array<ICountry>> = ref([
        "Panama", "Colombia", "Venezuela", "Mexico", "Costa Rica"
    ]) */
    
    let countries = ref([
        {
            code: "es",
            name: "Spain"
        },
        {
            code: "en",
            name: "UK"
        },
        {
            code: "fr",
            name: "France"
        },
        {
            code: "it",
            name: "Italy"
        },
        {
            code: "pt",
            name: "Portugal"
        }
    ])
</script>

<style scoped>
    li{
        font-size: 20px;
        font-family: Arial, Helvetica, sans-serif;
    }
</style>