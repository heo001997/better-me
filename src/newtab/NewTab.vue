<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Welcome from './components/Welcome.vue'
import Journey from './components/Journey.vue'

let showWelcome = ref(false) // This should be reactive

onMounted(() => {

})

onUnmounted(() => {
  
})

</script>

<template class="new-tab">
  <Header></Header>
  <section class="container">
    <Welcome v-if="showWelcome" class="mt-16 w-75 mx-auto"></Welcome>
    <Journey v-else></Journey>
  </section>
  <Footer></Footer>
</template>

<style lang="scss" scoped>
.container {
  min-height: 80vh;
}
</style>
