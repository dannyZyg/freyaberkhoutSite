<template>
  <Layout>
	<div>
    <ul>
      <li v-for="project in $page.projects.edges" :key="project.id">
        <g-link :to="project.node.path">
          {{ project.node.title }}
        </g-link>
      </li>
    </ul>

	</div>

  </Layout>
</template>
<page-query>
query Projects {
  projects: allProject {
    edges {
      node {
        id
        title
        tags
        image
        path
      }
    }
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: 'Freya Berkhout'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
