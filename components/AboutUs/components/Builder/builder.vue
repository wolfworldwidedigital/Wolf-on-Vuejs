<template>
  <RenderContent
    v-if="canShowContent"
    model="page"
    :content="content"
    :api-key="apiKey"
    :customComponents="getRegisteredComponents()"
  />
</template>
<script>
  import { getContent, RenderContent, isPreviewing } from '@builder.io/sdk-vue/vue3';

export default {
  components: { RenderContent, },
  data: () => ({
    canShowContent: false,
    content: null,
    apiKey: '27cace4a848242e1979ab3df0afb6dae',
  }),
  mounted() {
    getContent({
      model: 'page',
      apiKey: '27cace4a848242e1979ab3df0afb6dae',
      userAttributes: {
        urlPath: window.location.pathname,
      },
    }).then(res => {
      this.content = res;
      this.canShowContent = this.content || isPreviewing();
    });
  },
}
</script>
