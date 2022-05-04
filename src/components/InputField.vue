<template>
	<form class="wrapper" @submit.prevent="onSubmit">
		<input
			class="input"
			type="text"
			name="exxpense"
			v-model="exxpense"
			placeholder="Enter your expense here"
		/>
		<button class="input-btn">Add Expense</button>
	</form>
</template>

<script>
export default {
	name: 'InputField',
	props: {
		addExpense: {
			type: Function,
		},
	},
	data() {
		return {
			exxpense: '',
		};
	},
	methods: {
		onSubmit() {
			if (!this.exxpense) {
				alert('Please provide an expense');
				return;
			}

			let date = new Date();

			const newExpense = {
				id: Math.floor(Math.random() * 100000),
				date: date.toLocaleString(),
				value: this.exxpense,
			};

			this.$emit('add-expense', newExpense);

			this.exxpense = '';
		},
	},
};
</script>

<style>
.wrapper {
	display: flex;
	margin-bottom: 1rem;
}
.input {
	padding: 0.5rem;
	border-top-left-radius: 1rem;
	border-bottom-left-radius: 1rem;
	border: 1px solid #2c3e50;
	width: auto;
}
.input-btn {
	padding: 0.5rem;
	border-top-right-radius: 1rem;
	border-bottom-right-radius: 1rem;
	border: 1px solid #2c3e50;
	background-color: #2c3e50;
	color: #fff;
	cursor: pointer;
	transition: all 0.2s ease-in-out;
}
.input-btn:hover {
	background-color: #fff;
	color: #2c3e50;
}
</style>
