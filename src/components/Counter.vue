<template>
	<div>
		Your number is: {{ number }}
		<button @click="add">Add</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			number: 0,
		}
	},
	methods: {
		add() {
			this.number++
		},
	},
}
</script>
