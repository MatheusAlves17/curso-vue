<template>
    <div>
        <h1>Hello world</h1>
    </div>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
            }
        },
        watch:{
            
        },
        methods:{
            
        },
        computed:{
        },
        beforeUnmount(){
            console.log('beforeUnmount')
        },
        unmounted(){
            console.log('unmounted')
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