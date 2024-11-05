<script>
  import CtAs from "./CTAs.svelte";
</script>

<section
  class="py-16 md:py-24 flex flex-col gap-10 text-center items-center justify-center bg-transparent"
>
  <div
    class="bg-gray-200 border-2 border-lime-500 rounded-lg p-8 md:p-12 shadow-lg max-w-xl w-full mx-auto cta-box"
  >
    <h4
      class="text-2xl sm:text-3xl md:text-4xl poppins font-bold text-gray-900"
    >
      Transform Your <span class="poppins">Processes & Workflows</span>
    </h4>
    <p class="poppins text-lg sm:text-xl md:text-2xl text-gray-800 mt-2">
      ✦ Discover custom solutions now ✦
    </p>
    <div class="flex justify-center mt-6">
      <CtAs dark={true} />
    </div>
  </div>
</section>

<style>
  .cta-box {
    animation: float 2s ease-in-out infinite;
  }

  @keyframes float {
    0% {
      transform: translatey(0);
    }
    50% {
      transform: translatey(-25px);
    }
    100% {
      transform: translatey(0);
    }
  }
</style>
