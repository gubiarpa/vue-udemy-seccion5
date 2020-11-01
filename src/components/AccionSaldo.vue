<template>
    <div>
        <button @click="accionBtn">{{texto}}</button>
    </div>
</template>

<script>
export default {
    props: {
        texto: String
    },
    methods: {
        accionBtn() {
            this.$emit('accion')
        }
    }
}
</script>

<style>

</style>