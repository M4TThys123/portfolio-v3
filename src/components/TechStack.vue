<template>
  <section id="projects">
    <div class="container">
      <div class="row">
        <h1 class="section__title">
          Hier een aantal van mijn
          <span class="text--blue">projecten</span>
        </h1>
        <ul class="project__list">
          <li class="project">
            <div class="project__wrapper">
              <img src="./assets/fdnd.png" class="project__img" alt="" />
              <div class="project__description">
                <h3 class="project__description--title">
                  GitHub Issue feacher for FDND
                </h3>
                <h4 class="project__description--sub-title">
                  HTML, CSS, JavaScript & GitHub GraphQL API
                </h4>
                <p class="project__description--para">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Quidem asperiores eaque dolores saepe velit ut placeat
                  suscipit iure ratione quia.
                </p>
                <div class="project__description--links">
                  <a
                      href="https://github.com/M4TThys123/SPRINT-12-Proof-of-Concept"
                      class="project__description--link"
                      target="_blank" rel="noreferrer"
                  ><i class="bx bxl-github"></i
                  ></a>
                  <a
                      href="https://sprint-12-proof-of-concept.herokuapp.com/"
                      class="project__description--link"
                      target="_blank"
                  ><i class="bx bx-link"></i
                  ></a>
                </div>
              </div>
            </div>
          </li>
          <li class="project">
            <div class="project__wrapper">
              <img
                  src="./assets/visite-kaartje.png"
                  class="project__img"
                  alt=""
              />
              <div class="project__description">
                <h3 class="project__description--title">
                  Visite Kaartje - V2
                </h3>
                <h4 class="project__description--sub-title">
                  HTML, CSS, clientside JavaScript & Rest API
                </h4>
                <p class="project__description--para">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Quidem asperiores eaque dolores saepe velit ut placeat
                  suscipit iure ratione quia.
                </p>
                <div class="project__description--links">
                  <a
                      href="https://github.com/M4TThys123/SPRINT-7-Visitekaartje-V2"
                      class="project__description--link"
                      target="_blank"
                  ><i class="bx bxl-github"></i
                  ></a>
                  <a
                      href="https://m4tthys123.github.io/SPRINT-7-Visitekaartje-V2/"
                      class="project__description--link"
                      target="_blank"
                  ><i class="bx bx-link"></i
                  ></a>
                </div>
              </div>
            </div>
          </li>
          <li class="project">
            <div class="project__wrapper">
              <img src="./assets/beyco.png" class="project__img" alt="" />
              <div class="project__description">
                <h3 class="project__description--title">
                  Coffee page for Beyco
                </h3>
                <h4 class="project__description--sub-title">
                  HTML, CSS, JavaScript
                </h4>
                <p class="project__description--para">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                  Quidem asperiores eaque dolores saepe velit ut placeat
                  suscipit iure ratione quia.
                </p>
                <div class="project__description--links">
                  <a
                      href="https://github.com/M4TThys123/SPRINT-5-Chippr-Beyco"
                      class="project__description--link"
                      target="_blank"
                  ><i class="bx bxl-github"></i
                  ></a>
                  <a
                      href="https://github.com/M4TThys123/SPRINT-5-Chippr-Beyco"
                      class="project__description--link"
                      target="_blank"
                  ><i class="bx bx-link"></i
                  ></a>
                </div>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TechStackComponent"
}
</script>

<style scoped>
/* TECH STACK */
.language__list {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
}

.language {
  width: 25%;
  display: flex;
  align-items: center;
  flex-direction: column;
  position: relative;
}

.language__img--wrapper {
  display: flex;
  align-content: center;
  justify-content: center;
  padding: 25px 16px;
}

.language__img {
  width: 100%;
  /* max-width: 100px; */
  transition: all 300ms;
}

.language:hover .language__img {
  filter: brightness(80%);
  opacity: 0.86;
  transform: scale(0.9);
}

.language__name {
  position: absolute;
  bottom: 0;
  transform: scale(0);
  transition: all 300ms;
  font-size: 20px;
}
.language:hover .language__name {
  transform: scale(1);
}
</style>