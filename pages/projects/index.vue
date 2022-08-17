<script>
import ProjectCard from "../../components/ProjectCard";

export default {
  components: {
    ProjectCard,
  },
  data() {
    return {
      projects: [
        {
          title: "C3 Ejendomme",
          description: "Property Management Company based in Ikast.",
          img_url: "c3.jpg",
          url: "https://c3ejendomme.dk/",
          tags: [{ name: "WordPress" }, { name: "Design" }],
        },

        {
          title: "Terese Jarset",
          description: "Therapist and Sexologist based in Copenhagen.",
          img_url: "teresejarset.jpg",
          url: "https://teresejarset.dk/",
          tags: [{ name: "WordPress" }, { name: "Design" }],
        },

        {
          title: "BioKube",
          description: "Wastewater treatment company based in Sweden.",
          img_url: "biokube.jpg",
          url: "https://biokube.se/",
          tags: [{ name: "WordPress" }, { name: "Design" }],
        },

        {
          title: "Smørum Autoland",
          description: "Auto Repair Shop based in Smørum",
          img_url: "smorum.jpg",
          url: "https://smorumautoland.dk/",
          tags: [{ name: "WordPress" }, { name: "Design" }],
        },

        {
          title: "Aarstidernes have og anlaeg",
          description: "Gardening and tree cutting service based in Sjælland.",
          img_url: "have.jpg",
          url: "https://aarstiderneshaveanlaeg.dk/",
          tags: [{ name: "WordPress" }, { name: "Design" }],
        },

        {
          title: "Eachthing",
          description: "Design for a price comparison website focused on sustainability.",
          img_url: "eachthing.jpg",
          url: "https://github.com/josh-bm/Eachthing",
          tags: [{ name: "Vue" }, { name: "Nuxt" }, { name: "Design" }],
        },

        {
          title: "MobileLabel",
          description: "Design for a CMS in a locked PIM system.",
          img_url: "mobilelabel.png",
          url: "https://prduct.com/",
          tags: [{ name: "Vue" }, { name: "Design" }],
        },

        {
          title: "Quotr",
          description: "Quotes App with CRUD functionality using the MERN stack.",
          img_url: "quotr.png",
          url: "https://github.com/josh-bm/quotr-mern",
          tags: [{ name: "React" }, { name: "MongoDB" }, { name: "Express" }, { name: "Node" }],
        },
        {
          title: "Trip Event Planner",
          description: "Trip Event Planner App using ASP.NET.",
          img_url: "trip_planner.jpg",
          url: "https://github.com/josh-bm/TripEventPlanner",
          tags: [{ name: "C#" }, { name: "ASP.NET" }],
        },
        {
          title: "Movies API",
          description: "Simple Movies API using HTML, CSS, and JS.",
          img_url: "movies_api.jpg",
          url: "https://github.com/josh-bm/Movies-API",
          tags: [{ name: "HTML" }, { name: "CSS" }, { name: "JS" }],
        },

        {
          title: "Movies, books, and music store",
          description: "Movies, books, and music webshop using ASP.NET.",
          img_url: "mbmstore.jpg",
          url: "https://github.com/josh-bm/MbmStore",
          tags: [{ name: "C#" }, { name: "ASP.NET" }],
        },
        {
          title: "Pacman App",
          description: "Pacman Android game using Kotlin.",
          img_url: "pacman.png",
          url: "https://github.com/josh-bm/PacmanKotlin",
          tags: [{ name: "Kotlin" }],
        },

        {
          title: "Shopping List App",
          description: "Shopping List Android App using Kotlin.",
          img_url: "shopping.png",
          url: "https://github.com/josh-bm/Shopping-List-App",
          tags: [{ name: "Kotlin" }],
        },
        {
          title: "Web Developer Corporation",
          description: "Web Dev Corporation using Umbraco.",
          img_url: "aarhuswebdevcorp.png",
          url: "https://github.com/josh-bm/AarhusWebDevCorp",
          tags: [{ name: "Umbraco" }],
        },
        {
          title: "LoL Esports",
          description: "LoL Esports news blog with interviews using Drupal.",
          img_url: "lolesportsdrupal.jpg",
          url: "https://github.com/josh-bm/LoLEsports-Drupal",
          tags: [{ name: "Drupal" }],
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <Navbar />
    <div class="frame text-white">
      <h2 class="font-semibold text-2xl mb-4">Projects</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-10">
        <div class="" v-for="(project, i) in projects" :key="i">
          <project-card :project-data="project" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
