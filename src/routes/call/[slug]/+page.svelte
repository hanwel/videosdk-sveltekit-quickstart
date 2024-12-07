<script lang="ts">
	import type { PageData } from './$types';
	import { page } from '$app/stores';
	import Videocall from './Videocall.svelte';

	export let data: PageData;
	const JWT = data.JWT;
	export const slug = $page.url.pathname.split('/')[2];
</script>

<div class="flex flex-col">
	<script src="/coi-serviceworker.js"></script>
	<Videocall {JWT} {slug} />
</div>
