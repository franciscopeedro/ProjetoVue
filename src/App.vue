<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter ">
      <BarraLateral/>
    </div>
    <div class="column is-three-quarter ">
      <FormularioTarefas/>
      <div class="lista">
        <TarefA/>
        <TarefA/>
        <TarefA/>
        <TarefA/>
      </div>
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateral from './components/BarraLateral.vue';
import FormularioTarefas from './components/Formulario.vue';
import TarefA from './components/Tarefa.vue'

export default defineComponent({
  name: 'App',
  components: {
  BarraLateral,
  FormularioTarefas,
  TarefA
  }
});
</script>

<style>
.lista{
  padding:  1.25rem;

}
</style>
