<template>
  <div class="main container animate__animated animate__zoomIn">
    <form @submit.prevent="bmicalc()" class="s12 container">
      <div class="col container">
        <div class="input-field col s6">
          <i class="material-icons prefix">height</i>
          <input 
            id="icon_prefix"
            type="text"
            class="validate"
            v-model="height"
            required
          />
          <label for="icon_prefix">Height in cm</label>
        </div>
        <div class="input-field col s6">
          <i class="material-icons prefix">monitor_weight</i>
          <input
            id="icon_telephone"
            type="tel"
            class="validate"
            v-model="weight"
            required
          />
          <label for="icon_telephone">Weight in kg</label>
        </div>
        <button class="btn waves-effect waves-light indigo darken-4" type="submit" name="action">
          Calculate
          <i class="material-icons right">done</i>
        </button>
      </div>
    </form>
    <div class="container">
      <ul class="collection container">
        <li class="collection-item container avatar">
          <img src="https://media.self.com/photos/5be5c8322ef8df6252534830/master/pass/foot-scale.jpg" alt="" class="circle" />
          <p class="title">Your BMI is: </p>
          <p id="bmi" v-bind:class="{ good: bmi > 19 && bmi < 26, under: bmi < 19 && bmi > 5, bad: bmi > 26}"> {{bmi}} </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    const height = ref(null)
    const weight = ref(null)
    const bmi = ref(0)
    const result = ref(0)

    const bmicalc = () => {
      result.value = ( weight.value / ( height.value * height.value ) ) * 10000
      bmi.value = Math.round((result.value + Number.EPSILON) * 100) / 100
    }

    return{
      height,
      weight,
      bmi,
      bmicalc
    }
  }
}
</script>