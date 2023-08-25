<template>
    <h2>{{ ofirstName }}</h2>
    <h2>{{ cFirstName }} {{ cLastName }}</h2>
    <h2>{{ greet }} </h2>
    <h2>{{ cFirstName }} {{ cLastName }}</h2>
    <h2>{{ greetHero }}</h2>
    <h2>{{ state.firstName }} {{ state.lastName }}</h2>
    <h3>{{ reactiveGreet }}</h3>
</template>
<script>
import {ref} from 'vue'
export default{
  name:'Data', 
  setup(){
     const cFirstName=ref('DSSSK')
     const cLastName=ref('dutt')
     const cHeroName= ref('sdt')
     cFirstName.value='SSD'
     const greet=`Hello ${cFirstName.value}`
     const greetHero=`Hello ${cFirstName.value} ${cLastName.value} a.k.a ${cHeroName.value}`

     const state=reactive({
      firstName:'SD',
      lastName:'DS',
 })
 const reactiveGreet=`Hello ${state.firstName} ${state.lastName}`
     return{
      cFirstName,
      cLastName,
      cHeroName,
      greet,
      greetHero,
      state,
      reactiveGreet
     }
  },
  data(){
    return{
      ofirstName:'KSSSD',
    }
  },
}
</script>
<style scoped>
</style>
