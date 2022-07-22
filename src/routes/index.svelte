<script>
	let color = '#47b2e4';
	$: code = '';

	function resetSVG() { code = ''; color = '#47b2e4'};
</script>

<div style="--theme-color: {color}">
	<div class="mt-8">
		<div>
			<label for="comment" class="block text-gray-700 text-xl font-bold"
				>STEP 1: Paste SVG code here</label
			>
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

	<label for="iconcolor" class="block text-xl font-bold text-gray-700 mt-8"
		>STEP 2: Select colour here</label
	>
	<input type="color" class="mt-3" bind:value={color} style="height: 50px;" />

	<div class="mt-6">
		<ul
			role="list"
			class="grid grid-cols-2 gap-x-4 gap-y-8 sm:grid-cols-3 sm:gap-x-6 lg:grid-cols-4 xl:gap-x-8"
		>
			<li class="relative">
				<div class="rounded-lg bg-white">
					<p class="icon-very-small mx-auto">{@html code}</p>
					<p class="block  sr-only mt-2 text-sm font-medium text-gray-500 pointer-events-none">
						80px x 80px
					</p>
				</div>
			</li>
			<li class="relative">
				<div class="rounded-lg bg-white">
					<p class="icon-small mx-auto">{@html code}</p>
					<p class="block  sr-only mt-2 text-sm font-medium text-gray-500 pointer-events-none">
						80px x 80px
					</p>
				</div>
			</li>

			<li class="relative">
				<div class="rounded-lg bg-white">
					<p class="icon-medium mx-auto">{@html code}</p>
					<p class="block  sr-only mt-2 text-sm font-medium text-gray-500 pointer-events-none">
						80px x 80px
					</p>
				</div>
			</li>

			<li class="relative">
				<div class="rounded-lg bg-white">
					<p class="icon-large mx-auto">{@html code}</p>
					<p class="block  sr-only mt-2 text-sm font-medium text-gray-500 pointer-events-none">
						80px x 80px
					</p>
				</div>
			</li>
		</ul>
	</div>

	<div class="mx-auto">
		<button
			type="button"
			on:click={resetSVG}
			class="inline-flex items-center px-5 py-2 border border-transparent text-base font-medium rounded-full shadow-sm text-white bg-slate-900 hover:bg-slate-600 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-slate-500"
			>Reset</button
		>
	</div>
</div>

<style>
	.icon-very-small {
		fill: var(--theme-color);
		height: 20px;
		width: 20px;
	}

	.icon-small {
		fill: var(--theme-color);
		height: 40px;
		width: 40px;
	}

	.icon-medium {
		fill: var(--theme-color);
		height: 60px;
		width: 60px;
	}

	.icon-large {
		fill: var(--theme-color);
		height: 80px;
		width: 80px;
	}
</style>
