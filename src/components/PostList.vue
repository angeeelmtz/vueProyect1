<template>
    <div class="container">
        <PostDetail 
            v-for="element in info" 
            :key="element.title" 
            :title="element.title" 
            :content="element.content"
            @saludar="showAlert">
            {{ element }}
        </PostDetail>
    </div>
</template>

<script setup>
    import PostDetail from './PostDetail.vue';
    let info = [
        {
            title: "Titulo 1",
            content: "Este es el contenido de la caja 1"
        },
        {
            title: "Titulo 2",
            content: "Este es el contenido de la caja 2"
        },
        {
            title: "Titulo 3",
            content: "Este es el contenido de la caja 3"
        },
        {
            title: "Titulo 4",
            content: "Este es el contenido de la caja 4"
        },
        {
            title: "Titulo 5",
            content: "Este es el contenido de la caja 5"
        }
    ]

    function showAlert(msg){
        alert(msg)
    }

</script>

<style scoped>
    .container{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        gap: 16px;
        justify-content: center;
    }
</style>