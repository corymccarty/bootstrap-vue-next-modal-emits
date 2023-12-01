<script setup lang="ts">
import { useModal } from 'bootstrap-vue-next'
import { ref } from 'vue'

const { show } = useModal('test-modal')
const showModal = ref(false)
</script>

<template>
  <BButton @click="show()">Show Modal</BButton>
  <BModal
    id="test-modal"
    v-model="showModal"
    @show="console.debug('Test Modal: show')"
    @shown="console.debug('Test Modal: shown')"
    @hide="console.debug('Test Modal: hide')"
    @hidden="console.debug('Test Modal: hidden')"
  ></BModal>
</template>
