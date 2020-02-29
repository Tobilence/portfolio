<template>
  <v-app>
    <!-- Toolbar -->
    <Navbar></Navbar>

    <v-content class="ml-1">
      <router-view></router-view>
    </v-content>

  </v-app>
</template>

<script>
  import Navbar from '@/components/Navbar'

  export default {
    name: 'App',

    components: {
      Navbar
    },

    data: () => ({
      //
    })
  };
</script>