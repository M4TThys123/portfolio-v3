<template>
  <header class="blur">
    <nav>
      <router-link to="/" class="logo__link d-flex" @click="closeNav">
        <div class="personal__logo">Matthijs Blauw</div>
      </router-link>

      <div class="nav__menu nav__list">
        <ul class="nav__link--list nav__item">
          <li>
            <a href="#techstack" class="nav__link nav__link--anchor link__hover-effect link__hover-effect--black">Technologie</a>
          </li>
          <li>
            <a href="#projects" class="nav__link nav__link--anchor link__hover-effect link__hover-effect--black">Projecten</a>
          </li>
          <li>
            <a href="mailto:matthijs.blauw@gmail.com" class="nav__link nav__link--anchor nav__link--anchor-primary">Contact</a>
          </li>
        </ul>
      </div>

<!--      <HamburgerMenu @click="toggleNav" :is-nav-open="isNavOpen" class="menu__trigger"></HamburgerMenu>-->
    </nav>
  </header>
</template>

<script>
// import HamburgerMenu from "@/components/header/HamburgerMenu.vue";
export default {
  name: "HeaderComponent",
  components: {
    // HamburgerMenu
  },
  data() {
    return {
      isNavOpen: false,
      isScroll: true
    }
  },
  methods: {
    openNav(){
      console.log('click op de button')
      this.isNavOpen = !this.isNavOpen
      document.body.classList.add('no-scroll'); // Add no-scroll class
      // this.handleScroll(); // Toggle isScrolled
    },
    closeNav() {
      this.isNavOpen = false;
      document.body.classList.remove('no-scroll'); // Remove no-scroll class
      // this.handleScroll(); // Toggle isScrolled

    },

    toggleNav() {
      this.isNavOpen = !this.isNavOpen;

      if (this.isNavOpen) {
        document.body.classList.add('no-scroll');
      } else {
        document.body.classList.remove('no-scroll');
      }
    },
    // handleScroll() {
    //   if (window.pageYOffset > 0) {
    //     this.isScrolled = true;
    //   } else {
    //     this.isScrolled = false;
    //   }
    // }
  },


}
</script>

<style scoped>
/* NAVIGATION BAR */
nav{
  height: 100px;
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 12px;
}

.nav__link--anchor{
  margin: 0 12px;
  color: #242424;
  text-decoration: none;
  font-weight: 700;
}

.nav__link--list{
  display: flex;
}

.nav__link--anchor-primary{
  background-color: var(--color-blue);
  padding: 8px 20px;
  border-radius: 50px;
  color: white;
  transition: all 300ms ease;
}

.nav__link--anchor-primary:hover{
  background-color: #14539A;
}

.personal__logo{
  font-size: 24px;
  color: var(--color-blue);
  margin: 0 12px;
  font-weight: bold;
}

.color__scroll{
  fill: #192321;
}
/*global*/
a {
  text-decoration: none;
}

header{
  position: fixed;
  width: 100%;
  z-index: 999;
  padding: 0.75rem 1rem;
  top: 0;
  /*padding: 1.5rem 1.875rem 1rem;*/
  transition: all 0.3s ease;
}

/*Nav*/
nav{
  position: relative;
  height: 45px;

  display: flex;
  justify-content: space-between;
  align-items: center;

  max-width: 120rem;
  margin: auto;
}
.nav__menu{
  /*display: flex;*/
  /*justify-content: center;*/
}
.nav__list{
  margin-bottom: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
.nav__item{
  margin-right: 2em;
}
.logo__link{
  z-index: 999999;
}

.nav__link{
  /*color: #FFFFFF !important;*/
  transition:  .3s;

}

.nav__link:hover {
  text-decoration: underline;
  color: red;
}

.menu__trigger{
  display: none;
  z-index: 99999;
}


.blur{
  backdrop-filter: blur(24px);
  /*background-color: rgba(61, 149, 209, 0.4);*/
  /*background-color: rgba(57, 128, 112, 0.4);*/

}

@media screen and (max-width: 1024px) {
  .menu__trigger{
    display: block;
  }

  header{
    padding: 0.75rem 1rem;
  }

  nav {
    height: 32px;
  }
  .nav__menu{
    transition: .4s;
    margin-top: 2em;
  }
  .nav__list{
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;

    height: 100vh;
    padding: 4rem 1rem;

    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;


    transition: transform .3s ease-out;
    transform: translateY(-100%);
  }
  .nav__list--open{
    transform: translateY(0);
    padding-top: 5em;
  }
  .nav__item{
    font-size: 48px;
    font-weight: bold;
    font-family: Inter, sans-serif;
  }
}
.text-color__scroll{
  color: #192321;
}
.text-color__nav-open{
  color: #FFFFFF;
}
.nav__list--open{
  visibility: visible;
}

.logo-wrapper{
  display: flex;
  align-items: center;
}
.mobile-logo{
  display: block;

}
.desktop-logo{
  display: none;
}



/* SM (for tablets - screens ≥ than 768px wide) */
@media (width >= 768px) {
  /* CSS rules for tablets go here */
  .mobile-logo{
    display: none;

  }
  .desktop-logo{
    display: block;
  }
}

/* MD (for small laptops - screens ≥ than 992px wide) */
@media (width >= 992px) {
  /* CSS rules for small laptops go here */


}

/* LG (for laptops and desktops - screens ≥ than 1200px wide) */
@media (width >= 1200px) {
  /* CSS rules for laptops and desktops go here */
}
</style>