<script lang="ts">
  import Hero from './lib/components/custom/Hero.svelte';
  import Header from './lib/components/shared/Header.svelte';
</script>

<div class="font-body">
  <Header logoText={'RP'} />

  <main class="p-2">
    <Hero />

    <section id="skills" class="mt-8 p-4">
      <p
        class="text-gray-700 font-semibold text-2xl text-center border-b-8 hover:border-red-500 border-red-400 py-2 w-8"
      >
        Skills
      </p>

      <div class="skillList mt-4 flex flex-col space-y-1 w-full">
        <div
          class="bg-gray-800 text-green-50 p-1 font-semibold flex justify-center items-center w-full"
        >
          HTML
        </div>
        <div
          class="bg-gray-800 text-blue-50 p-1 font-semibold flex justify-center items-center w-full"
        >
          Javascript
        </div>
        <div
          class="bg-gray-300 text-blue-50 p-1 font-semibold flex justify-center items-center w-full"
        >
          Javascript
        </div>
      </div>
    </section>

    <section id="projects" class="mt-8 p-4">
      <p
        class="text-gray-700 font-semibold text-2xl text-center border-b-8 hover:border-red-500 border-red-400 py-2 w-8"
      >
        Projects
      </p>
      <div
        id="projectList"
        class="mt-4 flex flex-col space-y-4 sm:flex-row sm:space-y-0 sm:space-x-4 justify-around text-sm font-semibold text-gray-400"
      >
        <div
          class="w-full h-32 bg-gray-100 hover:bg-gray-200 flex justify-center items-center rounded cursor-pointer"
        >
          <a href="#" class="hover:text-red-500">Project #1</a>
        </div>
        <div
          class="w-full h-32 bg-gray-100 hover:bg-gray-200 flex justify-center items-center rounded cursor-pointer"
        >
          <a href="#" class="hover:text-red-500">Project #2</a>
        </div>
        <div
          class="w-full h-32 bg-gray-100 hover:bg-gray-200 flex justify-center items-center rounded cursor-pointer"
        >
          <a href="#" class="hover:text-red-500">Project #3</a>
        </div>
        <div
          class="w-full h-32 bg-gray-100 hover:bg-gray-200 flex justify-center items-center rounded cursor-pointer"
        >
          <a href="#" class="hover:text-red-500">Project #4</a>
        </div>
      </div>
    </section>
  </main>
</div>

<style>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>
