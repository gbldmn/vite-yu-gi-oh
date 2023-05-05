<script>
    import {store} from './store'
    import axios from 'axios';
    import HeaderComp from './components/HeaderComp.vue'
    import PersonagiComp from './components/PersonagiComp.vue'
    import ContaPersonaggi from './components/ContaPersonaggi.vue';

    export default{
        name: 'app',
        components: {
            HeaderComp,
            PersonagiComp,
            ContaPersonaggi
        },
        data(){
            return{
                store
            }
        },
        created(){
            this.chiamataApi()
        },
        methods: {
            chiamataApi(){
                            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=12&offset=0')
                .then( (res) =>{
                   console.log(res.data.data)



                   const datiApi = res.data.data
                   this.store.arrayCarte = datiApi
                })
            }
        }
    }

</script>

<template>
  <HeaderComp :titoloProps=" 'yu-gi-ho API' "/>
  <main class="container">
    <ContaPersonaggi/>
    <PersonagiComp/>
  </main>
</template>

<style lang="scss">
@use './style/main.scss';

</style>
