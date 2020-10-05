<template>
<div>
<SocialIcon/>
<SocialIcon/>
<SocialIcon/>
</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>

import SocialIcon from "~/components/SocialIcon.vue"

export default {
  name: 'Footer',
  data () {
    return {
      message: 'Try change me!'
    }
  },
  components: {
    SocialIcon, 
  },
  methods: {
    onClick () {
      this.message = 'Here you go :)'
    }
  },
}
</script>

<style>
.card {
  padding: 20px;
  background: #FFF;
}
</style>
