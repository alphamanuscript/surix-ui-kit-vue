<template>
  <div class="s-drawer-layout">
    <slot name="drawer"></slot>
    <div class="s-drawer-layout-main">
      <slot></slot>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-drawer-layout' })
export default class extends Vue {}
</script>
