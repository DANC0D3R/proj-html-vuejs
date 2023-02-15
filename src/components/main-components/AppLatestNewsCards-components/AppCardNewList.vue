<script>
import { store } from '../../../store';
import AppCardBigNews from './AppCardNewList-components/AppCardBigNews.vue';
import AppCardNews from './AppCardNewList-components/AppCardNews.vue';

export default {
    components:{
        AppCardBigNews,
        AppCardNews,
    },
    data(){
        return{
            store,
        }
    },
}
</script>

<template>
	<div class="my-row-between" id="news">
        <!-- Card Grande -->
		<div id="big-news">
			<AppCardBigNews/>
		</div>
        <!-- 4 Cards Piccole -->
		<div id="grid" class="my-row-between flex-wrap align-content-between">
			<!-- Ciclo che scorre i 4 post restanti e li inserisce nella griglia  -->
			<AppCardNews v-for="(item,index) in store.posts.slice(1,5)" :key="index" :card="item"/>
		</div>
	</div>
</template>

<style lang="scss">
@use '../../../assets/scss/variables' as *;
@use '../../../assets/scss/general.scss' as *;
#big-news, #grid{
    width: calc(100% / 2 - 1.2rem);
}
</style>