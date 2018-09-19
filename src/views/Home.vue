<template>
  <div>
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
    <EventStats />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';
import EventStats from '@/components/EventStats.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
    EventStats,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
