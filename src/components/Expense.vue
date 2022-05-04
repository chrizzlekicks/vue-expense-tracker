<template>
	<div class="expense">
		<h2>{{ expense.value }}</h2>
		<button @click="$emit('delete-expense', expense.id)">Delete</button>
	</div>
</template>

<script>
export default {
	name: 'Expense',
	props: {
		expense: { type: Object },
	},
};
</script>

<style scoped>
.expense {
	padding: 0.5rem;
	display: flex;
	justify-content: space-between;
	align-items: center;
	border: 1px solid #2c3e50;
	border-radius: 1rem;
	width: auto;
	margin: 0.5rem;
}
h2 {
	text-align: center;
}
button {
	padding: 1rem;
	background-color: #aa2a2a;
	border: 1px solid #aa2a2a;
	color: #fff;
	border-radius: 0.5rem;
	cursor: pointer;
}
</style>
