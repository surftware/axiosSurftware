

<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h4>{{msg2}}</h4>
    <p></p>
    
  </div>
</template>

<script>

export default {
  name: 'HelloSurftware',
  props: {
    msg: String,
    msg2:String
  }
}
</script>