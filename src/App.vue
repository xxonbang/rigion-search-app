<template>
  <div id="app">
    <Header></Header>
    <Contents></Contents>
  </div>
</template>

<script>
import Header from "./components/Header";
import Contents from "./components/Contents";
export default {
  components: {Header, Contents}
}
</script>

<style>
  .selector-for-some-widget {
    box-sizing: content-box;
  }
</style>
