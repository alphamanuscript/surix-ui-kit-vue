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

$font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
$font-family-alt: 'Helvetica Neue', sans-serif;
$drawer-width: 220px;
$header-height: 60px;
$background-color: #fafafb;
$drawer-background-color: #27375D;
$header-background-color: white;
$border-color: #eaecef;
$border-radius: 2px;
$padding: 20px;

$margin-y: 25px;

$text-light: #D6E3FF;
$text-color: #1D2945;
$text-secondary: #818796;

@mixin fill-viewport {
  min-width: 100vw;
  min-height: 100vh;
}

@mixin text-thin {
  font-weight: 300;
}

@mixin text-extra-thin {
  font-weight: 200;
}

* {
  box-sizing: border-box;
}

ul {
  list-style-type: none;
  padding: 0;
}

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


html {
  @include fill-viewport();
}

body {
  padding: 0;
  margin: 0;
  font-family: $font-family;
  @include fill-viewport;
  background-color: $background-color;
  color: $text-color;
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

.drawer-nav-layout {
  display: flex;
  flex-direction: row;
  height: 100%;

  .drawer {
    width: $drawer-width;
    background-color: $drawer-background-color;
    position: fixed;
    height: 100vh;
    @media screen and (max-width: 500px) {
      display: none;
    }
    z-index: 30;
  }

  .main {
    flex-grow: 1;
    position: relative;
    margin-left: $drawer-width;
    @media screen and (max-width: 500px) {
      margin-left: 0;
    }

    .main-header {
      position: fixed;
      width: 100%;
      top: 0px;
    }

    .page-content {
      margin-top: $header-height;
    }
  }
}

.main-header {
  background-color: rgba($header-background-color, 0.95);
  height: $header-height;
  box-shadow: 0px 0px 3px #ced0d2;
  z-index: 20;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: {
    left: $padding;
    right: $padding;
  }
}

.page-content {
  min-height: calc(100vh - 50px);
  z-index: 9;
  overflow-y: auto;
}

.drawer-header {
  height: $header-height;
  margin: 0;
  padding: {
    left: $padding;
    right: $padding;
  }
  display: flex;
  flex-direction: row;
  align-items: center;
  background-color: #2A4071;
  color: $text-light;
}

.drawer-content {
  @include text-thin;
  padding-top: $padding;
  .nav-group-header {
    text-transform: uppercase;
    font-size: 0.75em;
    color: #91a6d2;
    padding: 10px $padding;
    font-weight: 500;
  }
  .nav-item {
    color: #91a6d2;
    padding: 10px $padding;
    font-size: 0.85em;
    
    &.active {
      color: $text-light;
      background-color: #1b3158;
    }

    &:hover {
      background-color: #1b3158;
    }
  }

  .nav-group {
    .nav-item {
      padding-left: $padding * 2;
    }
  }

  .separator {
    border-bottom: 1px solid #172b4e;
  }
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
