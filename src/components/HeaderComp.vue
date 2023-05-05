<script>
    export default {
        name: 'HeaderComp',
        props: ['titoloProps']
    }
</script>


<template>
    <header>
    <div>
        <h1 class="text-center">{{ titoloProps }}</h1>
    </div>
    </header>
</template>