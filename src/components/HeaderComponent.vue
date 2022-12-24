<template>
    <label for="">CPF</label>
    <input type="text" maxlength="11" v-model="cpf">
    <label for="">Nome</label>
    <input type="text" minlength="3" v-model="nome">
    <label for="">Sobrenome</label>
    <input type="text" minlength="2" v-model="sobrenome">
    <select v-model="pagination">
        <option value="5">5</option>
        <option value="10">10</option>
        <option value="15">15</option>
    </select>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
                cpf:'',
                nome:'',
                sobrenome:'',
                pagination: 5
            }
        },
        watch:{
            cpf(vl){
                if(vl.length >= 11){
                    this.validityCPF()
                }
            },
            nome(vl){
                if(vl.length < 3) console.log('Digite um nome válido')
            },
            sobrenome(vl){
                if(vl.length < 2 ) console.log('Digite um sobrenome válido') 
            },
            pagination(){
                console.log('Requisição feita!')
            }
        },
        methods:{
            validityCPF(){
                console.log(`Validando... ${this.cpf}`)
            }
        },
        computed:{
            
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