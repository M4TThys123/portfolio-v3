<template>
  <section id="about-me" class="py-3">
    <!--    <NavComponent></NavComponent>-->

    <div class="flex flex-1">
      <div class="about-me__info row-class">
        <div class="about-me__info--container">
          <figure class="about-me__picture--mask">
            <img class="about-me__picture" src="https://avatars.githubusercontent.com/u/70703948?v=4"
              alt="Image of undraw websirtes" />
          </figure>
          <h1 class="about-me__picture--title">
            Hey! Ik ben
            <span class="text--blue">Matthijs Blauw</span>&nbsp;
            <span class="wave">👋🏻</span>
          </h1>
          <p class="about-me__info--para">
            Ik ben een <strong class="text--blue">Software Developer & Designer</strong> met een sterke passie voor het
            bouwen van robuuste en innovatieve oplossingen die een positieve impact hebben op de wereld en zorgen voor
            een uitstekende gebruikerservaring.
          </p>
          <div class="about-me__links">
            <a href="https://www.linkedin.com/in/matthijs-blauw-9a9573235/" class="about-me__link" target="_blank"
              rel="noreferrer"><i class="bx bxl-linkedin" /></a>
            <a href="https://github.com/M4TThys123" class="about-me__link" target="_blank" rel="noreferrer"><i
                class="bx bxl-github" /></a>
            <a href="mailto:matthijs.blauw@gmail.com" class="about-me__link" target="_blank"><i
                class="bx bx-envelope" /></a>
            <PDFLink pdf-file-name="Matthijs Blauw - Curriculum Vitae.pdf">
              <i class="bx bxs-file-pdf"></i>
            </PDFLink>
          </div>
        </div>
        <figure class="about-me__img--container">
          <img src="images/undraw_websites_%2314539A.svg" alt="Undraw website image" class="about-me__img" />
        </figure>
      </div>
    </div>
  </section>
</template>

<script>
// import NavComponent from "@/components/Nav.vue";

import PDFLink from "@/components/PDFLink.vue";

export default {
  name: "AboutComponent",
  components: { PDFLink }
}
</script>

<style scoped>
/* ABOUT ME */
#about-me {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  margin-top: 100px;
}

.about-me__info {
  display: flex;
  flex-direction: column;
}

.about-me__info--container {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 600px;
  margin: 0 auto;
  text-align: center;
}

.about-me__picture--mask {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  overflow: hidden;
  margin-bottom: 28px;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.16);
  animation: animate-profile-picture 800ms 200ms backwards;
}

@keyframes animate-profile-picture {
  0% {
    transform: scale(0);
  }

  80% {
    transform: scale(1.1);
  }

  100% {
    transform: scale(1);
  }
}

.about-me__picture {
  width: 100%;
  transform: scale(1.5);
  padding-top: 5px;
}

.about-me__picture--title {
  margin-bottom: 16px;
  animation: fade-up-animation 650ms 400ms backwards;
}

.about-me__info--para {
  font-size: 20px;
  margin-bottom: 28px;
  animation: fade-up-animation 650ms 600ms backwards;
}

.about-me__link {
  font-size: 35px;
  color: #242424;
  padding: 0 16px;
}

.about-me__links {
  animation: fade-up-animation 650ms 800ms backwards;
}

@keyframes fade-up-animation {
  0% {
    opacity: 0;
    transform: translateY(40px);
  }

  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.about-me__img--container {
  flex: 1;
  display: flex;
  align-items: center;
}

.about-me__img {
  width: 100%;
  animation: fade-in-animation 1200ms 800ms backwards;
}

@keyframes fade-in-animation {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

.wave {
  display: inline-block;
  animation: animate-wave 500ms infinite ease-in-out;
}

@keyframes animate-wave {
  0% {
    transform: rotate(0);
  }

  50% {
    transform: rotate(30deg);
  }

  100% {
    transform: rotate(0);
  }
}
</style>