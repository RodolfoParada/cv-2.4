<script>
import TheCard from '../components/TheCard.vue'
// import projects from '../Json.js/proyectos'
export default {
  components: {
    TheCard
  },
  data() {
    return {
      // projects: projects,
      projects: [
        {
          id: 1,
          projectName: 'Proyecto Batatabit',
          projectDescription:
            'Descripción: Es un proyecto Web, se utilizó buenas prácticas, metodologías First mobile, metodología BEM, Responsive con media Queries responsive se utilizó Html y Css.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/batatabit/'
        },
        {
          id: 2,
          projectName: 'Proyecto GAMEZONE',
          projectDescription:
            'Descripción: Es un Ecommerce, se utilizó buenas prácticas, metodologías First mobile, metodología BEM, Responsive con media Queries se utilizó Html y Css.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/E-COMMERCE/'
        },
        {
          id: 3,
          projectName: 'Proyecto Barbería',
          projectDescription:
            'Descripción: Es una pagina de una Barbería,su utilizó buenas prácticas, metodologías First mobile, metodología BEM, Responsive con media Queries se utilizó Html y Css.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/cursohtmlAlura/'
        },
        {
          id: 4,
          projectName: 'Proyecto Fuente de Soda',
          projectDescription:
            'Descripción: Es una pagina de una Fuente de Soda,su utilizó buenas prácticas, metodologías First mobile, metodología BEM, Responsive con media Queries se utilizó Html y Css.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/FuenteSoda1/index.html'
        },
        {
          id: 5,
          projectName: 'Proyecto Auto-Limpio',
          projectDescription:
            'Descripción: Es una pagina de Limpieza de Autos,su utilizó buenas prácticas, metodologías First mobile, metodología BEM, Responsive con media Queries se utilizó Html y Css.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/AutoLimpio/'
        },
        {
          id: 6,
          projectName: 'Proyecto Encriptar-Desencriptar',
          projectDescription:
            'Descripción: Es un encriptador y desencriptador de mensajes, se utilizó metodologías First mobile Bem lenguajes de Javascript con Html y Css.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/ChallengerOneDesafio1/'
        },
        {
          id: 7,
          projectName: 'Web Anime',
          projectDescription:
            'Descripción: Es una página web que se utilizó ccs y html usando buenas practicas.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/webAnime/'
        },
        {
          id: 8,
          projectName: 'Web Hotel',
          projectDescription:
            'Descripción: Es una página web que se utilizó ccs y html usando buenas practicas.',
          buttonText: 'Ver Proyecto',
          projectLink: 'https://rodolfoparada.github.io/WebHotel/'
        },
        {
          id: 9,
          projectName: 'En desarrollo ',
          projectDescription: 'Descripción: En desarrollo ',
          buttonText: 'Ver Proyecto',
          projectLink: ''
        },
        {
          id: 10,
          projectName: 'En desarrollo ',
          projectDescription: 'Descripción: En desarrollo ',
          buttonText: 'Ver Proyecto',
          projectLink: ''
        },
        {
          id: 11,
          projectName: 'En desarrollo ',
          projectDescription: 'Descripción: En desarrollo ',
          buttonText: 'Ver Proyecto',
          projectLink: ''
        },
        {
          id: 12,
          projectName: 'En desarrollo ',
          projectDescription: 'Descripción: En desarrollo ',
          buttonText: 'Ver Proyecto',
          projectLink: ''
        }
      ],
      pageSize: 6,
      page: 1
    }
  },
  computed: {
    pageCount() {
      return Math.ceil(this.projects.length / this.pageSize)
    },
    paginatedProjects() {
      const start = (this.page - 1) * this.pageSize
      const end = start + this.pageSize
      return this.projects.slice(start, end)
    }
  },
  methods: {
    goToPage(page) {
      if (page >= 1 && page <= this.pageCount) {
        this.page = page
      }
    }
  }
}
</script>

<template>
  <div class="proyectos">
    <h1>Proyectos</h1>
    <main>
      <div class="card-container">
        <div v-for="project in paginatedProjects" :key="project.id" class="column">
          <TheCard
            class="mb-2"
            :id="project.id"
            :projectName="project.projectName"
            :projectDescription="project.projectDescription"
            :buttonText="project.buttonText"
            :projectLink="project.projectLink"
          />
        </div>
      </div>
    </main>

    <div class="pagination-container mt-1">
      <div class="button-one">
        <button
          type="button"
          class="btn btn-outline-secondary"
          @click="goToPage(page - 1)"
          :disabled="page === 1"
        >
          Anterior
        </button>
      </div>
      <div class="mx-3">
        <span class="fw-bolder text-center">{{ page }}</span>
      </div>

      <div class="button-dos">
        <button
          type="button"
          class="btn btn-outline-secondary"
          @click="goToPage(page + 1)"
          :disabled="page === pageCount"
        >
          Siguiente
        </button>
      </div>
    </div>
  </div>
</template>

<style>
.card-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  max-width: 800px; /* Set your desired maximum width */
  margin: 0 auto; /* Center the container */
}

.column {
  flex: 0 0 calc(50% - 20px); /* Two columns with a small margin between them */
  max-width: calc(50% - 20px);
  margin: 10px; /* Adjust margin based on your design */
}

.pagination-container {
  display: flex;
  justify-content: center;
  margin-top: 20px; /* Add some margin for spacing */
}

.button-container {
  display: flex;
  justify-content: center;
  margin-top: 10px; /* Adjust margin based on your design */
}

.button-one {
  margin-right: 10px;
}
.button-dos {
  margin-left: 10px;
}
</style>
