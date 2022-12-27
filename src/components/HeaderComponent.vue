<template>
    <div class="card">
        <slot name="description"></slot>
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
        }
    }
</script>

<style scoped>
    .card{
        padding: 4rem;
        background: cornflowerblue;
        color: #f8f8f8;
        font-weight: 600;
        border-radius: 12px;
        max-width: 400px;
    }
</style>