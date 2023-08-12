<template>
  <section id="projects">
    <div class="container-class">
      <div class="row-class">
        <h2 class="section__title">
          Dit is mijn
          <span class="text--blue">Tech Stack</span>
        </h2>
      </div>

      <section class="language__list">
            <h3>Essentiële Webtechnologieën</h3>
            <div class="language" v-for="tech in technologie" :key="tech.id">
              <figure class="language__img--wrapper">
                <img :src="`/images/icons/${tech.url}`" alt="" class="language__img">
                <!--              <img src="/images/icons/Adobe_Illustrator.webp" alt="" class="language__img">-->
              </figure>
              <span class="language__name">{{ tech.name }}</span>
            </div>
      </section>

    </div>
  </section>
</template>

<script>
export default {
  name: "TechStackComponent",
  data() {
    return {
      technologie: [
        {
          id: 1,
          name: "HTML",
          url: "HTML5.webp"
        },
        {
          id: 2,
          name: "CSS",
          url: "CSS.webp"
        },
        {
          id: 3,
          name: "JavaScript",
          url: "JavaScript.webp"
        },
        {
          id: 4,
          name: "TypeScript",
          url: "TypeScript.webp"
        },
        // Add more objects for other technologies if needed
      ]

    };
  }

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