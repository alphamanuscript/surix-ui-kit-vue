<template>
  <div id="app">
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
        <s-app-bar slot="bar">
          New product
        </s-app-bar>
        <div class="page-content">
          <div class="banner">  
          </div>
          <div class="container mt-lg">
            <div class="panel mb-lg">
              <div class="panel-header">
                <div class="panel-title">
                  Basic details
                </div>
                <div class="panel-subtitle">
                  Basic information about the product
                </div>
              </div>
              <div class="panel-body">
                <div class="field-group">
                  <input type="text" class="text-field" placeholder="Enter name" />
                </div>
                <div class="field-group">
                  <textarea class="text-field" placeholder="Enter description"></textarea>
                </div>
                <div class="field-group">
                  <button class="button">Click Me</button>
                </div>
                <div class="field-group">
                  <button class="button fill">Click Me</button>
                </div>
              </div>
            </div>
            <div class="panel mb-lg">

            </div>
            <div class="panel mb-lg">

            </div>
          </div>
        </div>
      </s-app-bar-layout>
    </s-drawer-layout>
  </div>
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

.mt {
  margin-top: $margin-y;
  &-lg {
    margin-top: $margin-y * 2;
  }
}

.mb {
  margin-bottom: $margin-y;
  &-lg {
    margin-bottom: $margin-y * 2;
  }
}


#app {
  height: 100vh;
}

.text-thin {
  @include text-thin();
}

.text-extra-thin {
  @include text-extra-thin;
}


.container {
  margin-left: auto;
  margin-right: auto;
  max-width: 1000px;
}

.panel {
  background-color: white;
  width: 100%;
  height: 400px;
  border: 1px solid $border-color;
  border-radius: $border-radius;
  // box-shadow: 0px 0px 3px #ced0d2;

  .panel-header {
    padding: $padding;
    border-bottom: 1px solid $border-color;

    .panel-title {
      font-size: 1.6em;
      @include text-extra-thin;
    }

    .panel-subtitle {
      margin-top: 5px;
      font-size: 0.9em;
      @include text-extra-thin;
      font-family: $font-family-alt;
      color: $text-secondary;
    }
  }

  .panel-body {
    padding: $padding;
  }
}

.text-field {
  padding: 12px 15px;
  font-size: 1em;
  border-radius: 4px;//$border-radius;
  // border: 1px solid #cecece;
  outline: none;
  @include text-extra-thin();
  width: 100%;
  display: block;
  border: 0;
  box-shadow: 0px 0px 0px 1px #cecece inset;

  &:focus {
    // border-color: #85a7ef;
    // box-shadow: 0 0 0 2px rgba(81, 203, 238, 1) inset;
    border: 0;
    box-shadow: 0 0 0 2px #85a7ef inset;
  }

  resize: none;
  &.resizable {
    resize: vertical;
  }

  &::placeholder {
    color: $text-secondary;
  }
}

.button {
  $btn-bgd: #cecece;
  $btn-color: #555;
  // padding: 8px 15px;
  height: 36px;
  padding: {
    left: 15px;
    right: 15px;
  }
  border: 1px solid $btn-bgd;
  outline: none;
  border-radius: 3px;
  color: $btn-color;
  background: white;

  &:hover, &:active {
    color: #85a7ef;
    border: 1px solid #85a7ef;
    
  }

  &:active {
    box-shadow: 0 0 0 2px #b2c6f1;
  }

  &.fill {
    color: white;
    background-color: #4b83e6;
    border: none;

    &:hover, &:active {
      background-color: #3d68b5;
      // box-shadow: none;
    }
  }
}

.field-group {
  margin-bottom: $padding;
}

.banner {
  padding: $padding;
  height: 200px;
  background-color: white;
}

</style>
