<script setup>
  import { useFlash } from '@/composables/useFlash'
  let {flash} = useFlash()
</script>

<template>
  <main>
    <button @click="flash('test', 'This is the home page')">Click Me</button>
  </main>
</template>
