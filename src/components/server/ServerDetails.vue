<template>
  <div class="column">
    <p v-if="!server">Please select a server.</p>
    <p v-else>Server {{ server.id }} is currently: <strong>{{ server.status }}</strong></p>
    <hr>
    <button @click="resetStatus" class="button is-danger">Fix Server</button>
  </div>
</template>

<script>
  import { serverBus } from '../../main';
  export default {
    data: function(){
      return{
        server: null
      }
    },
    methods: {
      resetStatus(){
        this.server.status = 'Normal';
      }
    },
    created() {
      serverBus.$on('serverSelected', (server) => {
        this.server = server;
      });
    }
  }
</script>

<style>
</style>
