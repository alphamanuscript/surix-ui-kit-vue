<template>
  <div id="app">
    <div class="drawer-nav-layout">
      <div class="drawer">
        <div class="drawer-header">
          Happy Feet
        </div>
        <div class="drawer-content">
          <ul class="drawer-nav">
            <li>My Apps</li>
            <li>Marketplace</li>
            <li>Settings</li>
            <li>Manage Users</li>
          </ul>
        </div>
      </div>
      <div class="main">
        <div class="main-header">
          New product
        </div>
        <div class="page-content">
          <div class="banner">
            
          </div>
          <div class="container margin-top-lg">
            <div class="panel">

            </div>
            <div class="panel">

            </div>
            <div class="panel">

            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {},
})
export default class App extends Vue {}
</script>

<style lang="scss">

$font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
$drawer-width: 256px;
$header-height: 70px;
$background-color: #fcfdff;
$drawer-background-color: #27375D;
$header-background-color: white;
$border-color: #eaecef;
$border-radius: 2px;
$padding: 16px;

$text-light: #D6E3FF;
$text-color: #1D2945;

@mixin fill-viewport {
  min-width: 100vw;
  min-height: 100vh;
}

* {
  box-sizing: border-box;
}

ul {
  list-style-type: none;
  padding: 0;
}

.margin-top-lg {
  margin-top: 50px;
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
  background-color: rgba($header-background-color, 0.7);
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

.drawer-nav {
  li {
    color: $text-light;
    padding: $padding;
    font-size: 0.9em;
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
}

.banner {
  padding: $padding;
  height: 200px;
  background-color: white;
}

</style>
