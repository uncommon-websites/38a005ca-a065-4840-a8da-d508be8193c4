<script lang="ts">
  import { page } from '$app/stores';
  
  let mobileMenuOpen = $state(false);
</script>

<nav class="bg-black text-white py-3 md:py-4 px-4 md:px-6 flex items-center justify-between sticky top-0 z-50 border-b border-gray-900">
  <div class="flex items-center gap-4 md:gap-8">
    <a href="/" class="flex items-center gap-2">
      <div class="w-7 h-7 md:w-8 md:h-8 text-white">
        <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M5.0473 17.8386L5.69453 18.9586V18.9601H18.3003L18.9314 17.84H6.34063L6.82626 16.9993H19.4308L20.078 15.8807H7.47237L7.95715 15.0414H16.0358L16.0366 15.0429L16.0375 15.0414H20.5603L20.5612 15.0429L21.2084 13.9228L21.208 13.922L21.2084 13.9213H21.2075L14.9084 3.00677L14.9106 3.00296L14.9062 3.00296L13.6177 3.00296L5.0473 17.8386ZM14.261 4.12767L13.7751 4.96887L18.9438 13.9213H19.9139L14.261 4.12767ZM13.1286 6.08808L12.6467 6.9225L16.6749 13.9006L16.6634 13.9213H17.6511L13.1286 6.08808ZM11.9999 8.04225L8.60411 13.9213H15.3899L11.9999 8.04225ZM6.99833 3.30006C7.33866 3.10343 7.7248 2.99993 8.11786 3L2.30033 13.0776C2.10357 12.7371 2 12.3508 2 11.9575C2 11.5643 2.10357 11.178 2.30033 10.8375L6.17916 4.12006C6.37543 3.77951 6.65798 3.49669 6.99833 3.30006ZM9.08869 3H10.3816L3.43223 15.0384L2.785 13.9184L9.08869 3ZM11.3509 3H12.6424L4.56262 16.9963L3.91691 15.8777L11.3509 3ZM21.7064 13.0598C21.8988 12.7254 22 12.3463 22 11.9605C22 11.5746 21.8988 11.1956 21.7064 10.8611L17.8039 4.10233C17.6108 3.7681 17.3331 3.49057 16.9987 3.2976C16.6644 3.10463 16.2852 3.00302 15.8992 3.00296H15.8741L21.6931 13.082L21.7064 13.0598ZM17.7995 19.7994H6.17916C6.37472 20.1412 6.65692 20.4253 6.99728 20.6232C7.33763 20.8212 7.72414 20.9258 8.11786 20.9269H15.8829C16.2737 20.9261 16.6572 20.8212 16.994 20.6231C17.3309 20.4249 17.6089 20.1406 17.7995 19.7994Z"
            fill="currentColor"
          />
        </svg>
      </div>
      <span class="text-xl md:text-2xl font-medium tracking-tight">Remi</span>
    </a>
    
    <div class="hidden lg:flex items-center gap-6 text-[13px] font-medium text-gray-300">
      <a href="#services" class="hover:text-white transition-colors">Services</a>
      <a href="#how-it-works" class="hover:text-white transition-colors">How it works</a>
      <a href="#warranties" class="hover:text-white transition-colors">Warranties</a>
      <a href="#coverage" class="hover:text-white transition-colors">Coverage</a>
      <a href="#careers" class="hover:text-white transition-colors">Careers</a>
    </div>
  </div>

  <div class="flex items-center gap-2 md:gap-4">
    <a href="tel:916-999-7497" class="text-gray-300 hover:text-white transition-colors text-xs md:text-[13px] hidden sm:block">
      916.999.7497
    </a>
    <a href="#quote" class="bg-primary-600 hover:bg-primary-700 text-white px-3 md:px-4 py-1.5 md:py-2 rounded-full text-xs md:text-[13px] font-medium transition-colors whitespace-nowrap">
      Get a quote
    </a>
    
    <!-- Mobile menu button -->
    <button 
      onclick={() => mobileMenuOpen = !mobileMenuOpen}
      class="lg:hidden text-white p-2"
      aria-label="Toggle menu"
    >
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        {#if mobileMenuOpen}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        {:else}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        {/if}
      </svg>
    </button>
  </div>
</nav>

<!-- Mobile menu -->
{#if mobileMenuOpen}
  <div class="lg:hidden bg-black border-b border-gray-900 sticky top-[57px] md:top-[65px] z-40">
    <div class="px-4 py-4 flex flex-col gap-3 text-sm font-medium text-gray-300">
      <a href="#services" class="hover:text-white transition-colors py-2" onclick={() => mobileMenuOpen = false}>Services</a>
      <a href="#how-it-works" class="hover:text-white transition-colors py-2" onclick={() => mobileMenuOpen = false}>How it works</a>
      <a href="#warranties" class="hover:text-white transition-colors py-2" onclick={() => mobileMenuOpen = false}>Warranties</a>
      <a href="#coverage" class="hover:text-white transition-colors py-2" onclick={() => mobileMenuOpen = false}>Coverage</a>
      <a href="#careers" class="hover:text-white transition-colors py-2" onclick={() => mobileMenuOpen = false}>Careers</a>
    </div>
  </div>
{/if}
