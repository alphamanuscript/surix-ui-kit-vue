<template>
  <div class="s-app">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-app' })
export default class extends Vue {}
</script>