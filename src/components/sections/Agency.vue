<template>
    <section class="container">
        <div class="agency">
            <div class="section-title">
                <h2 class="title">Meet The New Agencv SEO Template From The Avada Team</h2>
                <p class="text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.</p>
            </div>
            <div class="cards">
                <div class="card">
                    <div class="top">
                        <div class="icon">
                            <i class="fas fa-road"></i>
                        </div>
                        <div class="title">
                            <h3>Estabilish Goals</h3>
                        </div>
                    </div>
                    <div class="text">
                        <p>Aliquam non elit lacus. Praesent aliquet, ipsum id scelerisque convallis mi ligula euismod odio vel dictum mi risus a mi.</p>
                    </div> 
                </div>
                <div class="card">
                    <div class="top">
                        <div class="icon">
                            <i class="fas fa-video"></i>
                        </div>
                        <div class="title">
                            <h3>Work With a Team</h3>
                        </div>
                    </div>
                    <div class="text">
                        <p>Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet consectetur adipisce.</p>
                    </div> 
                </div>
                <div class="card">
                    <div class="top">
                        <div class="icon">
                            <i class="fas fa-tint"></i>
                        </div>
                        <div class="title">
                            <h3>Get Results</h3>
                        </div>
                    </div>
                    <div class="text">
                        <p>Vestibulum scelerisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.</p>
                    </div> 
                </div>
            </div>
            <div class="desktop-img">
                <img class="image" src="../../assets/images/agency-seo-desk-front.jpg" alt="desktop image">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Agency'
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include sectionTitle;
.agency {
    margin-top: 100px;
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
            background-color: #fff;
            text-align: center;
            padding: 3rem 1.5rem;
            .top {
                transition: color .2s;
                .icon {
                    color: $Yellow_Orange;
                    font-size: 2rem;
                    margin-bottom: 2rem;
                }
                &:hover {
                    color: $Yellow_Orange;
                }
            }
            .text {
                font-size: 1.2rem;
                line-height: 2rem;
                color: $Scorpion;
                margin-top: 1rem;
            }
        }
    }
    .desktop-img {
        width: 100%;
        .image {
            display: block;
            width: 100%;
        }
    }
}
</style>