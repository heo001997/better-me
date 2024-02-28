<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Welcome',
  setup (){
    return {}
  },
  methods: {
    changeDaySkip(day){
      day.isSkip = !day.isSkip
    }
  },
  data: () => ({
    dialog: false,
    days: [
      {
        name: 'Mon',
        isSkip: false,
      },
      {
        name: 'Tue',
        isSkip: false,
      },
      {
        name: 'Wed',
        isSkip: false,
      },
      {
        name: 'Thu',
        isSkip: false,
      },
      {
        name: 'Fri',
        isSkip: false,
      },
      {
        name: 'Sat',
        isSkip: false,
      },
      {
        name: 'Sun',
        isSkip: false,
      },
    ]
  }),
})
</script>

<template>
  <section class="text-h4 text-center">
    <div>Looks like you aren't tracking any habits yet, so...<br/>what do you want to start doing every day? :)</div>

    <div class="pa-4 text-center">
      <v-dialog v-model="dialog" max-width="600">
        <template v-slot:activator="{ props: activatorProps }">
          <v-btn
              class="text-none font-weight-regular"
              prepend-icon="mdi-plus"
              text="Add New Habit"
              variant="tonal"
              v-bind="activatorProps"
          ></v-btn>
        </template>

        <v-card title="Add New Habit">
          <v-card-text>
            <v-row dense>
              <v-col
                  cols="12"
                  sm="12"
                  md="12"
              >
                <v-text-field
                    label="Name*"
                    placeholder="Meditate for one minute"
                    hide-details="auto"
                    required
                >
                </v-text-field>
              </v-col>

              <v-col
                  cols="12"
                  sm="12"
                  md="12"
              >
                <v-label text="Frequency*"></v-label>
                <small class="d-block text-caption text-medium-emphasis">
                  Click on the day of the week to skip, selected skip days will not break the streak.
                </small>
              </v-col>

              <v-col class="d-flex justify-space-between">
                <v-btn
                    v-for="day in days"
                    @click="changeDaySkip(day)"
                    :prepend-icon="day.isSkip ? 'mdi-skip-forward' : 'mdi-check'"
                    :class="day.isSkip ? 'bg-grey' : 'bg-green'"
                    rounded="circle"
                    size="small"
                    stacked
                >
                  {{ day.name }}
                </v-btn>
              </v-col>
            </v-row>
          </v-card-text>

          <v-divider></v-divider>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn
                text="Close"
                variant="plain"
                @click="dialog = false"
            ></v-btn>

            <v-btn
                color="primary"
                text="Save"
                variant="tonal"
                @click="dialog = false"
            ></v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
  </section>
</template>
