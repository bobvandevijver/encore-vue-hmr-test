<template>
  <div>
    <h1>Counter Hot Reloaded</h1>
    <p>Current count: {{count}}</p>
  </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class Test extends Vue {
        protected count: number = 0;

        private handle!: number;

        protected mounted() {
            this.handle = setInterval(() => {
                this.count++;
            }, 1000);
        }

        protected destroyed() {
            clearInterval(this.handle);
        }
    }
</script>

<style lang="css">
  h1 {
    background-color: white;
  }
</style>

