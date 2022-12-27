<template>
    <h1 class="title">
        <slot name="title"></slot>
    </h1>
    <h2 class="subtitle">
        <slot name="subtitle"></slot>
    </h2>
    <p class="paragraph">
        <slot name="paragraph"></slot>
    </p>
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

<style>
    .title{
        color:crimson
    }
    .subtitle{
        color: darkred;
    }
    .paragraph{
        color: blueviolet;
    }
</style>