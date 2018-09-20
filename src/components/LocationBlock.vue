<template>
  <section :class="$style.locationBlock">
    <div :class="$style.wrapper">
      <div :class="$style.location">
        <div :class="$style.locationContainer">
          <h1 :class="$style.name">Galleria Thingy thingy</h1>
          <p :class="$style.address">P. Remedio St., Banilad, Mandaue City</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'LocationBlock',
};
</script>

<style module>
.locationBlock {
  height: 40rem;
  background: url("@/assets/banner-image.jpg") center center no-repeat;
  background-size: cover;
}

.wrapper {
  composes: wrapper from "@/stylesheets/shared.css";
  display: flex;
  justify-content: flex-end;
}

@media (max-width: 500px) {
  .wrapper {
    justify-content: center;
  }
}

.location {
  position: relative;
  margin-top: 4.8rem;
}

.locationContainer {
  padding: 2.4rem 4.8rem;
  background-color: #111;
}

.location::before,
.location::after,
.locationContainer::before,
.locationContainer::after {
  content: "";
  position: absolute;
}

.location::before,
.location::after {
  top: 0;
  bottom: 0;
  width: 2px;
}

.location::before {
  left: 0;
  background-image: linear-gradient(
    to top,
    #d32c92,
    #6962ad
  );
}

.location::after {
  right: 0;
  background-image: linear-gradient(
    to top,
    #6962ad,
    #41c1c9
  );
}

.locationContainer::before,
.locationContainer::after {
  left: 0;
  right: 0;
  height: 2px;
}

.locationContainer::before {
  top: 0;
  background-image: linear-gradient(
    to right,
    #6962ad,
    #41c1c9
  );
}

.locationContainer::after {
  bottom: 0;
  background-image: linear-gradient(
    to right,
    #d32c92,
    #6962ad
  );
}

.name {
  font-size: 2rem;
}

.address {
  font-size: 1.4rem;
}
</style>
