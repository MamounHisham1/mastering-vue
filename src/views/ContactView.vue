<script setup>
import { useFlash } from '@/composables/useFlash'
import { ref } from 'vue'
let { flash } = useFlash()

let saveMessage = localStorage.getItem('message')
let message = ref(saveMessage || 'hello world')

let save = () => {
  localStorage.setItem('message', message.value)
  console.log(saveMessage)
}
</script>
<template>
  <main>
    <p>
      {{ message }}
    </p>
    <input type="text" v-model="message" />
    <button @click="save">Save</button>
  </main>
</template>
