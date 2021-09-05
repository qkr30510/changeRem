<template>
  <div class="container">
    <h1>px <span>to</span> rem</h1>
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
h1{
  text-align: center;
  margin:30px 0;
  font-size:30px;
  text-transform: uppercase;  
}
h1 span{
  text-transform:lowercase
}
</style>
