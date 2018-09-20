<template>
  <section :class="$style.sponsorsBlock">
    <div :class="$shared.wrapper">
      <div :class="$style.heading">
        <h1 :class="$style.title">Sponsors</h1>
      </div>

      <div :class="$style.sponsors">
        <a
          v-for="sponsor in sponsors"
          :key="sponsor.name"
          :class="$style.sponsor"
          :href="sponsor.url"
          target="_blank"
        >
          <img :src="sponsor.image" :alt="sponsor.name">
        </a>
      </div>
    </div>
  </section>
</template>

<script>
/* eslint-disable global-require */
export default {
  name: 'SponsorsBlock',

  data() {
    return {
      sponsors: [{
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }, {
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }, {
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }, {
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }, {
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }, {
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }, {
        name: 'Google',
        url: 'https://google.com/',
        image: require('@/assets/google.svg'),
      }],
    };
  },
};
</script>

<style module="$shared" src="@/stylesheets/shared.css"></style>
<style module>
.sponsorsBlock {
  padding: 8rem 0;
}

@media (max-width: 500px) {
  .sponsorsBlock {
    text-align: center;
  }
}

.heading {
  display: inline-block;
  padding: 0.5em 3em;
  margin-bottom: 6rem;
  position: relative;
  z-index: 1;
  font-size: 2.4rem;
  background-color: #111;
  box-shadow:
    -3rem 1.2rem 6rem -2rem #41c1c9,
    3rem 1.2rem 6rem -2rem #d32c92;
  overflow: hidden;
}

.heading::before {
  content: "";
  height: 2px;
  position: absolute;
  left: 0;
  right: 0;
  bottom: -1px;
  background-image: linear-gradient(
    to right,
    transparent,
    #d32c92 15%,
    #6962ad,
    #41c1c9 85%,
    transparent
  );
  opacity: 0.7;
}

.title {
  display: inline-block;
  margin: 0;
  font-size: 2.4rem;
  font-weight: 600;
  text-align: center;
  text-transform: uppercase;
  color: transparent;
  background-image: linear-gradient(
    to right,
    #41c1c9,
    #6962ad,
    #d32c92
  );
  background-clip: text;
  -webkit-background-clip: text;
}

.sponsors {
  display: flex;
  flex-wrap: wrap;
}

@media (max-width: 500px) {
  .sponsors {
    justify-content: center;
  }
}

.sponsor {
  display: block;
  margin: 1.6rem 3.2rem;
}

.sponsor img {
  width: 12rem;
  height: 6rem;
  object-fit: contain;
  object-position: center center;
}
</style>
