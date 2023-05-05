<script>
import { store } from '../store'
import SingoloPersonaggio from './SingoloPersonaggio.vue'


export default{
    name: 'PersonagiComp',
    components: {
        SingoloPersonaggio
    },
    data(){
        return{
            store
        }
    }

}

</script>



<template>
    <div class="text-center row">
        <SingoloPersonaggio 
        v-for="(elem,index) in store.arrayCarte"
        :key="index"
        :dettagliPersonaggio="elem"
        />
    </div>
</template>