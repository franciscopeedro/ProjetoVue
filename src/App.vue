<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter ">
      <BarraLateral/>
    </div>
    <div class="column is-three-quarter ">
      <FormularioTarefas @aoSalvarTarefa="salvarTarefa"/>
      <div class="lista">
        <TarefA v-for="(tarefa, index) in tarefas " :key="index" :tarefa="tarefa"/>
      </div>
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateral from './components/BarraLateral.vue';
import FormularioTarefas from './components/Formulario.vue';
import TarefA from './components/Tarefa.vue'
import ITarefa from './interfaces/ITareda';

export default defineComponent({
  name: 'App',
  components: {
  BarraLateral,
  FormularioTarefas,
  TarefA,
  },
  data (){
    return {
      tarefas: [] as ITarefa[]
    }
  },
  methods:{
    salvarTarefa(tarefa:ITarefa){
    this.tarefas.push(tarefa)}
  }
});
</script>

<style>
.lista{
  padding:  1.25rem;

}
</style>
