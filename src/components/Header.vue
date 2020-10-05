<template>
<div>
  <header class="header">
  <div>
    <h1>
      <strong>
        <g-link to="/">{{ $static.metadata.siteName | upperCase }}</g-link>
      </strong>
    </h1>
    <div>{{ $static.metadata.siteDescription | upperCase }}</div>
  </div>
    <nav class="nav">
      <g-link class="nav__link" to="/">Work</g-link>
      <g-link class="nav__link" to="/about/">About</g-link>
      <g-link class="nav__link" to="/contact/">Contact</g-link>
    </nav>
  </header>
</div>
</template>

<static-query>
query {
  metadata {
    siteName,
    siteDescription 
  }
}
</static-query>

<script>
export default {
  name: 'Header',
  data () {
    return {
      message: 'Try change me!'
    }
  },
  methods: {
    onClick () {
      this.message = 'Here you go :)'
    }
  },
  filters: {
    upperCase: function (value) {
      if (!value) return '';
      value = value.toString();
      return value.toUpperCase();
    }
  }
}
</script>

<style>
.card {
  padding: 20px;
  background: #FFF;
}
</style>
