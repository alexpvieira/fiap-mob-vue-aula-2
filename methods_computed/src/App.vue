<template>
	<div id="app">
		<p><label for="value_1">First value</label>
		<input name="value_1" type="number" v-model="value_1" /></p>

		<p><label for="value_2">Second value</label>
		<input name="value_2" type="number" v-model="value_2" /></p>

		<p><label for="total">Total method</label>
		<input name="total" type="number" v-model="total" disabled /></p>

		<p><label for="total">Total computed</label>
		<input name="total" :value="totalComputed" disabled /></p>

		<p><label for="total">Formated value</label>
		<input name="total" v-model="formated_value" disabled /></p>

		<button @click="calculateTotal()">Calculate total</button><br>
		<button @click="calculateTotalWithParamethers('sum')">Sum total</button><br>
		<button @click="calculateTotalWithParamethers('multiplicate')">Multiplicate total</button>
	</div>
</template>

<script>
export default {
	data() {
		return {
			value_1: 0,
			value_2: 0,
			total: 0,
			formated_value: ''
		}
	},

	methods: {
		calculateTotal() {
			this.total = parseInt(this.value_1) + parseInt(this.value_2)

			this.formatValue(this.total)
		},

		calculateTotalWithParamethers(type) {
			if (type === 'sum') {
				this.total = parseInt(this.value_1) + parseInt(this.value_2)
			}
			else if (type === 'multiplicate') {
				this.total = parseInt(this.value_1) * parseInt(this.value_2)
			}
		},

		formatValue(value) {
			this.formated_value = `R$ ${value}`
		}
	},

	computed: {
		totalComputed() {
			return parseInt(this.value_1) + parseInt(this.value_2)
		}
	}
}
</script>

<style>

</style>
