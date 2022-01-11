<template>
  <div class="my-sfc-component">
    <button @click="value = !value">Toggle</button>
    <pre>{{ value }}</pre>
  </div>
</template>
<script>
// import { computed } from 'vue';
import { ref } from "@vue/composition-api";

export default {
  props: {
    message: {
      type: String,
      default: "Hello World",
    },
  },
  setup() {
    const value = ref(false);
    return { value };
  },
};

// export default /*#__PURE__*/{
//   name: 'MySfcComponent', // vue component name
//   data() {
//     return {
//       counter: 5,
//       initCounter: 5,
//       message: {
//         action: null,
//         amount: null,
//       },
//     };
//   },
//   computed: {
//     changedBy() {
//       const { message } = this;
//       if (!message.action) return 'initialized';
//       return `${message.action} ${message.amount || ''}`.trim();
//     },
//   },
//   methods: {
//     increment(arg) {
//       const amount = (typeof arg !== 'number') ? 1 : arg;
//       this.counter += amount;
//       this.message.action = 'incremented by';
//       this.message.amount = amount;
//     },
//     decrement(arg) {
//       const amount = (typeof arg !== 'number') ? 1 : arg;
//       this.counter -= amount;
//       this.message.action = 'decremented by';
//       this.message.amount = amount;
//     },
//     reset() {
//       this.counter = this.initCounter;
//       this.message.action = 'reset';
//       this.message.amount = null;
//     },
//   },
// };
</script>

<style scoped>
.my-sfc-component {
  display: block;
  width: 400px;
  margin: 25px auto;
  border: 1px solid #ccc;
  background: #eaeaea;
  text-align: center;
  padding: 25px;
}
.my-sfc-component p {
  margin: 0 0 1em;
}
</style>
