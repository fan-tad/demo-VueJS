<template>
  <div>
    <h1>My Cart</h1>
    <span>Total est: {{total}}</span>
    <md-button @click="add">{{count}}</md-button>

  </div>
</template>

<script>
    import MyHeader from "../myHeader/MyHeader.vue"
    export default {

      name: 'my-cart',
      components: {MyHeader},
      data: function() {
        return {
            count: 0,
        }
      },
      props: {
          start: {
            type: Number,
            default: 0
          }
      },
      methods: {
          add: function () {
            this.count ++;
          }
      },
      computed:{
          total: function () {
            return this.start + this.count
          }
      }
    }
</script>

<style lang="scss" src="./MyCart.scss" scoped>
</style>
