<script lang="ts">
	import { goto } from '$app/navigation';
</script>

<div class="box py-2 px-4 flex gap-4 items-center">
	<span class="flex flex-grow-0 flex-shrink-0 bg-neutral-200 w-12 h-12 rounded-full" />

	<input
		class="bg-neutral-50 border border-neutral-300 outline-none rounded-lg px-4 py-2 w-full font-medium placeholder:text-neutral-600 text-left focus:ring-2 ring-offset-1 ring-brand-color-light"
		placeholder="Create Post"
		on:mousedown={() => goto('/create-post')}
		on:keydown={(e) => {
			if (e.key !== 'Tab') goto('/create-post');
		}}
	/>
</div>
