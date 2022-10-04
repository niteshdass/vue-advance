<template>
  <div class="home">
    <!-- <HelloWorld
      name="Nitesh das"
      phone="01747102896"
      email="dasnitesh780@gmail.com"
      about="I am a web developer"
    /> -->
    <Undo />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Undo from '@/components/Undo.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    Undo
},
  data () {
    return {
      phone: '01747102896',
    }
  }
}
</script>
