<template>
  <v-app>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <FooterComponent />
    </v-footer>
  </v-app>
</template>

<script>

export default {
    name: 'DefaultLayout',
}
</script>
