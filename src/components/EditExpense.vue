<template>
	<main>
		<article>
			<h3>Edit your expense</h3>
			<InputField inputText="Modify your expense" btnText="Edit expense" />
			<p @click="onHideEdit">Close</p>
		</article>
	</main>
</template>

<script>
import InputField from './InputField.vue';

export default {
	name: 'EditExpense',
	components: { InputField },
	props: {
		expenses: {
			type: Array,
		},
	},
	methods: {
		onHideEdit() {
			this.$emit('hide-edit');
		},
	},
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
	height: auto;
	border: 1px solid #c2c2c2;
	border-radius: 10px;
	background-color: #fff;
	box-shadow: 3px 12px 20px rgba(97, 100, 91, 0.2);
	padding: 1rem;
}
h3 {
	margin-bottom: 1rem;
}
p {
	margin-top: 0.75rem;
	text-decoration: underline;
	color: #c2c2c2;
	cursor: pointer;
}
p:hover {
	color: #2c3e50;
}
</style>
