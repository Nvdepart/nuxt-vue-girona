<template>
    <div>
        <div>{{contador}}</div>
        <v-btn class="sty" v-on:click="augmentar10()" >Augmentar 10</v-btn>
        <v-btn class="sty" @click="disminuir10()">Disminuir 10</v-btn>
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
            contador:0
        }
    },
    methods:{
        augmentar10:function(){
            this.contador += 10
        },
        disminuir10(){
            this.contador -= 10
        }
    }
}
</script>