<template>
  <header :class="$style.navbar">
    <div :class="[$shared.wrapper, $style.wrapper]">
      <img
        :class="$style.logo"
        src="@/assets/gdg-cebu-white.png"
        alt="GDG Cebu Logo"
      >

      <nav :class="$style.links">
        <router-link :to="{name: 'home'}">Home</router-link>
        <router-link :to="{path: '/speakers'}">Speakers</router-link>
        <router-link :to="{path: '/schedule'}">schedule</router-link>
        <router-link :to="{path: '/team'}">Team</router-link>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'TheNavbar',
};
</script>

<style module="$shared" src="@/stylesheets/shared.css"></style>
<style module>
.navbar {
  padding: 8rem 0;
}

.wrapper {
  display: flex;
  align-items: center;
}

.logo {
  display: block;
  height: 3.6rem;
}

.links {
  display: flex;
  margin-left: auto;
  font-size: 1.6rem;
  text-transform: uppercase;
  background: linear-gradient(to right, #d32c92, #41c1c9);
  background-clip: text;
  -webkit-background-clip: text;
  text-fill-color: transparent;
  -webkit-text-fill-color: transparent;
}

.links a {
  margin: 0 1rem;
  text-decoration: none;
  color: #41c1c9;
}
</style>
