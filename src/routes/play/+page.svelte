<main>
	<h1>Svordle</h1>

	<div id="board">
		{#each Array.from({ length: 6 }) as row, y}
			<div class="row" data-row={y}>
				{#each Array.from({ length: 5 }) as tile, x}
					<div class="tile" data-tile={x}></div>
				{/each}
			</div>
		{/each}
	</div>
</main>

<style>
	main {
		margin: 0 auto;
		width: 350px;
		text-align: center;
	}

	#board {
		height: 420px;
		display: grid;
		grid-template-rows: repeat(6, 1fr);
		grid-gap: 5px;
	}

	.row {
		display: grid;
		grid-template-columns: repeat(5, 1fr);
		grid-gap: 5px;
	}

	.tile {
		border: 2px solid #e5e5e5;
	}
</style>
