<template>
	<div class="wrapper">
		<input class="input" type="text" placeholder="Enter your expense here" />
		<button class="input-btn">Add Expense</button>
	</div>
</template>

<script>
export default {
	name: 'InputField',
};
</script>

<style>
.wrapper {
	display: flex;
	flex: 1;
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
