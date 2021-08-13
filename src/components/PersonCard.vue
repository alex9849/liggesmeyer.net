<template>
  <v-card
      class="mx-auto"
      max-width="500"
      outlined
  >
    <div class="row ma-0">
      <div class="col-12 col-sm-4">
        <v-avatar
            size="100%"
        >
          <v-img src="../assets/ALiggesmeyer-Profil.jpg"></v-img>
        </v-avatar>
      </div>
      <div class="pa-2 col-12 col-sm-8 d-flex flex-column" align="left">
        <div class="text-h5 text--primary pa-0"
        >
          {{ value.name }}
        </div>
        <div style="color: #666666">
          {{ value.subtitle }}
        </div>
        <div class="flex-grow-1"></div>
        <div class="d-flex flex-row">
          <div class="me-1" v-for="(link, i) in value.links" :key="i">
            <v-btn icon outlined
                   color="black"
                   :href="link.href"
                   target="_blank"
            >
              <v-icon>
                {{ link.icon }}
              </v-icon>
            </v-btn>
          </div>
        </div>
      </div>

    </div>
  </v-card>
</template>

<script>
export default {
  name: "PersonCard",
  props: {
    value: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>