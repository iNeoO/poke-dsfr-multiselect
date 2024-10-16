<template>
  <div>
    <button>dawdawdaw</button>
    <div style="padding-left: 5rem; padding-right: 5rem">
      {{ values }}
      <dsfr-multi-select
        v-model="values"
        :options="options"
        search
        select-all
        id-key="key"
        label-key="value"
      />
    </div>
  </div>
  <button>dawdawdaw</button>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import DsfrMultiSelect from './components/DsfrMultiSelect.vue'

const options = [
  { key: 'name', value: 'Alice', toto: 'titi' },
  { key: 'age', value: '25', toto: 'titi' },
  { key: 'city', value: 'Paris', toto: 'titi' },
  { key: 'profession', value: 'Engineer', toto: 'titi' },
  { key: 'hobby', value: 'Photography', toto: 'titi' },
  { key: 'favorite_color', value: 'Blue', toto: 'titi' },
]
const values = ref<string[]>([])
</script>
