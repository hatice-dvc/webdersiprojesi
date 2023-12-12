<template>
  <q-page class="row items-center justify-evenly">
    <router-link to="/sepet/siparis"
      >Bu ana sayfa içi rota bağlantısı</router-link
    >
    <example-component
      title="Example component"
      active
      :todos="todos"
      :meta="meta"
    ></example-component>
  </q-page>
</template>

<script setup lang="ts">
import { Todo, Meta } from 'components/models';
import ExampleComponent from 'components/ExampleComponent.vue';
import { ref } from 'vue';

const todos = ref<Todo[]>([
  {
    id: 1,
    content: 'ct1 2',
  },
  {
    id: 2,
    content: 'ct2 2',
  },
  {
    id: 3,
    content: 'ct3 2',
  },
  {
    id: 4,
    content: 'ct4 2',
  },
  {
    id: 5,
    content: 'ct5 2',
  },
]);
const meta = ref<Meta>({
  totalCount: 1200,
});
</script>
