<script>
import CardComp from './components/CardComp.vue'

export default {
  components: {
    CardComp
  }
}
</script>

<template>
  <div id="wrapper">
    <CardComp>
      <template v-slot:headerSlot>
        <h3>Escape from Tarkov</h3>
      </template>

      <template v-slot:default>
        <p>Egy extraction shooter amit éveken át lehet játszani</p>
      </template>

      <template v-slot:footerSlot>
        Értékelés: 2/10
      </template>
    </CardComp>

    <CardComp>
      <template #headerSlot>
        <h3>Németh Ádám</h3>
      </template>

      <template #default>
        <p>Hobbi: Motorozás</p>
      </template>
    </CardComp>
  </div>
</template>

<style>
#wrapper {
  display: flex;
  flex-wrap: wrap;
  padding: 20px;
}

h3 {
  margin: 0;
}

p {
  margin: 0;
}
</style>