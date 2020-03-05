<template>
  <Test/>
</template>

<script lang="ts">
    import Test from './Test.vue';
    import {Component, Vue} from 'vue-property-decorator';

    @Component({
        components: {Test},
    })
    export default class TestContainer extends Vue {

    }
</script>
