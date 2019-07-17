<template>
<div>
    <h1>Frases cordiales</h1>
    <input v-model="message" placeholder="Your message">
    <input v-model="name" placeholder="Your name">
    <p>{{ message }} {{ name }}</p>
</div>
</template>

<script>

export default {
  name: "SimpleInput",
  data() {
    return {
      name: "",
      message: ""
    };
  }
};
</script>

<style scoped>
</style>
