
import Cronometro from './Cronometro.vue';
<template>
    <div class="box has-text-weight-bold">
        <div class="columns">
            <div class="column is-7">
                {{tarefa.descricao|| ' Tarefa sem descrição'}}
            </div>
            <div class="column">
                <CronometroTempo :tempoEmSegundos="tarefa.duracaoEmSegundos"/>                
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import CronometroTempo from './Cronometro.vue';
import ITarefa from '@/interfaces/ITareda';

export default defineComponent({
    name: "TarefA",
    components: {
        CronometroTempo, 
    },
    props:{
        tarefa: {
            type: Object as PropType<ITarefa>,
                required: true
        }
    }
})
</script>

<style scoped>
.box{
    background: #faf0ca;
}
</style>