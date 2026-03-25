<script setup lang="ts">
defineProps<{
  profileimg: string;
  background: string;
  username: string;
  subheading: string;
  followers: string;
  following: string;
  projects: string;
}>();
</script>

<template>
  <div class="min-w-80 overflow-hidden rounded-2xl bg-white text-center shadow-lg">
    <div
      class="relative min-h-32 bg-cover bg-center"
      :style="{ backgroundImage: `url('/astro-profile-card/${background}')` }"
    >
      <slot />
    </div>
    <div class="px-6 pt-20 pb-6">
      <h1 class="mb-2 text-2xl font-bold text-gray-800">{{ username }}</h1>
      <h2 class="text-lg text-gray-600">{{ subheading }}</h2>
    </div>
    <div class="flex items-center justify-center gap-6 border-t border-gray-200 p-6">
      <div>
        <h3 class="text-sm text-gray-600">Followers</h3>
        <p class="text-2xl font-bold text-gray-800">{{ followers }}</p>
      </div>
      <div>
        <h3 class="text-sm text-gray-600">Following</h3>
        <p class="text-2xl font-bold text-gray-800">{{ following }}</p>
      </div>
      <div>
        <h3 class="text-sm text-gray-600">Projects</h3>
        <p class="text-2xl font-bold text-gray-800">{{ projects }}</p>
      </div>
    </div>
  </div>
</template>
