<template>
  <div>
    <b-navbar toggleable="lg" type="dark" class="navbar">
      <b-navbar-brand href="#">
        <b-icon icon="list" font-scale="3"></b-icon>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <img
          src="@/assets/img/logo-copy.png"
          srcset="
            @/assets/img/logo-copy@2x.png 2x,
            @/assets/img/logo-copy@3x.png 3x
          "
        />
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form class="mx-4">
            <b-icon icon="search" class="text-white" font-scale="1.5"></b-icon>
          </b-nav-form>

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.navbar {
  background-color: #201f1a !important;
  padding: 30px 100px;
}

</style>
