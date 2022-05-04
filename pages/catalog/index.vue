<template>
  <v-row justify="center" align="center">
    <v-col v-for="item in items" :key="item.id" cols="12" sm="8" md="6">
      <span>{{item.name}}</span>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'catalogPage',
  computed: {
    items: (state) => [
      {
        id: 1,
        name: 'item 1',
        price: 100
      }
    ]
  }
}
</script>
