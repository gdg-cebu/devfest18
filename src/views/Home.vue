<template>
  <div>
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
    <StatsBlock />
    <GalleryBlock />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';
import StatsBlock from '@/components/StatsBlock.vue';
import GalleryBlock from '@/components/GalleryBlock.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
    StatsBlock,
    GalleryBlock,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
