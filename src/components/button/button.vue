<template>
  <button class="s-button" :class="classObject">
    <slot></slot>
  </button>
</template>
<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component({ name: 's-button' })
export default class extends Vue {
  @Prop({ type: Boolean }) fill!: boolean;

  get classObject () {
    return {
      's-fill': this.fill
    };
  }
}
</script>