<template>
    <div class="main">
        <div class="content" role="form" aria-label="Formulário de tarefas">
            <form @submit.prevent="onSubmit">
                <div class="mb-3">
                    <label for="taskText" class="form-label">Tarefa</label>
                    <input
                        type="text"
                        id="taskText"
                        v-model="text"
                        class="form-control"
                        placeholder="Adicionar tarefa"
                        required
                        aria-required="true"
                    />
                </div>
                <div class="mb-3 form-check">
                    <input
                        type="checkbox"
                        id="taskReminder"
                        v-model="reminder"
                        class="form-check-input"
                    />
                    <label for="taskReminder" class="form-check-label">Definir lembrete</label>
                </div>
                <button type="submit" class="btn btn-primary">Salvar Tarefa</button>
            </form>
            <div class="col-md-4">
                <section>
                    <strong>00:00:00</strong>
                </section>
            <button class="button">
            <span class="icon">
                <i class="fas fa-play"></i>
            </span>
            <span>play</span>
        </button>
        <button class="button">
            <span class="icon">
                <i class="fas fa-stop"></i>
            </span>
            <span>stop</span>
        </button>    
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Formulario',
  data() {
    return {
      text: '',
      reminder: false
    }
  },
  methods: {
    onSubmit() {
      // Adicione aqui a lógica para lidar com o envio do formulário
      // Por exemplo, emitir um evento ou atualizar um array de tarefas
      // Exemplo:
      this.$emit('add-task', {
        text: this.text,
        reminder: this.reminder
      });
      // Limpar o formulário após o envio
      this.text = '';
      this.reminder = false;
    }
  }
});
</script>