<template>
    <div>
        <h1>{{titol}}</h1>
        <p v-html="descripcio"></p>
        {{contador}}
        <button class="sty" v-on:click="augmentar()">Augmentar</button>
        <button class="sty" @click="disminuir()">Disminuir</button>
    </div>
</template>
<style>
    .sty{
        background-color:rgb(23, 128, 56);
        text-align:center;
        border-radius:5px;
        padding:5px;
        margin:20px;
    }
</style>
<script>
    export default {
        data:function(){
            return{
                titol:"Contador vue",
                descripcio:"El contador <strong>del</strong> curs vue girona",
                contador:0
            }
        },
        methods:{
            augmentar:function(){
                this.contador++
                this.titol = "He augmentat"
            },
            disminuir:function(){
                this.contador--
                this.titol = "He disminuit"
            }
        }
    }
</script>