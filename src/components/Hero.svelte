<script>
  import CtAs from "./CTAs.svelte";
  import Header from "./Header.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  import Stars from "./Stars.svelte";
</script>

<SectionWrapper>
  <Header />
  <div
    class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <h2
      class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold"
    >
      <span class="text-emerald-600">Business</span>
      Automation <br />
      <span
        class="text-slate-400 line-through whitespace-nowrap"
        style="font-size: 85%;">Is Hard</span
      ><br />
      Just Got <span class="text-emerald-600">Easier.</span>
    </h2>

    <p
      class="text-xl sm:text-xl md:text-2xl text-center max-w-[1000px] mx-auto w-full"
    >
      Less complexity, more efficiency. We're the expert by your side. <span
        class=""
        >Tailored processes automation, comprehensive process documentation,
        detailed analytics, and much more.
      </span>
    </p>
    <CtAs />
    <Stars />
  </div>
</SectionWrapper>
