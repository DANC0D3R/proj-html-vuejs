<script >
import { store } from '../store';
import  AppCardNewList from './AppCardNewList.vue'

export default {
    components:{
        AppCardNewList,
    },
    data(){
        return{
            store,
        }
    }
}
</script>

<template>
    <section id="news">
			<div class="my-container">
                <!-- Titolo Sezione -->
				<div class="section-header">
					<h3>Latest News</h3>
					<p>Lorem Ipsum is simply dummy text of the printing and typesettin</p>
				</div>
				<AppCardNewList/>
			</div>
		</section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;
@use '../assets/scss/general.scss' as *;
.section-header{
    p{
        margin-bottom: 0;

        font-size: 16px;
        font-weight: 300;
    }
}
</style>