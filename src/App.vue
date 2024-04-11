<template>
  <h1>Hi</h1>
  <div v-if="showModal">
    <Modal :header="header" :content="content" :theme="theme" @close="showModal=false">
      <h1>Login Success</h1>
      <p>Welcome user ...</p>
      <template v-slot:links>
        <a href="">Sign up</a>
        <a href="">Sign in</a>
      </template>
    </Modal>
  </div>
  <button @click="showModal=true">open modal</button>
</template>

<script>
import Modal from "./components/Modal.vue"
export default {
  data() {
    return {
      header: "Login Success",
      content: "Welcome user KTZ",
      theme: "success",
      showModal: false
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