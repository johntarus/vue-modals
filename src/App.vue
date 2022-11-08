<template>
  <div v-if="showModal">
    <Modal theme='sale' @close='toggleModal'>
      <h1>Checking up on slot</h1>
      <p>creating modals in vue is amazing</p>
    </Modal>
  </div>
  <button @click="toggleModal">show modal</button>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  components: { Modal },
  data() {
    return {
      title: `Hello World Vue, I'm coming!`,
      header: `many give aways on the way`,
      showModal: false,
     }
  },
  methods: {
    toggleModal() {
        this.showModal = !this.showModal
      }
    }
  }
</script>