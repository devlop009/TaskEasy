<script>
  import ReviewCard from "./ReviewCard.svelte";
  import SectionWrapper from "./SectionWrapper.svelte";
  import Stars from "./Stars.svelte";

  let lim = true;

  let reviewsList = [
    {
      name: "Jenna F.",
      review:
        "With multiple locations opening, we needed a uniform way of handling onboarding for new hires, scheduling, and customer feedback. Task Easy created custom flows for us to make sure everything is in sync across different outlets. Now, it's our managers and team with real-time updates, and it's made our operations so much more efficient! Can't recommend them enough.",
      features: ["Restaurant Franchise Owner", "Smart Workflow Automation"],
    },
    {
      name: "Mike Taylor",
      review:
        "As an independent real estate agent, I could just never get any organization together, from lead generation down to follow-ups with clients, the team at Task Easy put together an incredibly detailed workflow for me and then automated it that shaved 30% off the time taken to complete repetitive tasks. They also spent extra time optimizing the flow. What I love is they documented everything, and now I'm always referring to this in my team. Thank you.",
      features: ["Real-Estate Agent", "Process Design & Docummentation"],
    },
    {
      name: "Michael Lee",
      review:
        "Task Easy's workflow maker was a game-changer. With their help, we’ve built a system that organizes everything from food prep to marketing campaigns, saving us countless hours. Their expertise in creating a customized workflow really shines.",
      features: [
        "Restaurant Owner",
        "Smart Workflow Automation",
        "Process Design & Docummentation",
      ],
    },
    {
      name: "Sam H Williams",
      review:
        "The documentation service with Task Easy saves me so much time. They diagrammed our entire valuation and closing processes and made a digital model so that we would have a crystal-clear reproducible system. The guys are extremely detail oriented. Definitely work with you guys again!",
      features: ["Investor", "Process Design & Docummentation"],
    },
    {
      name: "Carl Matthews",
      review:
        "Keeping track of memberships, bookings, payments was a nightmare for us. Task Easy a flow that handles all these tasks, sending reminders and updates to clients automatically. Our clients really appreciate the smooth communication.",
      features: ["Fitness Studio Owner", "Smart Workflow Automation"],
    },
    {
      name: "Mark Lawson",
      review:
        "Running an ecommerce business keeping track of inventory, orders, shipping, returns and much more. Task Easy documented my processes step by step and made them easy for my staff to follow. They also created a centralized place for us to monitor every platform we sell on. I have an operation I can trust to run smoothly! Thanks Again guys.",
      features: ["E-commerce", "Process Design & Docummentation"],
    },
    {
      name: "David West",
      review:
        "Task Easy created a process for onboarding clients and managing projects. Their documentation made it easy to keep everything in line, from kickoff meetings to progress updates Everything is well documented and automated. Now, my clients get a more professional experience, and I can keep up with multiple projects effortlessly.",
      features: ["Marketing Consultant", "Process Design & Docummentation"],
    },
  ];
</script>

<SectionWrapper id="reviews">
  <div
    class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
  >
    <div class="flex flex-col gap-2">
      <h3
        class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
      >
        See What <span class="text-emerald-400">Other Businesses</span> Have To Say
      </h3>
    </div>
    <div class="flex flex-col md:flex-row gap-8 w-fit mx-auto">
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} left={true} {index} />
        {/each}
      </div>
      <div class="w-[1px] bg-slate-400 hidden md:flex"></div>
      <div class="flex flex-col gap-8">
        {#each lim ? reviewsList.slice(0, 4) : reviewsList as reviewItem, index}
          <ReviewCard {reviewItem} {index} />
        {/each}
      </div>
    </div>
    <button on:click={() => (lim = !lim)} class="specialBtnDark">
      <p>{lim ? "Show More" : "Show Less"}</p>
    </button>
    <div class="flex flex-col gap-10">
      <p class="mx-auto text-lg sm:text-xl md:text-2xl font-semibold">
        Trusted by over 200 businesses world-wide
      </p>
      <Stars />
    </div>
  </div>
</SectionWrapper>
