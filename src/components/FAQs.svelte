<script>
  import SectionWrapper from "./SectionWrapper.svelte";

  let faqs = [
    {
      question: "How do you determine which tasks to automate?",
      ans: " We conducts an assessment of your operations to identify repetitive tasks that can be automated. This ensures our solutions  maximize efficiency and save time for your business.",
    },
    {
      question: "Do you provide maintenance and upgrades for the systems?",
      ans: "Yes, we offer ongoing maintenance for all workflows to ensure optimal performance and address any issues that may arise. Additionally, as teams use the systems and provide feedback, we continually improve them to enhance functionality and efficiency.",
    },
    {
      question: "Is pricing based on hourly rates or a fixed project fee?",
      ans: "We charge a fixed price for each project, based on the specific requirements and scope of the work. This allows for clear, upfront pricing with no surprises, ensuring that you know the total investment from the start.",
    },
    {
      question:
        "What if our employees don’t know how to use the custom systems?",
      ans: "We includes training with each custom system at no additional cost. Our sessions ensure that your team is well-prepared to use the systems effectively.",
    },
  ];

  let openIndex = null;

  function toggleFaq(index) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<SectionWrapper id="faqs">
  <div class="flex flex-col items-center justify-center py-20">
    <div
      class="w-full max-w-[65%] flex flex-col gap-10 sm:gap-14 md:gap-24 px-4"
    >
      <div class="flex flex-col gap-2 text-center">
        <h3 class="text-4xl sm:text-5xl md:text-6xl font-semibold">
          Frequently Asked Questions
        </h3>
      </div>

      <div class="flex flex-col gap-4 w-full">
        {#each faqs as faq, index}
          <div class="border-b border-gray-300 pb-4">
            <button
              type="button"
              on:click={() => toggleFaq(index)}
              aria-expanded={openIndex === index}
              aria-controls="faq-content-{index}"
              class="w-full flex items-center justify-between py-4 px-6 text-left text-lg font-medium text-white-400 transition-colors
                hover:border hover:border-white hover:bg-transparent"
            >
              <span class="text-xl">{faq.question}</span>
              <svg
                class="w-6 h-6 transition-transform duration-200"
                style="transform: rotate({openIndex === index ? 180 : 0}deg);"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M19 9l-7 7-7-7"
                />
              </svg>
            </button>

            <div
              id="faq-content-{index}"
              class="overflow-hidden transition-[max-height] duration-300"
              style="max-height: {openIndex === index ? '1000px' : '0'};"
            >
              <p class="pl-6 pt-4 text-white-600 text-sm">{faq.ans}</p>
              <!-- Increased padding here and reduced font size -->
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
</SectionWrapper>
