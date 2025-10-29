<template>
  <div class="q-pa-md">
    <q-table
      title="Popis knjiga"
      :rows="rows"
      :columns="columns"
      row-key="name"
      hide-bottom
    />
  </div>
</template>

<script>
const columns = [
  {
    name: 'knjigaID',
    required: true,
    label: 'Knjiga ID',
    align: 'center',
    field: row => row.name,
    format: val => `${val}`,
    style: {
      fontSize:'14px'
    },
    headerStyle: {
      fontSize: '16px'
    }

  },
  { name: 'Naslov', align: 'center', label: 'Naslov', field: 'naslov'},
  { name: 'Autor', align:'center', label: 'Autor', field: 'autor'},
  { name: 'Opis', align:'center', label: 'Opis', field: 'opis'},
  { name: 'Slika', align:'center', label: 'Slika', field: 'slika'},
  { name: 'Status', align:'center', label: 'Status', field: 'status' }
  ]

const rows = [
  {
    name: 1,
    naslov: 'Vlak u snijegu',
    autor: 'Mato Lovrak',
    opis: 'Opis',
    slika: 'Slika',
    status: 'Zauzeta',
  },
  {
    name: 2,
    naslov: 'Družba Pere Kvržice',
    autor: 'Mato Lovrak',
    opis: 'Opis',
    slika: 'Slika',
    status: 'Slobodna',
  },
  {
    name: 3,
    naslov: 'Zločin i kazna',
    autor: 'Fjodor Mihajlovič Dostojevski',
    opis: 'Opis',
    slika: 'Slika',
    status: 'Zauzeta',
  }
]

export default {
  setup () {
    return {
      columns,
      rows
    }
  }
}
</script>