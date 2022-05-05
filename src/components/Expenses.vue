<template>
	<section class="expenses">
		<Expense
			v-for="expense in expenses"
			:expense="expense"
			@delete-expense="$emit('delete-expense', expense.id)"
			@show-edit="$emit('show-edit', expense.value)"
		/>
	</section>
</template>

<script>
import Expense from './Expense.vue';

export default {
	name: 'Expenses',
	props: {
		expenses: { type: Array },
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
	margin: 40px 0.5rem;
}
</style>
