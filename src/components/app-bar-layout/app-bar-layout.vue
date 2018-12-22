<template>
  <div class="s-app-bar-layout">
    <slot name="app-bar"></slot>
    <div class="s-app-bar-layout-content">
      <slot></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-app-bar-layout' })
export default class extends Vue {}
</script>
