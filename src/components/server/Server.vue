<template>
  <tr>
    <th
      style="cursor: pointer;"
      @click="serverSelected">
      Server {{ server.id }}</th>
  </tr>
</template>

<script>
  import { serverBus } from '../../main';
  export default {
    props: ['server'],
    methods: {
      serverSelected(){
        serverBus.$emit('serverSelected', this.server);
      }
    }
  }
</script>

<style></style>
