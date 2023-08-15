<script setup lang="ts">
import { ref } from "vue";
const count = ref(0);
</script>

<template>
	<div class="counter-container">
		<h4>The current count is:</h4>
		<h1>{{ count }}</h1>
		<span class="button-wrapper">
			<button @click="count--">-</button>
			<button @click="count++">+</button>
		</span>
	</div>
</template>

<style scoped>
.counter-container {
	display: flex;
	align-items: center;
	justify-content: space-around;
	flex-direction: column;
	width: 40%;
	height: 50%;
	font-size: 50px;
	border: 1px solid gray;
	border-radius: 8px;
	background-color: white;
	padding: 1rem 2rem;
	color: #343a40;
}

.button-wrapper {
	display: flex;
	align-items: center;
	justify-content: space-around;
	flex-direction: row;
	width: 50%;
}

button {
	padding: 8px 8px;
	font-size: 25px;
	background-color: #2b52dd;
	color: white;
	border-radius: 8px;
	border: none;
	width: 3rem;
	height: 3rem;
	cursor: pointer;
}

button:hover {
	transform: scale(1.1);
}

@media (max-width: 400px) {
	button {
		width: 2rem;
		height: 2rem;
		font-size: 15px;
	}

	.button-wrapper {
		justify-content: space-between;
	}
}
</style>
