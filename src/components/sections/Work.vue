<template>
    <section class="container">
        <div class="work">
            <div class="section-title">
                <h2 class="title">Our Work</h2>
                <p class="text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
            </div>
            <div class="cards">
                <div class="card" v-for="(card, index) in cards" :key="index">
                    <div class="card-image">
                        <img class="img" :src="require('../../assets/images/' + card.img)" :alt="card.title">
                    </div>
                    <a class="card-link" :href="card.link">
                        <i class="fas fa-link"></i>
                    </a>
                </div>
            </div>
            <button class="button">View our work</button>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Work',
    data() {
        return {
            cards: [
                {
                    img: 'case-study-gallery-3-1.jpg',
                    link: '#',
                    title: 'case study 3'
                },
                {
                    img: 'case-study-gallery-2.jpg',
                    link: '#',
                    title: 'case study 2'
                },
                {
                    img: 'case-study-gallery-1-1.jpg',
                    link: '#',
                    title: 'case study 1'
                },
                {
                    img: 'case-study-gallery-4-1.jpg',
                    link: '#',
                    title: 'case study 4'
                },
                {
                    img: 'case-study-gallery-5-1.jpg',
                    link: '#',
                    title: 'case study 5'
                },
                {
                    img: 'case-study-gallery-6-1.jpg',
                    link: '#',
                    title: 'case study 6'
                }
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
.work {
    margin: 100px;
    text-align: center;
    .section-title .text {
        color: $Scorpion;
    } 
    .cards {
        display: grid;
        grid-template-columns: repeat(3, 32%);
        justify-content: space-between;
        row-gap: 1.5rem;
        margin: 100px 0 50px;
        .card {
            width: 100%;
            position: relative;
            &-image {
                width: 100%;
                .img {
                    display: block;
                    width: 100%;
                }
            }
            &-link {
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background-image: linear-gradient($Science_Blue, rgb(157, 201, 243));
                opacity: 0;
                transition: opacity .6s;
                display: flex;
                align-items: center;
                justify-content: center;
                color: white;
                font-size: 2.5rem;
            }
            &:hover {
                .card-link {
                    opacity: .8;
                }
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