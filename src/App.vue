<template>
    <div class="container is-fluid">
      <app-header></app-header>
      <hr>
      <div class="columns">
        <app-servers></app-servers>
        <app-server-details></app-server-details>
      </div>
      <hr>
      <app-footer></app-footer>
    </div>
</template>

<script>
  import Header from './components/shared/Header.vue';
  import Footer from './components/shared/Footer.vue';
  import Servers from './components/server/Servers.vue';
  import ServerDetails from './components/server/ServerDetails.vue';

  export default {
    components: {
      'app-header': Header,
      'app-servers': Servers,
      'app-server-details': ServerDetails,
      'app-footer': Footer
    }
  }

</script>

<style>
  .container
  {
    max-width: 800px;
    margin: auto;
    padding: 0 15px;
  }
</style>
