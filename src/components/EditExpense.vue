<template>
	<main>
		<article>
			<h3>Edit your expense</h3>
			<InputField />
		</article>
	</main>
</template>

<script>
import InputField from './InputField.vue';

export default {
	name: 'EditExpense',
	components: { InputField },
};
</script>

<style scoped>
main {
	background-color: rgba(247, 247, 247, 0.75);
	width: 100%;
	height: 100%;
	top: 0;
	position: absolute;
	z-index: 1;
	display: grid;
	place-items: center;
}
article {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	width: 450px;
	height: 125px;
	border: 1px solid #c2c2c2;
	border-radius: 10px;
	background-color: #eee;
	box-shadow: 3px 12px 20px rgba(97, 100, 91, 0.2);
}
</style>
