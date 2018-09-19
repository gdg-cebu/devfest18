<template>
  <section :class="$style.eventStats">
    <div :class="$shared.wrapper">
      <div :class="$style.stats">
        <p :class="$style.stat">
          <span :class="$style.value">600</span>
          <span :class="$style.label">Attendees</span>
        </p>
        <p :class="$style.stat">
          <span :class="$style.value">1</span>
          <span :class="$style.label">Day</span>
        </p>
        <p :class="$style.stat">
          <span :class="$style.value">24</span>
          <span :class="$style.label">Sessions</span>
        </p>
        <p :class="$style.stat">
          <span :class="$style.value">3</span>
          <span :class="$style.label">Tracks</span>
        </p>
      </div>

      <p :class="$style.details">
        The biggest Google tech conference in Cebu City, carefully crafted for
        you by your GDG community!
      </p>
      <p :class="$style.details">
        All about Android, Web, and Cloud from the world experts.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'StatsBlock',
};
</script>

<style module="$shared" src="@/stylesheets/shared.css"></style>
<style module>
.eventStats {
  padding: 8rem 0;
}

.stats {
  display: flex;
  margin-bottom: 2.4rem;
}

.stat {
  flex: 1 0 0;
  text-align: center;
  color: #41c1c9;
}

.value {
  display: block;
  font-size: 2.8rem;
  font-weight: 700;
}

.label {
  display: block;
  padding-top: 8px;
  margin-top: 8px;
  position: relative;
  font-size: 1.6rem;
  font-weight: 600;
}

.label::before {
  content: "";
  width: 5rem;
  height: 1px;
  position: absolute;
  top: 0;
  left: calc(50% - 2.5rem);
  background-image: linear-gradient(
    to right,
    transparent,
    #d32c92 15%,
    #6962ad,
    #41c1c9 85%,
    transparent
  );
}

.details {
  margin: 0;
  font-size: 1.4rem;
  font-weight: 600;
  line-height: 1.4;
  text-align: center;
  color: #41c1c9;
}
</style>
