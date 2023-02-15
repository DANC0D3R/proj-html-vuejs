<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNewMovieCarosell from './AppNewMovieCarosell.vue'
import AppMoviePlaylist from './AppMoviePlaylist.vue'
import AppComingSoon from './AppComingSoon.vue'

export default {
    components:{
        AppJumbotron,
        AppNewMovieCarosell,
        AppMoviePlaylist,
        AppComingSoon,
    }
}
</script>

<template>
	<AppJumbotron/>
    <AppNewMovieCarosell/>
    <AppMoviePlaylist/>
    <AppComingSoon/>
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
	
</style>