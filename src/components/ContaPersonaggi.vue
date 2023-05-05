<script>
import { store } from '../store'
export default {
    name: 'ContaPersonaggi',
    data(){
        return{
            store
        }
    }
}
</script>

<template>
    <div class="bg-dark p-2 ">
        <h3 class="red">
           IL MIO DECK E' COMPOSTO DA: {{ store.arrayCarte.length }} CARTE SCARSISSIME
        </h3>
    </div>
</template>