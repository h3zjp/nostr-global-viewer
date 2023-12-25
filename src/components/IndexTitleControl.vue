<script setup lang="ts">
const props = defineProps({
  feedRelays: {
    type: Array as () => string[],
    required: true
  }
})

function appVersion() {
  // @ts-ignore
  return __APP_VERSION__;
}
</script>
<template>
  <h1 class="p-index-title">
    <span class="p-index-title__main">Nostr</span>
    <span class="p-index-title__main">Feeds</span>
    <span class="p-index-title__sub">from nostr-relay.h3z.jp <a href="https://github.com/h3zjp/nostr-global-viewer" target="_blank" title="GitHub" rel="nofollow, noopener"><i class="fab fa-github" style="color: #000000;"></i></a></span>
    <span class="p-index-title__sub">Version: {{ appVersion() }}</span>
  </h1>
</template>
<style scoped lang="scss">
.p-index-title {
  font-family: "Koruri", sans-serif;
  letter-spacing: normal;
  color: #ffffff;
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin: 0;
  padding: 1rem 0;

  @media screen and (max-width: 880px) {
    flex-direction: row;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  &__main {
    font-size: 4rem;
    color: #ffffff;

    @media screen and (max-width: 880px) {
      font-size: 3rem;
    }
  }

  &__sub {
    font-size: 1.5rem;

    @media screen and (max-width: 880px) {
      font-size: 1.5rem;
      width: 100%;
    }
  }
}
</style>