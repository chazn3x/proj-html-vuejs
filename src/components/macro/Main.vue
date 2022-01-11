<template>
    <main>
        <Hero/>
        <div class="sections">
            <Agency/>
            <Services/>
        </div>
    </main>
</template>

<script>
import Hero from '../elements/Hero.vue'
import Agency from '../sections/Agency.vue'
import Services from '../sections/Services.vue'
export default {
    name: 'Main',
    components: {
        Hero,
        Agency,
        Services
    }
}
</script>

<style lang="scss" scoped>

</style>