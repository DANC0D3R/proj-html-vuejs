<script>
import { store } from '../store'

export default {
		props:{
			objectCategories: Object,
			objectInformation: Object,
		},
		data(){
			return{
				store
			}
		}
	}
</script>

<template>
    <footer>
		<section id="background">
			<div id="layover" class="w-100 h-100">
                <div class="my-container">
					<div class="my-row-between">
						<div class="col-3">
							<div class="title">	
								<h5>About Us</h5>
							</div>
							<p>Mauris malesuada arcu eu posuere eleifen. Ut egestas tortor at leo egestas tincidunt. Nam tincidunt metus tristique tristique viverra. Mauris erat ante, egestas vitae dapibus seds.</p>
							<!-- Icone Social -->
							<ul id="social-dots">
								<li v-for="(item,index) in store.socialIcons" :key="index">
									<a href="#" :class="item"></a>
								</li>
								<li>
									<a href="#" class="fa-brands fa-pinterest"></a>
								</li>
							</ul>
						</div>
						<div class="col-3">
							<div class="title">	
								<h5>{{ objectCategories.title }}</h5>
							</div>
							<ul class="list-column">
								<li v-for="(item,index) in objectCategories.list" :key="index">
									<a href="#" class="font-md">{{ item }}</a>
								</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</section>
		<div class="my-container" id="last-container">
			<div class="my-row-between">
				<div class="col-left">
					<ul>
						<li><a href="#" class="font-md">Tram and Conditions </a></li>
						<li><a href="#" class="font-md">Policy</a></li>
						<li><a href="#" class="font-md">About</a></li>
					</ul>
				</div>
				<div class="col-right">
					&copy;2020 <span class="color-green">&commat;Themepul</span> All Rights Reserved.
				</div>
			</div>
		</div>
	</footer>
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
@use '../assets/scss/variables' as *;
footer{
    color: #FFFFFF;
    #background{
        background-image: url('../assets/img/ft-bg.jpg');
        background-size: cover;
        #layover{
            background-color: $blue-grey;

            opacity: .92;
            .title{
                position: relative;

                margin-bottom: 2.25rem;
                h5::after{
                    content: "";

                    position: absolute;
                    left: 0;
                    bottom: -5px;

                    width: 33px;
                    height: 2px;

                    background: #FFFFFF;
                }
            }
            ul.list-column{
                li{
                    margin-bottom: 2rem;
                }
            }
            #social-dots{
                width: 80%;
                a{
                    text-align: center;
                    line-height: 2.5rem;

                    width: 2.5rem;
                    height: 2.5rem;

                    border-radius: 50%;
                    &.fa-facebook-f{
                        background-color: $facebook;
                    }
                    &.fa-twitter{
                        background-color: $twitter;
                    }
                    &.fa-linkedin-in{
                        background-color: $linkedin;
                    }
                    &.fa-instagram{
                        background-color: #C22D29;
                    }
                    &.fa-pinterest{
                        background-color: #AF0B1B;
                    }
                }
            }
        }
    }
    #last-container{
        .my-row-between{
            align-items: center;

            height: 4rem;
            ul{
                li{
                    padding-right: 1.5rem;
                }
            }
            a, .col-right{
                font-size: 1.15rem;
            }
        }
    }
}
</style>
