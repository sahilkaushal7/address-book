<template>
  <div>{{activeAddress.name}}</div>
</template>

<script>
export default {
  name: "Profile",
  props: ["activeAddress"]
};
</script>

<style scoped>
</style>