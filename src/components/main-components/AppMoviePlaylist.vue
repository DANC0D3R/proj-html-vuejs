<script>
export default{
    data(){
        return{
            pathBase: '/src/assets/img/',
            newMovies: [
                {
                    title: 'Quisque auctor Movie in Strack',
                    finalPath: '2-300x300.jpg',
                    views: 953,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'New Movie Quisque in Strack',
                    finalPath: '5-300x300.jpg',
                    views: 722,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'Movie Action Garila English',
                    finalPath: '3-300x300.jpg',
                    views: 364,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'Action Garila English Movie',
                    finalPath: '3-1-300x300.jpg',
                    views: 296,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'Donec English Action movie',
                    finalPath: '2-1-300x300.jpg',
                    views: 481,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'English Action movie in Strack',
                    finalPath: '4-1-300x300.jpg',
                    views: 277,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'Movie Auctor Quisque in Strack',
                    finalPath: '6-300x300.jpg',
                    views: 300,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'auctor Movie Quisque in Strack',
                    finalPath: '5-300x300.jpg',
                    views: 343,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'Donec Movie Quisque in Strack',
                    finalPath: '2-300x300.jpg',
                    views: 361,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                },
                {
                    title: 'New Movie Quisque in Strack',
                    finalPath: '1-2-300x300.jpg',
                    views: 503,
                    date: 'Febrary 12, 2016',
                    time: '2.30.00'
                }
            ]
        }
    }
}
</script>

<template>
    <section id="movie-playlist">
			<div class="my-container">
                <!-- Titolo Sezione -->
				<div class="section-header">
					<h3>Movie Playlist</h3>
					<p>Lorem Ipsum is simply dummy text of the printing and typesettin</p>
				</div>
				<div class="my-row-between">
					<!-- Video Youtube  -->
					<div id="yt-container" class="col-8 pe-4">
						<iframe class="w-100" height="545" src="https://www.youtube.com/embed/BP0k4SdquG0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
					</div>
					<!-- Lista movies con slider verticale  -->
					<div id="movie-list" class="col-4 ps-3">
						<div id="movie-list-header" class="py-3">
							<h5>New Movie</h5>
							<span>Plying 24</span>
						</div>
						<div id="movie-list-main" class="pb-5">
							<ul class="list-column">
								<!-- Ciclo che scorre gli oggetti movies dell'array newMovies  -->
								<li v-for="(item,index) in newMovies" :key="index" class="mt-4">
									<div class="my-row-between">
										<div class="movie-cover img-fluid">
											<img :src="pathBase + item.finalPath" :alt="item.title" class="img-fluid">
										</div>
										<div class="movie-info ps-3">
											<a href="movie-playlist">
                                                <h5>{{ item.title }}</h5>
                                            </a>
											<h6>{{ item.views }} views</h6>
											<div class="my-row-between">
												<span>{{ item.date }}</span>
												<span>{{ item.time }}</span>
											</div>
										</div>
									</div>
								</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
		</section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;
@use '../../assets/scss/general.scss' as *;
section{
    .section-header{
        p{
            margin-bottom: 0;

            font-size: 16px;
            font-weight: 300;
        }
    }
    #movie-list{
        #movie-list-header, #movie-list-main{
            padding-left: 1.25rem;
            padding-right: 1.25rem;

            background-color: $blue-grey;
        }
        #movie-list-main{
            max-height: 480px;

            margin-top: 1px;

            overflow-y: scroll;
            ul{
                li{
                    .movie-cover{
                        width: 30%;
                    }
                    .movie-info{
                        h6{
                            font-size: 13px;
                        }
                    }
                }
            }
        }
    }
}
</style>