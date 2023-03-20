<script setup>
import { ref, computed } from 'vue'

const professor = ref({
    nome: 'Eduardo da Silva',
    disciplinas: [
        'Desenvolvimento Web II', 
        'Desenvolvimento de Aplicativos para Dispositivos Móveis',
    ]
})

const possuiDisciplinas = computed(() => {
    return professor.value.disciplinas.length > 0 ? 'Sim' : 'Não'
})
</script>

<template>
    <div>
        <h1>Professor</h1>
        <p>Nome: {{ professor.nome }}</p>
        <p>Possui disciplinas: {{ possuiDisciplinas }}</p>
    </div>
</template>