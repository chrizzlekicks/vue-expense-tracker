<template>
	<div>
		<input type="text" placeholder="Enter your expense here" />
		<button>Add Expense</button>
	</div>
</template>

<style scoped>
div {
	display: flex;
	flex: 1;
}
input {
	padding: 0.5rem;
	border-top-left-radius: 1rem;
	border-bottom-left-radius: 1rem;
	border: 1px solid #2c3e50;
	width: auto;
}
button {
	padding: 0.5rem;
	border-top-right-radius: 1rem;
	border-bottom-right-radius: 1rem;
	border: 1px solid #2c3e50;
	background-color: #2c3e50;
	color: #fff;
	cursor: pointer;
	transition: all 0.2s ease-in-out;
}
button:hover {
	background-color: #fff;
	color: #2c3e50;
}
</style>
