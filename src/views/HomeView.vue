<template>
  <div class="home">
    <HelloWorld
      name="Nitesh das"
      phone="01747102896"
      email="dasnitesh780@gmail.com"
      about="I am a web developer"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  },
  data () {
    return {
      phone: '01747102896',
    }
  }
}
</script>
