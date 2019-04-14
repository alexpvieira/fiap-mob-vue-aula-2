<template>
    <div>
        <button @click="returnToFather()">Return to father</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: 'Returned message'
        }
    },

    methods: {
        returnToFather() {
            this.$emit('returnedValue', this.message)
        }
    }
}
</script>

<style>

</style>
