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
					dropdown: true,
					dropdownList: [
						{ label: 'Home'},
						{ label: 'Home 2'},
						{ label: 'Home 3'},
						{ label: 'Home 4'},
						{ label: 'Home 5'},
						{ label: 'Home 6'},
					]
				},
				{
					title: 'Celebrity',
					dropdown: true,
					dropdownList: [
						{ label: 'Celebrity'},
						{ label: 'Celebrity 2'},
					]
				},
				{
					title: 'Movie',
					dropdown: true,
					dropdownList: [
						{ label: 'Single Movie'},
						{ label: 'Top Rate Movie'},
						{ label: 'Movie Category'},
					]
				},
				{
					title: 'Page',
					dropdown: true,
					dropdownList: [
						{ label: 'My Account'},
					]
				},
				{
					title: 'Shop',
					type: 'Dropdwon',
					dropdownList: [
						{ label: 'Pricing Table'},
						{ label: 'Cart'},
						{ label: 'Wishlist'},
					]
				},
				{
					title: 'Blog',
					dropdown: false,
					type: 'link'
				},
				{
					title: 'Contact Us',
					dropdown: false,
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
	<!-- Passa l'array della navbar come prop all'header  -->
	<AppHeader :arraynav="navbar"></AppHeader>
	<AppMain></AppMain>
	<!-- Passa gli oggetti 'categories' e 'information' come props al footer  -->
	<AppFooter :objectCategories="categories" :objectInformation="information"></AppFooter>
</template>

<style lang="scss" scoped>
@use './assets/scss/general.scss' as *;
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap');
</style>
