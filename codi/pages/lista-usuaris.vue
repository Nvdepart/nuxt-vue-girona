<template>

<div>

            <v-row class="fila"> 
                <v-col
                cols="12"
                sm="4"
                class="columna"
                v-for="(usuari,posicio) in usuaris"
                :key="posicio">
                {{usuari.firstName}}    
                {{posicio}}/{{usuaris.length}}
                <v-img class="imgSty" v-bind:src="usuari.image"></v-img>
                </v-col>
            </v-row>
            <v-row>
                <v-col>
                    <pre>{{usuaris}}</pre>
                </v-col>
            </v-row>
</div>

</template>

<style>
    .imgSty{
        background-color:rgb(234, 237, 32);
        color:rgb(255, 255, 255);
        text-align:center;
        border-radius:5px;
        padding:5px;
        margin:2px;
    }
    .columna{
        background-color:rgb(23, 128, 56);
        color:rgb(255, 255, 255);
        text-align:center;
        border-radius:5px;
        padding:5px;
        margin:20px;
    }
    .fila{
        background-color: aqua;
        text-align:center;
        border-radius:5px;
        margin:20px;
    }
    .contenidor{
        background-color: blue;
        text-align:center;
        border-radius:5px;
        margin:20px;
    }
</style>

<script>
        export default{
            layout:"basic",
            created(){
                console.log("S'ha creat la pagina")
            },
            mounted(){
                console.log(this.laClasse)
                console.log("S'ha muntat la pagina")
                this.descarregarUsuaris()
            },
            data(){
                    return {
                        laClasse:"columna",
                        usuaris:[],
                        jordi:"Hola"
                    }
                },
            methods:{
                async descarregarUsuaris(){
                    console.log('Descarregant usuaris...')
                    let resposta = 
                    await fetch('https://dummyjson.com/users')
                    //console.log(resposta)
                    let json = await resposta.json()
                    this.usuaris= json.users
                    console.log(json)
                }
            }

        }

</script>