<template>
  <div v-if="visible">
    modal test
    <button @click="handleConfirm">confirm</button>
  </div>
</template>

<script>
export default {
  name: "ModalTest",

  props: {
    visible: {
      type: Boolean,
      default: false
    },
    confirm: Function
  },

  methods: {
    async handleConfirm() {
      if (this.confirm) {
        this.confirm()
      }
    }
  }
}
</script>