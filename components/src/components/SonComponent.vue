<template>
    <div>
        <h1>{{ msg }}</h1>
        <p>{{ text }}</p>
    </div>
</template>

<script>
export default {
    name: 'SonComponent',

    props: {
        msg: {
            type: String,
            required: true
        },
        text: {
            type: String,
            default: 'Default message'
        }
    }
}
</script>

<style scoped>
div {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
