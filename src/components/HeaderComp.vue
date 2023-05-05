<script>
    export default {
        name: 'HeaderComp',
        props: ['titoloProps']
    }
</script>


<template>
    <div>
        <h1 class="text-center">{{ titoloProps }}</h1>
    </div>
</template>