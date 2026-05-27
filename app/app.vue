<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
<script setup lang="ts">
useHead({
  title: "Matthiasvanhoutum",
  link: [
    {
      rel: "icon",
      type: "image/x-icon",
      href: "/favicon.png",
    },
  ],
  meta: [
    {
      name: "description",
      content: "Portfolio of Matthias van Houtum.",
    },
    {
      property: "og:title",
      content: "matthiasvanhoutum",
    },
    {
      property: "og:description",
      content: "Portfolio of Matthias van Houtum.",
    },
    {
      property: "og:image",
      content: "/img_8137.jpeg",
    },
    {
      property: "og:type",
      content: "website",
    },
    {
      name: "robots",
      content: "index, follow",
    },
  ],
});
</script>
