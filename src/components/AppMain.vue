<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNewMovieCarosell from './AppNewMovieCarosell.vue'

export default {
    components:{
        AppJumbotron,
        AppNewMovieCarosell,
    }
}
</script>

<template>
	<AppJumbotron />
    <AppNewMovieCarosell />
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
	
</style>