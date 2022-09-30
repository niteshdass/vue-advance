<template>
  <div class="home">
    <Child
      v-for="(user, item) in users"
      :key="item"
      :="feedItem(user).attr"
      @="feedItem(user).events"
    />
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
      users:[
        {
          id:1,
          name: 'Nitesh Das',
          phone: '01747102896',
          email: 'dasnitesh780@gmail.com'
        },
        {
          id:2,
          name: 'Nitesh Das 2',
          phone: '01747102896',
          email: 'dasnitesh780@gmail.com'
        },
        {
          id:3,
          name: 'Nitesh Das 3',
          phone: '01747102896',
          email: 'dasnitesh780@gmail.com'
        }
      ]
    }
  },
  methods: {
    feedItem (user) {
      return {
        attr: {
          name: user.name, phone: user.phone
        },
        events: {
          click: () => this.handleClick(user)
        }
      }
    },
    handleClick(user) {
      console.log('clicked');
      alert(`You clicked ${user.name}`);
    }
  }
}
</script>
