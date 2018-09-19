<template>
  <section :class="$style.gallery">
    <div :class="[$style.column, $style.column1]">
      <img :class="$style.cellHalfWidth" src="@/assets/banner-image.jpg" alt="">
      <img :class="$style.cellHalfWidth" src="@/assets/banner-image.jpg" alt="">
      <img :class="$style.cellTwiceTall" src="@/assets/banner-image.jpg" alt="">
      <img :class="$style.cell" src="@/assets/banner-image.jpg" alt="">
    </div>
    <div :class="[$style.column, $style.column2]">
      <img :class="$style.cellTwiceTall" src="@/assets/banner-image.jpg" alt="">
      <div :class="$style.cellAction">
        <p :class="$style.cellText">
          Last year's festival built lots of excitement. Check out photos from
          featured talks, hands-on learning sessions, and after-hours fun.
        </p>
        <a :class="$style.seePhotos" href="#">See Photos</a>
      </div>
      <img :class="$style.cell" src="@/assets/banner-image.jpg" alt="">
    </div>
    <div :class="[$style.column, $style.column3]">
      <img :class="$style.cellThriceTall" src="@/assets/banner-image.jpg" alt="">
      <img :class="$style.cellHalfWidth" src="@/assets/banner-image.jpg" alt="">
      <img :class="$style.cellHalfWidth" src="@/assets/banner-image.jpg" alt="">
    </div>
  </section>
</template>

<script>
export default {
  name: 'PhotoGallery',
};
</script>

<style module>
.gallery {
  display: flex;
  padding: 6px 0;
  position: relative;
}

.gallery::before,
.gallery::after {
  content: "";
  height: 3px;
  position: absolute;
  left: 0;
  right: 0;
  background-image: linear-gradient(
    to right,
    #d32c92,
    #6962ad,
    #41c1c9
  );
}

.gallery::before {
  top: 0;
}

.gallery::after {
  bottom: 0;
}

.column {
  flex: 1 0 0;
  display: flex;
  flex-wrap: wrap;
}

.cell {
  width: 100%;
  height: 15rem;
  object-fit: cover;
  object-position: center center;
  border: 1px solid transparent;
}

.cellHalfWidth {
  composes: cell;
  width: 50%;
}

.cellTwiceTall {
  composes: cell;
  height: 30rem;
}

.cellThriceTall {
  composes: cell;
  height: 45rem;
}

.cellAction {
  composes: cell;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 1.8rem;
  font-size: 1.4rem;
  line-height: 1.4;
  text-align: center;
}

.cellText {
  margin: 0;
  font-weight: 600;
  color: transparent;
  background-image: linear-gradient(
    to right,
    #d32c92,
    #6962ad,
    #41c1c9
  );
  background-clip: text;
  -webkit-background-clip: text;
}

.seePhotos {
  display: inline-block;
  padding: 0.75em 1.5em;
  border: 1px solid transparent;
  border-left: 1px solid #d32c92;
  border-right: 1px solid #41c1c9;
  margin-top: 1.6rem;
  position: relative;
  font-size: 1.2rem;
  text-transform: uppercase;
  text-decoration: none;
  color: #fff;
}

.seePhotos::before,
.seePhotos::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  height: 1px;
  background-image: linear-gradient(
    to right,
    #d32c92,
    #6962ad,
    #41c1c9
  );
}

.seePhotos::before {
  top: 0;
}

.seePhotos::after {
  bottom: 0;
}
</style>
