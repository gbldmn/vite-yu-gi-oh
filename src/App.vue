<script>
    import HeaderComp from './components/HeaderComp.vue'

    export default{
        name: 'app',
        components: {
            HeaderComp
        }
    }
</script>

<template>
  <HeaderComp :titoloProps=" 'yu-gi-ho API' "/>
</template>

<style lang="scss">
@use './style/main.scss';

</style>
