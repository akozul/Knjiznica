<template>
  <q-page padding>
    <!-- content -->
     <q-toolbar class="bg-grey-9 text-white">
      <q-toolbar-title>Popis knjiga</q-toolbar-title>
     </q-toolbar>
     <div class="q-pa-md" style="max-width: 350px">
    <q-list bordered separator>
      <q-item clickable v-ripple>
        <q-item-section>Popis knjiga</q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section>
          <q-item-label>Vlak u snijegu</q-item-label>
          <q-item-label caption>Mato Lovrak</q-item-label>
        </q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section>
          <q-item-label>Item with caption</q-item-label>
          <q-item-label caption>Caption</q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
  </div>
  </q-page>
</template>

<script setup>
//
</script>
