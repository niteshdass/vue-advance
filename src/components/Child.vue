<template>
  <div class="hello">
    <div class="box">
      <div class="title">
        <slot name="title"></slot>
      </div>
      <div class="content">
        <slot></slot>
      </div>
      <div class="footer">
        <slot name="footer"></slot>
      </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Child',
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
