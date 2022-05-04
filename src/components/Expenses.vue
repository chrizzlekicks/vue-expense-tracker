<template>
	<section class="expenses" v-for="expense in expenses">
		<Expense
			:expense="expense"
			@delete-expense="$emit('delete-expense', expense.id)"
		/>
	</section>
</template>

<script>
import Expense from './Expense.vue';

export default {
	name: 'Expenses',
	props: {
		expenses: Array,
	},
	components: {
		Expense,
	},
	emits: ['delete-expense'],
};
</script>

<style>
.expenses {
	display: flex;
	flex-direction: column;
	width: 100%;
	max-width: 1140px;
	margin: 0.5rem;
}
</style>
