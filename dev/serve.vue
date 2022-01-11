<script>
import Vue from 'vue';
import MySfcComponent from '@/my-sfc-component.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    MySfcComponent
  }
});
</script>

<template>
  <div id="app">
    <my-sfc-component />
  </div>
</template>
