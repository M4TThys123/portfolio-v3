<template>
  <section id="techstack" class="py-3">
    <div class="container-class">
      <div class="row-class">
        <h2 class="section__title mb-4">
          Dit is mijn
          <span class="text--blue">Tech-Stack</span>
        </h2>

        <section class="technologien mb-5">
          <h3 class="tech-title">Essentiële Webtechnologieën</h3>
          <section class="language__list">
            <div class="language" v-for="tech in technologien" :key="tech.id">
              <figure class="language__img--wrapper">
                <img :src="`/images/icons/${tech.url}`" alt="" class="language__img">
              </figure>
              <span class="language__name">{{ tech.name }}</span>
            </div>
          </section>
        </section>
        <section class="tools mb-5">
          <h3 class="tech-title">Ontwerp- en Ontwikkeltools</h3>
          <section class="language__list">
            <div class="language" v-for="tool in tools" :key="tool.id">
              <figure class="language__img--wrapper">
                <img :src="`/images/icons/${tool.url}`" alt="" class="language__img">
              </figure>
              <span class="language__name">{{ tool.name }}</span>
            </div>
          </section>
        </section>
        <section class="frameworks mb-5">
          <h3>Framework</h3>
          <section class="language__list">
            <div class="language" v-for="framework in frameworks" :key="framework.id">
              <figure class="language__img--wrapper">
                <img :src="`/images/icons/${framework.url}`" alt="" class="language__img">
              </figure>
              <span class="language__name">{{ framework.name }}</span>
            </div>
          </section>
        </section>
        <section class="platforms mb-5">
          <h3>Tools en Platforms</h3>
          <section class="language__list">
            <div class="language" v-for="platform in platforms" :key="platform.id">
              <figure class="language__img--wrapper">
                <img :src="`/images/icons/${platform.url}`" alt="" class="language__img">
              </figure>
              <span class="language__name">{{ platform.name }}</span>
            </div>
          </section>
        </section>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TechStackComponent",
  data() {
    return {
      technologien: [
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
        {
          id: 5,
          name: "C#",
          url: "CS.webp"
        },
        {
          id: 6,
          name: "SQL",
          url: "SQL.webp"
        },
        {
          id: 7,
          name: "PHP",
          url: "PHP.webp"
        },
        {
          id: 8,
          name: "Python",
          url: "Python.webp"
        },
      ],
      tools: [
        {
          id: 1,
          name: "Adobe XD",
          url: "Adobe_XD.webp"
        },
        {
          id: 2,
          name: "Adobe Illustrator",
          url: "Adobe_Illustrator.webp"
        },
        {
          id: 3,
          name: "Adobe Photoshop",
          url: "Adobe_Photoshop.webp"
        },
        {
          id: 4,
          name: "Webstorm",
          url: "Webstorm.webp"
        },
        {
          id: 5,
          name: "MySQL Workbench",
          url: "Workbench.webp"
        },
        {
          id: 6,
          name: "Docker Container",
          url: "Docker.webp"
        },
      ],
      frameworks: [
        {
          id: 1,
          name: "Svelte",
          url: "Svelte.webp"
        },
        {
          id: 2,
          name: "React",
          url: "React.webp"
        },
        {
          id: 3,
          name: "Vue.js",
          url: "Vue.webp"
        },
        {
          id: 4,
          name: ".NET",
          url: "Net.webp"
        },
        {
          id: 3,
          name: "Laravel",
          url: "Laravel.webp"
        },
      ],
      platforms: [
        {
          id: 1,
          name: "Prismic.io",
          url: "Prismic.webp"
        },
        {
          id: 2,
          name: "Hygraph",
          url: "Hygraph.webp"
        },
        {
          id: 3,
          name: "WordPress",
          url: "WordPress.webp"
        },
      ],
    };
  }

}
</script>

<style scoped>

h3 {
  text-align: center;
  color: #242424;
}

.technologien .language__list > .language > .language__img--wrapper > img,
.platforms .language__list > .language > .language__img--wrapper > img{
border-radius: 15px;
}

/* TECH STACK */
.language__list {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
  justify-content: center;
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
  padding: 25px 6px;
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

/* SM (for tablets - screens ≥ than 768px wide) */
@media (width >= 768px) {
  .language__img--wrapper {
    padding: 25px 8px;
  }
}



/* MD (for small laptops - screens ≥ than 992px wide) */
@media (width >= 992px) {
  .language__img--wrapper {
    padding: 25px 16px;
  }
}
</style>