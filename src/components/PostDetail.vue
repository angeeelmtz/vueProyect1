<template>
    <div class="post">
        <h4>{{ props.title }}</h4>
        <p>{{ props.content }}</p>
        <input type="text" v-model="message">
        <button @click="handleClick">Saludar</button>
    </div>
</template>

<script>
    import { defineComponent, ref } from 'vue';
    export default defineComponent({
        name: "PostDetail",
        props:{
            title: {},
            content: {}
        },
        emits:["saludar"],
        setup(props, {emit}){
            let message = ref('')
            const handleClick = () => {
                emit("saludar", message.value)
            }
            return {props, message, handleClick}
        }
    })
</script>

<style scoped>
    .post{
        width: 250px;
        height: 200px;
        padding: 10px;
        color: white;
        background-color: crimson;
        text-align: center;
        font-family: Arial, Helvetica, sans-serif;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
</style>