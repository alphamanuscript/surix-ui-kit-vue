<template>
  <div class="s-drawer">
    <div class="s-drawer-header">
      <slot name="header"></slot>
    </div>
    <div class="s-drawer-content">
      <slot></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-drawer' })
export default class extends Vue {};
</script>