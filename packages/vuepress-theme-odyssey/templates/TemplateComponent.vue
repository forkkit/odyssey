<template>
  <div>
    <header class="odo-doc-header">
      <div>
        <h1 class="odo-doc-header--title">{{$page.frontmatter.name}}</h1>
        <p class="odo-doc-header--lead">{{$page.frontmatter.lead}}</p>
      </div>
      <ul v-if="$page.frontmatter.links" class="odo-doc-header--links">
        <li v-bind:key="link.label" v-for="link in $page.frontmatter.links">
          <a :href="link.href" class="ods-button is-odo-button-shadow">{{ link.label }}</a> 
        </li>
      </ul>
    </header>
    <OdsTabs label="Button Documentation Types" :active="tabs.active" :tablist="tabs.tablist" :id="tabs.id">
      <template slot="tab-overview">
          <Content slot-key="overview" />
      </template>
      <template slot="tab-scss">
          <Content slot-key="scss" />
      </template>
      <template slot="tab-figma">
          <Content slot-key="figma" />
      </template>
    </OdsTabs>
  </div>
</template>

<script>
export default {
  name: 'TemplateComponent',
  data () {
     return {
       tabs: {
        id: 'docs',
        active: "tab-overview",
        tablist: [
          { id: "tab-overview", label: 'Overview' },
          { id: "tab-scss", label: 'SCSS' },
          { id: "tab-figma", label: 'Figma guide' },
        ]
      }
    }
  },
  components: {
    Example: () => import('../global-components/Example.vue'),
    OdsTabs: () => import('../global-components/OdsTabs.vue'),
  }
}
</script>
