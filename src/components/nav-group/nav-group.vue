<template>
  <div class="s-nav-group">
    <div class="s-nav-group-header">
      <slot name="header"></slot>
    </div>
    <div class="s-nav-group-content">
      <slot></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-nav-group' })
export default class extends Vue {}
</script>