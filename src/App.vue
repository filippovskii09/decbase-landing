<script setup>
	import Header from "./components/Header.vue";	
	import MainSection from "./components/sections/MainSection.vue";
	import ServicesSection from "./components/sections/ServicesSection.vue";
</script>

<template>
	<div class="h-full flex flex-col">
		<Header/>
		<main class="flex-1 min-h-full mt-12">
			<MainSection/>
			<ServicesSection/>
		</main>
	</div>
</template>