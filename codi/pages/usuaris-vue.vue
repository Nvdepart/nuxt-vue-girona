<template>
    <div>

        <v-btn class="sty" @click="descarregarUsuaris()">descarregar</v-btn>
        <v-btn class="sty" @click="descarregarUsuaris2()">async descarregar</v-btn>   
        <pre>
            {{usuaris}}
        </pre>
        

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
export default{
    data:function(){
        return{
            usuaris:[]
        }
    },
    methods:{
        descarregarUsuaris(){
            
            let f = fetch('https://dummyjson.com/users')
        
            let j = f.then(function(resposta){
                return resposta.json()
            })


            let self = this

            j.then(function(dades){
                console.log(dades)
                self.usuaris = dades
            })


            /*
            .then(res =>{
            
            return  res.json()
            } )
            .then((usuaris)=>{

                console.log(usuaris)
            });
            */
        },
        async descarregarUsuaris2(){
            let resposta = 
            await fetch("https://dummyjson.com/users")
            //console.log(resposta)
            let dades = await resposta.json()
            console.log(dades)
            this.usuaris = dades.users
        }
    }
}
        
</script>