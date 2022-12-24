<template>
    <nav>
        <ul>
            <li :class="{'active': home}">Home</li>
            <li :class="{'active': services}">Services</li>
            <li :class="{'active': about}">About</li>
        </ul>
    </nav>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
                home: false,
                services: true,
                about: false
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