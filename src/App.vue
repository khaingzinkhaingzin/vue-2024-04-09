<template>
  <h1>Hi</h1>
  <Modal />
</template>

<script>
import Modal from "./components/Modal.vue"
export default {
  data() {
    return {
      title: "You don't know JS"
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