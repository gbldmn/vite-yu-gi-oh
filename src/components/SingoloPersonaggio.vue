<script>
    export default{
        name: 'SingoloPersonaggio',
        props: ['dettagliPersonaggio']
    }
</script>



<template>
    
    <div class="col-12 col-md-6 col-lg-4">
     <div class="bg mt-3">
        <img class="mt-2 " :src="dettagliPersonaggio.card_images[0].image_url" alt="">
        <h3>{{ dettagliPersonaggio.name }}</h3>
        <h4>{{ dettagliPersonaggio.archetype}}</h4>
     </div>
    </div>
    
</template>