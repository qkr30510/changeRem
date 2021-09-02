<template>
  <div class="container">
    <h1>px을 => rem 바꾸기</h1>
    <div>
      <inputComponent/>
    </div>
  </div>
</template>

<script>
import input from '../components/inputComponent.vue'
export default {
  components: input,
  
  }
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;  
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
