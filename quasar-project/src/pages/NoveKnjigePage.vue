<template>
  <q-page padding>
    <!-- content -->
     <q-toolbar class="bg-grey-9 text-white">
      <q-toolbar-title>Nove knjige</q-toolbar-title>
     </q-toolbar>
     <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <img src="https://ezop-antikvarijat.hr/wp-content/uploads/2020/10/products-0a3bd4bac496b44163e2ef5d20283066.jpg">

        <q-card-section>
          <div class="text-h6">Knjiga Vlak u snijegu</div>
          <div class="text-subtitle2">Napisao Mato Lovrak</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          {{ Vlak}}
        </q-card-section>
    </q-card>

    <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

          <q-card-section>
            <div class="text-h6">Our Changing Planet</div>
            <div class="text-subtitle2">by John Doe</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            {{ lorem }}
          </q-card-section>
    </q-card>
    
        <q-card class="my-card">
      <img src="https://cdn.quasar.dev/img/mountains.jpg">

          <q-card-section>
            <div class="text-h6">Our Changing Planet</div>
            <div class="text-subtitle2">by John Doe</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            {{ lorem }}
          </q-card-section>
      </q-card>
      
  </div>
  </q-page>
</template>

<script>
export default {
  setup () {
    return {
      Vlak:'Kad se mnogo malih složi, tad se snaga stoput množi, a to znači da smo jači, kad se skupimo u zbor.',
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
      
    }
  }
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
