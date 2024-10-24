<script setup>
  import { useFlash } from '@/composables/useFlash'
  let {flash} = useFlash()
</script>

<template>
  <main>
    <button @click="flash('About', 'This is the about page', 'info')">Click Me</button>
  </main>
</template>
