<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <span>Product {{$route.params.id}}</span>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'productPage',
  validate({params}) {
    return /^\d+$/gi.test(params.id)
  }
}
</script>
