<template>
	<h1>Expense Tracker</h1>
	<InputField @add-expense="addExpense" />
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
		addExpense(newExpense) {
			this.expenses.push(newExpense);
		},
		deleteExpense(id) {
			console.log(id);
			this.expenses = this.expenses.filter((expense) => expense.id !== id);
		},
	},
	created() {
		this.expenses = [
			{ id: 0, date: '12/05/2021, 8:13:12 AM', value: 101 },
			{ id: 1, date: '01/03/2021, 11:36:59 AM', value: 187 },
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
