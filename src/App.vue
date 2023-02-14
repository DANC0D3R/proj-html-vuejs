<script>
import axios from 'axios'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
    components: {
    	AppHeader,
    	AppMain,
    	AppFooter,
    },
    data(){
		return{
			// HEADER 
			navbar: [
				{
					title: 'Home',
					type: 'Dropdwon',
					dropdownList: [
						'Home',
						'Home 2',
						'Home 3',
						'Home 4',
						'Home 5',
						'Home 6',
					]
				},
				{
					title: 'Celebrity',
					type: 'Dropdwon',
					dropdownList: [
						'Celebrity',
						'Celebrity',
					]
				},
				{
					title: 'Movie',
					type: 'Dropdwon',
					dropdownList: [
						'Single Movie',
						'Top Rate Movie',
						'Movie Category',
					]
				},
				{
					title: 'Page',
					type: 'Dropdwon',
					dropdownList: [
						'My Account',
					]
				},
				{
					title: 'Shop',
					type: 'Dropdwon',
					dropdownList: [
						'Pricing Table',
						'Cart',
						'Wishlist',
					]
				},
				{
					title: 'Blog',
					type: 'link'
				},
				{
					title: 'Contact Us',
					type: 'link'
				}
			],
			// FOOTER
			categories: {
				title: 'Movie Category',
				list: [
					'English New Movie',
					'Hindi All Movie',
					'Latest Tamil Movie',
					'New Top Rating Movie',
					'Hornn New Movie',
					'Animation New Movie'
				]
			},
			information: {
				title: 'Information',
				list: [
					'Youtube Video Post',
					'Actor Information',
					'New Promotion',
					'Latest Movie In English',
					'Latest Flim Product',
					'Video New Video'
				]
			}
			
		}
	}
}
</script>

<template>
	<AppHeader :arraynav="navbar"></AppHeader>
	<AppMain></AppMain>
	<AppFooter :objectCategories="categories" :objectInformation="information"></AppFooter>
</template>

<style lang="scss" scoped>
@use './assets/scss/general.scss' as *;
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
</style>
