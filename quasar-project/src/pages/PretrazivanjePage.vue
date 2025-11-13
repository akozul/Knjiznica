<script setup>
import { ref } from 'vue'

const query = ref('')
const searchByAuthor = ref(false)
const searchByTitle = ref(false)


const columns = [
  { name: 'knjigaID', required: true, label: 'Knjiga ID', align: 'center', field: 'knjigaID' },
  { name: 'Naslov', align: 'center', label: 'Naslov', field: 'naslov' },
  { name: 'Autor', align: 'center', label: 'Autor', field: 'autor' },
  { name: 'Opis', align: 'center', label: 'Opis', field: 'opis' },
  { name: 'Slika', align: 'center', label: 'Slika', field: 'slika' },
  { name: 'Stanje', align: 'center', label: 'Stanje', field: 'stanje' }
]


const rows = ref([])
</script>

<template>
  <div class="q-pa-md">

    
    <div class="q-gutter-md row items-center q-mb-md">
      <q-input filled v-model="query" label="Pretraži knjige..." class="col-6" />

      <div class="row items-center q-gutter-sm">
        <q-checkbox v-model="searchByAuthor" label="Autor" />
        <q-checkbox v-model="searchByTitle" label="Naslov" />
      </div>

      <q-btn label="Traži" color="primary" class="q-ml-md" />
    </div>

    
    <q-table
      title="Rezultati pretraživanja"
      :rows="rows"
      :columns="columns"
      row-key="knjigaID"
      flat
      bordered
      hide-bottom
    />
    
  </div>
</template>
