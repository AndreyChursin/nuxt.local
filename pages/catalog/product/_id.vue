<template>
   <v-row justify="center" align="center">
    <v-col cols="12" sm="3" md="4">
      <v-card>
        <v-card-title class="headline">Product name</v-card-title>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'productPage',
  validate(contecst) {
    console.log(contecst);
    return true;
    // /^\d+$/gi.test(params.id)
  },
}
</script>
