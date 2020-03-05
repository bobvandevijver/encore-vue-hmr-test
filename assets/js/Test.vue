<template>
  <div>
    <h1>Vue is </h1>

    <h2>{{counter}}</h2>

    <div>
      <button @click="counter++">Add 1</button>
    </div>
  </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class Test extends Vue {
        protected counter: number = 0;
    }
</script>

<style lang="css">
  h1 {
    background-color: green;
  }
</style>

