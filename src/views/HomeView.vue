<template>
  <div class="home">
    <Child>
        <h1>Slot</h1>
    </Child>
    <Child>
        <h1>Name</h1>
        <input />
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
