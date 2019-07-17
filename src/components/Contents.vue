<template>
  <div role="main" class="col-sm-9 ml-sm-auto col-md-10 pt-3">
  <!--  <div class="container" style="margin-left: 60px; margin-right: 0;">-->
<!--    <div class="row">-->
      <SideNav></SideNav>
      <Search></Search>
<!--    </div>-->
<!--  </div>-->
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
