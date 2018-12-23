<template>
  <div class="s-panel-body">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-panel-body' })
export default class extends Vue {}
</script>