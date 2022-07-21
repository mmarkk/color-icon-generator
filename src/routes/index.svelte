<script>
	let color = '#47b2e4';
	$: code = '';
</script>

<div style="--theme-color: {color}">
	<div class="mt-8">
		<div>
			<label for="comment" class="block text-gray-700 text-xl font-bold">Paste SVG code here</label>
			<div class="mt-1">
				<textarea
					rows="10"
					bind:value={code}
					name="comment"
					id="comment"
					class="shadow-sm focus:ring-indigo-500 focus:border-indigo-500 block w-full sm:text-sm border-gray-300 rounded-md"
				/>
			</div>
		</div>
	</div>

	<label for="iconcolor" class="block text-xl font-bold text-gray-700 mt-8">Select colour here</label
	>
	<input type="color" bind:value={color} style="height: 50px;" />

	<div style="--theme-color: {color}">
		<p class="icon mx-auto mt-8">{@html code}</p>
	</div>
</div>

<style>
	.icon {
		fill: var(--theme-color);
		height: 80px;
		width: 80px;
	}
</style>
