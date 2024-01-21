<template>
  <section id="projects">
    <div class="container-class">
      <div class="row-class">
        <h2 class="section__title">
          Hier een aantal van mijn
          <span class="text--blue">projecten</span>
        </h2>

        <section v-if="isLoading" class="spinner-border" role="status">
          <span class="sr-only">Loading...</span>
        </section>

        <ul class="project__list">
          <li class="project" v-for="project in projects" :key="project.data.id">
            <div class="project__wrapper">
              <PrismicImage :field="project.data.project_image" class="project__img" alt="project image"/>

              <div class="project__description">
                <div
                    v-html="asHTML(project.data.project_title)"
                    class="project__description--title"
                ></div>

                <div
                    v-html="asHTML(project.data.sub_title)"
                    class="project__description--sub-title"
                ></div>
                <div
                    v-html="asHTML(project.data.project_paragraph)"
                    class="project__description--para"
                ></div>

                <div class="project__description--links">
                  <a
                      :href="project.data.github_link"
                      class="project__description--link"
                      target="_blank"
                      rel="noreferrer"><i class="bx bxl-github" /></a
                  >
                  <a
                      :href="project.data.website_link"
                      class="project__description--link"
                      target="_blank"
                      rel="noreferrer"><i class="bx bx-link" /></a
                  >
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
import Prismic from 'prismic-javascript';
import { asHTML } from '@prismicio/helpers'
import { PrismicImage } from '@prismicio/vue'
export default {
  name: "ProjectsComponent",
  components: {
    PrismicImage
  },
  data() {
    return {
      projects: [],
      isLoading: true,
    };
  },
  created() {
    this.fetchProjects();
  },
  methods: {
    asHTML,
    async fetchProjects() {
      try {
        const apiEndpoint = 'https://portfolio-matthijs.cdn.prismic.io/api/v2';
        const api = await Prismic.api(apiEndpoint);
        const response = await api.query(Prismic.Predicates.at('document.type', 'projects'));

        this.projects = response.results;
        console.log(this.projects)

        this.isLoading = false;
      } catch (error) {
        console.error('Error fetching data from Prismic:', error);
      }
    },
  },
};

</script>

<style scoped>
/* PROJECTEN */
.project__img {
  width: 100%;
  transition: all 500ms ease;
}

.project__wrapper {
  display: flex;
  box-shadow: 0 20px 80px rgba(0, 0, 0, 0.45);
  border-radius: 20px;
  overflow: hidden;
  position: relative;
}

.project__wrapper::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: #1c1d25;
  opacity: 0;
  transition: opacity 450ms ease;
  z-index: 2;
}

.project:hover .project__wrapper::before {
  opacity: 0.7;
}

.project:hover .project__img {
  transform: scale(1.07);
  filter: blur(5px);
}

.project__list {
  padding-top: 40px;
  padding-left: 0 !important;

}
.project:hover .project__description {
  opacity: 1;
  transform: translateY(-50%);
}
.project__description {
  position: absolute;
  top: 50%;
  left: 90px;
  transform: translateY(100%);
  max-width: 550px;
  z-index: 3;
  opacity: 0;
  transition: transform 450ms, opacity 300ms;
}

.project__description--title{
  font-size: 38px;
  margin-bottom: 8px;
}
.project__description--para {
  margin: 16px 0;
}
.project__description--link {
  font-size: 30px;
  margin-right: 16px;
}

.project__description--title,
.project__description--sub-title,
.project__description--para,
.project__description--link {
  text-align: left;
  color: #fff;
}

.project {
  margin-bottom: 80px;
}

.project:last-child {
  margin-bottom: 40px;
}

h3{
  text-align: left !important;
  color: #fff;
}

</style>