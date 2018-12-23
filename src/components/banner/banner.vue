<template>
  <div class="s-banner">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-banner' })
export default class extends Vue {}
</script>