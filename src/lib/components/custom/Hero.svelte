<script lang="ts">
  import { onMount } from 'svelte';
  import { fly } from 'svelte/transition';

  let visible = false;

  onMount(() => {
    visible = true;
  });

  function typewriter(node, { speed = 100 }) {
    const valid =
      node.childNodes.length === 1 &&
      node.childNodes[0].nodeType === Node.TEXT_NODE;

    if (!valid) {
      throw new Error(
        `This transition only works on elements with a single text node child`
      );
    }

    const text = node.textContent;
    const duration = text.length * speed;

    return {
      duration,
      tick: (t) => {
        const i = ~~(text.length * t);
        node.textContent = text.slice(0, i);
      },
    };
  }
</script>

<div class="bg-gray-700 h-64 flex flex-col justify-center items-center">
  {#if visible}
    <p class="text-gray-100 text-2xl font-semibold" in:typewriter>
      Software Developer
    </p>
    <div
      class="text-red-400 text-sm "
      transition:fly={{ x: -500, duration: 3000 }}
    >
      <p>Javascript | Typescript | HTML | CSS</p>
    </div>
    <div
      class="text-gray-300 text-sm"
      transition:fly={{ x: 500, duration: 8000 }}
    >
      <p>NodeJS | Graphql | Postgres</p>
    </div>
  {/if}
</div>
