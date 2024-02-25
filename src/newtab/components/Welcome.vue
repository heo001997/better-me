<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Welcome',
  setup (){
    return {}
  }
})
</script>

<template>
  <section class="text-h4 text-center">
    <div>Looks like you aren't tracking any habits yet, so...<br/>what do you want to start doing every day? :)</div>
    
    <v-dialog width="500">
      <template v-slot:activator="{ props }">
        <v-btn class="mt-5" v-bind="props" text="Open Dialog"> </v-btn>
      </template>

      <template v-slot:default="{ isActive }">
        <v-card title="Dialog">
          <v-card-text>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn
              text="Close Dialog"
              @click="isActive.value = false"
            ></v-btn>
          </v-card-actions>
        </v-card>
      </template>
    </v-dialog>
  </section>
</template>
