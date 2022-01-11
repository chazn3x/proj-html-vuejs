<template>
  <div id="app">
    <Header :links="links"/>
    <Main/>
    <Footer :links="links"/>
  </div>
</template>

<script>
import Header from './components/macro/Header.vue'
import Main from './components/macro/Main.vue'
import Footer from './components/macro/Footer.vue'
export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      links: [
        {
          name: 'Home',
          link: '#',
          selected: true,
        },
        {
          name: 'Who We Are',
          link: '#',
          selected: false,
        },
        {
          name: 'What We Do',
          link: '#',
          selected: false,
        },
        {
          name: 'Where We Work',
          link: '#',
          selected: false,
        },
        {
          name: 'Careers',
          link: '#',
          selected: false,
          apply: true
        },
        {
          name: 'News',
          link: '#',
          selected: false,
        },
        {
          name: 'Get In Touch Now',
          link: '#',
          selected: false,
          button: true
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';
</style>
