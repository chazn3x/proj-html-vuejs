
<template>
    <section>
        <div class="container">
            <div class="feedback">
                <h2 class="title">What Our Clients Say</h2>
                <div class="clients">
                    <div class="client" v-for="(client, index) in clients" :key="index" :class="{'active' : selected == index}">
                        <div class="client-avatar">
                            <img :src="require('../../assets/images/' + client.avatar)" :alt="'testimonial' + index" class="img">
                        </div>
                        <p class="client-feedback">{{client.feedback}}</p>
                        <div class="client-name">
                            <span class="name">{{client.name}}</span><span class="role">, {{client.role}}</span>
                        </div>
                    </div>
                </div>
                <div class="dots">
                    <div class="dot" v-for="(dot,index) in clients" :key="index" :class="{'active' : selected == index}" @click="selected = index"></div>
                </div>
                <div class="logos">
                    <div class="logo">
                        <img src="../../assets/images/clients_partner_5-200x202.png" alt="" class="img">
                    </div>
                    <div class="logo">
                        <img src="../../assets/images/clients_partner_6-200x202.png" alt="" class="img">
                    </div>
                    <div class="logo">
                        <img src="../../assets/images/clients_partner_1-200x202.png" alt="" class="img">
                    </div>
                    <div class="logo">
                        <img src="../../assets/images/clients_partner_2-200x202.png" alt="" class="img">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Feedback',
    data() {
        return {
            clients: [
                {
                    avatar: 'testimonials-1.jpg',
                    feedback: 'Beauty is when you can appreciate yourself. When you love yourself, that’s when you’re most beautiful.',
                    name: 'Shelia McCourtney',
                    role: 'Architect'
                },
                {
                    avatar: 'testimonials-2.jpg',
                    feedback: 'Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience.',
                    name: 'Luis Desalvo',
                    role: 'Creo Tech'
                }
            ],
            selected: 0
        }
    },
    mounted() {
        setInterval(() => {
            if (this.selected < this.clients.length - 1) {
                this.selected++;
            } else this.selected = 0;
        }, 3000);
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
@import '../../assets/style/mixins/mixin.scss';
@include sectionTitle;
section {
    background: white;
}
.feedback {
    padding: 100px 0 70px;
    text-align: center;
    .clients {
        position: relative;
        width: 100%;
        height: 400px;
        .client {
            opacity: 0;
            transition: opacity .4s;
            padding: 3rem 0 2rem;
            width: 60%;
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            -webkit-transform: translateX(-50%);
            &-avatar {
                margin: 0 auto 30px;
                width: 150px;
                .img {
                    width: 100%;
                    border-radius: 50%;
                }
            }
            &-feedback {
                font-style: italic;
                letter-spacing: 2px;
                font-size: 1.1rem;
                line-height: 1.8rem;
                margin-bottom: 2rem;
            }
            &-name {
                font-size: 1.2rem;
                letter-spacing: 1px;
                .name {
                    font-weight: 700;
                }
                .role {
                    text-transform: uppercase;
                }
            }
            &.active {
                opacity: 1;
            }
        }
    }
    .dots {
        display: flex;
        justify-content: center;
        .dot {
            width: .8rem;
            height: .8rem;
            margin: 3px;
            border-radius: 50%;
            border: 1px solid black;
            cursor: pointer;
            transition: .3s;
            &.active {
                background-color: black;
            }
            &:hover {
                background-color: black;
            }
        }
    }
    .logos {
        border-top: .5px solid $Pale_Slate;
        margin-top: 90px;
        display: flex;
        padding: 3rem 0 0;
        justify-content: space-around;
        .logo {
            width: 100px;
            .img {
                width: 100%;
            }
        }
    }
}
</style>