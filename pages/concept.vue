<template>
  <InsameeAppContainer>
    <NuxtContent
      :document="content"
      class="prose prose-sm sm:prose lg:prose-lg xl:prose-xl mx-auto"
    />
  </InsameeAppContainer>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const content = await $content('concept').fetch()

    return {
      content,
    }
  },
  head() {
    return {
      title: 'Le concept',
    }
  },
}
</script>
