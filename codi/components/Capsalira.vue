<template>
    <v-container :style="estils()"
    >
        <v-row>
            <v-col>
                <h2><nuxt-link to="/porfoli">
                    {{marca}}
                </nuxt-link></h2>
            </v-col>
            <v-col align="end">
                <nuxt-link to="/lista-usuaris">Usuaris</nuxt-link>
                <nuxt-link to="/sobre-mi">Sobre mi</nuxt-link>
                <nuxt-link to="/">contacte</nuxt-link>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>

export default {
    //definir les propietats de component
    props: ['color','marca'],
    mounted(){
        console.log(this.color)
    },
    methods:{
        estils(){
            return{
                height:"20vh",
                backgroundColor:this.color
            }
        }
    }
}


</script>