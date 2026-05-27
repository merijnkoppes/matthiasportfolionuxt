<template>
  <div>
    <Navbar />
    <div class="page-content">
      <slot />
    </div>
    <Footer />
  </div>
</template>

<style scoped>
.page-content {
  padding-top: 98px;
}
</style>
