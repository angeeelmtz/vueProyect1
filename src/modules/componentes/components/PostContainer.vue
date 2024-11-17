<template>
    <div class="postContainer">
        <PostCard></PostCard>
        <PostCard></PostCard>
        <PostCard></PostCard>
        <PostCard></PostCard>
    </div>
</template>

<script lang="ts" setup>
    import PostCard from './PostCard.vue';
</script>

<style>
    .postContainer{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }
</style>