<script setup>
const props = defineProps(['operacao', 'resultado']);
</script>

<template>
    <div class="row">
        <div class="col-md-4">
            <input v-model="operacao.n1" type="number" class="form-control" placeholder="Digite o primeiro número">
        </div>
        <div class="col-md-4">
            <input v-model="operacao.n2" type="number" class="form-control" placeholder="Digite o segundo número">
        </div>
        <div class="col">
            <select v-model="operacao.filtro" class="form-select">
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">*</option>
                <option value="/">/</option>
            </select>
        </div>
    </div>
    <div class="row mt-4">
        <h3 class="mb-4">Resultado</h3>
        <label class="form-control"> {{ resultado }}</label>
    </div>
</template>

<style scoped>
    label,
    h3 {
        text-align: center;
    }
</style>