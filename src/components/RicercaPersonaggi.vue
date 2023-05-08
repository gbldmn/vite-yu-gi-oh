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
        <input type="text" placeholder="Ricerca carte" v-model="store.testoRicerca">
        <button @click="$emit('nomeEmit')">ricerca</button>
    </div>
</template>