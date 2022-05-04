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
	background-color: rgba(255, 255, 255, 0.85);
}
article {
	display: flex;
	flex-direction: column;
	align-items: center;
	width: 10rem;
	height: auto;
	border: 1px solid #c2c2c2;
}
</style>
