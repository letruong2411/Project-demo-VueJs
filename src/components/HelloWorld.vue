<template>
  <div class="hello">
   <h1>HelloWorld</h1>
  </div>
</template>

<script>
export default {
  data () {
    return {
		name: "hell0"
    }
  },
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
