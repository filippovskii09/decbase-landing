<template>
	  <div
    v-if="isLoginModalOpen"
    class="fixed w-full min-h-screen left-0 top-0 z-10 overflow-hidden text-white flex items-center justify-center">
    <div
      class="modal-info max-w-[600px] xl:w-1/2 lg:w-3/4 w-11/12 h-[320px] bg-[#CAA892] rounded-xl opacity-100 z-20 p-4">
			<h2 class="text-center">Sign Up</h2>
		</div>
    <div class="bg-black opacity-50 absolute w-full h-full"></div>
  </div>
</template>

<script setup>
import { onMounted, onUnmounted, watch } from 'vue';

const emit = defineEmits(['close']);
const props = defineProps({
	isLoginModalOpen: {
		type: Boolean,
		default: false,
		required: true
	}
});

const closeLoginModal = () => emit('close');

const handleKeydown = (e) => {
  if (e.code === "Escape") {
    closeLoginModal();
  }
};

const handleCloseOutside = (e) => {
  if (!e.target.closest(".modal-info") && !e.target.closest(".btn")) {
    closeLoginModal();
  }
};

watch(
  () => props.isLoginModalOpen,
  (newVal) => {
    if (newVal) {
      window.addEventListener('click', handleCloseOutside);
    } else {
      window.removeEventListener('click', handleCloseOutside);
    }
  }
);
onMounted(() => {
  window.addEventListener("keydown", handleKeydown);
});

onUnmounted(() => {
  window.removeEventListener("keydown", handleKeydown);
  window.removeEventListener("click", handleCloseOutside);
});
</script>