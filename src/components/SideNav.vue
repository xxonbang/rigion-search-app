<template>
  <div class="container-fluid">
    <div class="row">
      <nav class="col-sm-3 col-md-2 d-none d-sm-block bg-light sidebar">
        <ul class="nav nav-pills flex-column">
          <li class="nav-item">
            <a class="nav-link" href="/">코드조회</a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
    export default {
        name: "SideNav"
    }
</script>

<style scoped>
  .selected {
    color: white !important;
    background-color: #007bff;
    padding: .5rem 1rem !important;
  }

  body {
    padding-top: 3.5rem;
  }

  h1 {
    padding-bottom: 9px;
    margin-bottom: 20px;
    border-bottom: 1px solid #eee;
  }

  table {
    text-align: center;
    font-size: 14px;
    /* font-size: 0.8em; */
  }

  .navbar-brand {
    font-weight: bold;
    font-size: 25px;
  }

  /*
       * Sidebar
       */

  .sidebar {
    position: fixed;
    top: 51px;
    bottom: 0;
    left: 0;
    z-index: 1000;
    padding: 20px 0;
    overflow-x: hidden;
    overflow-y: auto;
    /* Scrollable contents if viewport is shorter than content. */
    border-right: 1px solid #eee;
  }

  .sidebar .nav {
    margin-bottom: 20px;
  }

  .sidebar .nav-item {
    width: 100%;
  }

  .sidebar .nav-item+.nav-item {
    margin-left: 0;
  }

  .sidebar .nav-link {
    border-radius: 0;
  }

  /* Placeholders */
  .placeholders {
    padding-bottom: 3rem;
  }

  .placeholder img {
    padding-top: 1.5rem;
    padding-bottom: 1.5rem;
  }

  /* calendar 이미지 위치조정 */
  .ui-datepicker-trigger {
    height: 25px;
    margin-left: 5px;
    margin-top: 7px;
  }

  /* login css */
  .bd-placeholder-img {
    font-size: 1.125rem;
    text-anchor: middle;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  @media (min-width: 768px) {
    .bd-placeholder-img-lg {
      font-size: 3.5rem;
    }
  }
</style>
