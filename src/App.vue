<template>
  <h1>Hi</h1>
  <teleport to=".modal" v-if="showModal">
    <Modal :header="header" :content="content" :theme="theme" @close="showModal=false">
      <h1>{{ header }}</h1>
      <p>{{ content }}</p>
      <template v-slot:links>
        <a href="">Sign up</a>
        <a href="">Sign in</a>
      </template>
    </Modal>
  </teleport>
  <button @click="showModal=true">open modal</button>

  <Modal theme="delete" v-if="showDeleteModal" @close="showDeleteModal=false">
    <h1>Are you sure?</h1>
    <p>You want to delete this content.</p>
  </Modal>
  <button @click="showDeleteModal=true">delete</button>
</template>

<script>
import Modal from "./components/Modal.vue"
export default {
  data() {
    return {
      header: "Login Success",
      content: "Welcome user KTZ",
      theme: "success",
      showModal: false,
      showDeleteModal: false,
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
button {
  margin: 2px;
}
</style>