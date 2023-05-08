<script>
import {store} from '../store'
export default {
    name: "RicercaPersonaggi",
    data(){
        return {
            store
        }
    }
}
</script>


<template>
    <div>
        <input type="text" placeholder="Ricerca carte" v-model="store.TestoRicerca">
    </div>
</template>