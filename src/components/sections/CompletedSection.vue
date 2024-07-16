<template>
  <section class="pb-28 pt-20 bg-[#F8F8F8]">
    <div class="container flex flex-col items-center">
      <h2 class="text-center max-w-[820px] mx-auto mb-20">
        3000+ Completed Work Which WE have Successfully Done
      </h2>
      <div class="info flex md:flex-row flex-col md:items-start items-center w-full md:gap-0 gap-12">
        <div class="info-column">
          <h3 class="info-column__number">980</h3>
          <p class="info-column__name">Project</p>
        </div>
        <div class="line-col 2xl:mt-24 lg:mt-16 md:mt-10 mt-0">
          <svg
            width="207"
            height="98"
            viewBox="0 0 207 98"
            fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <path d="M0 1H91.6307V97H207" stroke="#E0E0E0" stroke-width="2" />
          </svg>
        </div>
        <div class="info-column 2xl:mt-24 lg:mt-16 md:mt-10 mt-0">
          <h3 class="info-column__number">520</h3>
          <p class="info-column__name">Happy Client</p>
        </div>
        <div class="line-col 2xl:mt-24 lg:mt-16 md:mt-10 mt-0">
          <svg
            width="202"
            height="97"
            viewBox="0 0 202 97"
            fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <path d="M0 96H89.4174V1H202" stroke="#E0E0E0" stroke-width="2" />
          </svg>
        </div>
        <div class="info-column">
          <h3 class="info-column__number">330</h3>
          <p class="info-column__name">Winners</p>
        </div>
        <div class="line-col 2xl:mt-24 lg:mt-16 md:mt-10 mt-0">
          <svg
            width="207"
            height="98"
            viewBox="0 0 207 98"
            fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <path d="M0 1H91.6307V97H207" stroke="#E0E0E0" stroke-width="2" />
          </svg>
        </div>
        <div class="info-column 2xl:mt-24 lg:mt-16 md:mt-10 mt-0">
          <h3 class="info-column__number">120</h3>
          <p class="info-column__name">Recoment</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
	.info-column {
		@apply shadow-2xl flex flex-col items-center justify-center md:w-1/6 w-44 xl:h-44 lg:h-36 md:h-32 h-44;
		border-radius: 40px 0px 40px 0px;
	}
	.info-column__number {
		@apply font-bold;
	}
	.line-col {
		@apply md:w-1/6 w-auto;
	}
	.line-col svg {
		@apply md:rotate-0 rotate-90 md:h-auto h-full w-full;
	}
	.info p {
		@apply xl:text-base lg:text-sm text-xs ;
	}
</style>