<template>
    <div>
        <h2>Tipo de cuenta: {{cuenta}}</h2>
        <h2>Saldo: {{saldo}}</h2>
        <h2>Cuenta: {{estado ? 'Activa' : 'Inactiva'}}</h2>
        <select>
            <option v-for="(servicio, index) in servicios" :key="index">
                {{index + 1}} - {{ servicio }}
            </option>
        </select>
        <AccionSaldo texto="Aumentar saldo" />
        <AccionSaldo texto="Disminuir saldo" />
    </div>
</template>

<script>
import AccionSaldo from './AccionSaldo';
export default {
    components: {
        AccionSaldo
    },
    data() {
        return {
            saldo: 1000,
            cuenta: 'Visa',
            estado: false,
            servicios: ['giro', 'abono', 'transferencia']
        }
    },
    methods: {
        aumentar() {
            this.saldo += 100;
        },
        disminuir() {
            this.saldo -= 100;
        }
    }
}
</script>

<style>

</style>