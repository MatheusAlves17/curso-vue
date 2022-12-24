<template>
    <div>
        <ul v-for="todo in allTodos" :key="todo.id">
            <li>{{ todo.title }}</li>
        </ul>
    </div>
    <div>
        <ul v-for="item in todosNotCheck" :key="item.id">
            <input type="checkbox" v-model="item.completed">
            <li>{{item.title}}</li>
        </ul>
    </div>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
                todos:[
                    {
                        id: 1,
                        title: 'Tarefa 1',
                        completed: false
                    },
                    {
                        id: 1,
                        title: 'Tarefa 2',
                        completed: true
                    },
                    {
                        id: 1,
                        title: 'Tarefa 3',
                        completed: false
                    },
                    {
                        id: 1,
                        title: 'Tarefa 4',
                        completed: false
                    },
                    {
                        id: 1,
                        title: 'Tarefa 5',
                        completed: false
                    }
                ]
            }
        },
        methods:{

        },
        computed:{
            allTodos(){
                return this.todos.filter(todo => todo.completed);
            },
            todosNotCheck(){
                return this.todos.filter(todo => !todo.completed);
            }
        }
    }
</script>

<style>
    ul{
        display: flex;
        align-items: center;
        justify-content: center;
    }
    li{
        list-style-type: none;
        margin: 6px 12px;
        font-weight: 600;
        cursor: pointer;
    }
    .active{
        color:crimson
    }
</style>