<template>
  <div>
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
    <StatsBlock />
    <GalleryBlock />
    <OrganizerBlock />
    <TicketsBlock />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';
import StatsBlock from '@/components/StatsBlock.vue';
import GalleryBlock from '@/components/GalleryBlock.vue';
import OrganizerBlock from '@/components/OrganizerBlock.vue';
import TicketsBlock from '@/components/TicketsBlock.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
    StatsBlock,
    GalleryBlock,
    OrganizerBlock,
    TicketsBlock,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
