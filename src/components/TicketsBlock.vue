<template>
  <section :class="$style.tickets">
    <header :class="$style.header">
      <div :class="$style.heading">
        <h1 :class="$style.title">Tickets</h1>
      </div>
    </header>
  </section>
</template>

<script>
export default {
  name: 'TicketsBlock',
};
</script>

<style module>
.tickets {
  padding-bottom: 8rem;
}

.header {
  position: relative;
  text-align: center;
}

.header::before {
  content: "";
  height: 1px;
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  background-image: linear-gradient(
    to right,
    #d32c92,
    #6962ad,
    #41c1c9
  );
}

.heading {
  display: inline-block;
  padding: 0.5em 3em;
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
</style>
