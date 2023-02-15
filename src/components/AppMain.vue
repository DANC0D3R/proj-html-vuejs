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
    <div class="button-box">
        <button class="top-page">
        <a href="#"><i class="fa-brands fa-vuejs"></i></a>
    </button>
    </div>
</template>

<style lang="scss">
@use '../assets/scss/variables' as *;
@use '../assets/scss/general.scss' as *;
.button-box{
    position: fixed;
    bottom: 3rem;
    right: 3rem;

    width: 4rem;
    height: 4rem;

    transform: rotate(180deg);

    z-index: 2;
    .top-page{
        width: 100%;
        height: 100%;

        border: 2px solid $my-green;
        border-radius: 50%;

        background-color: $my-black;

        background-color: transparent;
        &:hover{
            background-color: #FFFFFF;
        }
        i{
            font-size: 2.8rem;
            &:hover{
            color: #FFFFFF;
        }
        }
    }
}
</style>