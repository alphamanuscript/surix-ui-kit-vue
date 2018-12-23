<template>
  <div class="s-field-group">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({ name: 's-field-group' })
export default class extends Vue {}
</script>
