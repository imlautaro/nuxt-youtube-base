<template>
	<div>
		<hello-world />
		<counter />
		<div v-if="fetchState.pending">Loading..</div>
		<div v-else-if="fetchState.error">Error</div>
		<div v-else>
			{{ data }}
		</div>
	</div>
</template>

<script setup>
import { useContext, useFetch, ref } from '@nuxtjs/composition-api'

const { $axios } = useContext()

const data = ref()

const { fetch, fetchState } = useFetch(async () => {
	data.value = await $axios.$get(
		'https://www.dolarsi.com/api/api.php?type=valoresprincipales'
	)
})
</script>
