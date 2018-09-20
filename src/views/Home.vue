<template>
  <div>
    <TheNavbar />
    <LandingBanner :class="$style.banner" />
    <StatsBlock />
    <GalleryBlock />
    <OrganizerBlock />
    <TicketsBlock />
    <LocationBlock />
    <SponsorsBlock />
  </div>
</template>

<script>
import TheNavbar from '@/components/TheNavbar.vue';
import LandingBanner from '@/components/LandingBanner.vue';
import StatsBlock from '@/components/StatsBlock.vue';
import GalleryBlock from '@/components/GalleryBlock.vue';
import OrganizerBlock from '@/components/OrganizerBlock.vue';
import TicketsBlock from '@/components/TicketsBlock.vue';
import LocationBlock from '@/components/LocationBlock.vue';
import SponsorsBlock from '@/components/SponsorsBlock.vue';

export default {
  name: 'Home',

  components: {
    TheNavbar,
    LandingBanner,
    StatsBlock,
    GalleryBlock,
    OrganizerBlock,
    TicketsBlock,
    LocationBlock,
    SponsorsBlock,
  },
};
</script>

<style module>
.banner {
  margin-top: -18rem;
}
</style>
