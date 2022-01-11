<template>
    <main>
        <Hero/>
        <div class="sections">
            <Agency/>
        </div>
    </main>
</template>

<script>
import Hero from '../elements/Hero.vue'
import Agency from '../sections/Agency.vue'
export default {
    name: 'Main',
    components: {
        Hero,
        Agency
    }
}
</script>

<style lang="scss" scoped>

</style>