<template>
    <div class="bg">
        <div v-for="(personaje, index) in personajes" :key="index">
            <TarjetaComponente v-bind:nombre="personaje.name" v-bind:imagen="personaje.image" />
        </div>
    </div>
</template>

<script>
    import TarjetaComponente from "./TarjetaComponente.vue";
    export default {
    name: "App",
    components: { 
        TarjetaComponente 
    },
    data(){
        return {
            personajes:[
                {
                    name:'Rick Sanchez',
                    image:'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
                },
                {
                    name:'Morty Smith',
                    image:'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
                },
                {
                    name:'Summer Smith',
                    image:'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
                },
                {
                    name:'Beth Smith',
                    image:'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
                },
                {
                    name:'Jerry Smith',
                    image:'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
                }
            ]
        }
    },

}; 
    
</script>


<style scoped>

.bg{
    background: url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png") no-repeat;
    background-size: cover;
    height: 100vh;
    padding: 20px;
}
</style>