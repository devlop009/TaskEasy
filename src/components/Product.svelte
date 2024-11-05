<script>
  import ProductCard from "./ProductCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  let productFeatures = [
    {
      featureList: [
        "Streamlined Workflows",
        "Tremendous Timesaving",
        "Integration Between Flows",
        "Flawless Execution",
      ],
      description:
        "Re-imagine your daily workflows by automating key tasks, automate repetitive tasks and free-up time to focus on meaningful work.",
      imgUrl: "assets/workflow.gif",
    },
    {
      featureList: [
        "Tailored Processes",
        "Enhance Process Efficiency",
        "Scalable For Future Needs",
        "Extensive Documentation",
      ],
      description:
        "Processes are built from ground-up, tailored to your business and your way of doing business. Designed to streamline operation and reduce inefficiencies. With each step clearly documented allowing your team to reference them in future, ensuring effectiveness over-time.",
      imgUrl: "assets/processes.gif",
    },
  ];
</script>

<SectionWrapper id="product">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <div class="flex flex-col gap-2">
      <p class="opacity-80 text-base sm:text-lg md:text-xl text-center">
        Get Started With <span class="text-emerald-400"> Task Easy </span> today
      </p>
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        Products
      </h3>
    </div>

    {#each productFeatures as productFeature, index}
      <ProductCard {productFeature} {index}>
        {#if index === 0}
          Smart Work-Flow <span class="text-emerald-400 font-medium"
            >Automation</span
          >
        {:else if index === 1}
          Process Design & <span class="text-emerald-400 font-medium"
            >Documentation</span
          >
        {/if}
      </ProductCard>
    {/each}
  </div>
</SectionWrapper>
