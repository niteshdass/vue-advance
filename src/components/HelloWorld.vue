<template>
  <div class="hello">
    <h1>Hi, i am {{ name }}</h1>
    <h2>My phone number is {{ phone }}</h2>
    <h2>My about is {{ about }}</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    name: {
      type: String,
      default: 'Nitesh Das',
      validator: function (value) {
        return value.length > 5
      }
    },
    phone: {
      type: [Number, String],
      required: true
    },
    about: {
      type: String,
      default: 'I am a web developer'
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
