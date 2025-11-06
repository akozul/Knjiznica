<template>
  <q-page padding>
    <!-- content -->
     <a :href="link.url" :target="link.target">{{ link.text }}</a>
     <h2>{{ poruka }}</h2>
     <p v-html="poruka"></p>
     <p v-html="porukica"></p>
     <p v-html="htmlText"></p>
     <p v-text="htmlText"></p>
     <p v-for="item in days" :key="item">
      <button v-if="item == 'Ponedjeljak'">
        {{ item }}*
      </button>
      <button v-else-if="Item == 'Srijeda'" v-show="false">
        {{ item }}
      </button>
      <button v-else>
        {{ item }}
      </button>
     </p>

     <q-input color="red" v-model="text1" label="Item name" @keyup="log()"></q-input>
  </q-page>
</template>

<script setup>
import {ref} from 'vue'
const poruka = "Test page"
const porukica = "Ovo je testna stranica za isprobavanje"
const days = ["Ponedjeljak", "Utorak", "Srijeda", "Četvrtak", "Petak", "Subota", "Nedjelja"]


const text1 = ref('')
text1.value = "Hello"
function log(){
  console.log(text1.value)
}

const link = {
  url: 'http://www.google.com',
  target:'_blank',
  text: 'Google' 
}
</script>
