<script lang="ts">
	export let id: string = '';
	export let labelClass: string =
		'mb-2 text-sm font-medium text-gray-900 sr-only dark:text-gray-300';
	export let inputClass: string =
		'block p-4 pl-10 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500';
	export let btnClass: string =
		'text-white absolute right-2.5 bottom-2.5 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800';
	export let placeholder: string = 'Search';
	export let value = '';
</script>

<form on:submit>
	<label for={id} class={labelClass}>Search</label>
	<div class="relative">
		<div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
			<svg
				class="w-5 h-5 text-gray-500 dark:text-gray-400"
				fill="none"
				stroke="currentColor"
				viewBox="0 0 24 24"
				xmlns="http://www.w3.org/2000/svg"
				><path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
				/></svg
			>
		</div>
		<input
			{...$$restProps}
			on:blur
			on:change
			on:click
			on:focus
			on:keydown
			on:keypress
			on:keyup
			on:mouseenter
			on:mouseleave
			on:mouseover
			on:paste
		       	bind:value
			type="search"
			{id}
			class={inputClass}
			{placeholder}
		/>
		<button type="submit" class={btnClass}>Search</button>
	</div>
</form>
