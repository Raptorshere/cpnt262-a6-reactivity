<script>
let name = 'Kevin';
let colour = 'red';
let boardGames = ["Battleship", "Monopoly", "Taboo", "Yahtzee"];

let child = {
  name: "Charlie", 
  age: 16, 
  hobby: "Playing board games"
};

const handleClick = () => {
  colour = 'blue';
};

const functionInput = (e) => {
 colour = e.target.value

}

setTimeout(() => {
boardGames = [...boardGames, "Jenga"];
}, 3000) ;

setTimeout(() => {
child.hobby = "Making puzzles";
}, 3000);

import Button from './button.svelte'
</script>


<main class= "text-center p-4, max-width-96px, margin-40px-auto">

<h1 class="text-3xl font-bold underline">Hello {name}</h1>
<div class="pointer-events-none focus:pointer-events-auto"></div>
<p>{colour}: colours</p>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<button on:click={handleClick}>Update the color</button>
<input type="text" on:input={functionInput}>
  

<div class="text-bold">Board Games: Arrays of objects</div>
<ul>
  {#each boardGames as item}
    <li>{item}</li>
  {/each}
</ul>

<p>{child.name} is an average school-age kid. He is {child.age} years old and enjoys {child.hobby}</p>

<button>Toggle</button>
</main>

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }

  /* :global(main) {
		background-color: #f2eee2;
		color: #0084f6;
		transition: background-color 0.3s
	}
	:global(main.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
  } --> */
  </style>

 <!-- <style lang="postcss">
	:global(main) {
		background-color: #f2eee2;
		color: #0084f6;
		transition: background-color 0.3s
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	} -->
<!-- </style> -->

