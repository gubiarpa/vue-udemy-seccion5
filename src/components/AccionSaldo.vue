<template>
    <div>
        <button @click="accionBtn" :disabled="desactivar">{{texto}}</button>
    </div>
</template>

<script>
export default {
    props: {
        texto: String,
        desactivar: {
            type: Boolean,
            default: false
        }
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