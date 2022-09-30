<template>
  <div class="hello">
    <div class="box">
      <h1>{{ name }}</h1>
      <h3>{{ phone }}</h3>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Child',
  props: {
    name: {
      type: String,
      default: 'Nitesh Das'
    },
    phone: {
      type: String,
      default: '01747102896'
    }
  },
   data () {
    return {
      phone1: '01747102896jj',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .box {
    background-color: #fff;
    border: 1px solid #eee;
    border-radius: 5px;
    box-shadow: 0 2px 3px #ccc;
    padding: 20px;
    text-align: center;
    margin: 0 auto;
    max-width: 50%;
  }
  .title {
    color: #42b983;
  }
  .content {
    color: #b11635;
  }
  .footer {
    color: #f39c12;
  }

</style>
