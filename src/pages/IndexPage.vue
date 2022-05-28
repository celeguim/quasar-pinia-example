<template>
  <q-page padding>
    <p class="col-12 text-h6 text-center">Store1</p>
    <div class="row q-pa-md q-gutter-sm">
      <div class="col">
        <q-banner class="col bg-blue-4 text-white">
          <q-btn @click="store.increment"> Increment </q-btn>
        </q-banner>
      </div>
      <q-banner class="col bg-blue-4 text-white">
        <div class="col">Counter: {{ store.counter }}</div>
        <div class="col">Double Count: {{ store.doubleCount }}</div>
      </q-banner>
    </div>

    <q-banner> </q-banner>
    <p class="col-12 text-h6 text-center">Store2</p>
    <div class="row q-pa-md q-gutter-sm">
      <div class="col">
        <q-banner class="col bg-green-4 text-white">
          <q-btn @click="store2.increment"> Increment </q-btn>
        </q-banner>
      </div>
      <q-banner class="col bg-green-4 text-white">
        <div class="col">Counter: {{ store2.counter }}</div>
        <div class="col">Double Count: {{ store2.doubleCount }}</div>
      </q-banner>
    </div>
  </q-page>
</template>

<script>
import { useCounterStore } from "src/stores/store1";
import { useCounterStore2 } from "src/stores/store2";

export default {
  setup() {
    const store = useCounterStore();
    const store2 = useCounterStore2();

    return {
      // you can return the whole store instance to use it in the template
      store,
      store2,
    };
  },
};
</script>
