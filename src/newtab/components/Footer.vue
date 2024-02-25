<script>
import { defineComponent } from 'vue'

export default defineComponent ({
  name: 'Footer'
})
</script>

<template>
  <footer>
    <div class="new-tab-footer d-flex justify-space-between pl-2">
      <v-breadcrumbs :items="['Tips', 'Web extensions', 'Devices']"></v-breadcrumbs>
      <v-breadcrumbs :items="['Give me feedback please! :-)', 'Better Me 2024', 'by heo001997']"></v-breadcrumbs>
    </div>
  </footer>
</template>

<style lang="scss">
</style>
