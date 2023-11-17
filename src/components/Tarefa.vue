
import Cronometro from './Cronometro.vue';
<template>
    <div class="box has-text-weight-bold">
        <div class="columns">
            <div class="column is-7">
                descrição
            </div>
            <div class="column">
                <CronometroTempo :tempoEmSegundos="15"/>                
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import CronometroTempo from './Cronometro.vue';

export default defineComponent({
    name: "TarefA",
    components: {
        CronometroTempo, 
    },
})
</script>

<style scoped>
.box{
    background: #faf0ca;
}
</style>