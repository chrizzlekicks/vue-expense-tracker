<template>
	<EditExpense v-if="showEditExpense" @hide-edit="hideEdit" />
	<main>
		<h1>Expense Tracker</h1>
		<InputField
			@add-expense="addExpense"
			inputText="Enter your expense here"
			btnText="Add expense"
		/>
		<Expenses
			:expenses="expenses"
			@delete-expense="deleteExpense"
			@show-edit="showEdit"
		/>
	</main>
</template>

<script>
import InputField from './components/InputField.vue';
import Expenses from './components/Expenses.vue';
import EditExpense from './components/EditExpense.vue';

export default {
	name: 'App',
	components: { InputField, Expenses, EditExpense },
	data() {
		return {
			expenses: [],
			showEditExpense: false,
		};
	},
	methods: {
		addExpense(newExpense) {
			this.expenses.push(newExpense);
		},
		deleteExpense(id) {
			this.expenses = this.expenses.filter((expense) => expense.id !== id);
		},
		showEdit(value) {
			this.showEditExpense = true;
			console.log(value);
		},
		hideEdit() {
			this.showEditExpense = false;
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

<style scoped>
main {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	width: 100vw;
	height: 100vh;
}

h1 {
	margin-bottom: 40px;
}
</style>
