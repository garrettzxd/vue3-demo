<template>
  <div class="hello">
    <h1>{{ props.msg }}</h1>
    <button @click="visibleControl">show modal</button>
    <modal-test ref="confirm" :visible="visible" :confirm="confirm" />
  </div>
</template>

<script setup>
import {defineOptions,defineProps,ref} from "vue";
import ModalTest from './ModalTest.vue';

defineOptions({name: 'App'})
const props = defineProps({
  msg: String
})
const visible = ref(false)

const visibleControl = () => {
  visible.value = true;
}

const confirm = () => {
  console.log('confirm')
}
</script>

<!--<script>-->
<!--export default {-->
<!--  methods: {-->
<!--    confirm() {-->
<!--      return new Promise((resolve) => {-->
<!--        setTimeout(() => {-->
<!--          resolve()-->
<!--        }, 1000)-->
<!--      })-->
<!--    }-->
<!--  },-->
<!--}-->
<!--</script>-->
