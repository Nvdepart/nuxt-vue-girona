<template>
    <div>
        porfoli
        <Hola></Hola>
    </div>
</template>
<script>
 import Hola from '../prova/Hola.vue'
 let usuaris = []
 export default{
    components:{
         Hola:Hola,
    },
    layout:"basic"
}
</script>