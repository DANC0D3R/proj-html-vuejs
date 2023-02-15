<script>
import AppJumbotron from './AppJumbotron.vue'
import AppNewMovieCarosell from './AppNewMovieCarosell.vue'
import AppMoviePlaylist from './AppMoviePlaylist.vue'
import AppComingSoon from './AppComingSoon.vue'
import AppNewMovieCards from './AppNewMovieCards.vue'
import AppLatestNewsCards from './AppLatestNewsCards.vue'
import AppForm from './AppForm.vue';

export default {
    components:{
        AppJumbotron,
        AppNewMovieCarosell,
        AppMoviePlaylist,
        AppComingSoon,
        AppNewMovieCards,
        AppLatestNewsCards,
        AppForm,
    }
}
</script>

<template>
	<AppJumbotron/>
    <AppNewMovieCarosell/>
    <AppMoviePlaylist/>
    <AppComingSoon/>
    <AppNewMovieCards/>
    <AppLatestNewsCards/>
    <AppForm/>
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
	
</style>