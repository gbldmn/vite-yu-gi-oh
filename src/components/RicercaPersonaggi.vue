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
        <select name="seleziona" id="" v-model="store.testoRicerca">
            <option v-for="(elem, index) in store.arrayArchetypes"
            :key="index" :value=" elem.archetype_name"> {{ elem.archetype_name }} </option>
        </select>
        <!-- <input type="text" placeholder="Ricerca carte" v-model="store.testoRicerca"> -->
        <button @click="$emit('nomeEmit')">ricerca</button>
    </div>
</template>