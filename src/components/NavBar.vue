<template>
  <b-navbar spaced="true">
    <template slot="brand">
      <b-navbar-item tag="router-link" :to="{ path: '/' }">
        <img src="../assets/wt-logo.png" alt="WeTransfer" />
      </b-navbar-item>
    </template>
    <template slot="start">
      <b-navbar-item>
        <router-link to="/">Home</router-link>
      </b-navbar-item>
      <b-navbar-item>
        <router-link to="/about">About</router-link>
      </b-navbar-item>
    </template>

    <template slot="end">
      <b-navbar-item tag="div">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light">
            Log in
          </a>
        </div>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style lang="scss" scoped>
  .navbar-item {
    img {
      max-height: 4rem;
    }
  }
</style>
