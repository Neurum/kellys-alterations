<template>
  <div id="nav">
    <div class="logo">
      <div class="first-letter">K</div>
      <div class="second-letter">A</div>
    </div>
    <div class="nav-links">
      <router-link class="underline" to="/">Home</router-link>
      <router-link class="underline" to="/about">About</router-link>
      <router-link class="underline" to="/pricing">Pricing</router-link>
      <router-link class="underline" to="/gallery">Gallery</router-link>
      <router-link class="underline" to="/testimonials"
        >Testimonials</router-link
      >
      <router-link class="underline" to="/contact">Contact</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style lang="scss" scoped>
#nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 6rem;
  background: #fcecdd;

  margin-bottom: 2rem;

  & a {
    text-decoration: none;
    color: #2f2f2f;
  }
}

.logo {
  width: 5%;
  height: 6rem;
  position: relative;
  font-size: 5rem;
  font-family: 'Dancing Script', cursive;
  color: #2f2f2f;
}

.first-letter {
  font-size: 5rem;
  position: absolute;
  top: 0px;
  left: 20px;
}
.second-letter {
  font-size: 5rem;
  position: absolute;
  top: 10px;
  left: 41px;
}
.nav-links {
  width: 35%;
  display: flex;
  justify-content: space-evenly;
  font-size: 3.5rem;
}

a {
  &.router-link-exact-active {
    font-weight: 700;
    &:before {
      visibility: visible !important;
      transform: scaleX(1) !important;
    }
    &:after {
      visibility: visible !important;
      transform: scaleX(1) !important;
    }
  }

  &.underline {
    position: relative;

    &:before {
      content: '';
      position: absolute;
      width: 100%;
      height: 2px;
      bottom: 0;
      left: 0;
      background-color: #2f2f2f;
      visibility: hidden;
      transform: scaleX(0);
      transition: all 0.3s ease-in-out 0s;
    }

    &:after {
      content: '';
      position: absolute;
      width: 100%;
      height: 2px;
      top: 0;
      left: 0;
      background-color: #2f2f2f;
      visibility: hidden;
      transform: scaleX(0);
      transition: all 0.3s ease-in-out 0s;
    }

    &:hover {
      &:before,
      &:after {
        visibility: visible;
        transform: scaleX(1);
      }
    }
  }
}
</style>
