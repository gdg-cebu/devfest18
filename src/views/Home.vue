<template>
  <div>
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
    <EventStats />
    <PhotoGallery />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';
import EventStats from '@/components/EventStats.vue';
import PhotoGallery from '@/components/PhotoGallery.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
    EventStats,
    PhotoGallery,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
