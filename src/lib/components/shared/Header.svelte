<script lang="ts">
  import Icon, { Menu } from 'svelte-hero-icons';

  export let logoText;

  let displayMenu = true;

  const toggleMenu = () => (displayMenu = !displayMenu);
</script>

<header
  class="flex flex-wrap flex-row justify-between md:items-center md:space-x-4 bg-white py-6 px-6 relative"
>
  <a href="#" class="block font-semibold p-1 bg-gray-700 text-white">
    <span>{logoText}</span>
  </a>

  <button
    class="inline-block md:hidden w-8 h-8 bg-gray-200 text-gray-600 p-1"
    on:click={toggleMenu}
  >
    <Icon src={Menu} size="24" />
  </button>

  {#if displayMenu}
    <nav
      class="absolute md:relative top-16 left-0 md:top-0 z-20 md:flex flex-col md:flex-row md:space-x-6 w-full md:w-auto bg-white shadow-md rounded-lg md:rounded-none md:shadow-none md:bg-transparent p-6 pt-0 md:p-0"
    >
      <a href="#" class="block py-1 text-gray-600 hover:underline">Home</a>
      <a href="#" class="block py-1 text-gray-600 hover:underline">Resume</a>
      <a href="#" class="block py-1 text-gray-600 hover:underline">Contact</a>
    </nav>
  {/if}
</header>
