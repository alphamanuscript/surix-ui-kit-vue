<template>
  <s-app>
    <s-drawer-layout>
      <s-drawer slot="drawer">
        <div slot="header">
          Happy Feet
        </div>
        <div>
          <s-nav-group>
            <div slot="header">
              Current App
            </div>
            <s-nav-item>Compose</s-nav-item>
            <s-nav-item active>Inbox</s-nav-item>
            <s-nav-item>Reports</s-nav-item>
          </s-nav-group>
          <s-nav-separator />
          <s-nav-item>Apps</s-nav-item>
          <s-nav-item>Marketplace</s-nav-item>
          <s-nav-separator />
          <s-nav-item>Settings</s-nav-item>
          <s-nav-item>Manage users</s-nav-item>
        </div>
      </s-drawer>
      <s-app-bar-layout>
        <s-app-bar slot="app-bar">
          New product
        </s-app-bar>
        <div>
          <s-banner></s-banner>
          <s-container class="mt-lg">
            <s-panel class="mb-lg">
              <s-panel-header>
                <div slot="title">
                  Basic details
                </div>
                <div slot="subtitle">
                  Basic information about the product
                </div>
              </s-panel-header>
              <s-panel-body>
                <s-field-group>
                  <s-text-field placeholder="Enter name" />
                </s-field-group>
                <s-field-group>
                  <s-text-field multiline  placeholder="Enter description"></s-text-field>
                </s-field-group>
                <s-field-group>
                  <s-button>Click Me</s-button>
                </s-field-group>
                <s-field-group>
                  <s-button fill>Click Me</s-button>
                </s-field-group>
              </s-panel-body>
            </s-panel>
            <s-panel class="mb-lg">
            </s-panel>
            <s-panel class="mb-lg">
            </s-panel>
          </s-container>
        </div>
      </s-app-bar-layout>
    </s-drawer-layout>
  </s-app>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import * as components from './components';

@Component({
  components,
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import 'variables';

.s-panel {
  height: 400px;
}



</style>
