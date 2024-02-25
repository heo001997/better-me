<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Welcome from './components/Welcome.vue'

const link = ref('https://github.com/guocaoyi/create-chrome-ext')

onMounted(() => {

})

onUnmounted(() => {
  
})

const isShowWelcome = () => {
  return true
}

</script>

<template class="new-tab">
  <Header></Header>
  <section class="container w-75 mx-auto">
    <Welcome v-if="isShowWelcome"></Welcome>
  </section>
  <Footer></Footer>
</template>

<style lang="scss" scoped>
.container {
  min-height: 90vh;
}
</style>
