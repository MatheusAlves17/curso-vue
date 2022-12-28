<template>
<!-- <div :class="['dialog-default',{'dialog-success': status === 'success'}]"> -->
    <!-- <div :class="`dialog-default dialog-${status}`"> -->
    <div :class="comportamento">
        <p>Seu formulário foi enviado com sucesso!</p>
        <button @click="fechar()">X</button>
    </div>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
            }
        },
        props:
            // ['status'] ou
            {
                status: {
                    type: String,
                    default: 'default'
                }
            }

        ,
        watch:{
            
        },
        methods:{
            fechar(){
                this.$emit('feche')
                console.log('feche')
            }
        },
        computed:{
            comportamento(){
                return [
                    'dialog-default',
                    this.status ? `dialog-${this.status}` : ''
                ]
            }
        }
    }
</script>

<style scoped>
    .dialog-default{
        padding: 3px;
        border-radius: 16px;
        color: #f8f8f8;
        background: #272727;
    }
    .dialog-success{
        background: #42b983;
    }
    .dialog-fail{
        background: #b94242;
    }
</style>