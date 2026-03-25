<script setup lang="ts">
import AppProfileCard from "@/components/AppProfileCard.vue";
</script>

<template>
  <div
    class="flex min-h-screen flex-wrap items-center justify-center gap-8 bg-linear-to-br from-sky-300 to-sky-800"
  >
    <AppProfileCard
      profileimg="/profile.jpg"
      background="/beach.jpg"
      username="Smart Ace"
      subheading="ScriptoForms Maintainer"
      followers="3"
      following="10"
      projects="40"
    >
      <slot />
    </AppProfileCard>
  </div>
</template>
