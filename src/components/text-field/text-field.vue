<template>
    
  <input v-if="!multiline"
    class="s-text-field"
    type="text"
    :placeholder="placeholder"
  />
  <textarea v-else
    class="s-text-field"
    :placeholder="placeholder"
  ></textarea>
  
</template>
<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component({ name: 's-text-field' })
export default class extends Vue {
  @Prop({ type: Boolean }) multiline = false;
  @Prop({ type: String }) placeholder!: string;
}
</script>
