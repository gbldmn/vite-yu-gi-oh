<script>
    import {store} from './store'
    import axios from 'axios';
    import HeaderComp from './components/HeaderComp.vue'
    import PersonagiComp from './components/PersonagiComp.vue'

    export default{
        name: 'app',
        components: {
            HeaderComp,
            PersonagiComp
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
                            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
                .then( (res) =>{
                   console.log(res.data)



                   const datiApi = res.data
                   this.store.arrayCarte = datiApi
                })
            }
        }
    }

</script>

<template>
  <HeaderComp :titoloProps=" 'yu-gi-ho API' "/>
  <main class="container">
    <PersonagiComp/>
  </main>
</template>

<style lang="scss">
@use './style/main.scss';

</style>
