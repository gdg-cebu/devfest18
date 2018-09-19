<template>
  <div>
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
    <StatsBlock />
    <GalleryBlock />
    <OrganizerBlock />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';
import StatsBlock from '@/components/StatsBlock.vue';
import GalleryBlock from '@/components/GalleryBlock.vue';
import OrganizerBlock from '@/components/OrganizerBlock.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
    StatsBlock,
    GalleryBlock,
    OrganizerBlock,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
