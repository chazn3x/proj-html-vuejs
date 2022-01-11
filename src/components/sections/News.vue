<template>
    <section class="container">
        <div class="news">
            <div class="section-title">
                <h2 class="title">Our News</h2>
                <p class="text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
            </div>
            <div class="cards">
                <div class="card" v-for="(card, index) in cards" :key="index">
                    <a class="card-img" href="#">
                        <img class="img" :src="require('../../assets/images/' + card.img)" :alt="card.title">
                    </a>
                    <div class="card-title">
                        <a href="#"><h3>{{card.title}}</h3></a>
                    </div>
                    <div class="card-date">November 1st, 2017</div>
                    <div class="card-text">
                        <p>ALorem ipsum dolor sit amet, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque augue, at gravida mi blandit</p>    
                    </div> 
                </div>
            </div>
            <a class="button" href="#">Go to news</a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'News',
    data() {
        return {
            cards: [
                {
                    img: 'related-service-2-700x441.jpg',
                    title: 'Why You Need A SEO Agency Now'
                },
                {
                    img: 'related-service-4-700x441.jpg',
                    title: 'SEO Tips For Your Startup'
                },
                {
                    img: 'blog-post-6-700x441.jpg',
                    title: 'Image Optimization For Your Site'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include sectionTitle;
@include button;
.news {
    margin: 100px 0;
    text-align: center;
    .section-title .text {
        color: $Scorpion;
    } 
    .cards {
        display: grid;
        grid-template-columns: repeat(3, 32%);
        justify-content: space-between;
        margin: 100px 0 50px;
        .card {
            width: 100%;
            text-align: center;
            &-img {
                display: block;
                width: 100%;
                height: 250px;
                position: relative;
                overflow: hidden;
                .img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                    position: absolute;
                    top: 0;
                    left: 0;
                    transition: 1s;
                }
                &:hover {
                    .img {
                        transform: scale(1.1);
                        -webkit-transform: scale(1.1);
                        opacity: .9;
                    }
                }
            }
            &-title {
                color: $Yellow_Orange;
                margin: .7rem 0 .3rem;
            }
            &-text {
                font-size: 1.1rem;
                line-height: 2rem;
                color: $Scorpion;
                margin-top: 1rem;
            }
        }
    }
    .button {
        background-color: $Yellow_Orange;
        &:hover {
            background-color: $Tulip_Tree-light-vibrant;
        }
    }
}
</style>