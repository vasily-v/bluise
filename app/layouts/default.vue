<template>
  <main :class="[$route.name]" class="main px-4 md:px-0">
    <div class="container mx-auto">
      <site-header />
      <nuxt class="nuxt" />
    </div>

    <svg class="divider -mx-4 sm:mx-0" width="100%" viewBox="0 0 10 1">
      <polygon stroke="none" stroke-width="0" fill="#0b3765" points="0,0.6 0,1 10,1 10,0" />
    </svg>

    <site-footer />
  </main>
</template>

<script>
import SiteHeader from '@/components/partials/header.vue';
import SiteFooter from '@/components/partials/footer.vue';

export default {
  components: {
    SiteHeader,
    SiteFooter,
  },
  mounted() {
    window.WonderPush = window.WonderPush || [];
    WonderPush.push([
      'init',
      {
        webKey: '9597e7d139620620fc1da3a80bd11ed5fd4df8affe08d26c70bcbfd783878dd2',
      },
    ]);
  },
};
</script>

<style lang="scss">
.divider {
  position: relative;
  min-width: 100vw;
  margin-top: auto;
}

.nuxt {
  transition: all 0.5s cubic-bezier(0.55, 0, 0.1, 1);
}
</style>
