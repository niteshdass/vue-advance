<template>
  <div class="home">
    <Child>
      <template #title>
        <h1>My name is Nitesh Das</h1>
      </template>
      <p>I am a web developer</p>
      <template v-slot:footer>
        <p>My phone number is 01747102896</p>
      </template>
    </Child>
  </div>
</template>

<script>
// @ is an alias to /src
import Child from '../components/Child.vue'

export default {
  name: 'HomeView',
  components: {
    Child
  },
  data () {
    return {
      phone: '01747102896',
    }
  }
}
</script>
