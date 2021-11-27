<template>
  <Layout :sidebar="false">
    <div class="content">
      <h1>HIPAA Compliance Policies</h1>
      <nav>
        <!-- To use other icons here, you need to import them in the Shortcut component -->
        <Shortcut link="/purpose" text="Purpose and Scope" icon="align-center-icon" />
        <Shortcut link="/roles" text="Roles and Responsibilities" icon="users-icon" />
        <Shortcut link="/policies" text="Policies" icon="check-square-icon" />
      </nav>
      <p />
      <span class="sitelink">Visit <a href="https://polymentalhealth.com/" title="Poly Mental Health Main Site">Poly Mental Health</a> main site</span>
    </div>
  </Layout>
</template>


<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Shortcut from '~/components/Shortcut.vue'

export default {
  components: {
    Shortcut
  },
  data() {
    return {
      description: 'The ultimate static generated documentation theme for the JAM-stack'
    }
  },
  metaInfo: {
    title: 'HIPAA Compliance Policies',
    meta: [
      { key: 'description', name: 'description', content: 'HIPAA Compliance Policies.' }
    ]
  }
}
</script>

<style lang="scss" scoped>
.content {
  display: flex;
  flex-direction: column;
}

h1 {
  text-align: center;
  max-width: 600px;
  margin: 1.5em auto 1.5em;

  @include respond-above(md) {
    max-width: 1000px;
  }
}

h2 {
  font-size: 1.4rem;
  margin: 0;
}

nav {
  display: flex;
  justify-content: space-between;
  flex-direction: column;

  @include respond-above(sm) {
    flex-direction: row;
  }
}

.git {
  margin: 3em 0 0;
  align-self: center;

  @include respond-above(md) {
    margin: 5em 0 0;
  }
}

p.lead {
  margin: 1rem auto 3rem auto;
  max-width: 50em;
}

.sitelink {
  margin: 1rem;
  text-align: center;
  a {
    font-weight: bold;
  }
}
</style>
