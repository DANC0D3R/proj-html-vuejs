<script>
import AppCardMovie from './AppCardMovie.vue'
export default {
    components:{
        AppCardMovie,
    },
    data(){
        return{
            movieCardsArray: [
                {
                    title: 'Hurry Animate Blue Strack New Movie',
                    category: 'Top Rating',
                    finalPath: '1.jpg',
                    views: 381,
                    stars: 0,
                    time: '2.30.00',
                    release: 'February 12, 2016',
                    genres: 'Drama, Action Releas'
                },
                {
                    title: 'Animate Blue Strack New Movie',
                    category: 'Latest Movie',
                    finalPath: '5-1.jpg',
                    views: 344,
                    stars: 0,
                    time: '2.30.00',
                    release: 'February 12, 2016',
                    genres: 'Drama, Action Releas'
                },
                {
                    title: 'Blue Strack New Animate Movie',
                    category: 'Coming Soon',
                    finalPath: '3.jpg',
                    views: 420,
                    stars: 0,
                    time: '2.30.00',
                    release: 'February 12, 2016',
                    genres: 'Drama, Action Releas'
                },
                {
                    title: 'Nulla Strack New Animate Movie',
                    category: 'TV Series',
                    finalPath: '4.jpg',
                    views: 325,
                    stars: 0,
                    time: '2.30.00',
                    release: 'February 12, 2016',
                    genres: 'Drama, Action Releas'
                },
                {
                    title: 'Quisque In Strack New Movie',
                    category: 'Top Rating',
                    finalPath: '3-222x300.jpg',
                    views: 340,
                    stars: 1,
                    time: '2.30.00',
                    release: 'February 12, 2016',
                    genres: 'Drama, Action Releas'
                },
                {
                    title: 'New Movie Quisque In Strack',
                    category: 'Latest Movie',
                    finalPath: '2.jpg',
                    views: 503,
                    stars: 0,
                    time: '2.30.00',
                    release: 'February 12, 2016',
                    genres: 'Drama, Action Releas'
                }
            ]
        }
    }
}
</script>

<template>
	<div class="my-row-between flex-wrap">
		<!-- Ciclo che scorre gli oggetti dell'array movieCardsArray, passaggio dell'oggetto (card) come prop alla componente AppCardMovie  -->
		<AppCardMovie v-for="(item,index) in movieCardsArray" :key="index" :card="item" />
	</div>
</template>

<style lang="scss">
@use '../assets/scss/variables' as *;
@use '../assets/scss/general.scss' as *;
	
</style>