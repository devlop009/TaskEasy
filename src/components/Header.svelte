<script>
  import { openModal } from "../store";
</script>

<header class="flex flex-col bg-transparent w-full z-20">
  <div
    class="max-w-[1400px] mx-auto w-full flex items-center justify-between p-4 py-6"
  >
    <a href="/">
      <h1 class="font-semibold">
        Task <span class="text-emerald-400">Easy</span>
      </h1>
    </a>
    <button
      on:click={() => ($openModal = true)}
      class="md:hidden grid place-items-center"
    >
      <i class="fa-solid fa-bars"></i>
    </button>
    <nav class="hidden md:flex items-center gap-4 lg:gap-6">
      <a
        href="#product"
        class="duration-200 hover:text-emerald-400 cursor-pointer">Product</a
      >
      <a
        href="#reviews"
        class="duration-200 hover:text-emerald-400 cursor-pointer">Reviews</a
      >
      <a href="#faqs" class="duration-200 hover:text-emerald-400 cursor-pointer"
        >FAQs</a
      >
      <button class="specialBtnDark">
        <a
          href="https://app.youform.com/forms/lij83rwv"
          target="_blank"
          class="specialBtnDark"
        >
          <p>Get Started</p>
        </a>
      </button>
    </nav>
  </div>
</header>
