<template>
	<AutoLink
		:to="to"
		class="flex mb-3 leading-none items-center gap-1 text-primary text-lg font-bold hover:underline group w-fit"
	>
		<slot />
		<ChevronRightIcon
			class="h-5 w-5 stroke-[3px] motion-safe:group-hover:translate-x-1 motion-safe:transition-transform group-hover:text-brand"
		/>
	</AutoLink>
</template>

<script setup lang="ts">
import { ChevronRightIcon } from '@modrinth/assets'

import AutoLink from './AutoLink.vue'

defineProps<{
	to: unknown
}>()
</script>
