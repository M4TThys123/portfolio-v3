<template>
  <div id="app">

    <AboutComponent></AboutComponent>

    <ProjectsComponent></ProjectsComponent>

<!--    <TechStackComponent></TechStackComponent>-->
<!--    <ProjectsComponent></ProjectsComponent>-->

  </div>
</template>

<script>
import AboutComponent from "@/components/About.vue";
// import ProjectsComponent from "@/components/Projects.vue";
// import TechStackComponent from "@/components/TechStack.vue";
import ProjectsComponent from "@/components/Projects.vue";

export default {
  name: 'App',
  components: {
    ProjectsComponent,
    // TechStackComponent,
    // ProjectsComponent,
    AboutComponent,
    },
}
</script>

<style>
:root {
  --color-blue: #29539A;

}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Lato", sans-serif;
}

html {
  scroll-behavior: smooth;
}

h1,
h2,
h5,
h6,
span {
  color: #242424;
  text-align: center;
  line-height: 1.25;
}

h1 {
  font-size: 36px;
}

h3{
  text-align: left;
  color: #fff;

}

p {
  line-height: 1.5;
  font-size: 16px;
}

a {
  text-decoration: none;
  position: relative;
  transition: opacity 300ms ease;
}

i:hover {
  opacity: 0.7;
}

li {
  list-style-type: none;
}

.flex {
  display: flex;
}

.flex-1 {
  flex: 1;
}

.container {
  padding: 50px 0;
}

.row {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  padding: 0 12px;
}

.text--blue {
  color: #3043C8;
}

section:nth-child(even) {
  background-color: #f8f8f8;
}

.section__title {
  margin-bottom: 20px;
}

/* Breakpoints */

/* Small phones, tablets, large smartphones */
@media (max-width: 768px) {
  nav {
    height: 68px;
  }

  h1 {
    font-size: 28px;
  }
  .about-me__info--para {
    font-size: 18px;
  }
  .language {
    width: calc(100% / 3);
  }
  .project__description--para p{
    font-size: 14px;
  }

  .project__description {
    left: 30px;
    padding-right: 30px;
  }
}

/* Small phones */
@media (max-width: 480px) {
  .nav__link:not(:last-child) {
    display: none;
  }

  .project__description--para {
    display: none;
  }

  .project__description {
    padding: 0;
    left: 0;
    width: 100%;
  }

  .project__description--links {
    display: flex;
    justify-content: center;
  }

  .project__description--title {
    font-size: 32px;
    line-height: 1;
  }

  .project__description--sub-title h4{
    text-align: center;
    margin: 12px 0;
  }
}

</style>
