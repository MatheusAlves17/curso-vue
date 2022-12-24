<template>
    <h1 class="header">Hello world</h1>
    <div>
        <div class="todo-list" v-for="todo in todos" :key="todo.id">
            {{ todo.title }}
            <img :src="todo.photo" :alt="todo.title">
        </div>
    </div>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
                todos: [
                    {
                        id: 1,
                        title: 'Título I',
                        photo: 'https://via.placeholder.com/150'
                    },
                    {
                        id: 2,
                        title: 'Título II',
                        photo: 'https://via.placeholder.com/150'
                    },
                    {
                        id: 3,
                        title: 'Título III',
                        photo: 'https://via.placeholder.com/150'
                    },
                    {
                        id: 4,
                        title: 'Título IV',
                        photo: 'https://via.placeholder.com/150'
                    },
                ]
            }
        }
    }
</script>

<style>
    .header{
        background: #7787;
        color: #f8f8f8;
    }
    .todo-list{
        align-items: flex-start;
        background: #7787;
        color: #f8f8f8;
        padding: 3px 6px;
        margin: 4px 0 0 0;
        border-radius: 12px;
    }
</style>