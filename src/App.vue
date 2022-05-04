<template>
	<h1>Expense Tracker</h1>
	<InputField />
	<Expenses :expenses="expenses" @delete-expense="deleteExpense" />
</template>

<script>
import InputField from './components/InputField.vue';
import Expenses from './components/Expenses.vue';

export default {
	name: 'App',
	components: { InputField, Expenses },
	data() {
		return {
			expenses: [],
		};
	},
	methods: {
		deleteExpense(id) {
			this.expenses = this.expenses.filter((expense) => expense.id !== id);
		},
	},
	created() {
		this.expenses = [
			{ id: 0, value: 12 },
			{ id: 1, value: 187 },
		];
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
	display: flex;
	flex-direction: column;
	align-items: center;
}
</style>
