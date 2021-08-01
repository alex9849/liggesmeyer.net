<template>
  <v-card
      class="mx-auto"
      max-width="500"
      outlined
  >
    <v-row class="ma-1">
      <v-col cols="4">
        <v-avatar
            size="100%"
        >
          <v-img src="../assets/ALiggesmeyer-Profil.jpg"></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="8">
        <v-card-title class="text-h5 text--primary pa-0 justify-center">
          Alexander Liggesmeyer
        </v-card-title>
      </v-col>

    </v-row>
  </v-card>
</template>

<script>
export default {
  name: "PersonCard"
}
</script>

<style scoped>

</style>