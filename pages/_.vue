<template>
  <section>
    <p>URL: {{ $route.fullPath }}</p>
    <p>SSR: {{ ssr ? 'true' : 'false' }}</p>
  </section>
</template>

<script>
// Tiny trick: use _.vue as "catch-alls"
export default {
  asyncData() {
    return {
      ssr: process.server
    }
  }
}
</script>
