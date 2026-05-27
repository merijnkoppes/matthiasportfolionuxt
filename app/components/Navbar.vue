<template>
  <header class="navbar">
    <div class="container">
      <div class="wrapper">
        <NuxtLink to="/" class="title"> Matthias van Houtum </NuxtLink>

        <nav class="normal-menu">
          <NuxtLink
            to="/"
            class="link"
            active-class="active"
            exact-active-class="active"
          >
            About
          </NuxtLink>

          <NuxtLink
            to="/video"
            class="link"
            active-class="active"
            exact-active-class="active"
          >
            Video
          </NuxtLink>

          <NuxtLink
            to="/photo"
            class="link"
            active-class="active"
            exact-active-class="active"
          >
            Photo
          </NuxtLink>
        </nav>

        <button
          class="burger-menu"
          type="button"
          aria-label="Open menu"
          @click="toggleMobileMenu"
        >
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>

      <nav
        ref="mobileMenu"
        class="mobile-menu"
        :class="{ show: isMobileMenuOpen }"
        :style="{ height: mobileMenuHeight }"
      >
        <NuxtLink
          to="/"
          class="link"
          active-class="active"
          exact-active-class="active"
          @click="closeMobileMenu"
        >
          About
        </NuxtLink>

        <NuxtLink
          to="/video"
          class="link"
          active-class="active"
          exact-active-class="active"
          @click="closeMobileMenu"
        >
          Video
        </NuxtLink>

        <NuxtLink
          to="/photo"
          class="link"
          active-class="active"
          exact-active-class="active"
          @click="closeMobileMenu"
        >
          Photo
        </NuxtLink>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
const isMobileMenuOpen = ref(false);
const mobileMenu = ref<HTMLElement | null>(null);
const mobileMenuHeight = ref("0");

const toggleMobileMenu = async () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value;

  await nextTick();

  if (isMobileMenuOpen.value && mobileMenu.value) {
    mobileMenuHeight.value = `${mobileMenu.value.scrollHeight}px`;
    return;
  }

  mobileMenuHeight.value = "0";
};

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false;
  mobileMenuHeight.value = "0";
};
</script>

<style scoped lang="scss">
.navbar {
  z-index: 101;
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  margin: 0;
  padding: 0;
  user-select: none;
  background-color: #fff;
}

.container {
  position: relative;
  z-index: 5;
  background-color: #fff;
  border-bottom: 2px solid #000;
  width: 1120px;
  padding: 20px 20px 20px 0;
  font-family:
    Georgia,
    Times,
    Times New Roman,
    serif;
}

.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.link {
  color: #1a1b1f;
  letter-spacing: 0.25px;
  margin: 0 15px;
  font-size: 18px;
  font-weight: 200;
  line-height: 20px;
  text-decoration: none;
}

.link.active {
  border-bottom: 2px solid #000;
  font-weight: 400;
}

.normal-menu {
  margin-right: 50px;
}

.title {
  color: #000;
  padding-left: 55px;
  font-family:
    Georgia,
    Times,
    Times New Roman,
    serif;
  font-size: 18px;
  text-decoration: none;
}

.burger-menu {
  display: none;
  flex-direction: column;
  cursor: pointer;
  margin-right: 50px;
  z-index: 102;
  padding: 0;
  border: 0;
  background: transparent;
}

.burger-menu span {
  height: 2px;
  width: 20px;
  background: #000;
  margin: 2px 0;
  transition: 0.4s;
}

.mobile-menu {
  display: none;
  flex-direction: column;
  position: absolute;
  width: 100%;
  background-color: #fff;
  overflow: hidden;
  transition: height 0.5s ease-out;
  top: 60px;
  left: 0;
  height: 0;
  padding-top: 10px;
  border-bottom: 2px solid #000;
  z-index: 100;
  /* margin-top: 10px; */
}

.mobile-menu.show {
  border-bottom: 2px solid #000;
  display: flex;
  height: auto;
}

@media (max-width: 768px) {
  .normal-menu {
    display: none;
  }

  .mobile-menu {
    display: flex;
  }

  .burger-menu {
    display: flex;
  }

  .link {
    text-align: center;
    width: auto;
    margin: 10px auto;
  }
}
</style>
