<script setup>
import { onMounted, onUnmounted, ref } from "vue";
import LogoIcon from "./icons/IconLogo.vue";
import LoginModal from "./LoginModal.vue";

const isOpen = ref(false);
const isLoginModalOpen = ref(false);
const smallHeader = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
  if (isOpen.value) {
    document.documentElement.style.overflow = "hidden";
  } else {
    document.documentElement.style.overflow = "";
  }
};

const openLoginModal = () => {
  isLoginModalOpen.value = true;
  isOpen.value = false;
};

const closeLoginModal = () => {
  isLoginModalOpen.value = false;
  document.documentElement.style.overflow = "";
};

const handleChangeHeaderSize = () => {
  const scrollPos = window.scrollY;
  scrollPos >= 50 ? (smallHeader.value = true) : (smallHeader.value = false);
};

onMounted(() => {
  window.addEventListener("scroll", handleChangeHeaderSize);
  if (isOpen.value) document.documentElement.style.overflow = "hidden";
});
onUnmounted(() => window.removeEventListener("scroll", handleChangeHeaderSize));
</script>

<template>
  <header
    class="md:py-8 py-4 bg-white fixed left-0 top-0 w-full transition-all duration-300 ease-in-out"
    :class="{ 'md:py-2 py-2': smallHeader }">
    <div class="container flex items-center flex-wrap relative">
      <div class="flex-1">
        <a href="#">
          <LogoIcon />
        </a>
      </div>
      <div
        class="flex md:translate-x-0 -translate-x-full bg-white transition-all duration-500 ease-in-out items-center xl:gap-16 lg:gap-10 gap-5 md:static fixed md:w-fit w-full h-full left-0 top-0 md:flex-row flex-col justify-center z-20"
        :class="{ 'translate-x-0 overflow-auto': isOpen }">
        <div>
          <nav>
            <ul
              class="flex md:flex-row flex-col md:text-left text-center xl:gap-10 lg:gap-6 gap-3 flex-wrap">
              <li class="menu__item"><a href="" class="menu__link">HOME</a></li>
              <li class="menu__item">
                <a href="" class="menu__link">PROJECT</a>
              </li>
              <li class="menu__item">
                <a href="" class="menu__link">SERVICES</a>
              </li>
              <li class="menu__item">
                <a href="" class="menu__link">ABOUT</a>
              </li>
              <li class="menu__item"><a href="" class="menu__link">BLOG</a></li>
              <li class="menu__item"><a href="" class="menu__link">SHOP</a></li>
              <li class="menu__item">
                <a href="" class="menu__link">CONTACT</a>
              </li>
            </ul>
          </nav>
        </div>
        <button
          @click="openLoginModal"
          class="btn bg-[#CAA892] lg:text-base md:text-sm text-xl lg:px-5 md:px-3 px-6 py-1">
          Sign Up
        </button>
      </div>
      <button @click="toggleMenu" class="burger-button md:hidden flex">
        <span :class="{ open: isOpen }"></span>
        <span :class="{ open: isOpen }"></span>
        <span :class="{ open: isOpen }"></span>
      </button>
    </div>
  </header>
  <LoginModal :isLoginModalOpen="isLoginModalOpen" @close="closeLoginModal" />
</template>

<style scoped>
.menu__link {
  @apply lg:text-base md:text-xs text-xl font-semibold text-[#111111] transition-all hover:text-gray-400;
}
.burger-button {
  position: relative;
  width: 30px;
  height: 25px;
  flex-direction: column;
  justify-content: space-between;
  cursor: pointer;
  z-index: 25;
}

.burger-button span {
  display: block;
  width: 100%;
  height: 4px;
  background: black;
  transition: transform 0.3s, opacity 0.3s;
}

.burger-button span.open:nth-child(1) {
  transform: translateY(10px) rotate(45deg);
}

.burger-button span.open:nth-child(2) {
  opacity: 0;
}

.burger-button span.open:nth-child(3) {
  transform: translateY(-10px) rotate(-45deg);
}
</style>
