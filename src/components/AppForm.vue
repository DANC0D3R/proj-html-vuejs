<script>
	export default {
		
	}
</script>

<template>
	<div id="form" class="my-container">
		<div class="form-group text-center w-100">
			<input class="rounded-pill bg-mygreen" type="text" placeholder="First Name" name="FirstName">
			<input class="mx-4 rounded-pill bg-mygreen" type="text" placeholder="Last Name" name="LastName"> 
			<input class="rounded-pill bg-mygreen" type="email" placeholder="Email Address" name="Email"> <br>
			<input id="send" class="rounded-pill bg-mydark text-center d-block mx-auto" type="send" placeholder="Subscribe"> 
		</div>
	</div>
</template>

<style lang="scss">
@use '../assets/scss/variables' as *;
@use '../assets/scss/general.scss' as *;
#form{
    position: relative;
    bottom: 50px;

    height: 500px;

    margin-top: 150px;

    background-image: url('../assets/img/form-bg-1.png');
    background-repeat: no-repeat;
    background-size: cover; 
    .form-group{
        position: absolute;
        top: 25%;
        input{
            padding: 1rem 1.5rem;
            &::placeholder{
                color: #FFFFFF;
            }
        }
        input:not(#send){
            width: 25%;

            margin-bottom: 3rem;
            
            border: 1px solid #FFFFFF;

            outline: none;
            &:focus{
                border: 2px solid rgba(255,255,255,0.4);
            }
        }
        input#send{
            width: 12.5%;
            cursor: pointer;
            &::placeholder{
                font-weight: 700;
            }
        }
    }
}
</style>