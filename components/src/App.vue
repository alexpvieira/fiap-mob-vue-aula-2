<template>
	<div id="app">
		<SonComponent :msg="message"/>

		<ListComponent />

		<ReturnComponent @returnedValue="returnedMethod" />
	</div>
</template>

<script>
import SonComponent from './components/SonComponent.vue'
import ListComponent from './components/ListComponent.vue'
import ReturnComponent from './components/ReturnComponent.vue'

export default {
	name: 'app',

	components: {
		SonComponent,
		ListComponent,
		ReturnComponent
	},

	data() {
		return {
			message: 'Hello World - FIAP Vue'
		}
	},

	methods: {
		returnedMethod(message) {
			this.message = message
		}
	}
}
</script>

<style>

</style>
