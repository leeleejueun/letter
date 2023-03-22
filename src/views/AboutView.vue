<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="move"> {{$route.query.id}} </button>
  </div>
</template>

<script>
export default{
  methods: {
    move(){  this.$router.push('/')  }
  },
}
</script>
