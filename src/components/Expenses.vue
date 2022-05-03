<template>
	<section class="expenses" v-for="expense in expenses" :key="expense.id">
		<Expense :expense="expense" />
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
