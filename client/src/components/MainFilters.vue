<template>
  <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md q-my-md row items-start">
    <q-input outlined dense v-model="autor" label="Автор" />

    <q-input outlined dense v-model="book" label="Книга" />
    <div>
      <q-btn label="Поиск" type="submit" color="primary" />
      <q-btn label="Сбросить" type="reset" color="secondary" flat class="q-ml-sm" />
    </div>
  </q-form>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const autor = ref('');
const book = ref('');

const onSubmit = async () => {
  if (!autor.value.length && !book.value.length) return;
};
const onReset = () => {
  autor.value = '';
  book.value = '';
};
</script>

<style scoped></style>
