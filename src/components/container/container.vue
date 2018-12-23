<template>
  <div class="s-container">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-container' })
export default class extends Vue {}
</script>