<script >
import { store } from '../store';
import AppCardMovieList from './AppCardMovieList.vue'

export default {
    components:{
        AppCardMovieList,
    },
    data(){
        return{
            categorySelected: '',
            store,
        }
    }
}
</script>

<template>
    <section id="movie-cards">
			<div class="my-container">
                <!-- Titolo Sezione -->
				<div class="section-header">
					<h3>New Movie</h3>
					<p>Lorem Ipsum is simply dummy text of the printing and typesettin</p>
				</div>
				<nav class="w-50">
					<ul>
						<li v-for="(item,index) in store.mediaCategories" :key="index" class="movie-category" @click="categorySelected=item.name">
							<a href="#movie-cards">{{ item.name }}</a>
						</li>
					</ul>
				</nav>
                <!-- Passa la prop della categoria selezionata alla lista movie -->
                <AppCardMovieList :category-selected="categorySelected"/>
			</div>
		</section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;
@use '../assets/scss/general.scss' as *;
section{
    .section-header{
        p{
            margin-bottom: 0;

            font-size: 16px;
            font-weight: 300;
        }
    }
    nav{
        margin-bottom: 75px;
        ul{
            li.movie-category{
                a{
                    font-size: 18px;
                    
                    cursor: pointer;
                }
            }
        }
    }
}
</style>