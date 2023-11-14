<script>
let name = 'Kevin';
let colour = 'red';

const handleClick = () => {
  colour = 'blue';
};

const functionInput = (e) => {
 colour = e.target.value

}
</script>

<main class= "text-center p-4, max-width-96px, margin-40px-auto">

<h1 class="text-3xl font-bold underline">Hello {name}</h1>
<div class="pointer-events-none focus:pointer-events-auto"></div>
<p>{colour}: colours</p>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<button on:click={handleClick}>Update the color</button>
<input type="text" on:input={functionInput}>
  
</main>

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
  </style>

