<template>
    <div class="postCard">
        <h3>Titulo</h3>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsam dignissimos, aliquid illo, sapiente molestiae in veniam quas incidunt debitis, nostrum totam rem architecto nobis quae cumque odio animi dolor voluptatem.</p>
        <PostButton></PostButton>
    </div>
</template>

<script lang="ts" setup>  
    import PostButton from './PostButton.vue';
</script>

<style scoped>
    .postCard{
        border: radius 15px;
        padding: 10px;
        margin: 5px;
        border: 1px solid #ccc;
    }
</style>