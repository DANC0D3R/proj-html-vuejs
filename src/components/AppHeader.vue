<script>
import { store } from '../store'
export default {
    props:{
        arraynav: Array
    },
    data(){
        return{
            store
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
						<div class="pe-3">
							<i class="fa-regular fa-envelope me-1"></i>
							<span>Superhit Top Movie </span>
							<b class="color-green">** King Star **</b>
						</div>	
                        <!-- Social -->				
						<ul>
							<!-- Ciclo che scorre le icone nell'array presente nel file store -->
							<li v-for="(item,index) in store.socialIcons" :key="index">
								<a href="#">
									<i :class="item"></i>
								</a>
							</li>
							<li>
								<a href="#">
									<i class="fa-brands fa-google-plus-g"></i>
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
					<!-- Barra di Ricerca -->
					<div id="searchbar" class="mt-4">
						<input type="text" class="border-secondary p-3 bg-my-black" placeholder="Search ...">
						<button class="py-3 px-4" id="search">Search</button>
					</div>
				</div>
			</div>
		</section>
		<!-- NAVBAR  -->
		<nav class="my-container">
			<div class="my-row-between align-items-center">
                <!-- Menu -->
				<ul>
					<!-- Ciclo che scorre gli item -->
					<li v-for="(item,index) in arraynav" :key="index" class="nav-item">
						<a href="#">
							<h4>
								{{ item.title }}
								<!-- Se l'item ha un dropdwon al suo interno si visualizza l'arrow down -->
								<i v-if="item.dropdownList" class="fa-solid fa-caret-down"></i>
							</h4>
						</a>
						<!-- Dropdown -->
                        <!-- Se la proprietà 'dropdown' dell'item risulta vera si visualizza il menu -->
						<div v-if="item.dropdown" class="dropdown dropdown-menu bg-my-black p-3">
							<ul class="list-column my-3">
								<!-- Ciclo che scorre i dropdown-item nell'array della proprietà 'dropdownList' presente negli item del menu -->
								<li v-for="(link,index) in item.dropdownList" :key="index">
									<a href="#">
										{{ link.label }}
									</a> 
								</li>					
							</ul>
						</div>
					</li>
				</ul>
				<div id="cart" class="ms-3">
					<i class="fa-solid fa-basket-shopping"></i>
					<span class="green-dot">0</span>
					<!-- Dropdown -->
					<div class="dropdown-menu">No products in the cart.</div>
				</div>
			</div>
		</nav>
	</header>
</template>

<style lang="scss">
@use '../assets/scss/general.scss' as *;
@use '../assets/scss/variables' as *;

header{
    #top-container{
        .my-row-between{
            align-items: center;
            height: 4rem;
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
                        font-size: 0.8rem;
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
            // Barra di Ricerca
            input{
                width: 250px;

                caret-color: $my-green;

                outline: none;
            }
            #search{
                border: none;

                background-color: $my-green;
            }
            
        }
    }
    // Navbar
    nav{
        ul{	
            li.nav-item{
                position: relative;
                &:hover{
                    .dropdown{
                        display: block;
                    }
                }
                h4{
                    font-size: 1.2rem;

                    margin-bottom: 0;

                    padding: 2rem 2.5rem 2rem 0;
                    i{
                        position: relative;

                        font-size: 1.2rem;
                    }
                }		
                // Dropdown
                .dropdown{
                    top: 70%;
                    left: -1rem;
                    li{
                        position: relative;
                        line-height: 3rem;
                        &:hover{
                            .second-dropdown{
                                display: block;
                            }
                        }
                        
                        span.arrow{
                            position: absolute;
                            right: 1px;

                            font-size: 1.25rem;
                        }
                        .second-dropdown{
                            top: 0;
                            left: 100%;
                        }
                    }
                }
            }
        }
        #cart{
            position: relative;
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
            }
            &:hover{
                .dropdown-menu{
                    display: block;
                    top: 50px;
                    right: -1rem;

                    width: 320px;

                    padding: 35px;
                }
            }
        }
    }
}
</style>