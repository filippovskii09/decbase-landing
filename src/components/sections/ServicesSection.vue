<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

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
        :slides-per-view="2"
        :space-between="37"
				:breakpoints="{
					768: {
        		slidesPerView: 3,
        		spaceBetween: 37,
      		},
				}"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
				class="pb-10"
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
  @apply xl:py-10 py-8 xl:px-7 px-5 rounded-e-sm flex lg:flex-row flex-col gap-5 shadow-xl;
  border-radius: 15px 0px 15px 0px;
}
.column__image {
  height: 40px;
}
.column__info {
  @apply flex flex-col gap-1.5;
}
.column__title {
	@apply xl:text-2xl lg:text-xl md:text-lg text-base font-bold;
}
.column p {
	@apply lg:text-base md:text-sm;
}
</style>
