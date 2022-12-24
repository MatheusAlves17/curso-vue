<template>
    <nav>
        <ul>
            <li :class="{'active': home}">Home</li>
            <li :class="{'active': services}">Services</li>
            <li :class="{'active': about}">About</li>
        </ul>
    </nav>
    <div>
        <form>
            <input type="text" name="name" id="name" v-model="name">
            <br>
            <select v-model="esporte">
                <option value="">Escolha</option>
                <option value="futebol">futebol</option>
                <option value="vôlei">vôlei</option>
                <option value="basquete">basquete</option>
            </select>
            <br>
            <label>Quer receber nossas notificações?</label>
            <input type="radio" v-model="notificações" value="sim">sim
            <input type="radio" v-model="notificações" value="não">não
            <br>
            <label>Aceita nossos termos?</label>
            <input type="checkbox" v-model="termos">
            <br>
            <input type="checkbox" v-model="preferencias" value="Azul">Azul
            <input type="checkbox" v-model="preferencias" value="Verde">Verde
            <input type="checkbox" v-model="preferencias" value="Amarelo">Amarelo
            <input type="checkbox" v-model="preferencias" value="Vermelho">Vermelho
            <input type="text" v-model="cpf" @keyup.enter="enviar"/>
            <button type="submit">Enviar</button>
        </form>
        <p>{{ name }} | {{ esporte }} | Receber notificações? {{ notificações }} | Aceita nossos termos? {{ termos }} | {{ preferencias }}</p>
    </div>
</template>

<script>
    export default{
        name: 'HeaderComponent',
        data(){
            return {
                home: false,
                services: true,
                about: false,
                name: "Harry Potter",
                esporte: '',
                notificações: '',
                termos: '',
                preferencias: [],
                cpf: ''
            }
        },
        methods:{
            enviar(){
                console.log("Enviou!")
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