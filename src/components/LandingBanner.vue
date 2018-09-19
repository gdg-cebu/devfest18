<template>
  <section :class="$style.banner">
    <div :class="[$shared.wrapper, $style.wrapper]">
      <img
        :class="$style.logo"
        src="@/assets/banner-logo.png"
        alt="Banner Logo"
      >
      <button :class="$style.buyTicket">Buy Ticket</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'LandingBanner',
};
</script>

<style module="$shared" src="@/stylesheets/shared.css"></style>
<style module>
.banner {
  height: 70rem;
  background: url("@/assets/banner-image.jpg") center center;
  background-size: cover;
}

.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: flex-start;
  height: 100%;
  padding-bottom: 10rem;
}

.logo {
  width: 32rem;
}

.buyTicket {
  padding: 1em 2.75em;
  border: 1px solid #41c1c9;
  margin-top: 2rem;
  font-size: 1.6rem;
  text-transform: uppercase;
  color: #41c1c9;
  background: none;
}
</style>
