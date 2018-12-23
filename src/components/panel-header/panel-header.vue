<template>
  <div class="s-panel-header">
    <div class="s-panel-title">
      <slot name="title"></slot>
    </div>
    <div class="s-panel-subtitle">
      <slot name="subtitle"></slot>
    </div>
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-panel-header' })
export default class extends Vue {}
</script>