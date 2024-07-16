<script setup>
import Header from "./components/Header.vue";	
import AboutSection from "./components/sections/AboutSection.vue";
import MainSection from "./components/sections/MainSection.vue";
import ServicesSection from "./components/sections/ServicesSection.vue";
import WorkingSection from "./components/sections/WorkingSection.vue";
import CompletedSection from "./components/sections/CompletedSection.vue";
</script>

<template>
	<div class="h-full flex flex-col">
		<Header/>
		<main class="flex-1 min-h-full mt-12">
			<MainSection/>
			<ServicesSection/>
			<AboutSection/>
			<WorkingSection/>
			<CompletedSection/>
		</main>
	</div>
</template>