<script lang="ts">
  export let text = "Learn more";
  export let href = "#";
</script>

<div class="bg-black text-white text-[10px] md:text-[11px] font-medium py-2.5 md:py-3 px-3 md:px-4 flex flex-col sm:flex-row justify-between items-center gap-2 sm:gap-4 tracking-wide">
  <div class="flex-1 text-center">
    <span class="opacity-90">
      <span class="hidden sm:inline">Trusted partner of Sunrun • Keep your solar warranty when you replace your roof</span>
      <span class="sm:hidden">Trusted Sunrun partner • Keep your solar warranty</span>
    </span>
  </div>
  <a {href} class="bg-primary-600 hover:bg-primary-700 text-white px-2.5 md:px-3 py-1 md:py-1.5 rounded text-[9px] md:text-[10px] font-bold uppercase tracking-wider transition-colors whitespace-nowrap">
    {text}
  </a>
</div>
