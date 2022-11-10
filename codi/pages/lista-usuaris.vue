<template>
    <v-container class="contenidor"> 
            <v-row class="fila"> 
                <v-col
                class="columna"
                v-for="(usuari,posicio) in usuaris"
                :key="posicio">
                {{usuari.firstName}}    
                {{posicio}}/{{usuaris.length}}
                <v-img v-bind:src="usuari.image"></v-img>
                </v-col>
            </v-row>
    </v-container>



</template>

<style>
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