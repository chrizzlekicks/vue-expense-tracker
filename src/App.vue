<script setup>
import InputField from './components/InputField.vue';
import Expense from './components/Expense.vue';
</script>

<template>
	<h1>Expense Tracker</h1>
	<InputField />
	<ul id="expense-wrapper">
		<Expense />
		<Expense />
		<Expense />
	</ul>
</template>

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
#expense-wrapper {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	max-width: 1140px;
	width: 100%;
	margin: 1rem;
}
</style>
