<template>
	<div>
		Your number is: {{ number }}
		<button @click="add">Add</button>
	</div>
</template>

<script setup>
import { ref } from '@nuxtjs/composition-api'

const number = ref(0)

const add = () => {
	number.value++
}
</script>
