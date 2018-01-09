<template>
  <div class="column">
    <table class="table is-bordered is-fullwidth is-hoverable">
      <thead>
        <tr>
          <th>Server No.</th>
        </tr>
      </thead>
      <tbody>
        <app-server
            v-for="server in servers"
            :server="server">
        </app-server>
      </tbody>
    </table>
  </div>
</template>

<script>

  import Server from './Server.vue'

  export default {
    data: function(){
      return{
        servers: [
          { id:1, status: 'Normal' },
          { id:2, status: 'Critical' },
          { id:3, status: 'Unknown' },
          { id:4, status: 'Normal' }
        ]
      };
    },
    components: {
      appServer: Server
    }
  }
</script>

<style></style>
