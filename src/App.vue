<template>
  <h1>Hi</h1>
  <Modal :header="header" :content="content" :theme="theme" />
</template>

<script>
import Modal from "./components/Modal.vue"
export default {
  data() {
    return {
      header: "Login Success",
      content: "Welcome user KTZ",
      theme: "success",
    }
  },
  components: {
    Modal
  }
}
</script>

<style scoped>
h1 {
  color: blue;
}
</style>