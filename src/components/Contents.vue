<template>
  <div role="container" class="col-sm-9 ml-sm-auto col-md-10 pt-3">
      <SideNav></SideNav>
      <Search></Search>
  </div>
</template>

<script>
  import SideNav from "./SideNav";
  import Search from "./Search";

  export default {
    name: "Contents",
    components: {Search, SideNav}
  }
</script>

<style scoped>

</style>
