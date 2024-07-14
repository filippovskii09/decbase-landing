<script setup>
	import { ref } from "vue";
	import LogoIcon from "./icons/IconLogo.vue";

	const isOpen = ref(false);

	const toggleMenu = () => {
  	isOpen.value = !isOpen.value;
	};
</script>

<template>
  <header class="md:py-8 py-4 bg-white fixed left-0 top-0 w-full">
    <div class="container flex items-center flex-wrap relative">
      <div class="flex-1">
        <a href="#">
          <LogoIcon />
        </a>
      </div>
			<div class="md:flex hidden items-center xl:gap-16 lg:gap-10 gap-5 md:static fixed">
	      <div>
	        <nav>
	          <ul class="flex xl:gap-10 lg:gap-6 gap-3">
	            <li class="menu__item"><a href="" class="menu__link">HOME</a></li>
	            <li class="menu__item">
	              <a href="" class="menu__link">PROJECT</a>
	            </li>
	            <li class="menu__item">
	              <a href="" class="menu__link">SERVICES</a>
	            </li>
	            <li class="menu__item"><a href="" class="menu__link">ABOUT</a></li>
	            <li class="menu__item"><a href="" class="menu__link">BLOG</a></li>
	            <li class="menu__item"><a href="" class="menu__link">SHOP</a></li>
	            <li class="menu__item">
	              <a href="" class="menu__link">CONTACT</a>
	            </li>
	          </ul>
	        </nav>
	      </div>
				<button class="btn bg-[#CAA892] lg:text-base text-sm lg:px-5 px-3 py-1 origin-top-left hover:rotate-6">Sign Up</button>
			</div>
			<button @click="toggleMenu" class="burger-button md:hidden flex">
      	<span :class="{'open': isOpen}"></span>
      	<span :class="{'open': isOpen}"></span>
      	<span :class="{'open': isOpen}"></span>
    	</button>
    </div>
  </header>
</template>

<style scoped>
	.menu__link {
		@apply lg:text-base text-xs font-semibold text-[#111111] ;
	}
	.burger-button {
  position: relative;
  width: 30px;
  height: 25px;
  flex-direction: column;
  justify-content: space-between;
  cursor: pointer;
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
