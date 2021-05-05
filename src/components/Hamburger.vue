<template>
  <div class="nav-btn">
    <button @click="navOpen" :class="openNav && 'active'" class="menu-btn">
      <span class="top"></span>
      <span class="mid"></span>
      <span class="bottom"></span>
    </button>
    <transition name="translateX">
      <nav class="mobile-menu-nav" v-if="openNav">
        <ul class="mobile-nav-bar">
          <li @click="navOpen" class="nav-link">
            <router-link to="/">Home</router-link>
          </li>
          <li @click="navOpen" class="nav-link">
            <router-link to="/about">About</router-link>
          </li>
          <li @click="navOpen" class="nav-link">
            <router-link to="/pricing">Pricing</router-link>
          </li>
          <li @click="navOpen" class="nav-link">
            <router-link to="/gallery">Gallery</router-link>
          </li>
          <li @click="navOpen" class="nav-link">
            <router-link to="/testimonials">Testimonials</router-link>
          </li>
          <li @click="navOpen" class="nav-link">
            <router-link to="/contact">Contact</router-link>
          </li>
        </ul>
      </nav>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      openNav: false,
    };
  },
  methods: {
    navOpen() {
      this.openNav = !this.openNav;
      console.log(this.openNav);
    },
  },
};
</script>

<style lang="scss" scoped>
.nav-btn {
  width: 100;
  background: #2f2f2f;
  position: fixed;
  top: 20px;
  right: 1.1%;
  z-index: 99;
}
.menu-btn {
  display: block;
  width: 50px;
  height: 50px;
  background: #2f2f2f;
  border: none;
  position: relative;
  z-index: 100;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  cursor: pointer;
  outline: none;
}

.menu-btn span {
  display: block;
  width: 30px;
  height: 2px;
  margin: auto;
  background: #fcecdd;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  transition: all 0.4s ease;
}

.top {
  transform: translateY(-12px);
}
.bottom {
  transform: translateY(12px);
}

button.active .top {
  transform: rotate(135deg);
}
button.active .mid {
  transform: translateX(20px) rotate(360deg);
  opacity: 0;
}
button.active .bottom {
  transform: rotate(-135deg);
}

@media screen and (min-width: 1200px) {
  .menu-btn span {
    transition: all 0s;
  }
}
nav {
  position: fixed;
  width: 100%;
  height: 100%;
  background: #2f2f2f;
  top: 0;
  right: 0;
  z-index: 99;
}
.mobile-menu-wrapper {
  height: 100%;
}
.mobile-nav-bar {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  font-size: 8rem;
  list-style: none;
}
.nav-link a {
  color: #fcecdd;
  list-style: none;
  text-decoration: none;
}

.mobile-menu-nav {
  height: 100%;
  transition: all 0.3s ease-in-out;
}
.translateX-enter-from,
.translateX-leave-active {
  right: -100%;
  opacity: 0;
}

@media screen and (max-width: 1000px) {
  .nav-btn {
    right: calc(100% - 98%);
  }
}
@media screen and (max-width: 850px) {
  .nav-btn {
    right: calc(100% - 90%);
  }
}
</style>
