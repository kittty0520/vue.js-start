<template>
	<div id="app">
		<form action="" v-on:submit.prevent="submitForm">
			<div>
				<label for="username">id: </label>
				<input type="text" id="username" v-model="username" />
			</div>
			<div>
				<label for="password">password: </label>
				<input type="password" id="password" v-model="password" />
			</div>
			<button type="submit">login</button>
		</form>
	</div>
</template>

<script>
import axios from 'axios';
export default {
	name: 'App',
	data: function () {
		return {
			username: '',
			password: '',
		};
	},
	components: {},
	methods: {
		submitForm: function () {
			// event.preventDefault();
			var url = 'https://jsonplaceholder.typicode.com/users';
			var data = {
				username: this.username,
				password: this.password,
			};
			axios
				.post(url, data)
				.then((res) => console.log(res))
				.catch((error) => console.log(error));
		},
	},
};
</script>

<style></style>
