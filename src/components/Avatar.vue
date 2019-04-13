<template>
  <b-img v-bind="mainProps"
         src="https://pp.userapi.com/c628322/v628322236/34d65/ii9Npj5Ty2k.jpg"
         rounded
         alt="Zakhar Lazorin">
  </b-img>
</template>

<script>
export default {
  name: 'Avatar',
  data() {
    return {
      mainProps: {
        width: 75,
        height: 175,
        class: 'm1',
      }
    }
  }
}
</script>
<style scoped>
</style>
