<template>
	<header>
		<h1>{{ title }}</h1>
		<button v-on:click="sendEvent">send</button>
	</header>
</template>

<script>
export default {
	props: ['title'],
	methods: {
		sendEvent: function () {
			this.$emit('renew');
		},
	},
};
</script>

<style></style>
