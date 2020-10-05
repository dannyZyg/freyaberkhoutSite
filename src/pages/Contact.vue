<template>
  <Layout>
  <h1>Contact Page</h1>
  <p>Say hi :)</p>
  <Form/>

  </Layout>
</template>

<script>

import Form from '~/components/Form.vue'

export default {
  metaInfo: {
    title: 'Contact'
  },
  components: {
    Form
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
