<script>
import { store } from '../store'

export default {
		data(){
			return{
                store,
				socialIcons: [
				"fa-brands fa-facebook-f",
				"fa-brands fa-twitter",
				"fa-brands fa-linkedin-in",
				"fa-brands fa-instagram",
				"fa-brands fa-google-plus-g",
				]
			}
		}       
	}
</script>

<template>
    <header>
        <!-- Parte Superiore -->
		<div class="my-container" id="top-container">
			<div class="my-row-between">
                <!-- Parte Sinistra -->
				<div class="col-left ">
					<div class="my-row-between">
						<div>
							<i class="fa-regular fa-envelope me-1"></i>
							<span>Superhit Top Movie </span>
							<p class="color-green">** King Star **</p>
						</div>
                        <!-- Icone Social -->
						<ul>
							<li v-for="(item,index) in socialIcons" :key="index">
								<a href="#">
									<i :class="item"></i>
								</a>
							</li>
						</ul> 
					</div>
				</div>
                <!-- Parte Destra -->
				<div class="col-right">
					<a id="login" href="#">
						<i class="fa-solid fa-lock me-1"></i>
						<span>Login</span> 
					</a>
				</div>
			</div>
		</div>
		<!-- Parte Centrale -->
        <section>
            <div class="my-container py-3">
                <div class="my-row-between mb-4">
                    <!-- Logo -->
                    <div id="logo">
                        <img src="../assets/img/cropped-logo.png" alt="logo">
                    </div>
                    <!-- Barra di Ricerca  -->
                    <div id="searchbar" class="mt-4">
                        <input type="text" class="border-secondary p-3" placeholder="Search ...">
                        <button class="py-3 px-4">Search</button>
                    </div>
                </div>
            </div>
        </section>
        <!-- Barra di Navigazione  -->
		<nav class="my-container">
			<div class="my-row-between align-items-center">
                <!-- Menu -->
				<ul>
					<li v-for="(item,index) in store.menu" :key="index">
						<a href="#">
							<h4>
								{{ item.name }}
								<!-- Se l'item ha un dropdwon al suo interno si visualizza l'arrow sown  -->
								<i v-if="item.dropdownList" class="fa-solid fa-caret-down"></i>
							</h4>
						</a>

					</li>
				</ul>
				<div id="cart">
					<i class="fa-solid fa-basket-shopping"></i>
					<span class="green-dot">0</span>
				</div>
			</div>
		</nav>
	</header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/general.scss' as *;
@use '../assets/scss/variables' as *;
header{
    #top-container{
        .my-row-between{
            align-items: center;

            height: 4rem;
            i, span{
                color:#FFFFFF;
            }
            p{
                display: inline;
            }
            .col-left{
                ul{
                    i{
                        margin-left: 1rem;
                        &.fa-facebook-f{
                            color: $facebook;
                        }
                        &.fa-twitter{
                            color: $twitter;
                        }
                        &.fa-linkedin-in{
                            color: $linkedin
                        }
                        &.fa-instagram{
                            color: #FF0000;
                        }
                        &.fa-google-plus-g{
                            color: #FF6A00;
                        }

                    }
                }
            }
            .col-right{
                #login{
                    i{
                        font-size: .8rem;
                    }
                    span{
                        vertical-align: middle;
                    }
                }
            }
        }
    }
    section{
        border-top: $border-blue-grey;
        border-bottom: $border-blue-grey;
        .my-row-between{
            input{
                width: 255px;

                caret-color: $my-green;
                background-color: $my-black;

                outline: none;
            }
            button{
                border: none;

                background-color: $my-green;
            }
        }
    }
    nav{
        ul{			
            h4{
                margin-bottom: 0;

                padding: 2rem 2.5rem 2rem 0;

                font-size: 1.2rem;
                i{
                    position: relative;

                    font-size: 1.2rem;
                }
            }		
        }
        #cart{
            position: relative;

            color: #FFFFFF;
            .green-dot{
                position: absolute;
                top: -12px;
                left: 7px;
                
                display: inline-block;
                text-align: center;
                line-height: 1.2rem;

                width: 1.2rem;
                height: 1.2rem;

                font-size: .75rem;
                
                border-radius: 50%;

                color: #FFFFFF;
                background-color: $my-green;
            }
        }
    }
}
</style>
