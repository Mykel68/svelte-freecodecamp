<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let productFeatures = [
    {
      featureList: [],
      description:
    },
  ];
</script>

<SectionWrapper id="product">
  <div
    class="'flex flex-col gap-10 sm:gap-14 md:ga24 flex-1 items-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
        Start your lifetime <span class="text-indigo-400">fitness journey</span>
      </p>
      <h3
        class="text-3xl sm:text-4xl md:text-5xl mx-auto w-full font-semibold text-center"
      >
        Features For You
      </h3>
    </div>
    <div
      class="grid grid-cols-1 md:grid-cols-2 gap-14 md:gap-14 lg:gap-20 relative text-base"
    >
      {#each productFeatures as productFeature, index}
        <ProductCard {productFeature} {index}>
          {#if index === 0}{:else if index === 1}{:else}{/if}
        </ProductCard>
      {/each}
    </div>
  </div>
</SectionWrapper>
