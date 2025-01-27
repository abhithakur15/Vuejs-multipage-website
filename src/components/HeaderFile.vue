<template>
  <header :class="headerClasses">
    <nav class="navbar navbar-expand-lg">
      <div class="container">
        <a class="navbar-brand" href="#"><img src="../assets/images/logo.png" alt="" class="img-fluid"></a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
          @click="toggleNavbar"
        >
          <span class="toggler-icon top-bar"></span>
          <span class="toggler-icon middle-bar"></span>
          <span class="toggler-icon bottom-bar"></span>
        </button>
        <div
          class="collapse navbar-collapse"
          :class="{ show: isNavbarOpen }"
          id="navbarSupportedContent"
        >
          <ul class="navbar-nav mx-auto mb-2 mb-lg-0">
            <li
              class="nav-item"
              v-for="(item, index) in navItems"
              :key="index"
              :class="{ active: activeNavItem === index }"
              @click="setActiveNavItem(index)"
            >
              <a class="nav-link nav_link_a" :href="item.path">{{ item.name }}</a>
            </li>
          </ul>
          <div class="d-flex">
            <ButtonOne text="Get A Quote " path="/Contact"></ButtonOne>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import ButtonOne from './ButtonOne.vue';

export default {
  name: 'HeaderFile',
  components: {
    ButtonOne,
  },
  data() {
    return {
      isSticky: false,
      isFadeInDown: false,
      isAnimated: false,
      isNavbarOpen: false,
      activeNavItem: null,
      navItems: [
        { name: 'Home', path: '/' },
        { name: 'About', path: '/about' },
        { name: 'Services', path: '/Services' },
        { name: 'Team', path: '/Team' },
        { name: 'Contact', path: '/Contact' },
      ],
    };
  },
  computed: {
    headerClasses() {
      return {
        sticky: this.isSticky,
        fadeInDown: this.isFadeInDown,
        animated: this.isAnimated,
      };
    },
  },
  methods: {
    handleScroll() {
      const scrollTop = window.scrollY;

      this.isSticky = scrollTop > 200;
      this.isFadeInDown = scrollTop > 200;
      this.isAnimated = scrollTop > 200;
    },
    setActiveNavItem(index) {
      this.activeNavItem = index;
      this.isNavbarOpen = false; // Close the navbar when a link is clicked
    },
    toggleNavbar() {
      this.isNavbarOpen = !this.isNavbarOpen;
    },
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
};
</script>

<style scoped>
:root {
  --white: #fff;
}

#navbarSupportedContent ul li a {
  color: var(--white);
  font-size: 16px;
  font-weight: 400;
}

#navbarSupportedContent ul li {
  margin: 0 10px;
}

header.sticky {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 10;
}

header.animated {
  transition: all 0.3s ease-in-out;
}

header.fadeInDown {
  animation: fadeInDown 0.5s;
}

.navbar-toggler {
  cursor: pointer;
}

.navbar-collapse.show {
  display: block !important;
}

.nav-item.active a {
  font-weight: bold;
  text-decoration: underline;
}

@keyframes fadeInDown {
  from {
    transform: translateY(-20px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}
</style>
