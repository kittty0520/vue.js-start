<template>
	<div id="app">
		<app-header v-bind:title="str" v-on:renew="renewStr"></app-header>
	</div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
export default {
	name: 'App',
	data: function () {
		return {
			str: 'Header',
		};
	},
	components: {
		'app-header': AppHeader,
	},
	methods: {
		renewStr: function () {
			this.str = 'hi';
		},
	},
};
</script>

<style></style>
