<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNewMovieCarosell from './AppNewMovieCarosell.vue'
import AppMoviePlaylist from './AppMoviePlaylist.vue'
import AppComingSoon from './AppComingSoon.vue'
import AppNewMovieCards from './AppNewMovieCards.vue'

export default {
    components:{
        AppJumbotron,
        AppNewMovieCarosell,
        AppMoviePlaylist,
        AppComingSoon,
        AppNewMovieCards,
    }
}
</script>

<template>
	<AppJumbotron/>
    <AppNewMovieCarosell/>
    <AppMoviePlaylist/>
    <AppComingSoon/>
    <AppNewMovieCards/>
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
	
</style>