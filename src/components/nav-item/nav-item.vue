<template>
  <div class="s-nav-item" :class="classObject">
    <slot></slot>
  </div>
</template>
<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component({ name: 's-nav-item' })
export default class extends Vue {
  @Prop({ type: Boolean }) active!: boolean;
  get classObject () {
    return {
      's-active': this.active
    }
  }
}
</script>
