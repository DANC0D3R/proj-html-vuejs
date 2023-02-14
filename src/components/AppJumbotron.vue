<script>
	export default {
		data(){
			return{
				silderFlag: true
			}
		},
		computed:{
			// Funzione che restituisce il path dell'immagine in base alla flag
			sliderImg(){
				const imgPath = '/src/assets/img/slider.jpg'
				if(this.silderFlag == true ){
					return imgPath
				}
				else{
					return '/src/assets/img/slider-2.jpg'
				}
			}
		},
		methods: {
			// Alternare la flag
			changeImg(){
				if(this.silderFlag){
					this.silderFlag = false
				}
				else{
					this.silderFlag = true
				}
			}
		},
	}
</script>

<template>
	<div id="jumbotron">
		<img :src="sliderImg" alt="slider-image" class="img-fluid h-100">
        <!-- Al click sull'arrow cambia l'immagine -->
		<div class="arrow-slider left rounded-circle" @click="changeImg()">
			<i class="fa-brands fa-vuejs"></i>
		</div>
        <!-- Al click sull'arrow cambia l'immagine -->
		<div class="arrow-slider right rounded-circle" @click="changeImg()">
			<i class="fa-brands fa-vuejs"></i>
		</div>
		<div id="slider-content" class="text-center">
			<h5>Welcome To Our Movie Site</h5>
			<h2>OUR SPECIAL <span class="color-green">MOVIES</span></h2>
			<p>Lorem Ipsum is simply dummy text of the printing and typesetting industrioy. Lorem Ipsum has been the industry standard dummy text ever since the 1500s, when an unknown</p>
			<button class="rounded-pill">Read More</button>
		</div>
	</div>
</template>

<style lang="scss">
@use '../assets/scss/variables' as *;
@use '../assets/scss/general.scss' as *;
#jumbotron{
    position: relative;

    height: 93vh;
    img{
        object-fit: cover;
        
        cursor: pointer;
    }
    &:hover{
        .arrow-slider{
            display: block;
        }
    }
    .arrow-slider{
        display: none;
        text-align: center;

        position: absolute;
        bottom: 50%;

        width: 3rem;
        height: 3rem;
        cursor: pointer;
        &:hover{
            background-color: rgba(0,0,0,0.8);
        }
        &.left{
            transform: translateY(+50%) rotate(90deg);
            left: 2rem;
        }
        &.right{
            transform: translateY(+50%) rotate(-90deg);
            right: 2rem;
        }
        i{
            color: $my-green;
            
            font-size: 2rem;
            line-height: 3rem;
        }
    }
    #slider-content{
        position: absolute;
        top: 30%;
        right: 25%;

        width: 30%;
        h2, h2 span{
            font-size: 3.5rem;
            font-weight: 300;
            letter-spacing: -3px;
        }
        button{
            padding: .65rem 2rem;
        }
    }
}
</style>