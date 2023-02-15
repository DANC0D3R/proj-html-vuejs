<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNewMovieCarosell from './AppNewMovieCarosell.vue'
import AppMoviePlaylist from './AppMoviePlaylist.vue'

export default {
    components:{
        AppJumbotron,
        AppNewMovieCarosell,
        AppMoviePlaylist,
    }
}
</script>

<template>
	<AppJumbotron/>
    <AppNewMovieCarosell/>
    <AppMoviePlaylist/>
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
	
</style>