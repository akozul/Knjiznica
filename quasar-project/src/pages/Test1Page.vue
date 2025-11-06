<template>
  <q-page padding>
    <h4>Ovo je test1page</h4>

    <div class="q-pa-md q-gutter-sm">
      <q-btn push color="white" text-color="primary" label="Unread Mails">
        <q-badge color="orange" floating>{{ unread }}</q-badge>
      </q-btn>

      <q-btn dense color="purple" round icon="email" class="q-ml-md">
        <q-badge color="red" floating>{{ open }}</q-badge>
      </q-btn>
    </div>

    <div class="q-pa-md q-gutter-sm">
      <q-card
        class="my-card bg-secondary text-white"
        v-for="item in msg"
        :key="item.title"
      >
        <q-card-section>
          <div class="text-h6">{{ item.title }}</div>
          <div class="text-subtitle2">{{ item.author }}</div>
        </q-card-section>

        <q-card-section>
          {{ item.lorem }}
        </q-card-section>

        <q-separator dark />

        <q-card-actions>
          <q-btn flat @click="openMsg">Uključ</q-btn>
          <q-btn flat @click="deleteMsg">Isključ</q-btn>
        </q-card-actions>
      </q-card>

      <div class="q-pa-md row items-start q-gutter-md">
        <q-input v-model="title" label="Title" />
        <q-input v-model="author" label="Author" />
        <q-input v-model="text" label="Text" />
        <q-btn color="primary" label="Save" @click="save" />
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const msg = ref([
  {
    title: 'Pater noster',
    author: 'Jesus Christ',
    lorem: 'Páter nóster, qui es in cáelis, sanctificétur nómen túum...'
  },
  {
    title: 'Ave Maria',
    author: 'Lk, Anđeo Gabrijel',
    lorem: 'Ave Maria, gratia plena, Dominus tecum...'
  }
])

const unread = ref(22)
const open = ref(4)

const title = ref('')
const author = ref('')
const text = ref('')

function openMsg() {
  open.value--
  console.log('Uključ ' + open.value)
}

function deleteMsg() {
  unread.value--
  console.log('Isključ ' + unread.value)
}

function save() {
  console.log(title.value + ' ' + author.value + ' ' + text.value)
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
