<script lang="ts">
  const steps = [
    {
      num: "01",
      title: "Get your quote",
      desc: "Get a guaranteed quote in minutes online. No surprises, no change orders, just transparent pricing.",
      img: "/generated/image-contractor-reviewing-project-plans-and-d-1765510448955-3.webp"
    },
    {
      num: "02",
      title: "Schedule & prep",
      desc: "We handle all permits and inspections. Your dedicated Remi expert coordinates everything.",
      img: "/generated/image-roofing-contractor-on-ladder-inspecting--1765510455277-5.webp"
    },
    {
      num: "03",
      title: "Installation",
      desc: "Our licensed, bonded, and insured contractors complete your roof. Get automated text updates throughout.",
      img: "/generated/image-professional-roofing-crew-installing-new-1765510438531-0.webp"
    },
    {
      num: "04",
      title: "Enjoy peace of mind",
      desc: "Your new roof is complete with a 5-year workmanship warranty. You saved 6-8 weeks compared to traditional contractors.",
      img: "/generated/image-happy-homeowner-couple-standing-in-front-1765510445989-2.webp"
    }
  ];
</script>

<section class="bg-white py-24 px-6" id="how-it-works">
  <div class="max-w-[1200px] mx-auto">
    <h2 class="text-[40px] leading-tight font-light text-gray-900 mb-16 max-w-[600px]">
      Get your new roof in four simple steps. Save 6-8 weeks on average.
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
      {#each steps as step}
        <div class="flex flex-col">
          <div class="bg-black text-white text-xs font-bold w-8 h-8 flex items-center justify-center rounded mb-6">
            {step.num}
          </div>
          <h3 class="text-xl font-normal mb-2">{step.title}</h3>
          <p class="text-gray-500 text-sm leading-relaxed mb-6 min-h-[80px]">{step.desc}</p>
          <div class="rounded-xl overflow-hidden h-[200px] bg-gray-100">
            <img src={step.img} alt={step.title} class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-500" />
          </div>
        </div>
      {/each}
    </div>

    <div class="bg-[#f9f9f7] rounded-2xl p-12 flex flex-col md:flex-row items-center justify-between gap-8">
      <div>
        <h3 class="text-2xl font-light mb-2">Questions about the process?</h3>
        <p class="text-gray-500 text-sm">Call us at 916.999.7497 or email support@remihq.com</p>
      </div>
      <div class="flex gap-4">
        <a href="tel:916-999-7497" class="px-6 py-3 bg-white border border-gray-200 hover:bg-gray-50 rounded-lg text-sm font-medium transition-colors">
          Call us
        </a>
        <a href="#quote" class="px-6 py-3 bg-primary-600 hover:bg-primary-700 text-white rounded-lg text-sm font-medium transition-colors flex items-center gap-2">
          Get a quote
        </a>
      </div>
    </div>
  </div>
</section>
