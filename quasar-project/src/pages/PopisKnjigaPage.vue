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
  { name: 'Stanje', align:'center', label: 'Stanje', field: 'stanje' }
  ]

const rows = [
  {
    name: 1,
    naslov: 'The Very Hungry Caterpillar',
    autor: 'Eric Carle',
    opis: 'As an added bonus, it includes read-aloud audio of Eric Carle reading his classic story. This fine audio production pairs perfectly with the classic story, and it makes for a fantastic new way to encounter this famous, famished caterpillar.',
    slika: 'Slika',
    stanje: 3,
  },
  {
    name: 2,
    naslov: 'Palace of Palms: Tropical Dreams and the Making of Kew',
    autor: 'Kate Teltscher',
    opis: 'The body is assaulted by heat, light and the smell of damp vegetation. In Palace of Palms, Kate Teltscher tells the extraordinary story of its creation and of the Victoriansâ€™ obsession with the palms that filled it.',
    slika: 'Slika',
    stanje: 1,
  },
  {
    name: 3,
    naslov: 'Zločin i kazna',
    autor: 'Fjodor Mihajlovič Dostojevski',
    opis: 'Opis',
    slika: 'Slika',
    stanje: 'Zauzeta',
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