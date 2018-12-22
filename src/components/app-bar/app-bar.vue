<template>
  <div class="s-app-bar text-thin">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-app-bar' })
export default class extends Vue {}
</script>