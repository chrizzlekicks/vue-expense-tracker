<template>
	<div class="expense" :key="expense.id">
		<h2>Euro: {{ expense.value }}</h2>
		<p>{{ expense.date }}</p>
		<section>
			<button class="edit-btn">Edit</button>
			<button class="delete-btn" @click="onClick">Delete</button>
		</section>
	</div>
</template>

<script>
export default {
	name: 'Expense',
	props: {
		expense: { type: Object },
	},
	methods: {
		onClick(id) {
			this.$emit('delete-expense', id);
		},
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
	margin: 0.25rem;
	color: #fff;
	border-radius: 0.5rem;
	cursor: pointer;
}
section {
	display: flex;
	justify-content: space-around;
	align-items: center;
}
.delete-btn {
	background-color: #aa2a2a;
	border: 1px solid #aa2a2a;
}
.edit-btn {
	background-color: #0a9ba6;
	border: 1px solid #0a9ba6;
}
</style>
