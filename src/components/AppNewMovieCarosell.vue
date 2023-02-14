<script >
export default{
    data(){
        return{
            movieList:[
                {
                    img:'1.jpg',
                    title: 'Hurry Animate Blue Strack New Movie',
                    category: 'Top Rating',
                    views: '381',
                    star: '0/10'
                },
                {
                    img: '2.jpg',
                    title: 'Quisque Auctor Movie In Strack',
                    category: 'Coming Soon',
                    views: '947',
                    star: '4/10'
                },
                {
                    img: '5.jpg',
                    title: 'New Movie Quisque In Strack',
                    category: 'Latest Movie',
                    views: '721',
                    star: '0/10'
                },
            ]
        }
    },
    methods:{
        prova(arr, old_index1, new_index1, old_index2, new_index2){
            this.array_move(arr, old_index1, new_index1);

            this.array_move(arr, old_index2, new_index2);
        },
        array_move(arr, old_index, new_index){
            if (new_index >= arr.length) { 
                let k = new_index - arr.length + 1; 
                while (k--) { 
                    arr.push(undefined); 
                } 
            }
            arr.splice(new_index, 0, arr.splice(old_index, 1)[0]); 
            return arr; 
        },
        getImagePath(imgPath) {
            return new URL(`../assets/img/${imgPath}`, import.meta.url).href;
        }

    }
}
</script>

<template>
    <section>
        <div class="container py-5">
            <div class="row">
                <div class="col-11 mb-5 carousel-top-box">
                    <p class="m-0 mb-3 text-white">
                        <span class="fw-bold fs-5">New Movie</span>
                        <p class="m-0 text-white">Lorem Ipsum is simply dummy text of the printing and typesettin</p>
                    </p>
                </div>
                <!-- Controlli scorrimento carosello -->
                <div class="col-1 mb-5">
                    <p class="d-flex justify-content-between">
                        <!-- Sinistra -->
                        <div class="arrow-slider left rounded-circle" @click="array_move(movieList, 2 , 0, 1, 2)">
                            <i class="fa-brands fa-vuejs"></i>
                        </div>
                        <!-- Destra -->
                        <div class="arrow-slider right rounded-circle" @click="array_move(movieList, 0 , 2, 1, 0)">
                            <i class="fa-brands fa-vuejs"></i>
                        </div>
                    </p>
                </div>
                <div v-for="movie,index in movieList" class="col-4 p-0" :class="index == 1 ? `div_centrale mt-4` : ``">
                    <img :src=getImagePath(movie.img) alt="1">
                    <p class="text-white m-0">
                        <i class="fa-solid fa-star"></i>
                        {{movie.star}}
                    </p>
                    <h2 class="text-white m-0 text-up">
                        {{movie.title}}
                    </h2>
                    <h2 class="text-white m-0 text-down">
                        Category: {{movie.category}}
                    </h2>
                    <a href="#" class="button-left">Details</a>
                    <a href="#" class="button-right">{{movie.views}} Views</a>
                </div>
            </div>
        </div>        
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;

section{
    background-color: $my-black;
    .carousel-top-box{
        border-left: 1px solid $my-green;
        border-bottom: 1px solid $blue-grey;
    }
    .arrow-slider{
        margin:  0px;

        padding: 0 8px;

        cursor: pointer;
        &.left{
            transform: rotate(90deg);
        }
        &.right{
            transform: rotate(-90deg);
        }
        i{
            font-size: 1.5rem;

            color: $my-green;
        }
    }
    img{
        width: 100%;
        height: 100%;

        border-radius: 25px;
    }
    div.col-4.div_centrale{
        height: 650px;

        z-index: 1;
        img{
            filter: brightness(0.6);
        }

        h2.text-up{
            filter: brightness(1);
        }

        h2.text-down{
            filter: brightness(1);
        }

        p{
            filter: brightness(1);
        }

        a.button-left{
            filter: brightness(1);
        }

        a.button-right{
            filter: brightness(1);
        }
        .fa-star{
        color: $my-green;
        }
    }
    div.col-4{
        position: relative;

        height: 550px;

        margin-top: 60px;
        img{
            filter: brightness(0.3);
        }
        p{
            position: absolute;
            top: 35px;
            right: 25px;
            
            filter: brightness(0.3);
        }
        h2.text-up{
            position: absolute;
            left: 25px;
            bottom: 175px;

            font-size: 1.2rem;

            filter: brightness(0.3);
        }
        h2.text-down{
            position: absolute;
            left: 25px;
            bottom: 125px;

            font-size: 1.2rem;

            filter: brightness(0.3);
        }
        a.button-left{
            position: absolute;
            left: 0;
            bottom: 20px;

            text-align: end;

            width: 80px;

            padding: 0.5rem 1rem;

            border-top-right-radius: 25px;
            border-bottom-right-radius: 25px;

            color: #FFFFFF;
            background-color: $my-black;

            text-decoration: none;

            filter: brightness(0.3);
        }
        a.button-right{
            position: absolute;
            right: 0;
            bottom: 20px;

            width: 110px;

            padding: 0.5rem 1rem;

            border-top-left-radius: 25px;
            border-bottom-left-radius: 25px;

            color: #FFFFFF;
            background-color: $my-black;

            text-decoration: none;

            filter: brightness(0.3);
        }
    }
}
</style>