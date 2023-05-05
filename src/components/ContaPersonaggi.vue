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
    <div>
        <h3 class="red">
            il mio deck è formato da: {{ store.arrayCarte.length }} carte scarsissime
        </h3>
    </div>
</template>