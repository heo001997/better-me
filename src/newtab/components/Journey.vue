<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Journey',
  setup (){
    return {}
  },
  methods: {

  },
  data: () => ({
    
  }),
})
</script>

<template>
  <section>
    <div class="header">
      <div class="left">
        <div> < </div>  
        <div>HABITS</div>  
      </div>
      <div class="middle">
        <div class="date">
          <div class="month">Feb</div>  
          <div class="day">4</div>  
          <div class="weekday">SUN</div>  
        </div>
        <div class="date">
          <div class="month">Feb</div>  
          <div class="day">5</div>  
          <div class="weekday">MON</div>  
        </div>
        <div class="date">
          <div class="month">Feb</div>  
          <div class="day">6</div>  
          <div class="weekday">TUE</div>  
        </div>
        <div class="date">
          <div class="month">Feb</div>  
          <div class="day">7</div>  
          <div class="weekday">WED</div>  
        </div>
        <div class="date">
          <div class="month">Feb</div>  
          <div class="day">8</div>  
          <div class="weekday">THU</div>  
        </div>
      </div>
      <div class="right">
        <div> > </div>  
        <div>Theme switch</div>  
        <div>current streak</div>  
        <div>longest streak</div>  
        <div>total count</div>  
      </div>
    </div>
  </section>
</template>
