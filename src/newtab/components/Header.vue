<script>
import { defineComponent, ref, onMounted, onUnmounted } from 'vue'

export default defineComponent ({
  name: 'Header',
  setup() {
    const getTime = () => {
      const date = new Date()
      const hour = String(date.getHours()).padStart(2, '0')
      const minute = String(date.getMinutes()).padStart(2, '0')
      const second = String(date.getSeconds()).padStart(2, '0')
      return `${hour}:${minute}:${second}`
    }

    const time = ref(getTime())
    const intervalor = ref(null)

    onMounted(() => {
      intervalor.value = setInterval(() => {
        time.value = getTime()
      }, 1000)
    })

    onUnmounted(() => {
      clearInterval(intervalor.value)
    })

    return { time }
  }
})
</script>

<template>
  <section>
    <h1 class="pl-2">{{ time }}</h1>
  </section>
</template>
