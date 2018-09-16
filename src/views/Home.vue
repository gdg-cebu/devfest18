<template>
  <div class="home">
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
