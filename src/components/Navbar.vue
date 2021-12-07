<template>
  <v-container>
    <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      <v-spacer />
       <v-btn outlined class="ml-1">
         <router-link to="/">Home </router-link>
        </v-btn>
    
      <v-btn outlined class="ml-3">
        <router-link to="/photos">Photos </router-link>
      </v-btn>

    </v-app-bar>
  </v-container>
</template>

<script>
  export default {
    name: 'Navbar',
  }
</script>
