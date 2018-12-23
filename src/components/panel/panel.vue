<template>
  <div class="s-panel">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-panel' })
export default class extends Vue {}
</script>
