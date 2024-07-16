<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from 'swiper/modules';

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
			modules: [Navigation],
    };
  },
};
</script>

<template>
  <section class="pt-10">
    <div class="container">
      <h4>WHAT WE DO</h4>
      <h2>Our Service</h2>
      <swiper
				:modules="modules"        
				:slides-per-view="2"
        :space-between="15"
				:breakpoints="{
					768: {
        		slidesPerView: 3,
        		spaceBetween: 37,
      		},
				}"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
				class="lg:py-10 md:py-8 py-6"
			>
        <swiper-slide>
          <div class="column">
            <img
              src="../../assets/services/design.png"
              class="column__image"
              width="40px"
              height="40px"
              alt="design-icon" />
            <div class="column__info">
              <h5 class="column__title">Interior Design</h5>
              <p>
                Lorem ipsum dolor amet consectetur adipiscing elit sed eiusmod
                tempor incididunt ut labore.
              </p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="column bg-[#CAA892]">
            <img
              src="../../assets/services/architector.png"
              class="column__image"
              width="40px"
              height="40px"
              alt="design-icon" />
            <div class="column__info">
              <h5 class="column__title text-white">Interior Design</h5>
              <p class="text-white">
                Lorem ipsum dolor amet consectetur adipiscing elit sed eiusmod
                tempor incididunt ut labore.
              </p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="column">
            <img
              src="../../assets/services/plan.png"
              class="column__image"
              width="40px"
              height="40px"
              alt="design-icon" />
            <div class="column__info">
              <h5 class="column__title">Interior Design</h5>
              <p>
                Lorem ipsum dolor amet consectetur adipiscing elit sed eiusmod
                tempor incididunt ut labore.
              </p>
            </div>
          </div>
        </swiper-slide>
				<swiper-slide>
          <div class="column bg-[#CAA892]">
            <img
              src="../../assets/services/architector.png"
              class="column__image"
              width="40px"
              height="40px"
              alt="design-icon" />
            <div class="column__info">
              <h5 class="column__title text-white">Interior Design</h5>
              <p class="text-white">
                Lorem ipsum dolor amet consectetur adipiscing elit sed eiusmod
                tempor incididunt ut labore.
              </p>
            </div>
          </div>
        </swiper-slide>
				<swiper-slide>
          <div class="column">
            <img
              src="../../assets/services/plan.png"
              class="column__image"
              width="40px"
              height="40px"
              alt="design-icon" />
            <div class="column__info">
              <h5 class="column__title">Interior Design</h5>
              <p>
                Lorem ipsum dolor amet consectetur adipiscing elit sed eiusmod
                tempor incididunt ut labore.
              </p>
            </div>
          </div>
        </swiper-slide>
				<swiper-slide>
          <div class="column bg-[#CAA892]">
            <img
              src="../../assets/services/architector.png"
              class="column__image"
              width="40px"
              height="40px"
              alt="design-icon" />
            <div class="column__info">
              <h5 class="column__title text-white">Interior Design</h5>
              <p class="text-white">
                Lorem ipsum dolor amet consectetur adipiscing elit sed eiusmod
                tempor incididunt ut labore.
              </p>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<style scoped>
.column {
  @apply xl:py-10 sm:py-8 py-4 xl:px-7 sm:px-5 px-3 rounded-e-sm flex lg:flex-row flex-col sm:gap-5 gap-3 shadow-xl;
  border-radius: 15px 0px 15px 0px;
}
.column__image {
  @apply sm:h-10 h-7 sm:w-10 w-7;
}
.column__info {
  @apply flex flex-col gap-1.5;
}
.column__title {
	@apply xl:text-2xl lg:text-xl md:text-lg sm:text-base text-sm font-bold;
}
.column p {
	@apply lg:text-base md:text-sm text-xs;
}
</style>
