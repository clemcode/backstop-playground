<template>
  <ul>
    <li v-for="link of navigation" :key="link._path">
      <TheNav v-if="link.children" :navigation="link.children" />
      <NuxtLink v-else :to="link._path">{{ link.title }}</NuxtLink>
    </li>
  </ul>
</template>

<script setup>
defineProps({
  navigation: {
    type: Array,
    required: true
  }
})
</script>