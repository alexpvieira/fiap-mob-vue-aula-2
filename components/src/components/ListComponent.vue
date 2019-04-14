<template>
    <div>
        <ul>
            <li v-for="framework in frameworks">
                {{ framework }}
            </li>
        </ul>

        <p>{{ framework_message }}</p>
    </div>
</template>

<script>
export default {
    name: 'ListComponent',

    props: ['framework_message'],

    data() {
        return {
            frameworks: ['Vue', 'React', 'Angular']
        }
    }
}
</script>

<style>
</style>