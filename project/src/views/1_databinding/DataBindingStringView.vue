<template>
  <div>
    <h1>Hello {{ userName }}</h1>
    <p>{{ msg }}</p>
    <p></p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      userName: 'Devkya',
      msg: 'Welcome Vue Learning',
      arr: [],
      obj: []
    }
  }
}
</script>
<style scoped>
.text-red {
  color: red;
}
</style>
