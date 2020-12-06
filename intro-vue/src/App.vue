<template>
<div>
  <input type="number" v-model="age">
  <div v-if="age < 18">
    Usia anda dibawah umur 18 tahun    
  </div>
  <div v-else-if="age > 25">
    Anda sudah terlalu tua
  </div>
  <div v-else>
    Usia anda mencukupi
  </div>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
export default{
  data(){
    return {
      age: 21
    }
  }
}

</script>

