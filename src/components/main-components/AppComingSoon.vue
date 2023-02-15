<script >
export default{

}
</script>

<template>
    <section id="coming-soon">
			<div id="bg-layover" class="w-100 h-100">
				<div id="coming-info" class="text-center">
					<h3 class="color-green">COMING SOON MOVIE</h3>
					<h2>MAX STILL</h2>
					<div id="actors" class="py-3">
						<h3 class="mb-4">JON PLAYER <span class="color-green">&amp; </span>EMILY ROSE</h3>
						<h5>THE COUNTDOWN IS FINISHED!</h5>
					</div>
				</div>
			</div>
		</section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;
@use '../../assets/scss/general.scss' as *;
section{
    position: relative;

    height: 80vh;

    background-image: url('../../assets/img/coming-bg.jpg');
    background-position: center;
    background-size: cover;
    #bg-layover{
        background-color: rgba(15,24,40, 0.5);
        #coming-info{
            position: absolute;
            bottom: 50%;
            left: 50%;

            width: 25%;
            
            transform: translateY(50%);
            h2{
                font-size: 5rem;
                font-weight: 300;
            }
            #actors{
                background-color: $my-black;
                span{
                    font-size: 25px;
                }
            }
        }
    }
}
</style>