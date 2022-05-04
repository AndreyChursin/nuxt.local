<template>
  <v-row justify="center" align="center">
    <v-col v-for="product in products" :key="product.id" cols="12" sm="3" md="4">
      <v-card @click.prevent="openProduct(product)">
        <v-card-title class="headline">{{product.name}}</v-card-title>
        <v-card-text>
          <span>Price: {{product.price}}</span>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'catalogPage',
  computed: {
    products: (state) => [
      {
        id: 1,
        name: 'item 1',
        price: 100,
        description: 'description item 1'
      },
      {
        id: 2,
        name: 'item 2',
        price: 200,
        description: 'description item 2'
      },
      {
        id: 3,
        name: 'item 3',
        price: 3000,
        description: 'description item 3'
      },
    ]
  },
  methods: {
    openProduct(product) {
      this.$router.push('/catalog/product/' + product.id)
    }
  }
}
</script>
