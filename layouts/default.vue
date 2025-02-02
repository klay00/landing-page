<script setup lang="ts">
  const route = useRoute();
</script>
<template>
  <NuxtLoadingIndicator color="hsl(var(--primary))" />
  <main>
    <slot />
    <!-- <HeaderSection />
     <div>
     </div>
    <FooterSection /> -->
  </main>
</template>
