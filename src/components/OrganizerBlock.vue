<template>
  <section :class="$style.organizer">
    <div :class="$style.wrapper">
      <div :class="$style.column">
        <div :class="$style.section">
          <h1 :class="$style.heading">Organizer</h1>
          <p :class="$style.text">
            GDG Cebu and GBG Cebu are the proud organizers of
            <strong>DevFest x BizFest 2018</strong>.
          </p>
        </div>
        <div :class="$style.section">
          <h1 :class="$style.heading">What is GDG?</h1>
          <p :class="$style.text">
            Google Developers Group (GDG) is an open and volunteer geek
            community who creates exciting projects and share experience
            about Google technologies with passion.
          </p>
        </div>
      </div>

      <div :class="$style.column">
        <img :class="$style.image" src="@/assets/banner-image.jpg" alt="">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'OrganizerBlock',
};
</script>

<style module>
.organizer {
  padding: 8rem 0;
}

.wrapper {
  composes: wrapper from '@/stylesheets/shared.css';
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.column {
  width: 45%;
}

@media (max-width: 500px) {
  .wrapper {
    flex-wrap: wrap;
  }

  .column {
    width: 100%;
  }

  .column:last-of-type {
    margin-top: 3.2rem;
  }
}

.heading {
  display: inline-block;
  font-size: 1.6rem;
  font-weight: 600;
  text-transform: uppercase;
  color: #41c1c9;
}

@supports (background-clip: text) or (-webkit-background-clip: text) {
  .heading {
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
}

.text {
  font-size: 1.4rem;
  font-weight: 600;
  line-height: 1.4;
}

.image {
  width: 100%;
}
</style>
